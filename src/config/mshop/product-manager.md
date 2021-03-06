
# decorators
## excludes

Excludes decorators added by the "common" option from the product manager

```
mshop/product/manager/decorators/excludes = Array
(
)
```

* Default: Array
* Type: array - List of decorator names
* Since: 2014.03

Decorators extend the functionality of a class by adding new aspects
(e.g. log what is currently done), executing the methods of the underlying
class only in certain conditions (e.g. only for logged in users) or
modify what is returned to the caller.

This option allows you to remove a decorator added via
"mshop/common/manager/decorators/default" before they are wrapped
around the product manager.

```
 mshop/product/manager/decorators/excludes = array( 'decorator1' )
```

This would remove the decorator named "decorator1" from the list of
common decorators ("\Aimeos\MShop\Common\Manager\Decorator\*") added via
"mshop/common/manager/decorators/default" for the product manager.

See also:

* mshop/common/manager/decorators/default
* mshop/product/manager/decorators/global
* mshop/product/manager/decorators/local

## global

Adds a list of globally available decorators only to the product manager

```
mshop/product/manager/decorators/global = Array
(
    [0] => Changelog
)
```

* Default: Array
* Type: array - List of decorator names
* Since: 2014.03

Decorators extend the functionality of a class by adding new aspects
(e.g. log what is currently done), executing the methods of the underlying
class only in certain conditions (e.g. only for logged in users) or
modify what is returned to the caller.

This option allows you to wrap global decorators
("\Aimeos\MShop\Common\Manager\Decorator\*") around the product manager.

```
 mshop/product/manager/decorators/global = array( 'decorator1' )
```

This would add the decorator named "decorator1" defined by
"\Aimeos\MShop\Common\Manager\Decorator\Decorator1" only to the product
manager.

See also:

* mshop/common/manager/decorators/default
* mshop/product/manager/decorators/excludes
* mshop/product/manager/decorators/local

## local

Adds a list of local decorators only to the product manager

```
mshop/product/manager/decorators/local = Array
(
)
```

* Default: Array
* Type: array - List of decorator names
* Since: 2014.03

Decorators extend the functionality of a class by adding new aspects
(e.g. log what is currently done), executing the methods of the underlying
class only in certain conditions (e.g. only for logged in users) or
modify what is returned to the caller.

This option allows you to wrap local decorators
("\Aimeos\MShop\Product\Manager\Decorator\*") around the product manager.

```
 mshop/product/manager/decorators/local = array( 'decorator2' )
```

This would add the decorator named "decorator2" defined by
"\Aimeos\MShop\Product\Manager\Decorator\Decorator2" only to the product
manager.

See also:

* mshop/common/manager/decorators/default
* mshop/product/manager/decorators/excludes
* mshop/product/manager/decorators/global

# lists
## decorators/excludes

Excludes decorators added by the "common" option from the product list manager

```
mshop/product/manager/lists/decorators/excludes = Array
(
)
```

* Default: Array
* Type: array - List of decorator names
* Since: 2014.03

Decorators extend the functionality of a class by adding new aspects
(e.g. log what is currently done), executing the methods of the underlying
class only in certain conditions (e.g. only for logged in users) or
modify what is returned to the caller.

This option allows you to remove a decorator added via
"mshop/common/manager/decorators/default" before they are wrapped
around the product list manager.

```
 mshop/product/manager/lists/decorators/excludes = array( 'decorator1' )
```

This would remove the decorator named "decorator1" from the list of
common decorators ("\Aimeos\MShop\Common\Manager\Decorator\*") added via
"mshop/common/manager/decorators/default" for the product list manager.

See also:

* mshop/common/manager/decorators/default
* mshop/product/manager/lists/decorators/global
* mshop/product/manager/lists/decorators/local

## decorators/global

Adds a list of globally available decorators only to the product list manager

```
mshop/product/manager/lists/decorators/global = Array
(
)
```

* Default: Array
* Type: array - List of decorator names
* Since: 2014.03

Decorators extend the functionality of a class by adding new aspects
(e.g. log what is currently done), executing the methods of the underlying
class only in certain conditions (e.g. only for logged in users) or
modify what is returned to the caller.

This option allows you to wrap global decorators
("\Aimeos\MShop\Common\Manager\Decorator\*") around the product list
manager.

```
 mshop/product/manager/lists/decorators/global = array( 'decorator1' )
```

This would add the decorator named "decorator1" defined by
"\Aimeos\MShop\Common\Manager\Decorator\Decorator1" only to the product
list manager.

See also:

* mshop/common/manager/decorators/default
* mshop/product/manager/lists/decorators/excludes
* mshop/product/manager/lists/decorators/local

## decorators/local

Adds a list of local decorators only to the product list manager

```
mshop/product/manager/lists/decorators/local = Array
(
)
```

* Default: Array
* Type: array - List of decorator names
* Since: 2014.03

Decorators extend the functionality of a class by adding new aspects
(e.g. log what is currently done), executing the methods of the underlying
class only in certain conditions (e.g. only for logged in users) or
modify what is returned to the caller.

This option allows you to wrap local decorators
("\Aimeos\MShop\Product\Manager\Lists\Decorator\*") around the product
list manager.

```
 mshop/product/manager/lists/decorators/local = array( 'decorator2' )
```

This would add the decorator named "decorator2" defined by
"\Aimeos\MShop\Product\Manager\Lists\Decorator\Decorator2" only to the
product list manager.

See also:

* mshop/common/manager/decorators/default
* mshop/product/manager/lists/decorators/excludes
* mshop/product/manager/lists/decorators/global

## name

Class name of the used product list manager implementation

```
mshop/product/manager/lists/name = Standard
```

* Default: Standard
* Type: string - Last part of the class name
* Since: 2014.03

Each default product list manager can be replaced by an alternative imlementation.
To use this implementation, you have to set the last part of the class
name as configuration value so the manager factory knows which class it
has to instantiate.

For example, if the name of the default class is

```
 \Aimeos\MShop\Product\Manager\Lists\Standard
```

and you want to replace it with your own version named

```
 \Aimeos\MShop\Product\Manager\Lists\Mylist
```

then you have to set the this configuration option:

```
 mshop/product/manager/lists/name = Mylist
```

The value is the last part of your own class name and it's case sensitive,
so take care that the configuration value is exactly named like the last
part of the class name.

The allowed characters of the class name are A-Z, a-z and 0-9. No other
characters are possible! You should always start the last part of the class
name with an upper case character and continue only with lower case characters
or numbers. Avoid chamel case names like "MyList"!


## standard/aggregate/ansi

Counts the number of records grouped by the values in the key column and matched by the given criteria

```
mshop/product/manager/lists/standard/aggregate/ansi = 
 SELECT "key", COUNT("id") AS "count"
 FROM (
 	SELECT :key AS "key", mproli."id" AS "id"
 	FROM "mshop_product_list" AS mproli
 	:joins
 	WHERE :cond
 	GROUP BY :key, mproli."id"
 	ORDER BY :order
 	OFFSET :start ROWS FETCH NEXT :size ROWS ONLY
 ) AS list
 GROUP BY "key"
```

* Default: mshop/product/manager/lists/standard/aggregate
* Type: string - SQL statement for aggregating order items
* Since: 2014.07

Groups all records by the values in the key column and counts their
occurence. The matched records can be limited by the given criteria
from the order database. The records must be from one of the sites
that are configured via the context item. If the current site is part
of a tree of sites, the statement can count all records from the
current site and the complete sub-tree of sites.

As the records can normally be limited by criteria from sub-managers,
their tables must be joined in the SQL context. This is done by
using the "internaldeps" property from the definition of the ID
column of the sub-managers. These internal dependencies specify
the JOIN between the tables and the used columns for joining. The
":joins" placeholder is then replaced by the JOIN strings from
the sub-managers.

To limit the records matched, conditions can be added to the given
criteria object. It can contain comparisons like column names that
must match specific values which can be combined by AND, OR or NOT
operators. The resulting string of SQL conditions replaces the
":cond" placeholder before the statement is sent to the database
server.

This statement doesn't return any records. Instead, it returns pairs
of the different values found in the key column together with the
number of records that have been found for that key values.

The SQL statement should conform to the ANSI standard to be
compatible with most relational database systems. This also
includes using double quotes for table and column names.

See also:

* mshop/product/manager/lists/standard/insert/ansi
* mshop/product/manager/lists/standard/update/ansi
* mshop/product/manager/lists/standard/newid/ansi
* mshop/product/manager/lists/standard/delete/ansi
* mshop/product/manager/lists/standard/search/ansi
* mshop/product/manager/lists/standard/count/ansi

## standard/aggregate/mysql

Counts the number of records grouped by the values in the key column and matched by the given criteria

```
mshop/product/manager/lists/standard/aggregate/mysql = 
 SELECT "key", COUNT("id") AS "count"
 FROM (
 	SELECT :key AS "key", mproli."id" AS "id"
 	FROM "mshop_product_list" AS mproli
 	:joins
 	WHERE :cond
 	GROUP BY :key, mproli."id"
 	ORDER BY :order
 	LIMIT :size OFFSET :start
 ) AS list
 GROUP BY "key"
```

* Default: 
 SELECT "key", COUNT("id") AS "count"
 FROM (
 	SELECT :key AS "key", mproli."id" AS "id"
 	FROM "mshop_product_list" AS mproli
 	:joins
 	WHERE :cond
 	GROUP BY :key, mproli."id"
 	ORDER BY :order
 	OFFSET :start ROWS FETCH NEXT :size ROWS ONLY
 ) AS list
 GROUP BY "key"


See also:

* mshop/product/manager/lists/standard/aggregate/ansi

## standard/count/ansi

Counts the number of records matched by the given criteria in the database

```
mshop/product/manager/lists/standard/count/ansi = 
 SELECT COUNT(*) AS "count"
 FROM (
 	SELECT mproli."id"
 	FROM "mshop_product_list" AS mproli
 	:joins
 	WHERE :cond
 	ORDER BY mproli."id"
 	OFFSET 0 ROWS FETCH NEXT 10000 ROWS ONLY
 ) AS list
```

* Default: mshop/product/manager/lists/standard/count
* Type: string - SQL statement for counting items
* Since: 2014.03

Counts all records matched by the given criteria from the product
database. The records must be from one of the sites that are
configured via the context item. If the current site is part of
a tree of sites, the statement can count all records from the
current site and the complete sub-tree of sites.

As the records can normally be limited by criteria from sub-managers,
their tables must be joined in the SQL context. This is done by
using the "internaldeps" property from the definition of the ID
column of the sub-managers. These internal dependencies specify
the JOIN between the tables and the used columns for joining. The
":joins" placeholder is then replaced by the JOIN strings from
the sub-managers.

To limit the records matched, conditions can be added to the given
criteria object. It can contain comparisons like column names that
must match specific values which can be combined by AND, OR or NOT
operators. The resulting string of SQL conditions replaces the
":cond" placeholder before the statement is sent to the database
server.

Both, the strings for ":joins" and for ":cond" are the same as for
the "search" SQL statement.

Contrary to the "search" statement, it doesn't return any records
but instead the number of records that have been found. As counting
thousands of records can be a long running task, the maximum number
of counted records is limited for performance reasons.

The SQL statement should conform to the ANSI standard to be
compatible with most relational database systems. This also
includes using double quotes for table and column names.

See also:

* mshop/product/manager/lists/standard/insert/ansi
* mshop/product/manager/lists/standard/update/ansi
* mshop/product/manager/lists/standard/newid/ansi
* mshop/product/manager/lists/standard/delete/ansi
* mshop/product/manager/lists/standard/search/ansi
* mshop/product/manager/lists/standard/aggregate/ansi

## standard/count/mysql

Counts the number of records matched by the given criteria in the database

```
mshop/product/manager/lists/standard/count/mysql = 
 SELECT COUNT(*) AS "count"
 FROM (
 	SELECT mproli."id"
 	FROM "mshop_product_list" AS mproli
 	:joins
 	WHERE :cond
 	ORDER BY mproli."id"
 	LIMIT 10000 OFFSET 0
 ) AS list
```

* Default: 
 SELECT COUNT(*) AS "count"
 FROM (
 	SELECT mproli."id"
 	FROM "mshop_product_list" AS mproli
 	:joins
 	WHERE :cond
 	ORDER BY mproli."id"
 	OFFSET 0 ROWS FETCH NEXT 10000 ROWS ONLY
 ) AS list


See also:

* mshop/product/manager/lists/standard/count/ansi

## standard/delete/ansi

Deletes the items matched by the given IDs from the database

```
mshop/product/manager/lists/standard/delete/ansi = 
 DELETE FROM "mshop_product_list"
 WHERE :cond AND siteid = ?
```

* Default: mshop/product/manager/lists/standard/delete
* Type: string - SQL statement for deleting items
* Since: 2014.03

Removes the records specified by the given IDs from the product database.
The records must be from the site that is configured via the
context item.

The ":cond" placeholder is replaced by the name of the ID column and
the given ID or list of IDs while the site ID is bound to the question
mark.

The SQL statement should conform to the ANSI standard to be
compatible with most relational database systems. This also
includes using double quotes for table and column names.

See also:

* mshop/product/manager/lists/standard/insert/ansi
* mshop/product/manager/lists/standard/update/ansi
* mshop/product/manager/lists/standard/newid/ansi
* mshop/product/manager/lists/standard/search/ansi
* mshop/product/manager/lists/standard/count/ansi
* mshop/product/manager/lists/standard/aggregate/ansi

## standard/delete/mysql

Deletes the items matched by the given IDs from the database

```
mshop/product/manager/lists/standard/delete/mysql = 
 DELETE FROM "mshop_product_list"
 WHERE :cond AND siteid = ?
```

* Default: 
 DELETE FROM "mshop_product_list"
 WHERE :cond AND siteid = ?


See also:

* mshop/product/manager/lists/standard/delete/ansi

## standard/insert/ansi

Inserts a new product list record into the database table

```
mshop/product/manager/lists/standard/insert/ansi = 
 INSERT INTO "mshop_product_list" ( :names
 	"parentid", "key", "type", "domain", "refid", "start", "end",
 	"config", "pos", "status", "mtime", "editor", "siteid", "ctime"
 ) VALUES ( :values
 	?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?
 )
```

* Default: mshop/product/manager/lists/standard/insert
* Type: string - SQL statement for inserting records
* Since: 2014.03

Items with no ID yet (i.e. the ID is NULL) will be created in
the database and the newly created ID retrieved afterwards
using the "newid" SQL statement.

The SQL statement must be a string suitable for being used as
prepared statement. It must include question marks for binding
the values from the product list item to the statement before they are
sent to the database server. The number of question marks must
be the same as the number of columns listed in the INSERT
statement. The order of the columns must correspond to the
order in the saveItems() method, so the correct values are
bound to the columns.

