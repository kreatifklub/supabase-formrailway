FROM kong:2.8.1

USER root
RUN apk add --no-cache gettext

COPY kong.yml /home/kong/kong.template.yml

USER kong

ENTRYPOINT ["/bin/sh", "-c"]
CMD ["envsubst < /home/kong/kong.template.yml > /home/kong/kong.yml && exec /docker-entrypoint.sh kong docker-start"]
