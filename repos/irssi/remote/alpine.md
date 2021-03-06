## `irssi:alpine`

```console
$ docker pull irssi@sha256:af9eec132e6b1dd5b668691feae6dd76613ae3194e5068c1a7ab3b9e69e23af1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `irssi:alpine` - linux; amd64

```console
$ docker pull irssi@sha256:3956f59210123f88cb074b682fe44d8960c772b43cd2e0791b3c9b13c7fa59b3
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19140421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f3901291cd644ae1070253523e352a566ce21f879f6f423a2951784c26f6f2f`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 13 Sep 2017 14:32:25 GMT
ADD file:4583e12bf5caec40b861a3409f2a1624c3f3556cc457edb99c9707f00e779e45 in / 
# Wed, 13 Sep 2017 14:32:26 GMT
CMD ["/bin/sh"]
# Tue, 19 Sep 2017 10:51:00 GMT
RUN apk --no-cache add 	ca-certificates
# Tue, 19 Sep 2017 10:51:00 GMT
ENV HOME=/home/user
# Tue, 19 Sep 2017 10:51:01 GMT
RUN adduser -u 1001 -D user 	&& mkdir -p $HOME/.irssi 	&& chown -R user:user $HOME
# Tue, 19 Sep 2017 10:51:01 GMT
ENV LANG=C.UTF-8
# Tue, 19 Sep 2017 10:51:01 GMT
ENV IRSSI_VERSION=1.0.4
# Tue, 26 Sep 2017 00:53:03 GMT
RUN set -x 	&& apk add --no-cache --virtual .build-deps 		autoconf 		automake 		coreutils 		dpkg-dev dpkg 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		make 		ncurses-dev 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 	&& wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz 	&& wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1 	&& gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz 	&& rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc 	&& mkdir -p /usr/src/irssi 	&& tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1 	&& rm /tmp/irssi.tar.xz 	&& cd /usr/src/irssi 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-true-color 		--with-bot 		--with-proxy 		--with-socks 	&& make -j "$(nproc)" 	&& make install 	&& rm -rf /usr/src/irssi 	&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-cache --virtual .irssi-rundeps $runDeps perl-libwww 	&& apk del .build-deps
# Tue, 26 Sep 2017 00:53:03 GMT
WORKDIR /home/user
# Tue, 26 Sep 2017 00:53:04 GMT
USER [user]
# Tue, 26 Sep 2017 00:53:04 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:88286f41530e93dffd4b964e1db22ce4939fffa4a4c665dab8591fbab03d4926`  
		Last Modified: Tue, 27 Jun 2017 18:49:37 GMT  
		Size: 2.0 MB (1990402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f90494e7f1e5e8418d5dac1d0ae46b42c9a5d3d5b27f847316cee913f11d841`  
		Last Modified: Tue, 19 Sep 2017 10:51:53 GMT  
		Size: 351.4 KB (351406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae9bfcf8e8cd85ec3175b39c59b6c117c86ce0c0855283fb7755d174b4b9355`  
		Last Modified: Tue, 19 Sep 2017 10:51:52 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06425ad465d1f2a0f3b3195e1cb23ab98a9eee44cd81dcb9e6e33287e1b2e11b`  
		Last Modified: Tue, 26 Sep 2017 00:53:27 GMT  
		Size: 16.8 MB (16797350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