The SQL statement should conform to the ANSI standard to be
compatible with most relational database systems. This also
includes using double quotes for table and column names.

See also:

* mshop/product/manager/lists/standard/update/ansi
* mshop/product/manager/lists/standard/newid/ansi
* mshop/product/manager/lists/standard/delete/ansi
* mshop/product/manager/lists/standard/search/ansi
* mshop/product/manager/lists/standard/count/ansi
* mshop/product/manager/lists/standard/aggregate/ansi

## standard/insert/mysql

Inserts a new product list record into the database table

```
mshop/product/manager/lists/standard/insert/mysql = 
 INSERT INTO "mshop_product_list" ( :names
 	"parentid", "key", "type", "domain", "refid", "start", "end",
 	"config", "pos", "status", "mtime", "editor", "siteid", "ctime"
 ) VALUES ( :values
 	?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?
 )
```

* Default: 
 INSERT INTO "mshop_product_list" ( :names
 	"parentid", "key", "type", "domain", "refid", "start", "end",
 	"config", "pos", "status", "mtime", "editor", "siteid", "ctime"
 ) VALUES ( :values
 	?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?
 )


See also:

* mshop/product/manager/lists/standard/insert/ansi

## standard/newid/ansi

Retrieves the ID generated by the database when inserting a new record

```
mshop/product/manager/lists/standard/newid/ansi = mshop/product/manager/lists/standard/newid
```

* Default: mshop/product/manager/lists/standard/newid
* Type: string - SQL statement for retrieving the last inserted record ID
* Since: 2014.03

As soon as a new record is inserted into the database table,
the database server generates a new and unique identifier for
that record. This ID can be used for retrieving, updating and
deleting that specific record from the table again.

For MySQL:
```
 SELECT LAST_INSERT_ID()
For PostgreSQL:
 SELECT currval('seq_mproli_id')
For SQL Server:
 SELECT SCOPE_IDENTITY()
For Oracle:
 SELECT "seq_mproli_id".CURRVAL FROM DUAL
```

There's no way to retrive the new ID by a SQL statements that
fits for most database servers as they implement their own
specific way.

See also:

* mshop/product/manager/lists/standard/insert/ansi
* mshop/product/manager/lists/standard/update/ansi
* mshop/product/manager/lists/standard/delete/ansi
* mshop/product/manager/lists/standard/search/ansi
* mshop/product/manager/lists/standard/count/ansi
* mshop/product/manager/lists/standard/aggregate/ansi

## standard/newid/mysql

Retrieves the ID generated by the database when inserting a new record

```
mshop/product/manager/lists/standard/newid/mysql = SELECT LAST_INSERT_ID()
```

* Default: mshop/product/manager/lists/standard/newid

See also:

* mshop/product/manager/lists/standard/newid/ansi

## standard/search/ansi

Retrieves the records matched by the given criteria in the database

```
mshop/product/manager/lists/standard/search/ansi = 
 SELECT :columns
 	mproli."id" AS "product.lists.id", mproli."parentid" AS "product.lists.parentid",
 	mproli."siteid" AS "product.lists.siteid", mproli."type" AS "product.lists.type",
 	mproli."domain" AS "product.lists.domain", mproli."refid" AS "product.lists.refid",
 	mproli."start" AS "product.lists.datestart", mproli."end" AS "product.lists.dateend",
 	mproli."config" AS "product.lists.config", mproli."pos" AS "product.lists.position",
 	mproli."status" AS "product.lists.status", mproli."mtime" AS "product.lists.mtime",
 	mproli."editor" AS "product.lists.editor", mproli."ctime" AS "product.lists.ctime"
 FROM "mshop_product_list" AS mproli
 :joins
 WHERE :cond
 ORDER BY :order
 OFFSET :start ROWS FETCH NEXT :size ROWS ONLY
```

* Default: mshop/product/manager/lists/standard/search
* Type: string - SQL statement for searching items
* Since: 2014.03

Fetches the records matched by the given criteria from the product
database. The records must be from one of the sites that are
configured via the context item. If the current site is part of
a tree of sites, the SELECT statement can retrieve all records
from the current site and the complete sub-tree of sites.

As the records can normally be limited by criteria from sub-managers,
their tables must be joined in the SQL context. This is done by
using the "internaldeps" property from the definition of the ID
column of the sub-managers. These internal dependencies specify
the JOIN between the tables and the used columns for joining. The
":joins" placeholder is then replaced by the JOIN strings from
the sub-managers.

To limit the records matched, conditions can be added to the given
criteria object. It can contain comparisons like column names that
must match specific values which can be combined by AND, OR or NOT
operators. The resulting string of SQL conditions replaces the
":cond" placeholder before the statement is sent to the database
server.

If the records that are retrieved should be ordered by one or more
columns, the generated string of column / sort direction pairs
replaces the ":order" placeholder. In case no ordering is required,
the complete ORDER BY part including the "/*-orderby*/.../*orderby-*/"
markers is removed to speed up retrieving the records. Columns of
sub-managers can also be used for ordering the result set but then
no index can be used.

The number of returned records can be limited and can start at any
number between the begining and the end of the result set. For that
the ":size" and ":start" placeholders are replaced by the
corresponding values from the criteria object. The default values
are 0 for the start and 100 for the size value.

The SQL statement should conform to the ANSI standard to be
compatible with most relational database systems. This also
includes using double quotes for table and column names.

See also:

* mshop/product/manager/lists/standard/insert/ansi
* mshop/product/manager/lists/standard/update/ansi
* mshop/product/manager/lists/standard/newid/ansi
* mshop/product/manager/lists/standard/delete/ansi
* mshop/product/manager/lists/standard/count/ansi
* mshop/product/manager/lists/standard/aggregate/ansi

## standard/search/mysql

Retrieves the records matched by the given criteria in the database

```
mshop/product/manager/lists/standard/search/mysql = 
 SELECT :columns
 	mproli."id" AS "product.lists.id", mproli."parentid" AS "product.lists.parentid",
 	mproli."siteid" AS "product.lists.siteid", mproli."type" AS "product.lists.type",
 	mproli."domain" AS "product.lists.domain", mproli."refid" AS "product.lists.refid",
 	mproli."start" AS "product.lists.datestart", mproli."end" AS "product.lists.dateend",
 	mproli."config" AS "product.lists.config", mproli."pos" AS "product.lists.position",
 	mproli."status" AS "product.lists.status", mproli."mtime" AS "product.lists.mtime",
 	mproli."editor" AS "product.lists.editor", mproli."ctime" AS "product.lists.ctime"
 FROM "mshop_product_list" AS mproli
 :joins
 WHERE :cond
 ORDER BY :order
 LIMIT :size OFFSET :start
```

* Default: 
 SELECT :columns
 	mproli."id" AS "product.lists.id", mproli."parentid" AS "product.lists.parentid",
 	mproli."siteid" AS "product.lists.siteid", mproli."type" AS "product.lists.type",
 	mproli."domain" AS "product.lists.domain", mproli."refid" AS "product.lists.refid",
 	mproli."start" AS "product.lists.datestart", mproli."end" AS "product.lists.dateend",
 	mproli."config" AS "product.lists.config", mproli."pos" AS "product.lists.position",
 	mproli."status" AS "product.lists.status", mproli."mtime" AS "product.lists.mtime",
 	mproli."editor" AS "product.lists.editor", mproli."ctime" AS "product.lists.ctime"
 FROM "mshop_product_list" AS mproli
 :joins
 WHERE :cond
 ORDER BY :order
 OFFSET :start ROWS FETCH NEXT :size ROWS ONLY


See also:

* mshop/product/manager/lists/standard/search/ansi

## standard/update/ansi

Updates an existing product list record in the database

```
mshop/product/manager/lists/standard/update/ansi = 
 UPDATE "mshop_product_list"
 SET :names
 	"parentid" = ?, "key" = ?, "type" = ?, "domain" = ?, "refid" = ?, "start" = ?,
 	"end" = ?, "config" = ?, "pos" = ?, "status" = ?, "mtime" = ?, "editor" = ?
 WHERE "siteid" = ? AND "id" = ?
```

* Default: mshop/product/manager/lists/standard/update
* Type: string - SQL statement for updating records
* Since: 2014.03

Items which already have an ID (i.e. the ID is not NULL) will
be updated in the database.

The SQL statement must be a string suitable for being used as
prepared statement. It must include question marks for binding
the values from the product list item to the statement before they are
sent to the database server. The order of the columns must
correspond to the order in the saveItems() method, so the
correct values are bound to the columns.

The SQL statement should conform to the ANSI standard to be
compatible with most relational database systems. This also
includes using double quotes for table and column names.

See also:

* mshop/product/manager/lists/standard/insert/ansi
* mshop/product/manager/lists/standard/newid/ansi
* mshop/product/manager/lists/standard/delete/ansi
* mshop/product/manager/lists/standard/search/ansi
* mshop/product/manager/lists/standard/count/ansi
* mshop/product/manager/lists/standard/aggregate/ansi

## standard/update/mysql

Updates an existing product list record in the database

```
mshop/product/manager/lists/standard/update/mysql = 
 UPDATE "mshop_product_list"
 SET :names
 	"parentid" = ?, "key" = ?, "type" = ?, "domain" = ?, "refid" = ?, "start" = ?,
 	"end" = ?, "config" = ?, "pos" = ?, "status" = ?, "mtime" = ?, "editor" = ?
 WHERE "siteid" = ? AND "id" = ?
```

* Default: 
 UPDATE "mshop_product_list"
 SET :names
 	"parentid" = ?, "key" = ?, "type" = ?, "domain" = ?, "refid" = ?, "start" = ?,
 	"end" = ?, "config" = ?, "pos" = ?, "status" = ?, "mtime" = ?, "editor" = ?
 WHERE "siteid" = ? AND "id" = ?


See also:

* mshop/product/manager/lists/standard/update/ansi

## submanagers

List of manager names that can be instantiated by the product list manager

```
mshop/product/manager/lists/submanagers = Array
(
)
```

* Default: Array
* Type: array - List of sub-manager names
* Since: 2014.03

Managers provide a generic interface to the underlying storage.
Each manager has or can have sub-managers caring about particular
aspects. Each of these sub-managers can be instantiated by its
parent manager using the getSubManager() method.

The search keys from sub-managers can be normally used in the
manager as well. It allows you to search for items of the manager
using the search keys of the sub-managers to further limit the
retrieved list of items.


## type/decorators/excludes

Excludes decorators added by the "common" option from the product list type manager

```
mshop/product/manager/lists/type/decorators/excludes = Array
(
)
```

* Default: Array
* Type: array - List of decorator names
* Since: 2014.03

Decorators extend the functionality of a class by adding new aspects
(e.g. log what is currently done), executing the methods of the underlying
class only in certain conditions (e.g. only for logged in users) or
modify what is returned to the caller.

This option allows you to remove a decorator added via
"mshop/common/manager/decorators/default" before they are wrapped
around the product list type manager.

```
 mshop/product/manager/lists/type/decorators/excludes = array( 'decorator1' )
```

This would remove the decorator named "decorator1" from the list of
common decorators ("\Aimeos\MShop\Common\Manager\Decorator\*") added via
"mshop/common/manager/decorators/default" for the product list type manager.

See also:

* mshop/common/manager/decorators/default
* mshop/product/manager/lists/type/decorators/global
* mshop/product/manager/lists/type/decorators/local

## type/decorators/global

Adds a list of globally available decorators only to the product list type manager

```
mshop/product/manager/lists/type/decorators/global = Array
(
)
```

* Default: Array
* Type: array - List of decorator names
* Since: 2014.03

Decorators extend the functionality of a class by adding new aspects
(e.g. log what is currently done), executing the methods of the underlying
class only in certain conditions (e.g. only for logged in users) or
modify what is returned to the caller.

This option allows you to wrap global decorators
("\Aimeos\MShop\Common\Manager\Decorator\*") around the product list
type manager.

```
 mshop/product/manager/lists/type/decorators/global = array( 'decorator1' )
```

This would add the decorator named "decorator1" defined by
"\Aimeos\MShop\Common\Manager\Decorator\Decorator1" only to the product
list type manager.

See also:

* mshop/common/manager/decorators/default
* mshop/product/manager/lists/type/decorators/excludes
* mshop/product/manager/lists/type/decorators/local

## type/decorators/local

Adds a list of local decorators only to the product list type manager

```
mshop/product/manager/lists/type/decorators/local = Array
(
)
```

* Default: Array
* Type: array - List of decorator names
* Since: 2014.03

Decorators extend the functionality of a class by adding new aspects
(e.g. log what is currently done), executing the methods of the underlying
class only in certain conditions (e.g. only for logged in users) or
modify what is returned to the caller.

This option allows you to wrap local decorators
("\Aimeos\MShop\Product\Manager\Lists\Type\Decorator\*") around the
product list type manager.

```
 mshop/product/manager/lists/type/decorators/local = array( 'decorator2' )
```

This would add the decorator named "decorator2" defined by
"\Aimeos\MShop\Product\Manager\Lists\Type\Decorator\Decorator2" only
to the product list type manager.

See also:

* mshop/common/manager/decorators/default
* mshop/product/manager/lists/type/decorators/excludes
* mshop/product/manager/lists/type/decorators/global

## type/name

Class name of the used product list type manager implementation

```
mshop/product/manager/lists/type/name = Standard
```

* Default: Standard
* Type: string - Last part of the class name
* Since: 2014.03

Each default product list type manager can be replaced by an alternative imlementation.
To use this implementation, you have to set the last part of the class
name as configuration value so the manager factory knows which class it
has to instantiate.

For example, if the name of the default class is

```
 \Aimeos\MShop\Product\Manager\Lists\Type\Standard
```

and you want to replace it with your own version named

```
 \Aimeos\MShop\Product\Manager\Lists\Type\Mytype
```

then you have to set the this configuration option:

```
 mshop/product/manager/lists/type/name = Mytype
```

The value is the last part of your own class name and it's case sensitive,
so take care that the configuration value is exactly named like the last
part of the class name.

The allowed characters of the class name are A-Z, a-z and 0-9. No other
characters are possible! You should always start the last part of the class
name with an upper case character and continue only with lower case characters
or numbers. Avoid chamel case names like "MyType"!


## type/standard/count/ansi

Counts the number of records matched by the given criteria in the database

```
mshop/product/manager/lists/type/standard/count/ansi = 
 SELECT COUNT(*) AS "count"
 FROM (
 	SELECT mprolity."id"
 	FROM "mshop_product_list_type" AS mprolity
 	:joins
 	WHERE :cond
 	ORDER BY mprolity."id"
 	OFFSET 0 ROWS FETCH NEXT 10000 ROWS ONLY
 ) AS list
```

