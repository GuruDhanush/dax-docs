---
name: SelectColumns
shortDescription: Adds calculated columns to table expression with each column for each pair of name and expression.
parameters:
  - name: table
    definition: Table or table expression for which columns need to be added.
    datatype: Table
  - name: name
    definition: Name of the column to be added.
    datatype: String
  - name: expression
    definition: DAX expression that returns a value for each row of passed table.
returnType: Table
returnDescription: Returns table with same rows as passed table but with columns equal to count of name and expressions passed. All the other columns are removed

examples:
  - code: = SELECTCOLUMNS(
                Employee,
                "NewColumn", 1
                "NewColumn2", 2
                )
    description: |
      The following formula returns table with 'NewColumn' and 'NewColumn2' columns. Other columns from Employee are removed.  

related:
  - addcolumns

eleventyNavigation:
  key: SelectColumns
  parent: Table

lastUpdated: 2022-1-13
tags:
  - Table
layout: layouts/post.njk
---
  * SELECTCOLUMNS and ADDCOLUMNS has function signature.