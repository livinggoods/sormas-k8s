FROM bitnami/postgresql:10.12.0-debian-10-r34
USER root
RUN mkdir -p /var/lib/apt/lists/partial && apt-get update -y && apt-get install -y libpq-dev  postgresql-server-dev-all make gcc pgxnclient && pgxn install temporal_tables
RUN apt-get clean 
RUN apt-get purge -y && apt-get purge -y libpq-dev postgresql-server-dev-all make gcc pgxnclient
USER 1001