# Data dictionary

Synthetic demonstration data extracted from the supplied model.

## Sales

| Column | Data type |
|---|---|
| OrderID | string |
| OrderDate | dateTime |
| CustomerID | string |
| ProductID | string |
| Region | string |
| Quantity | int64 |
| Revenue | double |
| EstimatedCost | double |

## Customers

| Column | Data type |
|---|---|
| CustomerID | string |
| CustomerName | string |
| Segment | string |
| Region | string |

## Products

| Column | Data type |
|---|---|
| ProductID | string |
| ProductName | string |
| Category | string |
| UnitPrice | double |
| UnitCost | double |

## Targets

| Column | Data type |
|---|---|
| Year | int64 |
| Month | int64 |
| Region | string |
| TargetGBP | double |
| TargetDate | dateTime |

## Calendar

| Column | Data type |
|---|---|
| Date | dateTime |
| Year | int64 |
| Month | int64 |
| MonthName | string |
