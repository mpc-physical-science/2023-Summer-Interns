# Average Calc

This notebook will take as input a (variable length) list of values from the user.

The following should be calculated and clearly displayed:
- the number of values supplied
- the mean of the values
- the standard deviation of the values

## Functions to Consider
* len(x) - returns the number elements in list *x*
* string.split(separator, maxsplit) - splits a string into a list
	* separator - Specifies the separator to use when splitting the string (optional)
	* maxsplit -  Specifies how many splits to do. Default value is -1, which is "all occurrences" (optional)
* statistics.stdev(x) - returns the standard deviation of the values in *x*, requires `import statistics` prior to using