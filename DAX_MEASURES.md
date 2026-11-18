# DAX measures from the supplied semantic model

## Total Revenue

```dax
SUM(Sales[Revenue])
```

## Estimated Cost

```dax
SUM(Sales[EstimatedCost])
```

## Estimated Profit

```dax
[Total Revenue] - [Estimated Cost]
```

## Profit Margin %

```dax
DIVIDE([Estimated Profit], [Total Revenue])
```

## Orders

```dax
DISTINCTCOUNT(Sales[OrderID])
```

## Units Sold

```dax
SUM(Sales[Quantity])
```

## Customers

```dax
DISTINCTCOUNT(Sales[CustomerID])
```

## Average Order Value

```dax
DIVIDE([Total Revenue], [Orders])
```

## Target GBP

```dax
SUM(Targets[TargetGBP])
```

## Target Achievement %

```dax
DIVIDE([Total Revenue], [Target GBP])
```

## Target Variance GBP

```dax
[Total Revenue] - [Target GBP]
```

## Revenue (PY)

```dax
CALCULATE([Total Revenue], SAMEPERIODLASTYEAR('Calendar'[Date]))
```

## Revenue YoY %

```dax
DIVIDE([Total Revenue] - [Revenue (PY)], [Revenue (PY)])
```

## Profit (PY)

```dax
CALCULATE([Estimated Profit], SAMEPERIODLASTYEAR('Calendar'[Date]))
```

## Profit YoY %

```dax
DIVIDE([Estimated Profit] - [Profit (PY)], [Profit (PY)])
```

## Orders (PY)

```dax
CALCULATE([Orders], SAMEPERIODLASTYEAR('Calendar'[Date]))
```

## Orders YoY %

```dax
DIVIDE([Orders] - [Orders (PY)], [Orders (PY)])
```

## Units (PY)

```dax
CALCULATE([Units Sold], SAMEPERIODLASTYEAR('Calendar'[Date]))
```

## Units YoY %

```dax
DIVIDE([Units Sold] - [Units (PY)], [Units (PY)])
```

## Profit Margin (PY)

```dax
CALCULATE([Profit Margin %], SAMEPERIODLASTYEAR('Calendar'[Date]))
```

## Margin Change pp

```dax
([Profit Margin %] - [Profit Margin (PY)]) * 100
```

## Target Gap pp

```dax
([Target Achievement %] - 1) * 100
```
