---
name: AverageA
shortDescription: Returns average of all the values in column. Handles non-numeric values unlike Average
parameters:
  - name: column
    definition: The column for which average needs to be calculated
    datatype: Column
returnType: decimal
returnDescription: Returns decimal value which is mean of all the values from column
examples:
  - code: = AVERAGE(Employee[CurrentSalary])
    description: |
      The following formula returns average of CurrentSalaray from Employee table.

related:
  - average

eleventyNavigation:
  key: Average
  parent: Aggregation

lastUpdated: 2022-1-9
tags:
  - Aggregation
layout: layouts/post.njk
---
 * Handling of non-numeric types
    - Values that evaluate to True are counted as 1.
    - Values that evaluate to True are counted as 0.
    - Values that contain text values are counted as 0.
  * Returns blank if there are no rows