* Default: mshop/product/manager/lists/type/standard/count
* Type: string - SQL statement for counting items
* Since: 2014.03

Counts all records matched by the given criteria from the product
database. The records must be from one of the sites that are
configured via the context item. If the current site is part of
a tree of sites, the statement can count all records from the
current site and the complete sub-tree of sites.

As the records can normally be limited by criteria from sub-managers,
their tables must be joined in the SQL context. This is done by
using the "internaldeps" property from the definition of the ID
column of the sub-managers. These internal dependencies specify
the JOIN between the tables and the used columns for joining. The
":joins" placeholder is then replaced by the JOIN strings from
the sub-managers.

To limit the records matched, conditions can be added to the given
criteria object. It can contain comparisons like column names that
must match specific values which can be combined by AND, OR or NOT
operators. The resulting string of SQL conditions replaces the
":cond" placeholder before the statement is sent to the database
server.

Both, the strings for ":joins" and for ":cond" are the same as for
the "search" SQL statement.

Contrary to the "search" statement, it doesn't return any records
but instead the number of records that have been found. As counting
thousands of records can be a long running task, the maximum number
of counted records is limited for performance reasons.

The SQL statement should conform to the ANSI standard to be
compatible with most relational database systems. This also
includes using double quotes for table and column names.

See also:

* mshop/product/manager/lists/type/standard/insert/ansi
* mshop/product/manager/lists/type/standard/update/ansi
* mshop/product/manager/lists/type/standard/newid/ansi
* mshop/product/manager/lists/type/standard/delete/ansi
* mshop/product/manager/lists/type/standard/search/ansi

## type/standard/count/mysql

Counts the number of records matched by the given criteria in the database

```
mshop/product/manager/lists/type/standard/count/mysql = 
 SELECT COUNT(*) AS "count"
 FROM (
 	SELECT mprolity."id"
 	FROM "mshop_product_list_type" AS mprolity
 	:joins
 	WHERE :cond
 	ORDER BY mprolity."id"
 	LIMIT 10000 OFFSET 0
 ) AS list
```

* Default: 
 SELECT COUNT(*) AS "count"
 FROM (
 	SELECT mprolity."id"
 	FROM "mshop_product_list_type" AS mprolity
 	:joins
 	WHERE :cond
 	ORDER BY mprolity."id"
 	OFFSET 0 ROWS FETCH NEXT 10000 ROWS ONLY
 ) AS list


See also:

* mshop/product/manager/lists/type/standard/count/ansi

## type/standard/delete/ansi

Deletes the items matched by the given IDs from the database

```
mshop/product/manager/lists/type/standard/delete/ansi = 
 DELETE FROM "mshop_product_list_type"
 WHERE :cond AND siteid = ?
```

* Default: mshop/product/manager/lists/type/standard/delete
* Type: string - SQL statement for deleting items
* Since: 2014.03

Removes the records specified by the given IDs from the product database.
The records must be from the site that is configured via the
context item.

The ":cond" placeholder is replaced by the name of the ID column and
the given ID or list of IDs while the site ID is bound to the question
mark.

The SQL statement should conform to the ANSI standard to be
compatible with most relational database systems. This also
includes using double quotes for table and column names.

See also:

* mshop/product/manager/lists/type/standard/insert/ansi
* mshop/product/manager/lists/type/standard/update/ansi
* mshop/product/manager/lists/type/standard/newid/ansi
* mshop/product/manager/lists/type/standard/search/ansi
* mshop/product/manager/lists/type/standard/count/ansi

## type/standard/delete/mysql

Deletes the items matched by the given IDs from the database

```
mshop/product/manager/lists/type/standard/delete/mysql = 
 DELETE FROM "mshop_product_list_type"
 WHERE :cond AND siteid = ?
```

* Default: 
 DELETE FROM "mshop_product_list_type"
 WHERE :cond AND siteid = ?


See also:

* mshop/product/manager/lists/type/standard/delete/ansi

## type/standard/insert/ansi

Inserts a new product list type record into the database table

```
mshop/product/manager/lists/type/standard/insert/ansi = 
 INSERT INTO "mshop_product_list_type" ( :names
 	"code", "domain", "label", "pos", "status",
 	"mtime", "editor", "siteid", "ctime"
 ) VALUES ( :values
 	?, ?, ?, ?, ?, ?, ?, ?, ?
 )
```

* Default: mshop/product/manager/lists/type/standard/insert
* Type: string - SQL statement for inserting records
* Since: 2014.03

Items with no ID yet (i.e. the ID is NULL) will be created in
the database and the newly created ID retrieved afterwards
using the "newid" SQL statement.

The SQL statement must be a string suitable for being used as
prepared statement. It must include question marks for binding
the values from the product list type item to the statement before they are
sent to the database server. The number of question marks must
be the same as the number of columns listed in the INSERT
statement. The order of the columns must correspond to the
order in the saveItems() method, so the correct values are
bound to the columns.

The SQL statement should conform to the ANSI standard to be
compatible with most relational database systems. This also
includes using double quotes for table and column names.

See also:

* mshop/product/manager/lists/type/standard/update/ansi
* mshop/product/manager/lists/type/standard/newid/ansi
* mshop/product/manager/lists/type/standard/delete/ansi
* mshop/product/manager/lists/type/standard/search/ansi
* mshop/product/manager/lists/type/standard/count/ansi

## type/standard/insert/mysql

Inserts a new product list type record into the database table

```
mshop/product/manager/lists/type/standard/insert/mysql = 
 INSERT INTO "mshop_product_list_type" ( :names
 	"code", "domain", "label", "pos", "status",
 	"mtime", "editor", "siteid", "ctime"
 ) VALUES ( :values
 	?, ?, ?, ?, ?, ?, ?, ?, ?
 )
```

* Default: 
 INSERT INTO "mshop_product_list_type" ( :names
 	"code", "domain", "label", "pos", "status",
 	"mtime", "editor", "siteid", "ctime"
 ) VALUES ( :values
 	?, ?, ?, ?, ?, ?, ?, ?, ?
 )


See also:

* mshop/product/manager/lists/type/standard/insert/ansi

## type/standard/newid/ansi

Retrieves the ID generated by the database when inserting a new record

```
mshop/product/manager/lists/type/standard/newid/ansi = mshop/product/manager/lists/type/standard/newid
```

* Default: mshop/product/manager/lists/type/standard/newid
* Type: string - SQL statement for retrieving the last inserted record ID
* Since: 2014.03

As soon as a new record is inserted into the database table,
the database server generates a new and unique identifier for
that record. This ID can be used for retrieving, updating and
deleting that specific record from the table again.

For MySQL:
```
 SELECT LAST_INSERT_ID()
For PostgreSQL:
 SELECT currval('seq_mserlity_id')
For SQL Server:
 SELECT SCOPE_IDENTITY()
For Oracle:
 SELECT "seq_mserlity_id".CURRVAL FROM DUAL
```

There's no way to retrive the new ID by a SQL statements that
fits for most database servers as they implement their own
specific way.

See also:

* mshop/product/manager/lists/type/standard/insert/ansi
* mshop/product/manager/lists/type/standard/update/ansi
* mshop/product/manager/lists/type/standard/delete/ansi
* mshop/product/manager/lists/type/standard/search/ansi
* mshop/product/manager/lists/type/standard/count/ansi

## type/standard/newid/mysql

Retrieves the ID generated by the database when inserting a new record

```
mshop/product/manager/lists/type/standard/newid/mysql = SELECT LAST_INSERT_ID()
```

* Default: mshop/product/manager/lists/type/standard/newid

See also:

* mshop/product/manager/lists/type/standard/newid/ansi

## type/standard/search/ansi

Retrieves the records matched by the given criteria in the database

```
mshop/product/manager/lists/type/standard/search/ansi = 
 SELECT :columns
 	mprolity."id" AS "product.lists.type.id", mprolity."siteid" AS "product.lists.type.siteid",
 	mprolity."code" AS "product.lists.type.code", mprolity."domain" AS "product.lists.type.domain",
 	mprolity."label" AS "product.lists.type.label", mprolity."status" AS "product.lists.type.status",
 	mprolity."mtime" AS "product.lists.type.mtime", mprolity."editor" AS "product.lists.type.editor",
 	mprolity."ctime" AS "product.lists.type.ctime", mprolity."pos" AS "product.lists.type.position"
 FROM "mshop_product_list_type" AS mprolity
 :joins
 WHERE :cond
 ORDER BY :order
 OFFSET :start ROWS FETCH NEXT :size ROWS ONLY
```

* Default: mshop/product/manager/lists/type/standard/search
* Type: string - SQL statement for searching items
* Since: 2014.03

Fetches the records matched by the given criteria from the product
database. The records must be from one of the sites that are
configured via the context item. If the current site is part of
a tree of sites, the SELECT statement can retrieve all records
from the current site and the complete sub-tree of sites.

As the records can normally be limited by criteria from sub-managers,
their tables must be joined in the SQL context. This is done by
using the "internaldeps" property from the definition of the ID
column of the sub-managers. These internal dependencies specify
the JOIN between the tables and the used columns for joining. The
":joins" placeholder is then replaced by the JOIN strings from
the sub-managers.

To limit the records matched, conditions can be added to the given
criteria object. It can contain comparisons like column names that
must match specific values which can be combined by AND, OR or NOT
operators. The resulting string of SQL conditions replaces the
":cond" placeholder before the statement is sent to the database
server.

If the records that are retrieved should be ordered by one or more
columns, the generated string of column / sort direction pairs
replaces the ":order" placeholder. In case no ordering is required,
the complete ORDER BY part including the "/*-orderby*/.../*orderby-*/"
markers is removed to speed up retrieving the records. Columns of
sub-managers can also be used for ordering the result set but then
no index can be used.

The number of returned records can be limited and can start at any
number between the begining and the end of the result set. For that
the ":size" and ":start" placeholders are replaced by the
corresponding values from the criteria object. The default values
are 0 for the start and 100 for the size value.

The SQL statement should conform to the ANSI standard to be
compatible with most relational database systems. This also
includes using double quotes for table and column names.

See also:

* mshop/product/manager/lists/type/standard/insert/ansi
* mshop/product/manager/lists/type/standard/update/ansi
* mshop/product/manager/lists/type/standard/newid/ansi
* mshop/product/manager/lists/type/standard/delete/ansi
* mshop/product/manager/lists/type/standard/count/ansi

## type/standard/search/mysql

Retrieves the records matched by the given criteria in the database

```
mshop/product/manager/lists/type/standard/search/mysql = 
 SELECT :columns
 	mprolity."id" AS "product.lists.type.id", mprolity."siteid" AS "product.lists.type.siteid",
 	mprolity."code" AS "product.lists.type.code", mprolity."domain" AS "product.lists.type.domain",
 	mprolity."label" AS "product.lists.type.label", mprolity."status" AS "product.lists.type.status",
 	mprolity."mtime" AS "product.lists.type.mtime", mprolity."editor" AS "product.lists.type.editor",
 	mprolity."ctime" AS "product.lists.type.ctime", mprolity."pos" AS "product.lists.type.position"
 FROM "mshop_product_list_type" AS mprolity
 :joins
 WHERE :cond
 ORDER BY :order
 LIMIT :size OFFSET :start
```

* Default: 
 SELECT :columns
 	mprolity."id" AS "product.lists.type.id", mprolity."siteid" AS "product.lists.type.siteid",
 	mprolity."code" AS "product.lists.type.code", mprolity."domain" AS "product.lists.type.domain",
 	mprolity."label" AS "product.lists.type.label", mprolity."status" AS "product.lists.type.status",
 	mprolity."mtime" AS "product.lists.type.mtime", mprolity."editor" AS "product.lists.type.editor",
 	mprolity."ctime" AS "product.lists.type.ctime", mprolity."pos" AS "product.lists.type.position"
 FROM "mshop_product_list_type" AS mprolity
 :joins
 WHERE :cond
 ORDER BY :order
 OFFSET :start ROWS FETCH NEXT :size ROWS ONLY


See also:

* mshop/product/manager/lists/type/standard/search/ansi

## type/standard/update/ansi

Updates an existing product list type record in the database

```
mshop/product/manager/lists/type/standard/update/ansi = 
 UPDATE "mshop_product_list_type"
 SET :names
 	"code" = ?, "domain" = ?, "label" = ?, "pos" = ?,
 	"status" = ?, "mtime" = ?, "editor" = ?
 WHERE "siteid" = ? AND "id" = ?
```

* Default: mshop/product/manager/lists/type/standard/update
* Type: string - SQL statement for updating records
* Since: 2014.03

Items which already have an ID (i.e. the ID is not NULL) will
be updated in the database.

The SQL statement must be a string suitable for being used as
prepared statement. It must include question marks for binding
the values from the product list type item to the statement before they are
sent to the database server. The order of the columns must
correspond to the order in the saveItems() method, so the
correct values are bound to the columns.

The SQL statement should conform to the ANSI standard to be
compatible with most relational database systems. This also
includes using double quotes for table and column names.

See also:

* mshop/product/manager/lists/type/standard/insert/ansi
* mshop/product/manager/lists/type/standard/newid/ansi
* mshop/product/manager/lists/type/standard/delete/ansi
* mshop/product/manager/lists/type/standard/search/ansi
* mshop/product/manager/lists/type/standard/count/ansi

## type/standard/update/mysql

Updates an existing product list type record in the database

```
mshop/product/manager/lists/type/standard/update/mysql = 
 UPDATE "mshop_product_list_type"
 SET :names
 	"code" = ?, "domain" = ?, "label" = ?, "pos" = ?,
 	"status" = ?, "mtime" = ?, "editor" = ?
 WHERE "siteid" = ? AND "id" = ?
```

* Default: 
 UPDATE "mshop_product_list_type"
 SET :names
 	"code" = ?, "domain" = ?, "label" = ?, "pos" = ?,
 	"status" = ?, "mtime" = ?, "editor" = ?
 WHERE "siteid" = ? AND "id" = ?


See also:

* mshop/product/manager/lists/type/standard/update/ansi

## type/submanagers

List of manager names that can be instantiated by the product list type manager

```
mshop/product/manager/lists/type/submanagers = Array
(
)
```

* Default: Array
* Type: array - List of sub-manager names
* Since: 2014.03

Managers provide a generic interface to the underlying storage.
Each manager has or can have sub-managers caring about particular
aspects. Each of these sub-managers can be instantiated by its
parent manager using the getSubManager() method.

The search keys from sub-managers can be normally used in the
manager as well. It allows you to search for items of the manager
using the search keys of the sub-managers to further limit the
retrieved list of items.


# name

Class name of the used product manager implementation

```
mshop/product/manager/name = Standard
```

* Default: Standard
* Type: string - Last part of the class name
* Since: 2014.03

