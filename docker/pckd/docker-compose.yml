```yml
version: "3"

services:
  server:
    build:
      context: ./server
    volumes:
      - ./logs:/home/node/app/logs
    environment:
      - DATABASE_URL=postgresql://postgres:postgres@db/pckd
      - DATABASE_TYPE=postgres

      - JWT_SECRET=YourPasswordHere
      - IPREGISTRY_API_KEY=apikey
    depends_on:
      - db

  frontend:
    build:
      context: ./client
    ports:
      - 8013:80
    environment:
      - BACKEND_URL=http://server:4000

  db:
    image: postgres:13-alpine
    volumes:
      - ./db:/var/lib/postgresql/data
    environment:
      - POSTGRES_USER=postgres
      - POSTGRES_PASSWORD=YourPasswordHere
      - POSTGRES_DB=pckd
```
