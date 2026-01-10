FROM kong:2.8.1

USER root
RUN apk add --no-cache gettext
USER kong

COPY kong.yml /home/kong/kong.template.yml

ENTRYPOINT ["sh", "-c", "envsubst < /home/kong/kong.template.yml > /home/kong/kong.yml && exec kong docker-start"]