Each default manager can be replace by an alternative imlementation.
To use this implementation, you have to set the last part of the class
name as configuration value so the manager factory knows which class it
has to instantiate.

For example, if the name of the default class is

```
 \Aimeos\MShop\Product\Manager\Standard
```

and you want to replace it with your own version named

```
 \Aimeos\MShop\Product\Manager\Mymanager
```

then you have to set the this configuration option:

```
 mshop/product/manager/name = Mymanager
```

The value is the last part of your own class name and it's case sensitive,
so take care that the configuration value is exactly named like the last
part of the class name.

The allowed characters of the class name are A-Z, a-z and 0-9. No other
characters are possible! You should always start the last part of the class
name with an upper case character and continue only with lower case characters
or numbers. Avoid chamel case names like "MyManager"!


# property
## decorators/excludes

Excludes decorators added by the "common" option from the product property manager

```
mshop/product/manager/property/decorators/excludes = Array
(
)
```

* Default: Array
* Type: array - List of decorator names
* Since: 2015.01

Decorators extend the functionality of a class by adding new aspects
(e.g. log what is currently done), executing the methods of the underlying
class only in certain conditions (e.g. only for logged in users) or
modify what is returned to the caller.

This option allows you to remove a decorator added via
"mshop/common/manager/decorators/default" before they are wrapped
around the product property manager.

```
 mshop/product/manager/property/decorators/excludes = array( 'decorator1' )
```

This would remove the decorator named "decorator1" from the list of
common decorators ("\Aimeos\MShop\Common\Manager\Decorator\*") added via
"mshop/common/manager/decorators/default" for the product property manager.

See also:

* mshop/common/manager/decorators/default
* mshop/product/manager/property/decorators/global
* mshop/product/manager/property/decorators/local

## decorators/global

Adds a list of globally available decorators only to the product property manager

```
mshop/product/manager/property/decorators/global = Array
(
)
```

* Default: Array
* Type: array - List of decorator names
* Since: 2015.01

Decorators extend the functionality of a class by adding new aspects
(e.g. log what is currently done), executing the methods of the underlying
class only in certain conditions (e.g. only for logged in users) or
modify what is returned to the caller.

This option allows you to wrap global decorators
("\Aimeos\MShop\Common\Manager\Decorator\*") around the product property
manager.

```
 mshop/product/manager/property/decorators/global = array( 'decorator1' )
```

This would add the decorator named "decorator1" defined by
"\Aimeos\MShop\Common\Manager\Decorator\Decorator1" only to the product
property manager.

See also:

* mshop/common/manager/decorators/default
* mshop/product/manager/property/decorators/excludes
* mshop/product/manager/property/decorators/local

## decorators/local

Adds a list of local decorators only to the product property manager

```
mshop/product/manager/property/decorators/local = Array
(
)
```

* Default: Array
* Type: array - List of decorator names
* Since: 2015.01

Decorators extend the functionality of a class by adding new aspects
(e.g. log what is currently done), executing the methods of the underlying
class only in certain conditions (e.g. only for logged in users) or
modify what is returned to the caller.

This option allows you to wrap local decorators
("\Aimeos\MShop\Product\Manager\Property\Decorator\*") around the
product property manager.

```
 mshop/product/manager/property/decorators/local = array( 'decorator2' )
```

This would add the decorator named "decorator2" defined by
"\Aimeos\MShop\Product\Manager\Property\Decorator\Decorator2" only to
the product property manager.

See also:

* mshop/common/manager/decorators/default
* mshop/product/manager/property/decorators/excludes
* mshop/product/manager/property/decorators/global

## name

Class name of the used product property manager implementation

```
mshop/product/manager/property/name = Standard
```

* Default: Standard
* Type: string - Last part of the class name
* Since: 2015.01

Each default product property manager can be replaced by an alternative imlementation.
To use this implementation, you have to set the last part of the class
name as configuration value so the manager factory knows which class it
has to instantiate.

For example, if the name of the default class is

```
 \Aimeos\MShop\Product\Manager\Property\Standard
```

and you want to replace it with your own version named

```
 \Aimeos\MShop\Product\Manager\Property\Myproperty
```

then you have to set the this configuration option:

```
 mshop/product/manager/property/name = Myproperty
```

The value is the last part of your own class name and it's case sensitive,
so take care that the configuration value is exactly named like the last
part of the class name.

The allowed characters of the class name are A-Z, a-z and 0-9. No other
characters are possible! You should always start the last part of the class
name with an upper case character and continue only with lower case characters
or numbers. Avoid chamel case names like "MyProperty"!


## standard/count/ansi

Counts the number of records matched by the given criteria in the database

```
mshop/product/manager/property/standard/count/ansi = 
 SELECT COUNT(*) AS "count"
 FROM (
 	SELECT mpropr."id"
 	FROM "mshop_product_property" AS mpropr
 	:joins
 	WHERE :cond
 	ORDER BY mpropr."id"
 	OFFSET 0 ROWS FETCH NEXT 10000 ROWS ONLY
 ) AS list
```

* Default: mshop/product/manager/property/standard/count
* Type: string - SQL statement for counting items
* Since: 2015.01

Counts all records matched by the given criteria from the product
database. The records must be from one of the sites that are
configured via the context item. If the current site is part of
a tree of sites, the statement can count all records from the
current site and the complete sub-tree of sites.

As the records can normally be limited by criteria from sub-managers,
their tables must be joined in the SQL context. This is done by
using the "internaldeps" property from the definition of the ID
column of the sub-managers. These internal dependencies specify
the JOIN between the tables and the used columns for joining. The
":joins" placeholder is then replaced by the JOIN strings from
the sub-managers.

To limit the records matched, conditions can be added to the given
criteria object. It can contain comparisons like column names that
must match specific values which can be combined by AND, OR or NOT
operators. The resulting string of SQL conditions replaces the
":cond" placeholder before the statement is sent to the database
server.

Both, the strings for ":joins" and for ":cond" are the same as for
the "search" SQL statement.

Contrary to the "search" statement, it doesn't return any records
but instead the number of records that have been found. As counting
thousands of records can be a long running task, the maximum number
of counted records is limited for performance reasons.

The SQL statement should conform to the ANSI standard to be
compatible with most relational database systems. This also
includes using double quotes for table and column names.

See also:

* mshop/product/manager/property/standard/insert/ansi
* mshop/product/manager/property/standard/update/ansi
* mshop/product/manager/property/standard/newid/ansi
* mshop/product/manager/property/standard/delete/ansi
* mshop/product/manager/property/standard/search/ansi

## standard/count/mysql

Counts the number of records matched by the given criteria in the database

```
mshop/product/manager/property/standard/count/mysql = 
 SELECT COUNT(*) AS "count"
 FROM (
 	SELECT mpropr."id"
 	FROM "mshop_product_property" AS mpropr
 	:joins
 	WHERE :cond
 	ORDER BY mpropr."id"
 	LIMIT 10000 OFFSET 0
 ) AS list
```

* Default: 
 SELECT COUNT(*) AS "count"
 FROM (
 	SELECT mpropr."id"
 	FROM "mshop_product_property" AS mpropr
 	:joins
 	WHERE :cond
 	ORDER BY mpropr."id"
 	OFFSET 0 ROWS FETCH NEXT 10000 ROWS ONLY
 ) AS list


See also:

* mshop/product/manager/property/standard/count/ansi

## standard/delete/ansi

Deletes the items matched by the given IDs from the database

```
mshop/product/manager/property/standard/delete/ansi = 
 DELETE FROM "mshop_product_property"
 WHERE :cond AND siteid = ?
```

* Default: mshop/product/manager/property/standard/delete
* Type: string - SQL statement for deleting items
* Since: 2015.01

Removes the records specified by the given IDs from the product database.
The records must be from the site that is configured via the
context item.

The ":cond" placeholder is replaced by the name of the ID column and
the given ID or list of IDs while the site ID is bound to the question
mark.

The SQL statement should conform to the ANSI standard to be
compatible with most relational database systems. This also
includes using double quotes for table and column names.

See also:

* mshop/product/manager/property/standard/insert/ansi
* mshop/product/manager/property/standard/update/ansi
* mshop/product/manager/property/standard/newid/ansi
* mshop/product/manager/property/standard/search/ansi
* mshop/product/manager/property/standard/count/ansi

## standard/delete/mysql

Deletes the items matched by the given IDs from the database

```
mshop/product/manager/property/standard/delete/mysql = 
 DELETE FROM "mshop_product_property"
 WHERE :cond AND siteid = ?
```

* Default: 
 DELETE FROM "mshop_product_property"
 WHERE :cond AND siteid = ?


See also:

* mshop/product/manager/property/standard/delete/ansi

## standard/insert/ansi

Inserts a new product property record into the database table

```
mshop/product/manager/property/standard/insert/ansi = 
 INSERT INTO "mshop_product_property" ( :names
 	"parentid", "key", "type", "langid", "value",
 	"mtime", "editor", "siteid", "ctime"
 ) VALUES ( :values
 	?, ?, ?, ?, ?, ?, ?, ?, ?
 )
```

* Default: mshop/product/manager/property/standard/insert
* Type: string - SQL statement for inserting records
* Since: 2015.01

Items with no ID yet (i.e. the ID is NULL) will be created in
the database and the newly created ID retrieved afterwards
using the "newid" SQL statement.

The SQL statement must be a string suitable for being used as
prepared statement. It must include question marks for binding
the values from the product property item to the statement before they are
sent to the database server. The number of question marks must
be the same as the number of columns listed in the INSERT
statement. The order of the columns must correspond to the
order in the saveItems() method, so the correct values are
bound to the columns.

The SQL statement should conform to the ANSI standard to be
compatible with most relational database systems. This also
includes using double quotes for table and column names.

See also:

* mshop/product/manager/property/standard/update/ansi
* mshop/product/manager/property/standard/newid/ansi
* mshop/product/manager/property/standard/delete/ansi
* mshop/product/manager/property/standard/search/ansi
* mshop/product/manager/property/standard/count/ansi

## standard/insert/mysql

Inserts a new product property record into the database table

```
mshop/product/manager/property/standard/insert/mysql = 
 INSERT INTO "mshop_product_property" ( :names
 	"parentid", "key", "type", "langid", "value",
 	"mtime", "editor", "siteid", "ctime"
 ) VALUES ( :values
 	?, ?, ?, ?, ?, ?, ?, ?, ?
 )
```

* Default: 
 INSERT INTO "mshop_product_property" ( :names
 	"parentid", "key", "type", "langid", "value",
 	"mtime", "editor", "siteid", "ctime"
 ) VALUES ( :values
 	?, ?, ?, ?, ?, ?, ?, ?, ?
 )


See also:

* mshop/product/manager/property/standard/insert/ansi

## standard/newid/ansi

Retrieves the ID generated by the database when inserting a new record

```
mshop/product/manager/property/standard/newid/ansi = mshop/product/manager/property/standard/newid
```

* Default: mshop/product/manager/property/standard/newid
* Type: string - SQL statement for retrieving the last inserted record ID
* Since: 2015.01

As soon as a new record is inserted into the database table,
the database server generates a new and unique identifier for
that record. This ID can be used for retrieving, updating and
deleting that specific record from the table again.

For MySQL:
```
 SELECT LAST_INSERT_ID()
For PostgreSQL:
 SELECT currval('seq_mpropr_id')
For SQL Server:
 SELECT SCOPE_IDENTITY()
For Oracle:
 SELECT "seq_mpropr_id".CURRVAL FROM DUAL
```

There's no way to retrive the new ID by a SQL statements that
fits for most database servers as they implement their own
specific way.

See also:

* mshop/product/manager/property/standard/insert/ansi
* mshop/product/manager/property/standard/update/ansi
* mshop/product/manager/property/standard/delete/ansi
* mshop/product/manager/property/standard/search/ansi
* mshop/product/manager/property/standard/count/ansi

## standard/newid/mysql

Retrieves the ID generated by the database when inserting a new record

```
mshop/product/manager/property/standard/newid/mysql = SELECT LAST_INSERT_ID()
```

* Default: mshop/product/manager/property/standard/newid

See also:

* mshop/product/manager/property/standard/newid/ansi

## standard/search/ansi

Retrieves the records matched by the given criteria in the database

```
mshop/product/manager/property/standard/search/ansi = 
 SELECT :columns
 	mpropr."id" AS "product.property.id", mpropr."parentid" AS "product.property.parentid",
 	mpropr."siteid" AS "product.property.siteid", mpropr."type" AS "product.property.type",
 	mpropr."langid" AS "product.property.languageid", mpropr."value" AS "product.property.value",
 	mpropr."mtime" AS "product.property.mtime", mpropr."editor" AS "product.property.editor",
 	mpropr."ctime" AS "product.property.ctime"
 FROM "mshop_product_property" AS mpropr
 :joins
 WHERE :cond
 ORDER BY :order
 OFFSET :start ROWS FETCH NEXT :size ROWS ONLY
```

* Default: mshop/product/manager/property/standard/search
* Type: string - SQL statement for searching items
* Since: 2015.01

Fetches the records matched by the given criteria from the product
database. The records must be from one of the sites that are
configured via the context item. If the current site is part of
a tree of sites, the SELECT statement can retrieve all records
from the current site and the complete sub-tree of sites.

As the records can normally be limited by criteria from sub-managers,
their tables must be joined in the SQL context. This is done by
using the "internaldeps" property from the definition of the ID
column of the sub-managers. These internal dependencies specify
the JOIN between the tables and the used columns for joining. The
":joins" placeholder is then replaced by the JOIN strings from
the sub-managers.

To limit the records matched, conditions can be added to the given
criteria object. It can contain comparisons like column names that
must match specific values which can be combined by AND, OR or NOT
operators. The resulting string of SQL conditions replaces the
":cond" placeholder before the statement is sent to the database
server.

If the records that are retrieved should be ordered by one or more
columns, the generated string of column / sort direction pairs
replaces the ":order" placeholder. In case no ordering is required,
the complete ORDER BY part including the "/*-orderby*/.../*orderby-*/"
markers is removed to speed up retrieving the records. Columns of
sub-managers can also be used for ordering the result set but then
no index can be used.

The number of returned records can be limited and can start at any
number between the begining and the end of the result set. For that
the ":size" and ":start" placeholders are replaced by the
corresponding values from the criteria object. The default values
are 0 for the start and 100 for the size value.

The SQL statement should conform to the ANSI standard to be
compatible with most relational database systems. This also
includes using double quotes for table and column names.

See also:

* mshop/product/manager/property/standard/insert/ansi
* mshop/product/manager/property/standard/update/ansi
* mshop/product/manager/property/standard/newid/ansi
* mshop/product/manager/property/standard/delete/ansi
* mshop/product/manager/property/standard/count/ansi

## standard/search/mysql

Retrieves the records matched by the given criteria in the database

