# Create a new PostgreSQL container locally with exposed port and shared folder

```
docker run --name SOMETHING_postgres -p 5432:5432 -v pgdata:/var/lib/postgresql/data -e POSTGRES_PASSWORD=password postgres:10.10
```

