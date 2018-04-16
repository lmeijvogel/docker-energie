FROM alpine

RUN apk update
RUN apk add mysql-client curl

ENV SCHEMA_URL=https://raw.githubusercontent.com/lmeijvogel/meter-reader-api/${REPO_VERSION}/init_db.sql

RUN curl ${SCHEMA_URL} >/tmp/schema.db

CMD sleep 1 && mysql -h mariadb --user=${MYSQL_USER} --password=${MYSQL_PASSWORD} ${MYSQL_DATABASE} < /tmp/schema.db
