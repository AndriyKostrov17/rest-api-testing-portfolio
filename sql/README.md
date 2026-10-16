# SQL Practice — PostgreSQL

## Objective

This directory contains SQL exercises used to practice database querying and data verification techniques relevant to QA testing.

## Environment

- Database: PostgreSQL
- Practice dataset: Sakila
- Query language: SQL

Sakila is a separate learning database. It is not connected to the WordPress REST API used in this project.

## Topics Covered

- `SELECT` — retrieve data
- `WHERE` — filter records
- `ORDER BY` — sort results
- `LIMIT` — restrict the number of returned rows
- `COUNT()` — count records
- `JOIN` — combine related tables

## QA Applications

These techniques can help verify:

- Whether records satisfy specified conditions
- Whether query results are sorted correctly
- Whether the expected number of records is returned
- Whether related records can be retrieved through table relationships
- Whether database results match expected business rules

## SQL Examples

SQL scripts and examples will be added after the queries have been reviewed and verified against the Sakila schema.

## Limitations

- Queries are intended for practice and learning.
- No direct database access to the WordPress project is available.
- SQL results must not be presented as verification of WordPress API data unless a real, documented connection between the API and database has been established.