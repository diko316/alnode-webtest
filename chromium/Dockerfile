FROM diko316/alnode:v2.1

ENV CHROME_BIN=/usr/bin/chromium-browser

COPY ./bin /opt/tools/webtest

RUN auto-build \
        --no-builer \
		--apk-permanent \
            coreutils \
            xvfb \
            dbus \
            udev \
            libexif \
			chromium  && \
    chmod +x /opt/tools/webtest/xvfb-run.sh && \
    ln -s /opt/tools/webtest/xvfb-run.sh /usr/local/bin/xvfb-chromium
    

