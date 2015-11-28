
# SQL queries

# Find all rows that have an ingredient name of Brussels sprouts.
  EXPLAIN ANALYSE SELECT * FROM ingredients WHERE name = 'Brussels sprouts';

#Calculate the total count of rows of ingredients with a name of Brussels sprouts.
  EXPLAIN ANALYSE SELECT COUNT(*) FROM ingredients WHERE name = 'Brussels sprouts';

#Find all Brussels sprouts ingredients having a unit type of gallon(s).
  EXPLAIN ANALYSE SELECT * FROM ingredients WHERE name = 'Brussels sprouts' AND unit = 'gallon(s)';

#Find all rows that have a unit type of gallon(s), a name of Brussels sprouts or has the letter j in it.
  EXPLAIN ANALYSE SELECT * FROM ingredients WHERE (name = 'Brussels sprouts' OR name LIKE '%j%') AND unit = 'gallon(s)';


#Without indexing
![alt](https://www.dropbox.com/s/l7x7x35368d0351/without_index.png?dl=0)

#Indexing database
  CREATE INDEX ON ingredients(name);

#With indexing
![alt](https://www.dropbox.com/s/s557nd94wh7zi21/with_index.png?dl=0)
