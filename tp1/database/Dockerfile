FROM postgres:11.6-alpine

COPY 01-CreateScheme.sql /docker-entrypoint-initdb.d/01-CreateScheme.sql
COPY 02-InsertData.sql /docker-entrypoint-initdb.d/02-InsertData.sql

ENV POSTGRES_DB=db \
   POSTGRES_USER=usr \
   POSTGRES_PASSWORD=pwd