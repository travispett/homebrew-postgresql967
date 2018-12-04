# Homebrew postgres@9.6

Postgres 9.6.8 changed `pg_dump` to prepend "public." to all table references. This is annoying when a dump file is under version control and shared by users of Postgres < 9.6.8 who are also dumping that same file (Rails `structure.sql`). This repo is a tap for Postgres 9.6.7.

To uninstall the official Homebrew tap of Postgres and install this one:
```shell
brew uninstall postgresql@9.6
brew cleanup postgresql@9.6
```

To install this Homebrew tap:
```shell
brew install travispett/homebrew-postgresql967/postgresql@9.6
brew link -f postgresql@9.6
```

To uninstall this Homebrew tap and reinstall the main Postgres tap:
```shell
brew uninstall postgresql@9.6
brew cleanup postgresql@9.6
brew install postgresql@9.6
brew link -f postgresql@9.6
brew services restart postgresql@9.6
```
