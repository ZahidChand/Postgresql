# Connecting to a PostgreSQL Database

There are two ways to connect to a PostgreSQL database:

## Method 1

### Syntax:

```sh
psql -U <userName> -p <port> -h <host> <dbName>
```
In this syntax, the options are:

* `-U` is the username.
* `-p` specifies the port; the default port for PostgreSQL is 5432.
* `-h` specifies the host.
* `<dbName>` is the name of the database.


### Example

```sh
psql -U postgres -p 5432 -h localhost test
```

This command connects to the test database hosted on localhost using the postgres user.


## Method 2: Navigating to a Database after Logging In

After logging in using the username `postgres`, you can navigate to a database using the following steps:

1. **Connect to the PostgreSQL command-line interface** by typing:

    ```sh
    psql -U postgres -h localhost
    ```

    This command establishes a connection to the PostgreSQL server using the `postgres` username and `localhost` host.

2. Once logged in, type `\l` to **list all databases**.

3. To **navigate to a specific database**, use the command:

    ```sql
    \c <databaseName>
    ```

    Replace `<databaseName>` with the name of the database you want to connect to.

### Example:

To navigate to the `test` database, type:

```sql
\c test
```

