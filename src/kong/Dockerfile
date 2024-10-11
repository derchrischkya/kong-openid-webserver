FROM kong:2.5.0

USER root

# Install required dependencies (including OpenSSL development headers and build tools)
RUN apk update && \
    apk add --no-cache openssl-dev build-base git


# Copy the custom plugin into the Kong plugins directory
COPY /custom-plugins/token-introspection /usr/local/share/lua/5.1/kong/plugins/token-introspection


WORKDIR /custom-plugins


USER kong
