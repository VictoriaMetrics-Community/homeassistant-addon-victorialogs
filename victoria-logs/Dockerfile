ARG BUILD_FROM
FROM $BUILD_FROM

# Copy data for add-on
COPY start-victoria-logs /
WORKDIR /share/victoria-logs-data
ARG VERSION=v1.18.0-victorialogs

RUN /bin/bash -c 'set -ex && \
    ARCH=$(uname -m) && \
    if [ "$ARCH" == "x86_64" ]; then \
        wget https://github.com/VictoriaMetrics/VictoriaMetrics/releases/download/$VERSION/victoria-logs-linux-amd64-$VERSION.tar.gz -qO- | tar xvz -C /; \
    elif [[ "$ARCH" == "arm"* ]]; then \
        wget https://github.com/VictoriaMetrics/VictoriaMetrics/releases/download/$VERSION/victoria-logs-linux-arm-$VERSION.tar.gz -qO- | tar xvz -C /; \
    elif [ "$ARCH" == "aarch64" ]; then \
        wget https://github.com/VictoriaMetrics/VictoriaMetrics/releases/download/$VERSION/victoria-logs-linux-arm64-$VERSION.tar.gz -qO- | tar xvz -C /; \
    else \
        echo "Unsupported architecture $ARCH"; \
        return -1; \
    fi'

RUN chmod a+x /victoria-logs-prod
RUN chmod a+x /start-victoria-logs

CMD [ "/start-victoria-logs"]
