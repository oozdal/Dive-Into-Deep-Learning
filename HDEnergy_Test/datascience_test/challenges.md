# Programming Challenges for HD Energy -- Data Scientist position

#### Q1. Regular find function for list
Describe (with pseudocode or real code) how to find an element by value in an unsorted list (i.e. define the "find" function for a list, with a list and a value as inputs). The function should return the index of the element found. What should you return if the element is not in the list?
> For simplicity, you can assume a list of integers.


#### Q2. Optimised find function for sorted list
How would optimise the "find" function of Q1 if the input list is a sorted list?


#### Q3. Machine learning for energy consumption
The `train_data.csv` contains energy consumption data of some store for some given days in the past where the store was working at an acceptable level of energy consumption (every day in the train_data can be considered good data, i.e. the store was working at an acceptable level).

The date, energy and enthalpy variables are given. A relationship between enthalpy (average daily outside air enthalpy) and energy (the total store energy consumption) exists (enthalpy is the independent variable, and energy is the dependent variable).

Create a machine learning model that would determine days where the store is not working optimally. Use the model to determine which days in the `test_data.csv` were at an acceptable level of energy consumption, and which days were not (energy consumption is too high).

Explain the method chosen, and why it was chosen. If you made any assumptions, describe them also. You can supply graphs and other visual aids to help explain your solution. Provide all the code as well.

For convenience, `data.csv` contains all data (both the train and the test data) and can be used if needed.


#### Bonus Question: Produce the merge_ranges function.

Produce, in the language of your choice (Python strongly suggested), the `merge_ranges` function.

> This challenge is to produce the code to merge multiple ranges of values if the ranges intersect.

> The function should take a list of `DateRange`, and produces another list of `DateRange` which is the minimum representation of the input.

> A `DateRange` object is simply an object with a `start`, an `end`, with `start <= end`, where `start` and `end` are `date` objects. You can implement this object however you feel is most appropriate for the task.

Example:
Assume `date1 < date2 < date3 < date4 < date5 < date6`, then

+ `merge_ranges([DateRange(date1, date3), DateRange(date2, date4)]) == [DateRange(date1, date4)]`

+ `merge_ranges([DateRange(date1, date3), DateRange(date2, date5), DateRange(date4, date6)]) == [DateRange(date1, date6)]`

+ `merge_ranges([DateRange(date1, date2), DateRange(date3, date5), DateRange(date4, date6)]) == [DateRange(date1, date2), DateRange(date3, date6)]`

