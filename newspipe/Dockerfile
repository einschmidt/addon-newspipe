ARG BUILD_FROM
FROM $BUILD_FROM

ENV LANG C.UTF-8

# Build arguments
ARG BUILD_ARCH
ARG BUILD_DATE
ARG BUILD_REF
ARG BUILD_VERSION

# Install basics
RUN apk add --no-cache git \
            npm

# Install requirements for add-on
RUN curl -sSL https://raw.githubusercontent.com/python-poetry/poetry/master/get-poetry.py | python -

RUN git clone https://git.sr.ht/~cedric/newspipe

# Copy root filesystem
#COPY rootfs /

# Labels
LABEL \
    io.hass.name="newspipe" \
    io.hass.description="newspipe" \
    io.hass.arch="${BUILD_ARCH}" \
    io.hass.type="addon" \
    io.hass.version=${BUILD_VERSION} \
    maintainer="Berichta" \
    org.label-schema.description="newspipe" \
    org.label-schema.build-date=${BUILD_DATE} \
    org.label-schema.name="newspipe" \
    org.label-schema.schema-version="1.0" \
    org.label-schema.url="https://github.com/berichta/hassio-addons" \
    org.label-schema.usage="https://github.com/berichta/hassio-addons/blob/master/newspipe/README.md" \
    org.label-schema.vcs-ref=${BUILD_REF} \
    org.label-schema.vcs-url="https://github.com/berichta/hassio-addons" \
    org.label-schema.vendor="Berichta"