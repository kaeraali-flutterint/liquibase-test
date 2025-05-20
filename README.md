# Liquibase Demo

## Usage

Apply all migrations defined in changelog.yaml against the dev.db sqlite file:

```
liquibase update --defaults-file=dev.liquibase.properties
```

## Development

We prefer yaml for liquibase changes because these can be rolled back and are relatively easy to use. We specify the liquibase change schema in every file so that your editor can easily validate them

1. Create the new migration in the migrations directory
2. Run `liquibase update-sql` to show what SQL it would run
3. Raise a PR and get it merged
4. Manually run `liquibase update` against each environment from the main branch

## TODO

- [ ] Create a GitHub Action workflow to run [validate](https://github.com/liquibase-github-actions/validate), [update-testing-rollback](https://github.com/liquibase-github-actions/update-testing-rollback) and [update-sql](https://github.com/liquibase-github-actions/update-sql) against a sandbox environment on PRs
- [ ] Create a GitHub Action workflow to run [update](https://github.com/liquibase-github-actions/update) in a matrix for all environments on merge

