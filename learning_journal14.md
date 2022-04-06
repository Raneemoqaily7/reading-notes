# What I Learned 

- What is seaborn 
seaborn is a python data visulization library based on matplotlib , it provides a high level interface for drawing attractive and informative statiscal graphics.


- To see the code or report a bug,  the GitHub repository.(https://github.com/mwaskom/seaborn)

- Seaborn is a library for making statistical graphics in Python. It builds on top of matplotlib and integrates closely with pandas data structures.

- Seaborn is a library for making statistical graphics in Python. It builds on top of matplotlib and integrates closely with pandas data structures.

- Seaborn is the only library we need to import for this simple example. By convention, it is imported with the shorthand sns. Behind the scenes, seaborn uses matplotlib to draw its plots.

- we use the load_dataset() function to get quick access to an example dataset. 

- This plot shows the relationship between five variables in the tips dataset using a single call to the seaborn function relplot()

- The function relplot() is named that way because it is designed to visualize many different statistical relationships. While scatter plots are often effective, relationships where one variable represents a measure of time are better represented by a line. The relplot() function has a convenient kind parameter that lets you easily switch to this alternate representation:

- When statistical values are estimated, seaborn will use bootstrapping to compute confidence intervals and draw error bars representing the uncertainty of the estimate.

Statistical estimation in seaborn goes beyond descriptive statistics. For example, it is possible to enhance a scatterplot by including a linear regression model (and its uncertainty) using lmplot():

-  Statistical analyses require knowledge about the distribution of variables in your dataset. The seaborn function displot() supports several approaches to visualizing distributions. These include classic techniques like histograms and computationally-intensive approaches like kernel density estimation

- eaborn is a library for making statistical graphics in Python. It provides a high-level interface
to matplotlib and integrates closely with pandas data structures. Functions in the seaborn
library expose a declarative, dataset-oriented API that makes it easy to translate questions
about data into graphics that can answer them. When given a dataset and a specification
of the plot to make, seaborn automatically maps the data values to visual attributes such
as color, size, or style, internally computes statistical transformations, and decorates the plot
with informative axis labels and a legend. Many seaborn functions can generate figures with
multiple panels that elicit comparisons between conditional subsets of data or across different
pairings of variables in a dataset. seaborn is designed to be useful throughout the lifecycle of
a scientific project. By producing complete graphics from a single function call with minimal
arguments, seaborn facilitates rapid prototyping and exploratory data analysis. And by
offering extensive options for customization, along with exposing the underlying matplotlib
objects, it can be used to create polished, publication-quality figures.
