# Graphing Kinetic Energy

Using the data calculated from [Kinetic-Energy](../01-Kinetic-Energy/), create a plot which uses a *dataframe* to plot the data. While getting the data into a *dataframe* is more complex than a series of lists, this complexity pays off with an ease of printing and plotting the *dataframe*. 

We'll also use dataframes to plot more complex and detailed data from other projects. This assignment will get us started and make some room for experimentation with graphing using python libraries. 

## Dataframe
From [RealPython Pandas Dataframes ](https://realpython.com/pandas-dataframe/):
"*The pandas DataFrame is a structure that contains two-dimensional data and its corresponding labels. DataFrames are widely used in data science, machine learning, scientific computing, and many other data-intensive fields.
DataFrames are similar to SQL tables or the spreadsheets that you work with in Excel or Calc. In many cases, DataFrames are faster, easier to use, and more powerful than tables or spreadsheets because they’re an integral part of the Python and NumPy ecosystems.*"

Scientists like to use dataframes as they are extremely powerful and quite easy to use. Most of the complication of setting up the data is handled in the background so that one can focus on using the data as compared to the complexity of setting up the data to be used. 

Dataframes can be created from a dictionary, which is what we'll use for the Kinetic Energy assignment. A Python dictionary, is an array which allows for sub-scripting with strings, as well as an integer index.

For example a simple dictionary:
```python
car_weights = {
	"Kia": 4502,
	"Ford": 6015,
	"Fiat": 3305,
	"Dodge": 4073
}
print(f"{car_weights}")
{'Kia': 4502, 'Ford': 6015, 'Fiat': 3305, 'Dodge': 4073}
print(f"{car_weights['Kia']}")
4502
```
The dictionary we will want to use for creating our dataframe of kinetic energy is:
```python
table = {
    "Speeds": ["school", "town", "highway"],
    "Kia": [],
    "Ford": [],
    "Fiat": [],
    "Dodge": []
}
```
The first element 'Speeds' contains a list which describes the 3 speeds at which we want to show. The next four elements are referenced by the car names and also have an empty list, for which we will fill with the kinetic energy at each speed.

## Elements to Consider
* Similar to using plotly, where we needed to install plotly with-in Jupyterlab. We will need to install *numpy* and *pandas*:
	1. In a **JupyterLab Terminal window**- `conda install -c conda-forge -c numpy pandas`
	1. Restart Jupyterlab
* Python Pandas commands required
	```python
	# To use pandas, we will need to import it
	import pandas as pd
	# to convert our dictionary to a dataframe
	df = pd.DataFrame(table)
	# to make our numbers look like we wish
	pd.set_option('float_format', '{:,.2f}'.format)
	display(df)
	# use the plotly commands from assignment 2 to plot data
	fig = px.line(df, x='Speeds(mph)', y=['Kia', 'Ford', "Fiat", "Dodge"])
	# add fig.update commands to add titles, subtitles and appropriate size to plot
	```
