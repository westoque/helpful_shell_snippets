#### PostgreSQL

Create a new PostgreSQL container locally with exposed port and shared folder

```
docker run --name SOMETHING_postgres -p 5432:5432 -v pgdata:/var/lib/postgresql/data -e POSTGRES_PASSWORD=password postgres:10.10
```

Run `pg_restore` in a container

```
docker run --rm -i -t -v pgdata:/var/lib/postgresql/data -e POSTGRES_PASSWORD=password postgres:10.10 pg_restore
```

#### Login Using ECR

```
aws ecr get-login-password --region region | docker login --username AWS --password-stdin aws_account_id.dkr.ecr.region.amazonaws.com
```