```
mshop/product/manager/property/standard/search/mysql = 
 SELECT :columns
 	mpropr."id" AS "product.property.id", mpropr."parentid" AS "product.property.parentid",
 	mpropr."siteid" AS "product.property.siteid", mpropr."type" AS "product.property.type",
 	mpropr."langid" AS "product.property.languageid", mpropr."value" AS "product.property.value",
 	mpropr."mtime" AS "product.property.mtime", mpropr."editor" AS "product.property.editor",
 	mpropr."ctime" AS "product.property.ctime"
 FROM "mshop_product_property" AS mpropr
 :joins
 WHERE :cond
 ORDER BY :order
 LIMIT :size OFFSET :start
```

* Default: 
 SELECT :columns
 	mpropr."id" AS "product.property.id", mpropr."parentid" AS "product.property.parentid",
 	mpropr."siteid" AS "product.property.siteid", mpropr."type" AS "product.property.type",
 	mpropr."langid" AS "product.property.languageid", mpropr."value" AS "product.property.value",
 	mpropr."mtime" AS "product.property.mtime", mpropr."editor" AS "product.property.editor",
 	mpropr."ctime" AS "product.property.ctime"
 FROM "mshop_product_property" AS mpropr
 :joins
 WHERE :cond
 ORDER BY :order
 OFFSET :start ROWS FETCH NEXT :size ROWS ONLY


See also:

* mshop/product/manager/property/standard/search/ansi

## standard/update/ansi

Updates an existing product property record in the database

```
mshop/product/manager/property/standard/update/ansi = 
 UPDATE "mshop_product_property"
 SET :names
 	"parentid" = ?, "key" = ?, "type" = ?, "langid" = ?,
 	"value" = ?, "mtime" = ?, "editor" = ?
 WHERE "siteid" = ? AND "id" = ?
```

* Default: mshop/product/manager/property/standard/update
* Type: string - SQL statement for updating records
* Since: 2015.01

Items which already have an ID (i.e. the ID is not NULL) will
be updated in the database.

The SQL statement must be a string suitable for being used as
prepared statement. It must include question marks for binding
the values from the product property item to the statement before they are
sent to the database server. The order of the columns must
correspond to the order in the saveItems() method, so the
correct values are bound to the columns.

The SQL statement should conform to the ANSI standard to be
compatible with most relational database systems. This also
includes using double quotes for table and column names.

See also:

* mshop/product/manager/property/standard/insert/ansi
* mshop/product/manager/property/standard/newid/ansi
* mshop/product/manager/property/standard/delete/ansi
* mshop/product/manager/property/standard/search/ansi
* mshop/product/manager/property/standard/count/ansi

## standard/update/mysql

Updates an existing product property record in the database

```
mshop/product/manager/property/standard/update/mysql = 
 UPDATE "mshop_product_property"
 SET :names
 	"parentid" = ?, "key" = ?, "type" = ?, "langid" = ?,
 	"value" = ?, "mtime" = ?, "editor" = ?
 WHERE "siteid" = ? AND "id" = ?
```

* Default: 
 UPDATE "mshop_product_property"
 SET :names
 	"parentid" = ?, "key" = ?, "type" = ?, "langid" = ?,
 	"value" = ?, "mtime" = ?, "editor" = ?
 WHERE "siteid" = ? AND "id" = ?


See also:

* mshop/product/manager/property/standard/update/ansi

## submanagers

List of manager names that can be instantiated by the product property manager

```
mshop/product/manager/property/submanagers = Array
(
)
```

* Default: Array
* Type: array - List of sub-manager names
* Since: 2015.01

Managers provide a generic interface to the underlying storage.
Each manager has or can have sub-managers caring about particular
aspects. Each of these sub-managers can be instantiated by its
parent manager using the getSubManager() method.

The search keys from sub-managers can be normally used in the
manager as well. It allows you to search for items of the manager
using the search keys of the sub-managers to further limit the
retrieved list of items.


## type/decorators/excludes

Excludes decorators added by the "common" option from the product property type manager

```
mshop/product/manager/property/type/decorators/excludes = Array
(
)
```

* Default: Array
* Type: array - List of decorator names
* Since: 2015.01

Decorators extend the functionality of a class by adding new aspects
(e.g. log what is currently done), executing the methods of the underlying
class only in certain conditions (e.g. only for logged in users) or
modify what is returned to the caller.

This option allows you to remove a decorator added via
"mshop/common/manager/decorators/default" before they are wrapped
around the product property type manager.

```
 mshop/product/manager/property/type/decorators/excludes = array( 'decorator1' )
```

This would remove the decorator named "decorator1" from the list of
common decorators ("\Aimeos\MShop\Common\Manager\Decorator\*") added via
"mshop/common/manager/decorators/default" for the product property type manager.

See also:

* mshop/common/manager/decorators/default
* mshop/product/manager/property/type/decorators/global
* mshop/product/manager/property/type/decorators/local

## type/decorators/global

Adds a list of globally available decorators only to the product property type manager

```
mshop/product/manager/property/type/decorators/global = Array
(
)
```

* Default: Array
* Type: array - List of decorator names
* Since: 2015.01

Decorators extend the functionality of a class by adding new aspects
(e.g. log what is currently done), executing the methods of the underlying
class only in certain conditions (e.g. only for logged in users) or
modify what is returned to the caller.

This option allows you to wrap global decorators
("\Aimeos\MShop\Common\Manager\Decorator\*") around the product property
type manager.

```
 mshop/product/manager/property/type/decorators/global = array( 'decorator1' )
```

This would add the decorator named "decorator1" defined by
"\Aimeos\MShop\Common\Manager\Decorator\Decorator1" only to the product
property type manager.

See also:

* mshop/common/manager/decorators/default
* mshop/product/manager/property/type/decorators/excludes
* mshop/product/manager/property/type/decorators/local

## type/decorators/local

Adds a list of local decorators only to the product property type manager

```
mshop/product/manager/property/type/decorators/local = Array
(
)
```

* Default: Array
* Type: array - List of decorator names
* Since: 2015.01

Decorators extend the functionality of a class by adding new aspects
(e.g. log what is currently done), executing the methods of the underlying
class only in certain conditions (e.g. only for logged in users) or
modify what is returned to the caller.

This option allows you to wrap local decorators
("\Aimeos\MShop\Product\Manager\Property\Type\Decorator\*") around the
product property type manager.

```
 mshop/product/manager/property/type/decorators/local = array( 'decorator2' )
```

This would add the decorator named "decorator2" defined by
"\Aimeos\MShop\Product\Manager\Property\Type\Decorator\Decorator2" only
to the product property type manager.

See also:

* mshop/common/manager/decorators/default
* mshop/product/manager/property/type/decorators/excludes
* mshop/product/manager/property/type/decorators/global

## type/name

Class name of the used product property type manager implementation

```
mshop/product/manager/property/type/name = Standard
```

* Default: Standard
* Type: string - Last part of the class name
* Since: 2015.01

Each default product property type manager can be replaced by an alternative imlementation.
To use this implementation, you have to set the last part of the class
name as configuration value so the manager factory knows which class it
has to instantiate.

For example, if the name of the default class is

```
 \Aimeos\MShop\Product\Manager\Lists\Type\Standard
```

and you want to replace it with your own version named

```
 \Aimeos\MShop\Product\Manager\Lists\Type\Mytype
```

then you have to set the this configuration option:

```
 mshop/product/manager/property/type/name = Mytype
```

The value is the last part of your own class name and it's case sensitive,
so take care that the configuration value is exactly named like the last
part of the class name.

The allowed characters of the class name are A-Z, a-z and 0-9. No other
characters are possible! You should always start the last part of the class
name with an upper case character and continue only with lower case characters
or numbers. Avoid chamel case names like "MyType"!


## type/standard/count/ansi

Counts the number of records matched by the given criteria in the database

```
mshop/product/manager/property/type/standard/count/ansi = 
 SELECT COUNT(*) AS "count"
 FROM (
 	SELECT mproprty."id"
 	FROM "mshop_product_property_type" mproprty
 	:joins
 	WHERE :cond
 	ORDER BY mproprty."id"
 	OFFSET 0 ROWS FETCH NEXT 10000 ROWS ONLY
 ) AS list
```

* Default: mshop/product/manager/property/type/standard/count
* Type: string - SQL statement for counting items
* Since: 2015.01

Counts all records matched by the given criteria from the product
database. The records must be from one of the sites that are
configured via the context item. If the current site is part of
a tree of sites, the statement can count all records from the
current site and the complete sub-tree of sites.

As the records can normally be limited by criteria from sub-managers,
their tables must be joined in the SQL context. This is done by
using the "internaldeps" property from the definition of the ID
column of the sub-managers. These internal dependencies specify
the JOIN between the tables and the used columns for joining. The
":joins" placeholder is then replaced by the JOIN strings from
the sub-managers.

To limit the records matched, conditions can be added to the given
criteria object. It can contain comparisons like column names that
must match specific values which can be combined by AND, OR or NOT
operators. The resulting string of SQL conditions replaces the
":cond" placeholder before the statement is sent to the database
server.

Both, the strings for ":joins" and for ":cond" are the same as for
the "search" SQL statement.

Contrary to the "search" statement, it doesn't return any records
but instead the number of records that have been found. As counting
thousands of records can be a long running task, the maximum number
of counted records is limited for performance reasons.

The SQL statement should conform to the ANSI standard to be
compatible with most relational database systems. This also
includes using double quotes for table and column names.

See also:

* mshop/product/manager/property/type/standard/insert/ansi
* mshop/product/manager/property/type/standard/update/ansi
* mshop/product/manager/property/type/standard/newid/ansi
* mshop/product/manager/property/type/standard/delete/ansi
* mshop/product/manager/property/type/standard/search/ansi

## type/standard/count/mysql

Counts the number of records matched by the given criteria in the database

```
mshop/product/manager/property/type/standard/count/mysql = 
 SELECT COUNT(*) AS "count"
 FROM (
 	SELECT mproprty."id"
 	FROM "mshop_product_property_type" mproprty
 	:joins
 	WHERE :cond
 	ORDER BY mproprty."id"
 	LIMIT 10000 OFFSET 0
 ) AS list
```

* Default: 
 SELECT COUNT(*) AS "count"
 FROM (
 	SELECT mproprty."id"
 	FROM "mshop_product_property_type" mproprty
 	:joins
 	WHERE :cond
 	ORDER BY mproprty."id"
 	OFFSET 0 ROWS FETCH NEXT 10000 ROWS ONLY
 ) AS list


See also:

* mshop/product/manager/property/type/standard/count/ansi

## type/standard/delete/ansi

Deletes the items matched by the given IDs from the database

```
mshop/product/manager/property/type/standard/delete/ansi = 
 DELETE FROM "mshop_product_property_type"
 WHERE :cond AND siteid = ?
```

* Default: mshop/product/manager/property/type/standard/delete
* Type: string - SQL statement for deleting items
* Since: 2015.01

Removes the records specified by the given IDs from the product database.
The records must be from the site that is configured via the
context item.

The ":cond" placeholder is replaced by the name of the ID column and
the given ID or list of IDs while the site ID is bound to the question
mark.

The SQL statement should conform to the ANSI standard to be
compatible with most relational database systems. This also
includes using double quotes for table and column names.

See also:

* mshop/product/manager/property/type/standard/insert/ansi
* mshop/product/manager/property/type/standard/update/ansi
* mshop/product/manager/property/type/standard/newid/ansi
* mshop/product/manager/property/type/standard/search/ansi
* mshop/product/manager/property/type/standard/count/ansi

## type/standard/delete/mysql

Deletes the items matched by the given IDs from the database

```
mshop/product/manager/property/type/standard/delete/mysql = 
 DELETE FROM "mshop_product_property_type"
 WHERE :cond AND siteid = ?
```

* Default: 
 DELETE FROM "mshop_product_property_type"
 WHERE :cond AND siteid = ?


See also:

* mshop/product/manager/property/type/standard/delete/ansi

## type/standard/insert/ansi

Inserts a new product property type record into the database table

```
mshop/product/manager/property/type/standard/insert/ansi = 
 INSERT INTO "mshop_product_property_type" ( :names
 	"code", "domain", "label", "pos", "status",
 	"mtime", "editor", "siteid", "ctime"
 ) VALUES ( :values
 	?, ?, ?, ?, ?, ?, ?, ?, ?
 )
```

* Default: mshop/product/manager/property/type/standard/insert
* Type: string - SQL statement for inserting records
* Since: 2015.01

Items with no ID yet (i.e. the ID is NULL) will be created in
the database and the newly created ID retrieved afterwards
using the "newid" SQL statement.

The SQL statement must be a string suitable for being used as
prepared statement. It must include question marks for binding
the values from the product type item to the statement before they are
sent to the database server. The number of question marks must
be the same as the number of columns listed in the INSERT
statement. The order of the columns must correspond to the
order in the saveItems() method, so the correct values are
bound to the columns.

The SQL statement should conform to the ANSI standard to be
compatible with most relational database systems. This also
includes using double quotes for table and column names.

See also:

* mshop/product/manager/property/type/standard/update/ansi
* mshop/product/manager/property/type/standard/newid/ansi
* mshop/product/manager/property/type/standard/delete/ansi
* mshop/product/manager/property/type/standard/search/ansi
* mshop/product/manager/property/type/standard/count/ansi

## type/standard/insert/mysql

Inserts a new product property type record into the database table

```
mshop/product/manager/property/type/standard/insert/mysql = 
 INSERT INTO "mshop_product_property_type" ( :names
 	"code", "domain", "label", "pos", "status",
 	"mtime", "editor", "siteid", "ctime"
 ) VALUES ( :values
 	?, ?, ?, ?, ?, ?, ?, ?, ?
 )
```

* Default: 
 INSERT INTO "mshop_product_property_type" ( :names
 	"code", "domain", "label", "pos", "status",
 	"mtime", "editor", "siteid", "ctime"
 ) VALUES ( :values
 	?, ?, ?, ?, ?, ?, ?, ?, ?
 )


See also:

* mshop/product/manager/property/type/standard/insert/ansi

## type/standard/newid/ansi

Retrieves the ID generated by the database when inserting a new record

```
mshop/product/manager/property/type/standard/newid/ansi = mshop/product/manager/property/type/standard/newid
```

* Default: mshop/product/manager/property/type/standard/newid
* Type: string - SQL statement for retrieving the last inserted record ID
* Since: 2015.01

As soon as a new record is inserted into the database table,
the database server generates a new and unique identifier for
that record. This ID can be used for retrieving, updating and
deleting that specific record from the table again.

For MySQL:
```
 SELECT LAST_INSERT_ID()
For PostgreSQL:
 SELECT currval('seq_mproprty_id')
For SQL Server:
 SELECT SCOPE_IDENTITY()
For Oracle:
 SELECT "seq_mproprty_id".CURRVAL FROM DUAL
```

