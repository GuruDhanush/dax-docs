---
name: AddColumns
shortDescription: Adds calculated columns to table expression.
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
returnDescription: Returns table with new column added

examples:
  - code: = ADDCOLUMNS(
                Employee,
                "NewColumn", 1
                "NewColumn2", 2
                )
    description: |
      The following formula returns table with columns of Employee along with 'NewColumn' and 'NewColumn2' columns 

eleventyNavigation:
  key: AddColumns
  parent: Table

lastUpdated: 2022-1-11
tags:
  - Table
layout: layouts/post.njk
---
  * Multiple column and expressions can be added to AddColumns.
  * Minimum of one column needs to be added. 