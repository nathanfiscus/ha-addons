# https://developers.home-assistant.io/docs/add-ons/configuration#add-on-dockerfile
ARG BUILD_FROM
FROM $BUILD_FROM

# Execute during the build of the image
ARG TEMPIO_VERSION BUILD_ARCH
RUN \
    curl -sSLf -o /usr/bin/tempio \
    "https://github.com/home-assistant/tempio/releases/download/${TEMPIO_VERSION}/tempio_${BUILD_ARCH}"

RUN \
    apk add --no-cache \
        python3 \
        py3-cryptography \
        py3-boto3 \
        py3-prompt_toolkit \
        py3-google-auth \
        py3-requests

RUN python -m venv venv
RUN /bin/bash -c "source venv/bin/activate"
RUN ./venv/bin/pip install pyasyncore 

RUN curl -o /usr/bin/emailproxy.py https://raw.githubusercontent.com/simonrob/email-oauth2-proxy/main/emailproxy.py

# Copy root filesystem
COPY rootfs /

