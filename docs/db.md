# Database setup

## macos

### Install Postgres

`brew install postgres`

### Create and configure user and db

```
$ createuser orduser
$ createdb ordscanner
$ psql
?=# alter user orduser with encrypted password 'testtest';
?=# grant all privileges on database ordscanner to orduser;
```

### Reset the db

```
$ psql
$-# \c ordscanner
ordscanner=#TRUNCATE TABLE inscription_records;
```