There's no way to retrive the new ID by a SQL statements that
fits for most database servers as they implement their own
specific way.

See also:

* mshop/product/manager/property/type/standard/insert/ansi
* mshop/product/manager/property/type/standard/update/ansi
* mshop/product/manager/property/type/standard/delete/ansi
* mshop/product/manager/property/type/standard/search/ansi
* mshop/product/manager/property/type/standard/count/ansi

## type/standard/newid/mysql

Retrieves the ID generated by the database when inserting a new record

```
mshop/product/manager/property/type/standard/newid/mysql = SELECT LAST_INSERT_ID()
```

* Default: mshop/product/manager/property/type/standard/newid

See also:

* mshop/product/manager/property/type/standard/newid/ansi

## type/standard/search/ansi

Retrieves the records matched by the given criteria in the database

```
mshop/product/manager/property/type/standard/search/ansi = 
 SELECT :columns
 	mproprty."id" AS "product.property.type.id", mproprty."siteid" AS "product.property.type.siteid",
 	mproprty."code" AS "product.property.type.code", mproprty."domain" AS "product.property.type.domain",
 	mproprty."label" AS "product.property.type.label", mproprty."status" AS "product.property.type.status",
 	mproprty."mtime" AS "product.property.type.mtime", mproprty."editor" AS "product.property.type.editor",
 	mproprty."ctime" AS "product.property.type.ctime", mproprty."pos" AS "product.property.type.position"
 FROM "mshop_product_property_type" mproprty
 :joins
 WHERE :cond
 ORDER BY :order
 OFFSET :start ROWS FETCH NEXT :size ROWS ONLY
```

* Default: mshop/product/manager/property/type/standard/search
* Type: string - SQL statement for searching items
* Since: 2015.01

Fetches the records matched by the given criteria from the product
database. The records must be from one of the sites that are
configured via the context item. If the current site is part of
a tree of sites, the SELECT statement can retrieve all records
from the current site and the complete sub-tree of sites.

As the records can normally be limited by criteria from sub-managers,
their tables must be joined in the SQL context. This is done by
using the "internaldeps" property from the definition of the ID
column of the sub-managers. These internal dependencies specify
the JOIN between the tables and the used columns for joining. The
":joins" placeholder is then replaced by the JOIN strings from
the sub-managers.

To limit the records matched, conditions can be added to the given
criteria object. It can contain comparisons like column names that
must match specific values which can be combined by AND, OR or NOT
operators. The resulting string of SQL conditions replaces the
":cond" placeholder before the statement is sent to the database
server.

If the records that are retrieved should be ordered by one or more
columns, the generated string of column / sort direction pairs
replaces the ":order" placeholder. In case no ordering is required,
the complete ORDER BY part including the "/*-orderby*/.../*orderby-*/"
markers is removed to speed up retrieving the records. Columns of
sub-managers can also be used for ordering the result set but then
no index can be used.

The number of returned records can be limited and can start at any
number between the begining and the end of the result set. For that
the ":size" and ":start" placeholders are replaced by the
corresponding values from the criteria object. The default values
are 0 for the start and 100 for the size value.

The SQL statement should conform to the ANSI standard to be
compatible with most relational database systems. This also
includes using double quotes for table and column names.

See also:

* mshop/product/manager/property/type/standard/insert/ansi
* mshop/product/manager/property/type/standard/update/ansi
* mshop/product/manager/property/type/standard/newid/ansi
* mshop/product/manager/property/type/standard/delete/ansi
* mshop/product/manager/property/type/standard/count/ansi

## type/standard/search/mysql

Retrieves the records matched by the given criteria in the database

```
mshop/product/manager/property/type/standard/search/mysql = 
 SELECT :columns
 	mproprty."id" AS "product.property.type.id", mproprty."siteid" AS "product.property.type.siteid",
 	mproprty."code" AS "product.property.type.code", mproprty."domain" AS "product.property.type.domain",
 	mproprty."label" AS "product.property.type.label", mproprty."status" AS "product.property.type.status",
 	mproprty."mtime" AS "product.property.type.mtime", mproprty."editor" AS "product.property.type.editor",
 	mproprty."ctime" AS "product.property.type.ctime", mproprty."pos" AS "product.property.type.position"
 FROM "mshop_product_property_type" mproprty
 :joins
 WHERE :cond
 ORDER BY :order
 LIMIT :size OFFSET :start
```

* Default: 
 SELECT :columns
 	mproprty."id" AS "product.property.type.id", mproprty."siteid" AS "product.property.type.siteid",
 	mproprty."code" AS "product.property.type.code", mproprty."domain" AS "product.property.type.domain",
 	mproprty."label" AS "product.property.type.label", mproprty."status" AS "product.property.type.status",
 	mproprty."mtime" AS "product.property.type.mtime", mproprty."editor" AS "product.property.type.editor",
 	mproprty."ctime" AS "product.property.type.ctime", mproprty."pos" AS "product.property.type.position"
 FROM "mshop_product_property_type" mproprty
 :joins
 WHERE :cond
 ORDER BY :order
 OFFSET :start ROWS FETCH NEXT :size ROWS ONLY


See also:

* mshop/product/manager/property/type/standard/search/ansi

## type/standard/update/ansi

Updates an existing product property type record in the database

```
mshop/product/manager/property/type/standard/update/ansi = 
 UPDATE "mshop_product_property_type"
 SET :names
 	"code" = ?, "domain" = ?, "label" = ?, "pos" = ?,
 	"status" = ?, "mtime" = ?, "editor" = ?
 WHERE "siteid" = ? AND "id" = ?
```

* Default: mshop/product/manager/property/type/standard/update
* Type: string - SQL statement for updating records
* Since: 2015.01

Items which already have an ID (i.e. the ID is not NULL) will
be updated in the database.

The SQL statement must be a string suitable for being used as
prepared statement. It must include question marks for binding
the values from the product type item to the statement before they are
sent to the database server. The order of the columns must
correspond to the order in the saveItems() method, so the
correct values are bound to the columns.

The SQL statement should conform to the ANSI standard to be
compatible with most relational database systems. This also
includes using double quotes for table and column names.

See also:

* mshop/product/manager/property/type/standard/insert/ansi
* mshop/product/manager/property/type/standard/newid/ansi
* mshop/product/manager/property/type/standard/delete/ansi
* mshop/product/manager/property/type/standard/search/ansi
* mshop/product/manager/property/type/standard/count/ansi

## type/standard/update/mysql

Updates an existing product property type record in the database

```
mshop/product/manager/property/type/standard/update/mysql = 
 UPDATE "mshop_product_property_type"
 SET :names
 	"code" = ?, "domain" = ?, "label" = ?, "pos" = ?,
 	"status" = ?, "mtime" = ?, "editor" = ?
 WHERE "siteid" = ? AND "id" = ?
```

* Default: 
 UPDATE "mshop_product_property_type"
 SET :names
 	"code" = ?, "domain" = ?, "label" = ?, "pos" = ?,
 	"status" = ?, "mtime" = ?, "editor" = ?
 WHERE "siteid" = ? AND "id" = ?


See also:

* mshop/product/manager/property/type/standard/update/ansi

## type/submanagers

List of manager names that can be instantiated by the product property type manager

```
mshop/product/manager/property/type/submanagers = Array
(
)
```

* Default: Array
* Type: array - List of sub-manager names
* Since: 2015.01

Managers provide a generic interface to the underlying storage.
Each manager has or can have sub-managers caring about particular
aspects. Each of these sub-managers can be instantiated by its
parent manager using the getSubManager() method.

The search keys from sub-managers can be normally used in the
manager as well. It allows you to search for items of the manager
using the search keys of the sub-managers to further limit the
retrieved list of items.


# sitemode

Mode how items from levels below or above in the site tree are handled

```
mshop/product/manager/sitemode = 3
```

* Default: 3
* Type: int - Constant from Aimeos\MShop\Locale\Manager\Base class
* Since: 2018.01

By default, only items from the current site are fetched from the
storage. If the ai-sites extension is installed, you can create a
tree of sites. Then, this setting allows you to define for the
whole product domain if items from parent sites are inherited,
sites from child sites are aggregated or both.

Available constants for the site mode are:
* 0 = only items from the current site
* 1 = inherit items from parent sites
* 2 = aggregate items from child sites
* 3 = inherit and aggregate items at the same time

You also need to set the mode in the locale manager
(mshop/locale/manager/standard/sitelevel) to one of the constants.
If you set it to the same value, it will work as described but you
can also use different modes. For example, if inheritance and
aggregation is configured the locale manager but only inheritance
in the domain manager because aggregating items makes no sense in
this domain, then items wil be only inherited. Thus, you have full
control over inheritance and aggregation in each domain.

See also:

* mshop/locale/manager/standard/sitelevel

# standard
## count/ansi

Counts the number of records matched by the given criteria in the database

```
mshop/product/manager/standard/count/ansi = 
 SELECT COUNT(*) AS "count"
 FROM (
 	SELECT mpro."id"
 	FROM "mshop_product" AS mpro
 	:joins
 	WHERE :cond
 	GROUP BY mpro."id"
 	ORDER BY mpro."id"
 	OFFSET 0 ROWS FETCH NEXT 10000 ROWS ONLY
 ) AS list
```

* Default: mshop/product/manager/standard/count
* Type: string - SQL statement for counting items
* Since: 2014.03

Counts all records matched by the given criteria from the product
database. The records must be from one of the sites that are
configured via the context item. If the current site is part of
a tree of sites, the statement can count all records from the
current site and the complete sub-tree of sites.

As the records can normally be limited by criteria from sub-managers,
their tables must be joined in the SQL context. This is done by
using the "internaldeps" property from the definition of the ID
column of the sub-managers. These internal dependencies specify
the JOIN between the tables and the used columns for joining. The
":joins" placeholder is then replaced by the JOIN strings from
the sub-managers.

To limit the records matched, conditions can be added to the given
criteria object. It can contain comparisons like column names that
must match specific values which can be combined by AND, OR or NOT
operators. The resulting string of SQL conditions replaces the
":cond" placeholder before the statement is sent to the database
server.

Both, the strings for ":joins" and for ":cond" are the same as for
the "search" SQL statement.

Contrary to the "search" statement, it doesn't return any records
but instead the number of records that have been found. As counting
thousands of records can be a long running task, the maximum number
of counted records is limited for performance reasons.

The SQL statement should conform to the ANSI standard to be
compatible with most relational database systems. This also
includes using double quotes for table and column names.

See also:

* mshop/product/manager/standard/insert/ansi
* mshop/product/manager/standard/update/ansi
* mshop/product/manager/standard/newid/ansi
* mshop/product/manager/standard/delete/ansi
* mshop/product/manager/standard/search/ansi

## count/mysql

Counts the number of records matched by the given criteria in the database

```
mshop/product/manager/standard/count/mysql = 
 SELECT COUNT(*) AS "count"
 FROM (
 	SELECT mpro."id"
 	FROM "mshop_product" AS mpro
 	:joins
 	WHERE :cond
 	GROUP BY mpro."id"
 	ORDER BY mpro."id"
 	LIMIT 10000 OFFSET 0
 ) AS list
```

* Default: 
 SELECT COUNT(*) AS "count"
 FROM (
 	SELECT mpro."id"
 	FROM "mshop_product" AS mpro
 	:joins
 	WHERE :cond
 	GROUP BY mpro."id"
 	ORDER BY mpro."id"
 	OFFSET 0 ROWS FETCH NEXT 10000 ROWS ONLY
 ) AS list


See also:

* mshop/product/manager/standard/count/ansi

## delete/ansi

Deletes the items matched by the given IDs from the database

```
mshop/product/manager/standard/delete/ansi = 
 DELETE FROM "mshop_product"
 WHERE :cond AND siteid = ?
```

* Default: mshop/product/manager/standard/delete
* Type: string - SQL statement for deleting items
* Since: 2014.03

Removes the records specified by the given IDs from the product database.
The records must be from the site that is configured via the
context item.

The ":cond" placeholder is replaced by the name of the ID column and
the given ID or list of IDs while the site ID is bound to the question
mark.

The SQL statement should conform to the ANSI standard to be
compatible with most relational database systems. This also
includes using double quotes for table and column names.

See also:

* mshop/product/manager/standard/insert/ansi
* mshop/product/manager/standard/update/ansi
* mshop/product/manager/standard/newid/ansi
* mshop/product/manager/standard/search/ansi
* mshop/product/manager/standard/count/ansi

## delete/mysql

Deletes the items matched by the given IDs from the database

```
mshop/product/manager/standard/delete/mysql = 
 DELETE FROM "mshop_product"
 WHERE :cond AND siteid = ?
```

* Default: 
 DELETE FROM "mshop_product"
 WHERE :cond AND siteid = ?


See also:

* mshop/product/manager/standard/delete/ansi

## insert/ansi

Inserts a new product record into the database table

```
mshop/product/manager/standard/insert/ansi = 
 INSERT INTO "mshop_product" ( :names
 	"type", "code", "dataset", "label", "url", "status", "scale", "start", "end",
 	"config", "target", "editor", "mtime", "ctime", "siteid"
 ) VALUES ( :values
 	?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?
 )
```

* Default: mshop/product/manager/standard/insert
* Type: string - SQL statement for inserting records
* Since: 2014.03

Items with no ID yet (i.e. the ID is NULL) will be created in
the database and the newly created ID retrieved afterwards
using the "newid" SQL statement.

The SQL statement must be a string suitable for being used as
prepared statement. It must include question marks for binding
the values from the product item to the statement before they are
sent to the database server. The number of question marks must
be the same as the number of columns listed in the INSERT
statement. The order of the columns must correspond to the
order in the saveItems() method, so the correct values are
bound to the columns.

The SQL statement should conform to the ANSI standard to be
compatible with most relational database systems. This also
includes using double quotes for table and column names.

See also:

* mshop/product/manager/standard/update/ansi
* mshop/product/manager/standard/newid/ansi
* mshop/product/manager/standard/delete/ansi
* mshop/product/manager/standard/search/ansi
* mshop/product/manager/standard/count/ansi

## insert/mysql

Inserts a new product record into the database table

```
mshop/product/manager/standard/insert/mysql = 
 INSERT INTO "mshop_product" ( :names
 	"type", "code", "dataset", "label", "url", "status", "scale", "start", "end",
 	"config", "target", "editor", "mtime", "ctime", "siteid"
 ) VALUES ( :values
 	?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?
 )
```

* Default: 
 INSERT INTO "mshop_product" ( :names
 	"type", "code", "dataset", "label", "url", "status", "scale", "start", "end",
 	"config", "target", "editor", "mtime", "ctime", "siteid"
 ) VALUES ( :values
 	?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?
 )


