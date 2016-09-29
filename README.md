# db-migration
Test project to test liquibase functionality with existing database schema.

Used existing mysql db.

Steps:

1) generateChangeLog from existing database using
{code}
mvn liquibase:generateChangeLog
{code}

2) Sync this changeLogSet with database. It will insert record into DatabaseChangeLog.
{code}
mvn liquibase:changelogSync
{code}

3) Create new changeset file and execute update command.
{code}
mvn liquibase:update
{code}
