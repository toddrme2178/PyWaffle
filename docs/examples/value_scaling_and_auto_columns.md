# Value Scaling and Auto-columns

A more common case is, the chart size does not equal to the total number of values. Then the values might be scaled to fit the chart size.

Change argument `rounding_rule` to set a preferred rounding rule when scaling.

> **_NOTE:_** When `rounding_rule` is `ceil` or `nearest`, the total number of scaled value might be greater than chart size, while it would not be shown in the plot. Thus some block numbers might change if the order of values are changed.

With `rounding_rule`=`floor`, the values are scaled to 24, 23, 1 as block numbers.

```python
plt.figure(
    FigureClass=Waffle,
    rows=5,
    columns=10,
    values=[48, 46, 3],
    rounding_rule='floor'
)
```

<img class="img_middle" alt="Rounding rule" src="https://raw.githubusercontent.com/gyli/PyWaffle/master/examples/docs/value_scaling_and_auto_columns_rounding_rule.svg?sanitize=true">

To avoid scaling values as block numbers, pass an integer to either one of `rows` or `columns` parameter only. Then the absolute number of `values` would be used as block number directly and the other parameter would be calculated automatically.

In the following example, we set `rows=5`, `values=[48, 46, 3]` and leave `columns` empty. Then the block numbers would be the same to values. Since the sum of values is 97, the column number has to be 20 to fit all blocks.

```python
plt.figure(
    FigureClass=Waffle,
    rows=5,
    values=[48, 46, 3]
)
```

<img class="img_middle" alt="Ignore columns" src="https://raw.githubusercontent.com/gyli/PyWaffle/master/examples/docs/value_scaling_and_auto_columns_ignore_columns.svg?sanitize=true">