See also:

* mshop/product/manager/standard/insert/ansi

## newid/ansi

Retrieves the ID generated by the database when inserting a new record

```
mshop/product/manager/standard/newid/ansi = mshop/product/manager/standard/newid
```

* Default: mshop/product/manager/standard/newid
* Type: string - SQL statement for retrieving the last inserted record ID
* Since: 2014.03

As soon as a new record is inserted into the database table,
the database server generates a new and unique identifier for
that record. This ID can be used for retrieving, updating and
deleting that specific record from the table again.

For MySQL:
```
 SELECT LAST_INSERT_ID()
For PostgreSQL:
 SELECT currval('seq_mpro_id')
For SQL Server:
 SELECT SCOPE_IDENTITY()
For Oracle:
 SELECT "seq_mpro_id".CURRVAL FROM DUAL
```

There's no way to retrive the new ID by a SQL statements that
fits for most database servers as they implement their own
specific way.

See also:

* mshop/product/manager/standard/insert/ansi
* mshop/product/manager/standard/update/ansi
* mshop/product/manager/standard/delete/ansi
* mshop/product/manager/standard/search/ansi
* mshop/product/manager/standard/count/ansi

## newid/mysql

Retrieves the ID generated by the database when inserting a new record

```
mshop/product/manager/standard/newid/mysql = SELECT LAST_INSERT_ID()
```

* Default: mshop/product/manager/standard/newid

See also:

* mshop/product/manager/standard/newid/ansi

## rate/ansi

Updates the rating of the product in the database

```
mshop/product/manager/standard/rate/ansi = 
 UPDATE "mshop_product"
 SET "rating" = ?, "ratings" = ?
 WHERE "siteid" = ? AND "id" = ?
```

* Default: mshop/product/manager/standard/rate
* Type: string - SQL statement for update ratings
* Since: 2020.10

The SQL statement must be a string suitable for being used as
prepared statement. It must include question marks for binding
the values for the rating to the statement before they are
sent to the database server. The order of the columns must
correspond to the order in the rate() method, so the
correct values are bound to the columns.

The SQL statement should conform to the ANSI standard to be
compatible with most relational database systems. This also
includes using double quotes for table and column names.

See also:

* mshop/product/manager/standard/insert/ansi
* mshop/product/manager/standard/update/ansi
* mshop/product/manager/standard/newid/ansi
* mshop/product/manager/standard/delete/ansi
* mshop/product/manager/standard/search/ansi
* mshop/product/manager/standard/count/ansi

## rate/mysql

Updates the rating of the product in the database

```
mshop/product/manager/standard/rate/mysql = 
 UPDATE "mshop_product"
 SET "rating" = ?, "ratings" = ?
 WHERE "siteid" = ? AND "id" = ?
```

* Default: 
 UPDATE "mshop_product"
 SET "rating" = ?, "ratings" = ?
 WHERE "siteid" = ? AND "id" = ?


See also:

* mshop/product/manager/standard/rate/ansi

## search/ansi

Retrieves the records matched by the given criteria in the database

```
mshop/product/manager/standard/search/ansi = 
 SELECT :columns
 	mpro."id" AS "product.id", mpro."siteid" AS "product.siteid",
 	mpro."type" AS "product.type", mpro."code" AS "product.code",
 	mpro."label" AS "product.label", mpro."url" AS "product.url",
 	mpro."start" AS "product.datestart", mpro."end" AS "product.dateend",
 	mpro."status" AS "product.status", mpro."ctime" AS "product.ctime",
 	mpro."mtime" AS "product.mtime", mpro."editor" AS "product.editor",
 	mpro."target" AS "product.target", mpro."dataset" AS "product.dataset",
 	mpro."scale" AS "product.scale", mpro."config" AS "product.config",
 	mpro."rating" AS "product.rating", mpro."ratings" AS "product.ratings"
 FROM "mshop_product" AS mpro
 :joins
 WHERE :cond
 GROUP BY :columns :group
 	mpro."id", mpro."siteid", mpro."type", mpro."code", mpro."label", mpro."url",
 	mpro."target", mpro."dataset", mpro."scale", mpro."config", mpro."start", mpro."end",
 	mpro."status", mpro."ctime", mpro."mtime", mpro."editor", mpro."rating", mpro."ratings"
 ORDER BY :order
 OFFSET :start ROWS FETCH NEXT :size ROWS ONLY
```

* Default: mshop/product/manager/standard/search
* Type: string - SQL statement for searching items
* Since: 2014.03

Fetches the records matched by the given criteria from the product
database. The records must be from one of the sites that are
configured via the context item. If the current site is part of
a tree of sites, the SELECT statement can retrieve all records
from the current site and the complete sub-tree of sites.

As the records can normally be limited by criteria from sub-managers,
their tables must be joined in the SQL context. This is done by
using the "internaldeps" property from the definition of the ID
column of the sub-managers. These internal dependencies specify
the JOIN between the tables and the used columns for joining. The
":joins" placeholder is then replaced by the JOIN strings from
the sub-managers.

To limit the records matched, conditions can be added to the given
criteria object. It can contain comparisons like column names that
must match specific values which can be combined by AND, OR or NOT
operators. The resulting string of SQL conditions replaces the
":cond" placeholder before the statement is sent to the database
server.

If the records that are retrieved should be ordered by one or more
columns, the generated string of column / sort direction pairs
replaces the ":order" placeholder. In case no ordering is required,
the complete ORDER BY part including the "/*-orderby*/.../*orderby-*/"
markers is removed to speed up retrieving the records. Columns of
sub-managers can also be used for ordering the result set but then
no index can be used.

The number of returned records can be limited and can start at any
number between the begining and the end of the result set. For that
the ":size" and ":start" placeholders are replaced by the
corresponding values from the criteria object. The default values
are 0 for the start and 100 for the size value.

The SQL statement should conform to the ANSI standard to be
compatible with most relational database systems. This also
includes using double quotes for table and column names.

See also:

* mshop/product/manager/standard/insert/ansi
* mshop/product/manager/standard/update/ansi
* mshop/product/manager/standard/newid/ansi
* mshop/product/manager/standard/delete/ansi
* mshop/product/manager/standard/count/ansi

## search/mysql

Retrieves the records matched by the given criteria in the database

```
mshop/product/manager/standard/search/mysql = 
 SELECT :columns
 	mpro."id" AS "product.id", mpro."siteid" AS "product.siteid",
 	mpro."type" AS "product.type", mpro."code" AS "product.code",
 	mpro."label" AS "product.label", mpro."url" AS "product.url",
 	mpro."start" AS "product.datestart", mpro."end" AS "product.dateend",
 	mpro."status" AS "product.status", mpro."ctime" AS "product.ctime",
 	mpro."mtime" AS "product.mtime", mpro."editor" AS "product.editor",
 	mpro."target" AS "product.target", mpro."dataset" AS "product.dataset",
 	mpro."scale" AS "product.scale", mpro."config" AS "product.config",
 	mpro."rating" AS "product.rating", mpro."ratings" AS "product.ratings"
 FROM "mshop_product" AS mpro
 :joins
 WHERE :cond
 GROUP BY :group mpro."id"
 ORDER BY :order
 LIMIT :size OFFSET :start
```

* Default: 
 SELECT :columns
 	mpro."id" AS "product.id", mpro."siteid" AS "product.siteid",
 	mpro."type" AS "product.type", mpro."code" AS "product.code",
 	mpro."label" AS "product.label", mpro."url" AS "product.url",
 	mpro."start" AS "product.datestart", mpro."end" AS "product.dateend",
 	mpro."status" AS "product.status", mpro."ctime" AS "product.ctime",
 	mpro."mtime" AS "product.mtime", mpro."editor" AS "product.editor",
 	mpro."target" AS "product.target", mpro."dataset" AS "product.dataset",
 	mpro."scale" AS "product.scale", mpro."config" AS "product.config",
 	mpro."rating" AS "product.rating", mpro."ratings" AS "product.ratings"
 FROM "mshop_product" AS mpro
 :joins
 WHERE :cond
 GROUP BY :columns :group
 	mpro."id", mpro."siteid", mpro."type", mpro."code", mpro."label", mpro."url",
 	mpro."target", mpro."dataset", mpro."scale", mpro."config", mpro."start", mpro."end",
 	mpro."status", mpro."ctime", mpro."mtime", mpro."editor", mpro."rating", mpro."ratings"
 ORDER BY :order
 OFFSET :start ROWS FETCH NEXT :size ROWS ONLY


See also:

* mshop/product/manager/standard/search/ansi

## strict-events

Hide events automatically if they are over

```
mshop/product/manager/standard/strict-events = 1
```

* Default: 1
* Type: bool - TRUE to hide events after they are over (default), FALSE to continue to show them
* Since: 2019.10

Events are hidden by default if they are finished, removed from the
list view and can't be bought any more. If you sell webinars including
an archive of old ones you want to continue to sell for example, then
these webinars should be still shown.

Setting this configuration option to false will display event products
that are already over and customers can still buy them.


## update/ansi

Updates an existing product record in the database

```
mshop/product/manager/standard/update/ansi = 
 UPDATE "mshop_product"
 SET :names
 	"type" = ?, "code" = ?, "dataset" = ?, "label" = ?, "url" = ?, "status" = ?, "scale" = ?,
 	"start" = ?, "end" = ?, "config" = ?, "target" = ?, "editor" = ?, "mtime" = ?, "ctime" = ?
 WHERE "siteid" = ? AND "id" = ?
```

* Default: mshop/product/manager/standard/update
* Type: string - SQL statement for updating records
* Since: 2014.03

Items which already have an ID (i.e. the ID is not NULL) will
be updated in the database.

The SQL statement must be a string suitable for being used as
prepared statement. It must include question marks for binding
the values from the product item to the statement before they are
sent to the database server. The order of the columns must
correspond to the order in the saveItems() method, so the
correct values are bound to the columns.

The SQL statement should conform to the ANSI standard to be
compatible with most relational database systems. This also
includes using double quotes for table and column names.

See also:

* mshop/product/manager/standard/insert/ansi
* mshop/product/manager/standard/newid/ansi
* mshop/product/manager/standard/delete/ansi
* mshop/product/manager/standard/search/ansi
* mshop/product/manager/standard/count/ansi

## update/mysql

Updates an existing product record in the database

```
mshop/product/manager/standard/update/mysql = 
 UPDATE "mshop_product"
 SET :names
 	"type" = ?, "code" = ?, "dataset" = ?, "label" = ?, "url" = ?, "status" = ?, "scale" = ?,
 	"start" = ?, "end" = ?, "config" = ?, "target" = ?, "editor" = ?, "mtime" = ?, "ctime" = ?
 WHERE "siteid" = ? AND "id" = ?
```

* Default: 
 UPDATE "mshop_product"
 SET :names
 	"type" = ?, "code" = ?, "dataset" = ?, "label" = ?, "url" = ?, "status" = ?, "scale" = ?,
 	"start" = ?, "end" = ?, "config" = ?, "target" = ?, "editor" = ?, "mtime" = ?, "ctime" = ?
 WHERE "siteid" = ? AND "id" = ?


See also:

* mshop/product/manager/standard/update/ansi

# submanagers

List of manager names that can be instantiated by the product manager

```
mshop/product/manager/submanagers = Array
(
)
```

* Default: Array
* Type: array - List of sub-manager names
* Since: 2014.03

Managers provide a generic interface to the underlying storage.
Each manager has or can have sub-managers caring about particular
aspects. Each of these sub-managers can be instantiated by its
parent manager using the getSubManager() method.

The search keys from sub-managers can be normally used in the
manager as well. It allows you to search for items of the manager
using the search keys of the sub-managers to further limit the
retrieved list of items.


# type
## decorators/excludes

Excludes decorators added by the "common" option from the product type manager

```
mshop/product/manager/type/decorators/excludes = Array
(
)
```

* Default: Array
* Type: array - List of decorator names
* Since: 2014.03

Decorators extend the functionality of a class by adding new aspects
(e.g. log what is currently done), executing the methods of the underlying
class only in certain conditions (e.g. only for logged in users) or
modify what is returned to the caller.

This option allows you to remove a decorator added via
"mshop/common/manager/decorators/default" before they are wrapped
around the product type manager.

```
 mshop/product/manager/type/decorators/excludes = array( 'decorator1' )
```

This would remove the decorator named "decorator1" from the list of
common decorators ("\Aimeos\MShop\Common\Manager\Decorator\*") added via
"mshop/common/manager/decorators/default" for the product type manager.

See also:

* mshop/common/manager/decorators/default
* mshop/product/manager/type/decorators/global
* mshop/product/manager/type/decorators/local

## decorators/global

Adds a list of globally available decorators only to the product type manager

```
mshop/product/manager/type/decorators/global = Array
(
)
```

* Default: Array
* Type: array - List of decorator names
* Since: 2014.03

Decorators extend the functionality of a class by adding new aspects
(e.g. log what is currently done), executing the methods of the underlying
class only in certain conditions (e.g. only for logged in users) or
modify what is returned to the caller.

This option allows you to wrap global decorators
("\Aimeos\MShop\Common\Manager\Decorator\*") around the product type
manager.

```
 mshop/product/manager/type/decorators/global = array( 'decorator1' )
```

This would add the decorator named "decorator1" defined by
"\Aimeos\MShop\Common\Manager\Decorator\Decorator1" only to the product
type manager.

See also:

* mshop/common/manager/decorators/default
* mshop/product/manager/type/decorators/excludes
* mshop/product/manager/type/decorators/local

## decorators/local

Adds a list of local decorators only to the product type manager

```
mshop/product/manager/type/decorators/local = Array
(
)
```

* Default: Array
* Type: array - List of decorator names
* Since: 2014.03

Decorators extend the functionality of a class by adding new aspects
(e.g. log what is currently done), executing the methods of the underlying
class only in certain conditions (e.g. only for logged in users) or
modify what is returned to the caller.

This option allows you to wrap local decorators
("\Aimeos\MShop\Product\Manager\Type\Decorator\*") around the product
type manager.

```
 mshop/product/manager/type/decorators/local = array( 'decorator2' )
```

This would add the decorator named "decorator2" defined by
"\Aimeos\MShop\Product\Manager\Type\Decorator\Decorator2" only to the
product type manager.

See also:

* mshop/common/manager/decorators/default
* mshop/product/manager/type/decorators/excludes
* mshop/product/manager/type/decorators/global

## name

Class name of the used product type manager implementation

```
mshop/product/manager/type/name = Standard
```

* Default: Standard
* Type: string - Last part of the class name
* Since: 2014.03

Each default product type manager can be replaced by an alternative imlementation.
To use this implementation, you have to set the last part of the class
name as configuration value so the manager factory knows which class it
has to instantiate.

