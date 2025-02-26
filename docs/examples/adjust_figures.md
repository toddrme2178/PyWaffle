# Adjust Figures

## Background Color
Parameter `colors` accepts colors in a list or tuple. The length must be the same as `values`.

```python
fig = plt.figure(
    FigureClass=Waffle,
    rows=5,
    columns=10,
    values=[48, 46, 3],
    colors=["#983D3D", "#232066", "#DCB732"]
)
fig.set_facecolor('#DDDDDD')
```

<img class="img_middle" alt="Adjust Figures - Change Background Color" src="https://raw.githubusercontent.com/gyli/PyWaffle/master/examples/docs/adjust_figure_change_background.svg?sanitize=true">

---

## Plot Location

Use parameter `plot_anchor` to change the location of plot in the figure.

```python
fig = plt.figure(
    FigureClass=Waffle,
    rows=5,
    columns=10,
    values=[48, 46, 3],
    plot_anchor='S'
)
fig.set_facecolor('#DDDDDD')
```

<img class="img_middle" alt="Adjust Figures - Change Plot Location" src="https://raw.githubusercontent.com/gyli/PyWaffle/master/examples/docs/adjust_figure_location.svg?sanitize=true">

Parameter `tight` controls whether `tight_layout` in matplotlib is called when drawing.

---

## Tight Layout

By default, PyWaffle sets the figure with tight layout. Thus, when showing the plot, the following warning might pop up:

```
UserWarning: This figure includes Axes that are not compatible with tight_layout, so its results might be incorrect
```

It is usually not an issue when saving the plot to a file, so it could ignored. If you still want to remove the moving, you can either suppress warnings through Python's `warnings` module, or set PyWaffle parameter `tight` to False.