FROM centos:7

LABEL maintainer="xutongle@gmail.com"

ENV TERM="linux" \
	LANG="en_US.UTF-8" \
	LC_ALL="en_US.UTF-8"

RUN set -x \
	&& yum update -y \
	&& rm -rf /var/cache/yum/* \
	&& ln -sf /usr/share/zoneinfo/Asia/Shanghai  /etc/localtime \
	&& echo -e "/lib64\n/usr/lib64\n/usr/local/lib64\n/lib\n/usr/lib\n/usr/local/lib\n`cat /etc/ld.so.conf`" > /etc/ld.so.conf \
    && /sbin/ldconfig