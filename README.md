# About the FAA Dataset

The NTSB FAA Dataset includes information about flights, airports, carriers, and aircrafts. We are providing here a small subset of the full dataset (available in BigQuery) for the purpose of trying out Malloy; please note that the data is INCOMPLETE and to properly analyze this data the full dataset available in BigQuery should be used.

## Overview of models

This set of models is a great place to get introduced to Malloy for the first time. You can use this model to follow along with the [Malloy by Example document](https://malloydata.github.io/malloy/documentation/malloy-by-example.html).

**`1_airports`** - the simplest model, using only the airports table. Start here to get familiar with core concepts in Malloy.

**`2_flights`** - defines as a source each table, and defines join relationships between them;  adds a few useful fields

**`9_test`** - looks at the aircraft used by carriers. Demonstrates simplification of working with aggregates in Malloy.


**Aircraft**

|  id | tail_num | aircraft_serial | aircraft_model_code | aircraft_engine_code | year_built | aircraft_type_id | aircraft_engine_type_id | registrant_type_id | name                          | address1                | address2 | city         | state | zip        | region | county | country | certification | status_code | mode_s_code | fract_owner | last_action_date | cert_issue_date | air_worth_date |   |
|----:|----------|-----------------|---------------------|----------------------|-----------:|-----------------:|------------------------:|-------------------:|-------------------------------|-------------------------|----------|--------------|-------|------------|--------|--------|---------|---------------|-------------|-------------|-------------|------------------|-----------------|----------------|:-:|
| 100 | N10036   | 11906           | 7100510             | 17003                |      1,944 |                4 |                       1 |                  1 | FORSBERG CHARLES P            | PO BOX 1                | null     | NORTH SUTTON | NH    | 03260-0001 | E      | 013    | US      | 1N            | A           | 50003624    | null        | 2006-01-17       | 1982-04-27      | 1972-09-11     |   |
| 200 | N1006L   | 1234            | 05620R2             | null                 |      2,000 |                4 |                       1 |                  1 | BOEGER BOGIE M                | 7246 235TH ST           | null     | MEDIAPOLIS   | IA    | 52637-9184 | 3      | 057    | US      | null          | V           | 50003751    | null        | 2005-10-27       | 2005-10-27      | ∅              |   |
| 300 | N1009P   | 34994           | 2072704             | 17026                |      1,958 |                4 |                       1 |                  4 | FERRIER WILLIAM T             | 221 N CENTRAL AVE # D86 | null     | MEDFORD      | OR    | 97501-5927 | S      | 029    | US      | 1             | V           | 50004125    | null        | 2003-09-19       | 2003-09-19      | 1958-02-21     |   |
| 400 | N100EJ   | 380-1           | 6402618             | 30010                |      1,973 |                5 |                       4 |                  3 | CENTURION INVESTMENTS INC DBA | 18377 EDISON AVE        | null     | CHESTERFIELD | MO    | 63005-3628 | 3      | 189    | US      | 1T            | A           | 50002441    | null        | 2004-03-16       | 2001-03-22      | 1974-02-18     |   |
| 500 | N100KW   | D-10336         | 1151548             | 17032                |      1,980 |                4 |                       1 |                  3 | MIKRON AIR CORP               | 3505 TEXOMA PKWY        | null     | SHERMAN      | TX    | 75090      | 2      | 181    | US      | 1U            | A           | 50002652    | null        | 2003-12-16       | 1994-12-22      | 1980-01-29     |   |

**Aircraft Models**

| aircraft_model_code | manufacturer          | model | aircraft_type_id | aircraft_engine_type_id | aircraft_category_id | amateur | engines | seats | weight | speed |   |
|---------------------|-----------------------|-------|-----------------:|------------------------:|---------------------:|--------:|--------:|------:|-------:|------:|:-:|
| 05637J7             | WILCOX H L/WILCOX C N | CW    |                2 |                       0 |                    3 |       1 |       0 |     0 |      0 |     0 |   |
| 0563784             | WILCOX                | HW    |                2 |                       0 |                    1 |       1 |       0 |     0 |      0 |    60 |   |
| 0563788             | STOKES                | JS    |                2 |                       0 |                    1 |       1 |       0 |     0 |      0 |    60 |   |
| 05637F7             | KAMIN DENNIS ROBERT   | OZ    |                2 |                       0 |                    1 |       1 |       0 |     0 |      0 |     0 |   |
| 0610003             | MLB                   | 002   |                4 |                       1 |                    1 |       2 |       1 |     0 |      0 |     0 |   |
