FROM jumanjiman/caddy
USER root
RUN apk add --no-cache hugo
COPY caddyfile /etc/caddy/caddyfile
COPY hello /cgi-bin/
COPY landing_page /src
COPY build_landing_page /usr/bin/
RUN build_landing_page && \
    chown -R root:root /var/www && \
    mkdir /var/www/uploads && \
    mkdir /var/www/git && \
    chown caddy:caddy /var/www/uploads && \
    chown caddy:caddy /var/www/git
USER caddy
