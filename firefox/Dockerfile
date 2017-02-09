FROM diko316/alnode:v2.0

ADD ./bin /opt/tools/webtest

RUN auto-build \
        --no-builer \
		--apk-permanent \
            coreutils \
            udev \
            xvfb \
            dbus \
            fontconfig \
            ttf-freefont \
            firefox-esr \
            mesa-gl && \
    chmod +x /opt/tools/webtest/xvfb-run.sh && \
    ln -s /opt/tools/webtest/xvfb-run.sh /usr/local/bin/xvfb-run