For example, if the name of the default class is

```
 \Aimeos\MShop\Product\Manager\Type\Standard
```

and you want to replace it with your own version named

```
 \Aimeos\MShop\Product\Manager\Type\Mytype
```

then you have to set the this configuration option:

```
 mshop/product/manager/type/name = Mytype
```

The value is the last part of your own class name and it's case sensitive,
so take care that the configuration value is exactly named like the last
part of the class name.

The allowed characters of the class name are A-Z, a-z and 0-9. No other
characters are possible! You should always start the last part of the class
name with an upper case character and continue only with lower case characters
or numbers. Avoid chamel case names like "MyType"!


## standard/count/ansi

Counts the number of records matched by the given criteria in the database

```
mshop/product/manager/type/standard/count/ansi = 
 SELECT COUNT(*) AS "count"
 FROM (
 	SELECT mproty."id"
 	FROM "mshop_product_type" AS mproty
 	:joins
 	WHERE :cond
 	ORDER BY mproty."id"
 	OFFSET 0 ROWS FETCH NEXT 10000 ROWS ONLY
 ) AS list
```

* Default: mshop/product/manager/type/standard/count
* Type: string - SQL statement for counting items
* Since: 2014.03

Counts all records matched by the given criteria from the product
database. The records must be from one of the sites that are
configured via the context item. If the current site is part of
a tree of sites, the statement can count all records from the
current site and the complete sub-tree of sites.

As the records can normally be limited by criteria from sub-managers,
their tables must be joined in the SQL context. This is done by
using the "internaldeps" property from the definition of the ID
column of the sub-managers. These internal dependencies specify
the JOIN between the tables and the used columns for joining. The
":joins" placeholder is then replaced by the JOIN strings from
the sub-managers.

To limit the records matched, conditions can be added to the given
criteria object. It can contain comparisons like column names that
must match specific values which can be combined by AND, OR or NOT
operators. The resulting string of SQL conditions replaces the
":cond" placeholder before the statement is sent to the database
server.

Both, the strings for ":joins" and for ":cond" are the same as for
the "search" SQL statement.

Contrary to the "search" statement, it doesn't return any records
but instead the number of records that have been found. As counting
thousands of records can be a long running task, the maximum number
of counted records is limited for performance reasons.

The SQL statement should conform to the ANSI standard to be
compatible with most relational database systems. This also
includes using double quotes for table and column names.

See also:

* mshop/product/manager/type/standard/insert/ansi
* mshop/product/manager/type/standard/update/ansi
* mshop/product/manager/type/standard/newid/ansi
* mshop/product/manager/type/standard/delete/ansi
* mshop/product/manager/type/standard/search/ansi

## standard/count/mysql

Counts the number of records matched by the given criteria in the database

```
mshop/product/manager/type/standard/count/mysql = 
 SELECT COUNT(*) AS "count"
 FROM (
 	SELECT mproty."id"
 	FROM "mshop_product_type" AS mproty
 	:joins
 	WHERE :cond
 	ORDER BY mproty."id"
 	LIMIT 10000 OFFSET 0
 ) AS list
```

* Default: 
 SELECT COUNT(*) AS "count"
 FROM (
 	SELECT mproty."id"
 	FROM "mshop_product_type" AS mproty
 	:joins
 	WHERE :cond
 	ORDER BY mproty."id"
 	OFFSET 0 ROWS FETCH NEXT 10000 ROWS ONLY
 ) AS list


See also:

* mshop/product/manager/type/standard/count/ansi

## standard/delete/ansi

Deletes the items matched by the given IDs from the database

```
mshop/product/manager/type/standard/delete/ansi = 
 DELETE FROM "mshop_product_type"
 WHERE :cond AND siteid = ?
```

* Default: mshop/product/manager/type/standard/delete
* Type: string - SQL statement for deleting items
* Since: 2014.03

Removes the records specified by the given IDs from the product database.
The records must be from the site that is configured via the
context item.

The ":cond" placeholder is replaced by the name of the ID column and
the given ID or list of IDs while the site ID is bound to the question
mark.

The SQL statement should conform to the ANSI standard to be
compatible with most relational database systems. This also
includes using double quotes for table and column names.

See also:

* mshop/product/manager/type/standard/insert/ansi
* mshop/product/manager/type/standard/update/ansi
* mshop/product/manager/type/standard/newid/ansi
* mshop/product/manager/type/standard/search/ansi
* mshop/product/manager/type/standard/count/ansi

## standard/delete/mysql

Deletes the items matched by the given IDs from the database

```
mshop/product/manager/type/standard/delete/mysql = 
 DELETE FROM "mshop_product_type"
 WHERE :cond AND siteid = ?
```

* Default: 
 DELETE FROM "mshop_product_type"
 WHERE :cond AND siteid = ?


See also:

* mshop/product/manager/type/standard/delete/ansi

## standard/insert/ansi

Inserts a new product type record into the database table

```
mshop/product/manager/type/standard/insert/ansi = 
 INSERT INTO "mshop_product_type" ( :names
 	"code", "domain", "label", "pos", "status",
 	"mtime", "editor", "siteid", "ctime"
 ) VALUES ( :values
 	?, ?, ?, ?, ?, ?, ?, ?, ?
 )
```

* Default: mshop/product/manager/type/standard/insert
* Type: string - SQL statement for inserting records
* Since: 2014.03

Items with no ID yet (i.e. the ID is NULL) will be created in
the database and the newly created ID retrieved afterwards
using the "newid" SQL statement.

The SQL statement must be a string suitable for being used as
prepared statement. It must include question marks for binding
the values from the product type item to the statement before they are
sent to the database server. The number of question marks must
be the same as the number of columns listed in the INSERT
statement. The order of the columns must correspond to the
order in the saveItems() method, so the correct values are
bound to the columns.

The SQL statement should conform to the ANSI standard to be
compatible with most relational database systems. This also
includes using double quotes for table and column names.

See also:

* mshop/product/manager/type/standard/update/ansi
* mshop/product/manager/type/standard/newid/ansi
* mshop/product/manager/type/standard/delete/ansi
* mshop/product/manager/type/standard/search/ansi
* mshop/product/manager/type/standard/count/ansi

## standard/insert/mysql

Inserts a new product type record into the database table

```
mshop/product/manager/type/standard/insert/mysql = 
 INSERT INTO "mshop_product_type" ( :names
 	"code", "domain", "label", "pos", "status",
 	"mtime", "editor", "siteid", "ctime"
 ) VALUES ( :values
 	?, ?, ?, ?, ?, ?, ?, ?, ?
 )
```

* Default: 
 INSERT INTO "mshop_product_type" ( :names
 	"code", "domain", "label", "pos", "status",
 	"mtime", "editor", "siteid", "ctime"
 ) VALUES ( :values
 	?, ?, ?, ?, ?, ?, ?, ?, ?
 )


See also:

* mshop/product/manager/type/standard/insert/ansi

## standard/newid/ansi

Retrieves the ID generated by the database when inserting a new record

```
mshop/product/manager/type/standard/newid/ansi = mshop/product/manager/type/standard/newid
```

* Default: mshop/product/manager/type/standard/newid
* Type: string - SQL statement for retrieving the last inserted record ID
* Since: 2014.03

As soon as a new record is inserted into the database table,
the database server generates a new and unique identifier for
that record. This ID can be used for retrieving, updating and
deleting that specific record from the table again.

For MySQL:
```
 SELECT LAST_INSERT_ID()
For PostgreSQL:
 SELECT currval('seq_mproty_id')
For SQL Server:
 SELECT SCOPE_IDENTITY()
For Oracle:
 SELECT "seq_mproty_id".CURRVAL FROM DUAL
```

There's no way to retrive the new ID by a SQL statements that
fits for most database servers as they implement their own
specific way.

See also:

* mshop/product/manager/type/standard/insert/ansi
* mshop/product/manager/type/standard/update/ansi
* mshop/product/manager/type/standard/delete/ansi
* mshop/product/manager/type/standard/search/ansi
* mshop/product/manager/type/standard/count/ansi

## standard/newid/mysql

Retrieves the ID generated by the database when inserting a new record

```
mshop/product/manager/type/standard/newid/mysql = SELECT LAST_INSERT_ID()
```

* Default: mshop/product/manager/type/standard/newid

See also:

* mshop/product/manager/type/standard/newid/ansi

## standard/search/ansi

Retrieves the records matched by the given criteria in the database

```
mshop/product/manager/type/standard/search/ansi = 
 SELECT :columns
 	mproty."id" AS "product.type.id", mproty."siteid" AS "product.type.siteid",
 	mproty."code" AS "product.type.code", mproty."domain" AS "product.type.domain",
 	mproty."label" AS "product.type.label", mproty."status" AS "product.type.status",
 	mproty."mtime" AS "product.type.mtime", mproty."editor" AS "product.type.editor",
 	mproty."ctime" AS "product.type.ctime", mproty."pos" AS "product.type.position"
 FROM "mshop_product_type" AS mproty
 :joins
 WHERE :cond
 ORDER BY :order
 OFFSET :start ROWS FETCH NEXT :size ROWS ONLY
```

* Default: mshop/product/manager/type/standard/search
* Type: string - SQL statement for searching items
* Since: 2014.03

Fetches the records matched by the given criteria from the product
database. The records must be from one of the sites that are
configured via the context item. If the current site is part of
a tree of sites, the SELECT statement can retrieve all records
from the current site and the complete sub-tree of sites.

As the records can normally be limited by criteria from sub-managers,
their tables must be joined in the SQL context. This is done by
using the "internaldeps" property from the definition of the ID
column of the sub-managers. These internal dependencies specify
the JOIN between the tables and the used columns for joining. The
":joins" placeholder is then replaced by the JOIN strings from
the sub-managers.

To limit the records matched, conditions can be added to the given
criteria object. It can contain comparisons like column names that
must match specific values which can be combined by AND, OR or NOT
operators. The resulting string of SQL conditions replaces the
":cond" placeholder before the statement is sent to the database
server.

If the records that are retrieved should be ordered by one or more
columns, the generated string of column / sort direction pairs
replaces the ":order" placeholder. In case no ordering is required,
the complete ORDER BY part including the "/*-orderby*/.../*orderby-*/"
markers is removed to speed up retrieving the records. Columns of
sub-managers can also be used for ordering the result set but then
no index can be used.

The number of returned records can be limited and can start at any
number between the begining and the end of the result set. For that
the ":size" and ":start" placeholders are replaced by the
corresponding values from the criteria object. The default values
are 0 for the start and 100 for the size value.

The SQL statement should conform to the ANSI standard to be
compatible with most relational database systems. This also
includes using double quotes for table and column names.

See also:

* mshop/product/manager/type/standard/insert/ansi
* mshop/product/manager/type/standard/update/ansi
* mshop/product/manager/type/standard/newid/ansi
* mshop/product/manager/type/standard/delete/ansi
* mshop/product/manager/type/standard/count/ansi

## standard/search/mysql

Retrieves the records matched by the given criteria in the database

```
mshop/product/manager/type/standard/search/mysql = 
 SELECT :columns
 	mproty."id" AS "product.type.id", mproty."siteid" AS "product.type.siteid",
 	mproty."code" AS "product.type.code", mproty."domain" AS "product.type.domain",
 	mproty."label" AS "product.type.label", mproty."status" AS "product.type.status",
 	mproty."mtime" AS "product.type.mtime", mproty."editor" AS "product.type.editor",
 	mproty."ctime" AS "product.type.ctime", mproty."pos" AS "product.type.position"
 FROM "mshop_product_type" AS mproty
 :joins
 WHERE :cond
 ORDER BY :order
 LIMIT :size OFFSET :start
```

* Default: 
 SELECT :columns
 	mproty."id" AS "product.type.id", mproty."siteid" AS "product.type.siteid",
 	mproty."code" AS "product.type.code", mproty."domain" AS "product.type.domain",
 	mproty."label" AS "product.type.label", mproty."status" AS "product.type.status",
 	mproty."mtime" AS "product.type.mtime", mproty."editor" AS "product.type.editor",
 	mproty."ctime" AS "product.type.ctime", mproty."pos" AS "product.type.position"
 FROM "mshop_product_type" AS mproty
 :joins
 WHERE :cond
 ORDER BY :order
 OFFSET :start ROWS FETCH NEXT :size ROWS ONLY


See also:

* mshop/product/manager/type/standard/search/ansi

## standard/update/ansi

Updates an existing product type record in the database

```
mshop/product/manager/type/standard/update/ansi = 
 UPDATE "mshop_product_type"
 SET :names
 	"code" = ?, "domain" = ?, "label" = ?, "pos" = ?,
 	"status" = ?, "mtime" = ?, "editor" = ?
 WHERE "siteid" = ? AND "id" = ?
```

* Default: mshop/product/manager/type/standard/update
* Type: string - SQL statement for updating records
* Since: 2014.03

Items which already have an ID (i.e. the ID is not NULL) will
be updated in the database.

The SQL statement must be a string suitable for being used as
prepared statement. It must include question marks for binding
the values from the product type item to the statement before they are
sent to the database server. The order of the columns must
correspond to the order in the saveItems() method, so the
correct values are bound to the columns.

The SQL statement should conform to the ANSI standard to be
compatible with most relational database systems. This also
includes using double quotes for table and column names.

See also:

* mshop/product/manager/type/standard/insert/ansi
* mshop/product/manager/type/standard/newid/ansi
* mshop/product/manager/type/standard/delete/ansi
* mshop/product/manager/type/standard/search/ansi
* mshop/product/manager/type/standard/count/ansi

## standard/update/mysql

Updates an existing product type record in the database

```
mshop/product/manager/type/standard/update/mysql = 
 UPDATE "mshop_product_type"
 SET :names
 	"code" = ?, "domain" = ?, "label" = ?, "pos" = ?,
 	"status" = ?, "mtime" = ?, "editor" = ?
 WHERE "siteid" = ? AND "id" = ?
```

* Default: 
 UPDATE "mshop_product_type"
 SET :names
 	"code" = ?, "domain" = ?, "label" = ?, "pos" = ?,
 	"status" = ?, "mtime" = ?, "editor" = ?
 WHERE "siteid" = ? AND "id" = ?


See also:

* mshop/product/manager/type/standard/update/ansi

## submanagers

List of manager names that can be instantiated by the product type manager

```
mshop/product/manager/type/submanagers = Array
(
)
```

* Default: Array
* Type: array - List of sub-manager names
* Since: 2014.03

Managers provide a generic interface to the underlying storage.
Each manager has or can have sub-managers caring about particular
aspects. Each of these sub-managers can be instantiated by its
parent manager using the getSubManager() method.

The search keys from sub-managers can be normally used in the
manager as well. It allows you to search for items of the manager
using the search keys of the sub-managers to further limit the
retrieved list of items.
