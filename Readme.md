# Horizontal partitioning (Postgres SQL).

1. Create a Main table (which will consist different partition).

   Syntax => Create table table_name (fields) partition by range (column_name);.

2. Create child tables.

   Syntax just same as a Normal table.

4. Now alter attach these table to main table.

   Syntax => alter table main_table attach partition child_table_name for values from (value1) to (value2);


   Now after inserting any record into main table then it will automatically into  one of the child table based on the range values.
