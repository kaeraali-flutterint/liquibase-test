# Liquibase Demo

## Usage

Apply all migrations defined in changelog.yaml against the dev.db sqlite file:

```
liquibase update --defaults-file=dev.liquibase.properties
```

## Development

We prefer yaml for liquibase changes because these can be rolled back and are relatively easy to use. We specify the liquibase change schema in every file so that your editor can easily validate them

1. Create the new migration in the migrations directory
2. Raise a PR and view the checks
3. Get the PR merged and wait for the migrations to be run

# Known issues

- The sqlite databases aren't committed back to git
