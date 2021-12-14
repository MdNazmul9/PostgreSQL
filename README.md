# PostgreSQL

# PostgreSQL trigger function basic syntex

```
CREATE FUNCTION trigger_function()
	RETURNS TRIGGER
  	LANGUAGE PLPGSQL
AS $$
BEGIN
	-- trigger logic
END;
$$

```
# Trigger statement

```
CREATE TRIGGER trigger_name
	{BEFORE | AFTER} {event}
	ON table_name
	[FOR [EACH] { ROW | STATEMENT}]
		EXECUTE PROCEDURE trigger_function
	
```

# create table
```
create table book(
	isbn int,
	title varchar(50) not null,
	item_price numeric(6,2) not null,
	no_copies int default 10,
	total_price numeric(8,2),
	primary key(isbn)
);
```
# Insert value to the table
```
insert into book values (101, 'Database Management System', 450.5, 5);

insert into book values (102, 'Database Query Language', 350.5, 5);

```
# delete all row
```
delete from book;

```
# comment PostgresSQL
```
/* delete from book;*/
```

# Select All data from the table / query table
```
select * from book;
```
# Create a tigger for calculating total price 
```

```

