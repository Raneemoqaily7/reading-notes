# Data Visualization

## What is Data Visualization?
Data visualization is a field in data analysis that deals with visual representation of data. It graphically plots data and is an effective way to communicate inferences from data.

## Data Visualization in Python
Python offers several plotting libraries, namely Matplotlib, Seaborn and many other such data visualization packages with different features for creating informative, customized, and appealing plots to present data in the most simple and effective way.

**Matplotlib**

- It is used for basic graph plotting like line charts,  bar graphs, etc.

- It mainly works with datasets and arrays.

- Seaborn is considerably more organized and functional than Matplotlib and treats the entire dataset as a solitary unit.

**Seaborn**
- It is mainly used for statistics visualization and can perform complex visualizations with fewer commands.

- It works with entire datasets

- Matplotlib acts productively with data arrays and frames. It regards the aces and figures as objects.

**Line Charts**

A Line chart is a graph that represents information as a series of data points connected by a straight line. In line charts, each data point or marker is plotted and connected with a line or curve. 

**Using Matplotlib**
We are using random data points to represent the yield of apples. 
[Data_Visualization](https://www.simplilearn.com/ice9/free_resources_article_thumb/Data_Visualization_in_Python/Data_Visualization_in_Python_3.png. )


## A note on the Object-Oriented API vs. Pyplot
Matplotlib has two interfaces. The first is an object-oriented (OO) interface. In this case, we utilize an instance of axes.Axes in order to render visualizations on an instance of figure.Figure.

The second is based on MATLAB and uses a state-based interface. This is encapsulated in the pyplot module. See the pyplot tutorials for a more in-depth look at the pyplot interface.

Most of the terms are straightforward but the main thing to remember is that:

The Figure is the final image that may contain 1 or more Axes.

The Axes represent an individual plot (don't confuse this with the word "axis", which refers to the x/y axis of a plot).

We call methods that do the plotting directly from the Axes, which gives us much more flexibility and power in customizing our plot.

Note

In general, try to use the object-oriented interface over the pyplot interface.

matplotlib.spines
class matplotlib.spines.Spine(axes, spine_type, path, **kwargs)[source]
Bases: matplotlib.patches.Patch

An axis spine -- the line noting the data area boundaries.

Spines are the lines connecting the axis tick marks and noting the boundaries of the data area. They can be placed at arbitrary positions. See set_position for more information.

The default position is ('outward', 0).

Spines are subclasses of Patch, and inherit much of their behavior.

Spines draw a line, a circle, or an arc depending if set_patch_line, set_patch_circle, or set_patch_arc has been called. Line-like is the default.

Parameters
axesAxes
The Axes instance containing the spine.

spine_typestr
The spine type.

pathPath
The Path instance used to draw the spine.

Other Parameters
**kwargs
  - clear()
Clear the current spine.


- draw(renderer)
Draw the Artist (and its children) using the given renderer.

This has no effect if the artist is not visible (Artist.get_visible returns False).

Parameters
rendererRendererBase subclass.
Notes

- get_bounds(
Get the bounds of the spine.


- get_patch_transform(
Return the Transform instance mapping patch coordinates to data coordinates.

For example, one may define a patch of a circle which represents a radius of 5 by providing coordinates for a unit circle, and a transform which scales the coordinates (the patch coordinate) by 5.

