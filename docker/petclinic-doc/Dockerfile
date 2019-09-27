FROM docker.pkg.github.com/t-kiyono/github-actions-test/asciidoctorj

ARG POSTGRESQL_DRIVER_VERSION=42.2.6

RUN apt-get update && \
    apt-get install --no-install-recommends -y postgresql-client-11 && \
    apt-get clean && \
    rm -rf /var/cache/apt/archives/* && \
    rm -rf /var/lib/apt/lists/*

ADD https://github.com/schemaspy/schemaspy/releases/download/v6.0.0/schemaspy-6.0.0.jar /
RUN chmod 0664 /schemaspy-6.0.0.jar

ADD http://search.maven.org/remotecontent?filepath=org/postgresql/postgresql/${POSTGRESQL_DRIVER_VERSION}/postgresql-${POSTGRESQL_DRIVER_VERSION}.jar /drivers/postgresql-${POSTGRESQL_DRIVER_VERSION}.jar
RUN chmod 0664 /drivers/*
