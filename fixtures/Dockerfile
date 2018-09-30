FROM jumanjiman/caddy
USER root
RUN apk add --no-cache hugo
COPY caddyfile /etc/caddy/caddyfile
COPY hello /cgi-bin/
COPY landing_page /src
COPY build_landing_page /usr/bin/
USER caddy
