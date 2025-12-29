# CS50 Problem Set 7 - Movies

This repository contains my solution for the "Movies" problem from Harvard's CS50 course. The project involves writing complex SQL queries to analyze a large database of movies, stars, directors, and ratings from IMDb.

## Files

- `movies.db` (Which i couldn't push because of size) : A SQLite database containing five tables: `movies`, `stars`, `directors`, `people`, and `ratings`.

- `1.sql` through `13.sql` : Individual SQL files, where each file contains a single query to answer a specific question posed by the problem set.

## Description

The goal of this project is to practice advanced SQL techniques, particularly joining multiple tables to discover relationships between data.

The queries perform the following tasks:

- Filtering & Sorting: Retrieving movies based on release year or title patterns (e.g., "Harry Potter").
- Aggregation: Calculating counts of high-rated movies and average ratings for specific years.
- Multi-Table Joins: Linking `movies` to `people` via `stars` and `directors` tables to find cast and crew information.
- Nested Queries: Using subqueries to find specific IDs (e.g., finding the ID of "Kevin Bacon") to use in broader filters.
- Complex Logic: Answering advanced questions like "List all movies in which both Johnny Depp and Helena Bonham Carter starred."

## Output Behavior

Each `.sql` file outputs specific data sets:

- `1.sql`: Titles of all movies released in 2008.
- `2.sql`: The birth year of Emma Stone.
- `3.sql`: Titles of all movies with a release date on or after 2018, sorted alphabetically.
- `4.sql`: The number of movies with an IMDb rating of 10.0.
- `5.sql`: Titles and release years of all Harry Potter movies, sorted chronologically.
- `6.sql`: The average rating of all movies released in 2012.
- `7.sql`: Movies released in 2010 ordered by rating (descending), then title.
- `8.sql`: Names of all people who starred in "Toy Story".
- `9.sql`: Names of all people who starred in a movie released in 2004, ordered by birth year.
- `10.sql`: Names of all people who have directed a movie that received a rating of at least 9.0.
- `11.sql`: Titles of the five highest-rated movies (in order) that Chadwick Boseman starred in.
- `12.sql`: Titles of all movies in which both Johnny Depp and Helena Bonham Carter starred.
- `13.sql`: Names of all people who starred in a movie in which Kevin Bacon also starred.

## Example Run

To run a query, the contents of the SQL file are piped into the SQLite command-line tool.

```bash
$ cat 1.sql | sqlite3 movies.db
The Dark Knight
Iron Man
...
```

## How to Run

You can execute the queries using the sqlite3 command-line interface.

Run a single query file:

```bash
cat 1.sql | sqlite3 movies.db

```

Enter interactive mode:

```bash
sqlite3 movies.db
sqlite> .read 1.sql
```
