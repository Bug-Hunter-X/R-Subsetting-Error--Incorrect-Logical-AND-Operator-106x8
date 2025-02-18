# R Subsetting Bug
This repository demonstrates a common but subtle error in R programming related to subsetting data frames using logical AND operators. The bug arises from the incorrect use of the element-wise AND operator `&` instead of the logical AND operator `&&` when applying multiple conditions in subsetting. This leads to unexpected results, especially when dealing with multiple conditions.

## Bug Description
The code attempts to subset a data frame based on multiple conditions. The incorrect use of `&` causes the conditions to be evaluated element-wise, leading to the inclusion of rows that do not satisfy both conditions simultaneously. The correct approach involves using the `&&` operator to ensure that both conditions are evaluated for each row as a whole.

## Bug Solution
The solution involves replacing the `&` operator with the `&&` operator in the subsetting condition. This change ensures that both conditions are evaluated logically for each row, resulting in a correct subset of the data frame.