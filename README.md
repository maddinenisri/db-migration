# db-migration
Test project to test liquibase functionality with existing database schema.

### Used existing mysql db.

##Steps:

1) generateChangeLog from existing database using
```
mvn liquibase:generateChangeLog
```

2) Sync this changeLogSet with database. It will insert record into DatabaseChangeLog.
```
mvn liquibase:changelogSync
```

3) Create new changeset file and execute update command.
```
mvn liquibase:update
```
