# Some hints

## 03_capacity_vs_voltage.ipynb

```python

cap2 = c.get_cap(
    cycle=[1, 2, 3, 100, 200, 300],
    label_cycle_number=True,
    categorical_column=True,
    method="forth-and-forth",
    mode="areal",
)

px.line(
    cap2,
    x="capacity",
    y="voltage",
    color="cycle",
    color_discrete_sequence=px.colors.sequential.Viridis,
    title="Areal capacity vs. voltage",
    range_y=[-0.1, 2.1],
    range_x=[-0.01, 0.41],
    width=600,
    height=600,
    labels={"capacity": "Capacity (mAh/cm2)", "voltage": "Voltage (V vs Li/Li+)"},
)
```
