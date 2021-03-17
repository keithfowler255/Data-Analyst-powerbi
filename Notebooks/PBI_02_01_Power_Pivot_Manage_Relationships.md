
# Power Pivot
  1. It is useful to do two activities
    - Relation Ships
      - Relation ship(Among Tables) Vs Join(Among Queries)
      - Cardinality
        - One to One
        - One to Many
        - **Many to One**
        - Many to Many
      - Directions
        - **Single**
        - Both
      - Active Vs Inactive Relationships      
    - DAX Calculations
  
## Manage Relationships

https://docs.microsoft.com/en-us/power-bi/desktop-create-and-manage-relationships

https://docs.microsoft.com/en-us/power-bi/guidance/relationships-bidirectional-filtering

https://docs.microsoft.com/en-us/archive/blogs/cansql/relationships-in-power-bi-fixing-one-of-the-columns-must-have-unique-values-error-message

1. each table of database by default acting as one query

## Questions
----
1. What is composite models ?
  
    A model that combines data from more than one DirectQuery source or that combines DirectQuery with import data is called a composite model

    For more information refer [doc](https://docs.microsoft.com/en-us/power-bi/transform-model/desktop-composite-models#:~:text=A%20model%20that%20combines%20data,tables%20come%20from%20different%20sources.)

2. How many carinality's available?
  - One to One
  - One to Many
  - Many to One
  - Many to Many
    - Old versions of Power BI not supported. 
3. Fact to Dim what type of cardinality possible?
  - Many to One
4. Without Relationship, between two tables,will we get right data?
  - Wrong Data
5. Power BI creats relationships automatically based on what?
  - Column Names
6. Can you create Joins manually if column names are different?
  - Yes
7. Explain Single Vs Bi-directional Filters?
  - https://docs.microsoft.com/en-us/power-bi/guidance/relationships-bidirectional-filtering
8. What are the disadvantage of Bi-directional Join?
  - Negatively impact on model query performance
  - User confusing experiences
9. When to go for Bi-Directional Join? or Advantages of Bi-directional?
  - Special model relationships
    - one to one cardinality tables
    - Many to Many Cardinality Tables
    - **Note:** 99.99% we will have many to one relation tables in any dataset
  - Slicer items "with data"
  - Dimension-to-dimension analysis
  
  
   



```python

```
