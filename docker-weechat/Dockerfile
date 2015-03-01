# Weechat dockerfile
#
# https://github.com/emma-borhanian/irc_client/blob/master/docker-weechat/Dockerfile

FROM debian:sid
MAINTAINER Emma Borhanian emma.borhanian+docker-weechat@gmail.com

RUN apt-get update && \
    apt-get install -y weechat perl

EXPOSE 8001

ENV LANG en_US.UTF-8
ENV TERM screen-256color
ENV HOME /

CMD weechat -r "/set relay.network.password \"$WEECHAT_PASSWORD\";/set logger.file.mask \"\$plugin.\$name.log\";/relay add weechat 8001"
