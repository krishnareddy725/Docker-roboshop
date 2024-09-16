FROM mysql:5.7

# Environment variable names should use underscores, not dashes
ENV MYSQL_ROOT_PASSWORD=Roboshop@1 \
    MYSQL_DATABASE=cities \
    MYSQL_USER=shipping \
    MYSQL_PASSWORD=Roboshop@1

# Correct the path to initialization scripts
COPY scripts/* /docker-entrypoint-initdb.d/
