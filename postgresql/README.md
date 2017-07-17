POSTGRESQL VERSION (source: https://hub.docker.com/_/postgres/)

**POSTGRESQL-VERSION 9.6**

- DOCKER VERSION: paloit/deb-stretch-fr:1.0.0
- TAG NAME: paloit/postgresql-fr:9.6
- GOSU VERSION: 1.7
- PG KEY: B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8
- PG MAJOR: 9.6
- PG VERSION: 9.6.3-1.pgdg80+1
- COMMANDS:

        ./build paloit/deb-stretch-fr:1.0.0 paloit/postgresql-fr:9.6 1.7 B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8 9.6 9.6.3-1.pgdg80+1
        ./push paloit/postgresql-fr:9.6 true (docker hub repository)
        docker pull paloit/postgresql-fr:9.6

**ENVIRONMENT VARIABLES**

The PostgreSQL image uses several environment variables which are easy to miss. While none of the variables are required, they may significantly aid you in using the image.

- **POSTGRES_PASSWORD**

    This environment variable is recommended for you to use the PostgreSQL image. This environment variable sets the superuser password for PostgreSQL. The default superuser is defined by the POSTGRES_USER environment variable. In the above example, it is being set to "mysecretpassword".
    
    **Note:** The PostgreSQL image sets up trust authentication locally so you may notice a password is not required when connecting from localhost (inside the same container). However, a password will be required if connecting from a different host/container.

- **POSTGRES_USER**

    This optional environment variable is used in conjunction with POSTGRES_PASSWORD to set a user and its password. This variable will create the specified user with superuser power and a database with the same name. If it is not specified, then the default user of postgres will be used.

- **PGDATA**

    This optional environment variable can be used to define another location - like a subdirectory - for the database files. The default is /var/lib/postgresql/data, but if the data volume you're using is a fs mountpoint (like with GCE persistent disks), Postgres initdb recommends a subdirectory (for example /var/lib/postgresql/data/pgdata ) be created to contain the data.

- **POSTGRES_DB**

    This optional environment variable can be used to define a different name for the default database that is created when the image is first started. If it is not specified, then the value of POSTGRES_USER will be used.

- **POSTGRES_INITDB_ARGS**

    This optional environment variable can be used to send arguments to postgres initdb. The value is a space separated string of arguments as postgres initdb would expect them. This is useful for adding functionality like data page checksums: -e POSTGRES_INITDB_ARGS="--data-checksums".

- **POSTGRES_INITDB_XLOGDIR**

    This optional environment variable can be used to define another location for the Postgres transaction log. By default the transaction log is stored in a subdirectory of the main Postgres data folder (PGDATA). Sometimes it can be desireable to store the transaction log in a different directory which may be backed by storage with different performance or reliability characteristics.
