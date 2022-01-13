---
name: TopN
shortDescription: Adds calculated columns to table expression.
parameters:
  - name: n_value
    definition: Number or DAX expression that returns a number.
    datatype: Number
  - name: table
    definition: Table from which rows need to be pulled.
    datatype: Table
  - name: order_by_expression
    definition: DAX expression that is used to sort the table.
    datatype: Any
  - name: order
    definition: Defines sort order. 0 (default) for descending order and 1 for ascending order.
    datatype: Number
    optional: true
returnType: Table
returnDescription: Table with n_value rows.  

examples:
  - code: = TOPN(
                5
                Employee,
                "CurrentSalaray", 0
                "DateOfJoining", 1
                )
    description: |
      The following formula returns table with top 5 employees with highest current salary followed by checking earlier date of joining if there are ties   
  
eleventyNavigation:
  key: TopN
  parent: Table

lastUpdated: 2022-1-13
tags:
  - Table
layout: layouts/post.njk
---
  * Rows returned by TopN function are not sorted in any order.
  * TopN returns empty table if n_value is less than or equal to zero.
  * If there is a tie at Nth rows, then all rows under tie are returned. This can lead to return of more than n_value rows.