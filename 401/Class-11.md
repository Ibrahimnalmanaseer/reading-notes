# Data Visualization

## Matplotlib

Matplotlib is probably the single most used Python package for 2D-graphics. It provides both a very quick way to visualize data from Python and publication-quality figures in many formats.

### Simple plot

```
import numpy as np

X = np.linspace(-np.pi, np.pi, 256, endpoint=True)
C, S = np.cos(X), np.sin(X)
```

```
plt.figure(figsize=(10,6), dpi=80)
plt.plot(X, C, color="blue", linewidth=2.5, linestyle="-")
plt.plot(X, S, color="red",  linewidth=2.5, linestyle="-")
```

![exercice_3](https://user-images.githubusercontent.com/62019258/197654766-69f38f03-d9ad-42d6-8c9d-6f9ef0f27d40.png)


### Figures, Subplots, Axes and Ticks

- **Figures** : is the windows in the GUI that has "Figure #" as title. Figures are numbered starting from 1 as opposed to the normal Python way starting from 0.

![rrrr2](https://user-images.githubusercontent.com/62019258/197655418-b26b2c58-131e-4f77-a953-a0104bbd32b7.PNG)

- **Subplots** : With subplot you can arrange plots in a regular grid. You need to specify the number of rows and columns and the number of the plot. Note that the gridspec command is a more powerful alternative.
- **Axes**: are very similar to subplots but allow placement of plots at any location in the figure. So if we want to put a smaller plot inside a bigger one we do so with axes.

- **Ticks** Well formatted ticks are an important part of publishing-ready figures. Matplotlib provides a totally configurable system for ticks. There are tick locators to specify where ticks should appear and tick formatters to give ticks the appearance you want. Major and minor ticks can be located and formatted independently from each other. 
