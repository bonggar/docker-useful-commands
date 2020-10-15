### Import Large SQL file

Copy the dump file into docker container
- `docker cp file.sql container:/tmp/file.sql`

Import the dump file into database from container bash
- `psql -d dbName -U roleName < /tmp/file.sql`
