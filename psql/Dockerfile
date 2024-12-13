FROM postgres:latest

COPY ./pg_hba.conf /etc/postgresql/pg_hba.conf

RUN echo "hba_file = '/etc/postgresql/pg_hba.conf'" >> /usr/share/postgresql/postgresql.conf.sample

# COPY write_up_dump.sql /docker-entrypoint-initdb.d/
# COPY init-db.sh /docker-entrypoint-initdb.d/

EXPOSE 5432
# RUN chmod +x /docker-entrypoint-initdb.d/init-db.sh
