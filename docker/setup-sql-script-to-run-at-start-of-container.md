# Setup sql script to run when docker container starts
```
version: '3.7'
services:

  postgres:
    image: postgres:9.5-alpine
    volumes:
      - postgres-data:/var/lib/postgresql/data
      - ./path/to/script-file.sql:/docker-entrypoint-initdb.d/script-file.sql
    ports:
      - '5432:5432'
    environment:
      ...
```
