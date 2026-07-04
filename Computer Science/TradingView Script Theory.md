---
tags:
date: 29/10/2025
---
# Type System
### ~ Qualifiers 1 - theory:
1. TradingView uses *qualifiers* to enact duck-typing in following structure:
		Qualifier system: **const < input < simple < series**
	Here **const** is *weakest* qualifier & **series** the *strongest* and bears the meaning that any stronger qualifier can go anywhere its weaker subqualifier can (i.e. a const can fit anywhere input can)
2. Qualifiers can be cast to upper *only* - i.e. a *simple* can become a *series* but not the other way round
3. Return values with different qualifiers, if compared, will return the *stronger* qualifier

### ~ Qualifiers 2 - kinds:
1. *< const >*:
	 **Definition:** Defined at *first* runtime, they do not change over time and hence are calculated only once. Any literal or result which is calculated using only *consts* is, by default, also a *const*
	 **Naming:** `SNAKE_CASE`
	 **Conventions:** Optional `const` keyword (which enforces non-reassignment (although assigning to changing data is ok)). Any literal used more than once should become a *const*, it's ok if constants will be in the namespace of the function they are only used at (in fact should be done if you hope others will be interested in your script)
2. *< input >*:
	 **Definition:** Generally produced by `input.*()` functions these are the values that the user types in. Qualifies as *input* (with the exception for `input.source()` & `input.enum()` that return *series* & *simple* objects respectively)
	 **Naming:** Should end in `Input`
3. *< simple >*:
	 **Definition:** Something in the middle between a variable and a constant, this obscure qualifier stays consistent and unchanging throughout script's execution but defines at runtime. Consider this line:
	 ```Python
	 simple color warningColor = not 
     chart.is_standart ? color.new(color.orange, 70) : na
	 ```
	 Here `warningColor` may change but it will still be within a well-defined `color` range. However, am not really sure what qualifies as *simple* - needs further checking
	 **Conventions:** May include a `simple` keyword
1. *< series >*:
	 **Definition:** Also a very mysterious but most flexible qualifier of all. Qualifies somewhat like a list it relates to a structure that stores data of a bar, albeit in a dynamic way so that the current bar is at 0 (which is optional) and all others are +1 more into the past with the last one being the number of all available bars. Almost all functions return a series so it's possible to use the history-referencing operator on them without declaring a varible. Some built-ins (such as *open, high, low, close, volume, time, and bar_index* (which is a number of how many bars are there)) and the result of any operations on them will result in a *series* object.
### ~ Types:
1. *< color >*:
	 Special type for colors. Can be represented as either `#RRGGBB` or `#RRGGBBAA`
2. *Drawing types & < plot, hline > types*:
	 Allow scripts to make custom drawings on the chart. Return their unique ID by which they can later be referenced
3. *Collections*:
	**! ADD LATER !**
1. *UDT or User-defined type*:
	 **! ADD LATER !**
6. *void*:
	 Special data type that cannot be assigned to a variable or used in an expression and is used solely for the purpose to indicate that a function does not return anything
7. *na*:
	 Acronym for *not available*. Corresponds to *None* in Python however when declaring a variable with *na* a type should be specified:
	 ```Python
	 // Compilation error!
	 myVar = na
	 // Ok. `myVar` will later in program become a float
	 float myVar = na
	 ```
### ~ Type Template:
Like Generics in Python they are used to explicitly declare collections:
```Python
//@version=5
indicator("Type templates demo")

//@variable A variable initially assigned to `na` that accepts arrays of "int" values.
array<int> intArray = na
//@variable An empty matrix that holds "float" values.
floatMatrix = matrix.new<float>()
//@variable An empty map that holds "string" keys and "color" values.
stringColorMap = map.new<string, color>()
```
### ~ Tuples:
These however can be used anywhere except for ternary operator
```Python
//@function Calculates the sum and product of two values.
calcSumAndProduct(float a, float b) =>
    //@variable The sum of `a` and `b`.
    float sum = a + b
    //@variable The product of `a` and `b`.
    float product = a * b
    // Return a tuple containing the `sum` and `product`.
    [sum, product]

// Declare a tuple containing the sum and product of the `high` and `low`, respectively.
[hlSum, hlProduct] = calcSumAndProduct(high, low)
```
# Execution model

**~ Behaviour & Key Features:** The script is executed on your chart when one of the events triggering the execution of a script has occurred. Executes once per bar using the available OHLCV values for each bar. All bars, except for the rightmost one, are *historic bars* Upon reaching the utmost right bar - the *realitime bar*, - if trading is active, *indicators* will execute once per update and *strategies* only when the realtime bar closes (however this behaviour can be changed so strategies behave like indicators) and then the *realtime bar* becomes an *elapsed realtime bar*

**~ Execution on historical bars:** A script executes exactly once per historical bar

**~ Execution on realtime bars:** An *indicator* (or *strategy* with `calc_on_every_tick` set to true) will execute every time a change in the values of the bar changes. Current price is kept in *close*. Similarly, the *high* and *low* built-in variables represent the highest high and lowest low reached since the realtime bar’s beginning. However a *strategy* (without `calc_on_every_tick`) will execute exactly once even on a realtime bar

**~ Warnings on using functions that operate on historical data:** Make sure data input is consistent (i.e. no counting every other bar) - this may result in unexpected & faulty behaviour. However compiler generally tells you where such errors are


# Script & It's Structure
A Pine scripts fllows this general structure:
1. *< version >*
	 A compiler annotation that indicates which version of Pine Script will be used (currently available from 1 to 5). While not mandatory howerver heavily recomended. If ommited, will default to version 1. It should be at the beginning of the file (typically after a license) and follows this structure: `//@version=...`
2. *< declaration_statement >*
	 Any Pine script has to have one of three declarations statments: `indicator()`, `strategy()` or `library()`. These identify the type of the script and what can be done with it: what functions can be used, how it will be executed and whatnot. Along with some additional info such as the name of chart, where it will appear, what values will be shown, etc.
3. *< code >*
	 Here goes the logic of the script. **Notable interesting things:** Lines can be wrapped anyhow as long as that indentation is not a multiple of four (which is used to represent local scopes) so this code is valid:
	 ```Python
	 a = open +
	       close +
	          high +
	             low
	 ```
### ~ Compiler annotations:
Special comments that - for the most part - add description to things. For further study: [Compiler Annotations](https://www.tradingview.com/pine-script-docs/language/script-structure/#compiler-annotations)

### ~ Declaration Modes:
1. *< on each bar >* The variable will be reset on every bar
2. *< var >* The variable will be set on the first bar only
3. *< varip >* (*ip* stands for *intrabar persist*) A special case of var with very characteristic of persisting on rollbacks on realtime bars
# Custom / Interesting Operators
1. `[n (n >= 0)] -> Nan | series` - history-referencing operator that works on *series*. Can be executed once per function call / variable (i.e. no `open[1][4]`, just `open[5]`) Any fractional will be rounded down
2. `condition ? if_true : if_false` - conditional ternary operator (same logic implemets `iff()` function)

Links: [[ProgrammingMainNode]]