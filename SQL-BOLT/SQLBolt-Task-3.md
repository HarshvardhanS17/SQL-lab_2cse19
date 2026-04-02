# SQLBolt - Task 3

## Question 1

Find all the Toy Story movies ✓

```sql
SELECT * FROM movies WHERE title LIKE 'Toy%' ;
```

## Question 2

Find all the movies directed by John Lasseter

```sql
SELECT * FROM movies WHERE director = 'John Lasseter';
```

## Question 3

Find all the movies NOT directed by John Lasseter

```sql
SELECT * FROM movies WHERE director != 'John Lasseter';
```

## Question 4

Find all the WALL-* movies

```sql
SELECT * FROM movies WHERE title LIKE 'WALL-%';
```

