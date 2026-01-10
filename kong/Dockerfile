@ -1,6 +1,12 @@
FROM kong:2.8.1

USER 0

RUN apk add --no-cache gettext

COPY ./kong.yml /home/kong/temp.yml
RUN chown kong:kong /home/kong/temp.yml

USER kong

ENTRYPOINT /bin/sh -c "envsubst < /home/kong/temp.yml > /home/kong/kong.yml && exec /docker-entrypoint.sh kong docker-start"