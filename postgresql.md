# PostgreSQL

PostgreSQL is an open source relational database management system \(RDBMS\). It is the default database for macOS server.

## Installation

```bash
brew install postgres
```

After this, we can test the installation status by checking the version of installed PostgreSQL

```bash
postgres -V
```

## Usage

### Start PostgreSQL server

```bash
pg_ctl -D /usr/local/var/postgres start
```

Or you can start the PostgreSQL server and have it start up at login automatically

```bash
brew services start postgresql
```

### Stop PostgreSQL server

```bash
pg_ctl -D /usr/local/var/postgres stop
```

To make it stop starting up automatically at login

```bash
brew services stop postgresql
```

### Restart PostgreSQL server

```bash
pg_ctl -D /usr/local/var/postgres restart
```

Or if you're using `homebrew`

```bash
brew services restart postgresql
```

### Start PostgreSQL console

```bash
psql
```

### GUI tool

We can use `psequel` a free GUI tool for managing the local and remote PostgreSQL databases

Install `psequel` using `homebrew`

```bash
brew install psequel
```

