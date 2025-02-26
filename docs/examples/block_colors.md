# Block Colors

Parameter `colors` accepts colors in a list or tuple. The length must be the same as `values`.

```python
fig = plt.figure(
    FigureClass=Waffle,
    rows=5,
    columns=10,
    values=[48, 46, 3],
    colors=["#983D3D", "#232066", "#DCB732"]
)
```

<img class="img_middle" alt="Block Colors" src="https://raw.githubusercontent.com/gyli/PyWaffle/master/examples/docs/block_colors.svg?sanitize=true">

[Colormap](https://matplotlib.org/gallery/color/colormap_reference.html) could also be applied to waffle chart through parameter `cmap_name`, which sets colors automatically. 

> **_NOTE:_** Sequential colormaps do not work with PyWaffle and only Qualitative colormaps are supported, including `Pastel1`, `Pastel2`, `Paired`, `Accent`, `Dark2`, `Set1`, `Set2`, `Set3`, `tab10`, `tab20`, `tab20b`, `tab20c`.

```python
fig = plt.figure(
    FigureClass=Waffle,
    rows=5,
    columns=10,
    values=[48, 46, 3],
    cmap_name="tab10"
)
```

<img class="img_middle" alt="Block Colors with custom cmap_name" src="https://raw.githubusercontent.com/gyli/PyWaffle/master/examples/docs/block_colors_custom_cmap_name.svg?sanitize=true">
