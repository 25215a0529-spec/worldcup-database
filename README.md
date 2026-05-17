# World Cup Database Project

This project is part of the Relational Database Certification from freeCodeCamp.

## Project Overview

The project uses PostgreSQL and Bash scripting to:

* Create a relational database named `worldcup`
* Store World Cup teams and match data
* Insert data automatically from a CSV file
* Run SQL queries to analyze tournament statistics

## Technologies Used

* PostgreSQL
* Bash Scripting
* SQL
* Linux Terminal

## Files Included

### `worldcup.sql`

Database dump file containing:

* Database creation commands
* Table structures
* Inserted data

### `insert_data.sh`

Bash script that:

* Reads data from `games.csv`
* Inserts unique teams into the `teams` table
* Inserts match records into the `games` table

### `queries.sh`

Contains SQL queries to retrieve:

* Total goals
* Average goals
* Tournament winners
* Team statistics
* Champion history

## Database Structure

### Teams Table

| Column  | Type                    |
| ------- | ----------------------- |
| team_id | SERIAL PRIMARY KEY      |
| name    | VARCHAR UNIQUE NOT NULL |

### Games Table

| Column         | Type               |
| -------------- | ------------------ |
| game_id        | SERIAL PRIMARY KEY |
| year           | INT                |
| round          | VARCHAR            |
| winner_id      | FOREIGN KEY        |
| opponent_id    | FOREIGN KEY        |
| winner_goals   | INT                |
| opponent_goals | INT                |

## How to Run

### Restore Database

```bash
psql -U postgres < worldcup.sql
```

### Run Insert Script

```bash
./insert_data.sh
```

### Run Queries

```bash
./queries.sh
```

## Learning Outcomes

Through this project, I learned:

* PostgreSQL database creation
* Table relationships and foreign keys
* Bash scripting with SQL commands
* CSV data handling
* Writing analytical SQL queries

## Author

Poojitha Pathinavalasa
