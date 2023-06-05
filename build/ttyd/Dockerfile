FROM alpine


RUN apk add --no-cache tini ttyd nginx openssl openssh ca-certificates  && \
echo "export PS1='\[\033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w\[\033[00m\]\$ '" >> /etc/profile && \
echo "alias poweroff='kill 1'" >> /etc/profile

ENV TINI_KILL_PROCESS_GROUP=1

EXPOSE 7681 80
ENTRYPOINT ["/sbin/tini", "--"]
CMD [ "ttyd", "-s", "3", "-t", "titleFixed=/bin/sh", "-t", "rendererType=webgl", "-t", "disableLeaveAlert=true", "/bin/sh", "-i", "-l" ]
