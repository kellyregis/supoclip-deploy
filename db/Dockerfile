# Custom Postgres image that bakes the SupoClip schema init script.
# Coolify rewrites relative compose bind-mounts to a managed path that the repo
# file never lands in, so ./init.sql:/docker-entrypoint-initdb.d never works.
# Baking it into the image guarantees the schema is created on first boot.
FROM postgres:15-alpine
COPY init.sql /docker-entrypoint-initdb.d/init.sql
