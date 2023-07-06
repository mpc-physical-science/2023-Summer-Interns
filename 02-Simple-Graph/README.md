# Simple Graph

This project will get us started and make some room for experimetation with graphing using python libraries. The goal is to make a simple template for plotting an arbitrary fuction over some range. 

Please watch the first 15 minutes of [this video](https://youtu.be/FpCgG85g2Hw) (*the portion on Plotly Express*) to get an idea as to what *plotly* can do with a small change in parameters. Don't focus on the specific parameters as much as the breadth of types of charts with small changes. Also try to understand why plotting data is so important to understanding the data.

## Installation
1. In a **JupyterLab Terminal window**- `conda install -c conda-forge -c plotly jupyter-dash`
1. Restart Jupyterlab

## Example: plotly.ipynb
Examine the example code in the *plotly* notebook to solve some of the objectives. The assignment for this folder is at the bottom of this page.

## Common API Usage
Use `fig = px.line` to create a new *line* graph then use `fig.show()` to display it.
```python
import plotly.express as px
fig = px.line(
    x=x,
    x=y,
    xaxis_title='xaxis',
    yaxis_title='yaxis',
)

fig.show()
```
To continue to use the same graph, however, update some aspects of the graph, use `fig.update_layout()` followed by `fig.show()`.
```python
fig = px.update_layout(
    title='Title For the Plot',
    width=width_in_pixels,
    height=height_in_pixels
)
fig.show()
```

## Assignment
Be sure to use each step in the assignment in your *Markdown* text for the particular step. This will help document your work. To get started copy the code from the first example "*A simple line graph*" into your notebook then follow the steps below.

### Steps
1. Create a new plotly graph using the values 2, 4, 6,19, 23, 49 for x and 1, 2, 9, 39, 103, 210 for y.
2. Create a new plotly graph using the function y = 3 + x + x^2
3. Update #2 with a title for y showing the function in the title 
4. Update #3 to have a width of 400pixels and a height of 800 pixels
