FROM alpine:3.15
RUN set -eux \ 
    && apk add --no-cache --update \
        py3-pip=20.3.4-r1 \
        python3-dev=3.9.18-r0 \
        gcc=10.3.1_git20211027-r0 \
        linux-headers=5.10.41-r0 \
        musl-dev=1.2.2-r9 \
        libffi-dev=3.4.2-r1  \
        openssl-dev=1.1.1w-r1 \
        git=2.34.8-r0

WORKDIR /code
COPY docker/requirements.txt .
RUN set -eux \
    && pip install \
        --no-cache-dir \
        --ignore-installed \
        -r requirements.txt \
    && rm -f requirements.txt
