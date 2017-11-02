FROM diko316/alnode-firefox:firefox-v1.2

COPY . $PROJECT_ROOT

EXPOSE 443

RUN auto-build \
        --no-builer \
        --apk-permanent \
        python \
        curl \
        linux-headers \
        build-base \
        paxctl \
        libgcc \
        libstdc++ \
        gnupg \
    && npm install -g "@angular/cli" \
    && apk del curl \
                linux-headers \
                build-base \
                paxctl \
                libgcc \
                libstdc++ \
                gnupg \
    && rm -rf /etc/ssl \
                /usr/share/man \
                /usr/include/* \
                /tmp/* \
                /var/cache/apk/* \
                /root/.npm \
                /root/.node-gyp \
                /root/.gnupg
