FROM ubuntu:18.10

LABEL maintainer="xutongle@gmail.com"

ENV TERM="linux" \
	LANG="C.UTF-8" \
	LC_ALL="C.UTF-8"

RUN set -x \
	&& apt-get update \
	&& apt-get install -y --no-install-recommends ca-certificates apt-transport-https \
	&& rm -r /var/lib/apt/lists/* \
	&& ln -sf /usr/share/zoneinfo/Asia/Shanghai  /etc/localtime \
	&& rm -f /etc/ld.so.conf.d/libc.conf \
	&& echo -e "/lib64\n/usr/lib64\n/usr/local/lib64\n/lib\n/usr/lib\n/usr/local/lib" > /etc/ld.so.conf.d/libc.conf \
	&& /sbin/ldconfig