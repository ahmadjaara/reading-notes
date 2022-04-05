# Matplotlib

matplotlib is probably the single most used Python package for 2D-graphics. It provides both a very quick way to visualize data from Python and publication-quality figures in many formats. We are going to explore matplotlib in interactive mode covering most common cases.

code to import it
import matplotlib.pyplot as plt

simple plot

code :

    import numpy as np

    X = np.linspace(-np.pi, np.pi, 256, endpoint=True)
    C, S = np.cos(X), np.sin(X)

to plot the sin and the cos graph using **linespace** to determine the value of the x axis

Changing colors and line widths

    plt.plot(X, C, color="blue", linewidth=2.5, linestyle="-")

Setting limits

    plt.xlim(X.min()*1.1, X.max()*1.1)

Setting ticks

to change the apperance of the value in plot

    plt.xticks( [-np.pi, -np.pi/2, 0, np.pi/2, np.pi])
Moving spines

Spines are the lines connecting the axis tick marks and noting the boundaries of the data area.

    ax.spines['right'].set_color('none')
    ax.spines['top'].set_color('none')
Adding a legend

    plt.legend(loc='upper left', frameon=False)

Figures

A figure is the windows in the GUI that has "Figure #" as title. Figures are numbered starting from 1 as opposed to the normal Python way starting from 0. 

Subplots

With subplot you can arrange plots in a regular grid. You need to specify the number of rows and columns and the number of the plot. 

Axes

Axes are very similar to subplots but allow placement of plots at any location in the figure. So if we want to put a smaller plot inside a bigger one we do so with axes.

Animation

The most easy way to make an animation in matplotlib is to declare a FuncAnimation object that specifies to matplotlib what is the figure to update, what is the update function and what is the delay between frames.
