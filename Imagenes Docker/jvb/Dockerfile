Cd ARG JITSI_REPO=jitsi
FROM ${JITSI_REPO}/base-java

RUN \
	apt-dpkg-wrap apt-get update && \
	apt-dpkg-wrap apt-get install -y jitsi-videobridge2 jq curl iproute2 && \
	apt-cleanup

EXPOSE 8080

COPY rootfs/ /

COPY  sip-communicator.properties /etc/jitsi/videobridge/

COPY config /etc/jitsi/videobridge/

VOLUME /config
