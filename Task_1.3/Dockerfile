FROM postgres:latest
ENV POSTGRES_PASSWORD=postgres
ENV POSTGRES_USER=postgres
ENV POSTGRES_DB=testdb
ENV POSTGRES_HOST=db
COPY init_scripts/init.sql /docker-entrypoint-initdb.d/init.sql