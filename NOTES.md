# Setting up the Working Environment

## docker

```bash
docker pull postgres
docker volume create  pgdata

docker run --name postgres_test -v pgdata:/var/lib/postgresql/data -e POSTGRES_PASSWORD=mysecrectpassword -p 5432:5432 -d postgres
docker exec -it postgres_test bash

docker container rm --force psotgres_test
apt-get update
apt-get install wget

cd /tmp;
wget http://linux.dell.com/dvdstore/ds21.tar.gz
wget http://linux.dell.com/dvdstore/ds21_postgresql.tar.gz
tar -zxvf ds2.tar.gz
tar -zxvf ds2_postgresql.tar.gz
cd /tmp/ds2/pgsqlds2
sed -e 's/SYSDBA=ds2/SYSDBA=postgres' -e 's/PASSWORD="ds2"/password="mysecrectpassword"/' pgsqlds2_create_all.sh > pgsqlds2_create_all_custom.sh
bash pgsqlds2_create_all_custom.sh

```

## Azure Data Studio

## PostgreSQL


# Data types

## ANSI SQL Data types

+ Character types
+ Binary types
+ Numeric types
  + Exact
  + Approximate
+ Date/time types
+ Boolean type
+ Array type

## extral data type

+ UUID
+ XML
+ JSON
+ BIT STRING
+ ENUM
+ GEOMETRIC
+ NETWORK
+ RANGE
+ DOMAIN

# Doing math
# Handling character data
# Data and time functions
# Windowing functions
# Conditional functions and subqueries
# Using array and range functions
# Metadata functions

