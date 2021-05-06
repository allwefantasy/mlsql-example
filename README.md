# mlsql-example

Usage:

```sql
-- import lib
include lib.`github.com/allwefantasy/mlsql-example` 
where 
-- commit="8b5a0ea7842733115f73c7748c10fb010af46537" and
alias="example";

-- load data
load delta.`python_data.vega_datasets` 
as vega_datasets;

-- use script in mlsql-example to process table.
set targetTable="vega_datasets" ;
set size="1" ;
include local.`example.pkg.util.limit_table`;
```