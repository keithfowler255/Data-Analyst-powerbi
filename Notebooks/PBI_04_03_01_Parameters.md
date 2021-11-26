# Parameters

- let us assume development servername and database name
    - Server name: rritec
    - Databasename: Adventureworksdw2012

- let us assume Testing servername and database name
    - Server name: rritec_test
    - Databasename: Adventureworksdw2012_test

- let us assume production servername and database name
    - Server name: rritec_prod
    - Databasename: Adventureworksdw2012_prod
- Import three tables DimDate,DimCustomer and FactInternetSales tables from sqlserver and observe M-Language source line of code of each query
- Create two paramatrs with the name of Servername and DBName and passvalues as rritec and AdventureWorksDW2012 respectively
- Double click on each Query source step and change static values to above parameters.


## Reference M-Language
let
    Source = Sql.Database("rritec", "AdventureWorksDW2012"),
    dbo_DimDate = Source{[Schema="dbo",Item="DimDate"]}[Data]
in
    dbo_DimDate

let
    Source = Sql.Database("rritec", "AdventureWorksDW2012"),
    dbo_DimCustomer = Source{[Schema="dbo",Item="DimCustomer"]}[Data]
in
    dbo_DimCustomer

let
    Source = Sql.Database("rritec", "AdventureWorksDW2012"),
    dbo_FactInternetSales = Source{[Schema="dbo",Item="FactInternetSales"]}[Data],
    #"Filtered Rows" = Table.SelectRows(dbo_FactInternetSales, each [OrderDate] >= RangeStart and [OrderDate] <= RangeEnd)
in
    #"Filtered Rows"
