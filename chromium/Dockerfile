FROM diko316/alnode:latest

ENV CHROME_BIN=/usr/bin/chromium-browser

COPY ./bin /opt/tools/webtest

RUN auto-build \
        --no-builer \
		--apk-permanent \
            coreutils \
            xvfb \
            dbus \
            fontconfig \
            ttf-freefont \
            firefox-esr \
            udev \
            mesa-gl \
            x11vnc \
            libexif \
			chromium \
            chromium-chromedriver && \
    chmod +x /opt/tools/webtest/xvfb-run.sh && \
    ln -s /opt/tools/webtest/xvfb-run.sh /usr/local/bin/xvfb-run
