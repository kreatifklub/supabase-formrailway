FROM kong:2.8.1

USER root
RUN apk add --no-cache gettext

COPY kong.yml /home/kong/kong.template.yml

USER kong

ENTRYPOINT sh -c "envsubst < /home/kong/kong.template.yml > /home/kong/kong.yml && kong start"
