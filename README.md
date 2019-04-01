# data-processing
Me doing datascience stuff

# dji data set
https://archive.ics.uci.edu/ml/datasets/Dow+Jones+Index

- create postgres user
sudo su postgres
create user dji_db with password 'hellohello';
create database dji with owner dji_db;
- connect
\c dji
- run code from notebook
select * from dow_jones_index;
if bad thing happen -> 
DROP TABLE dow_jones_index; 
and re run in the jupyter notebook
- start grafana
sudo service grafana-server start
- go to http://localhost:3000
user admin, pass admin
create panel, example ->

```sql
SELECT
  date AS "time",
  percent_change_price
FROM dow_jones_index
WHERE
 date >  1299214800

ORDER BY 1```

save
