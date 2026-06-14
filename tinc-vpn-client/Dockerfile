FROM ghcr.io/hassio-addons/base:21.0.0
# https://github.com/hassio-addons/app-base/pkgs/container/base
# https://developers.home-assistant.io/blog/2026/04/02/builder-migration/
# https://github.com/home-assistant/supervisor/issues/6794
ENV LANG C.UTF-8

# Setup base
RUN apk --no-cache --no-progress upgrade && \
    apk --no-cache --no-progress add tinc && \
    rm -rf /tmp/*

# Copy Bash script
COPY run.sh /
RUN chmod a+x /run.sh

CMD [ "/run.sh" ]
