---
name: Average
shortDescription: Returns average of all the numbers in column.
parameters:
  - name: column
    definition: The column for which average needs to be calculated
    datatype: Column
returnType: decimal
returnDescription: Returns decimal value which is mean of all numbers from column

examples:
  - code: = AVERAGE(Employee[CurrentSalary])
    description: |
      The following formula returns average of CurrentSalaray from Employee table.

related:
  - averagea

eleventyNavigation:
  key: Average
  parent: Aggregation

lastUpdated: 2022-1-9
tags:
  - Aggregation
layout: layouts/post.njk
---
  * Returns blank if column contains text.
  * Zeroes are counted toward average count but blank values are ignored.