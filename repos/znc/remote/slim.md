## `znc:slim`

```console
$ docker pull znc@sha256:56048c332240f194acdf808f172bdcbd7451cf8f4cdb36208ac22d2415dad6c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `znc:slim` - linux; amd64

```console
$ docker pull znc@sha256:a387dade1273d4e27c2673b46ad1d2439e55d497e9bec7316b1573625f733348
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22802889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc759b7facc9b62cebe61bccbdc5e05f49253149e863426d8524f956328ed4f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 13 Sep 2017 14:32:20 GMT
ADD file:9d67752278c0e5a1298cd2d6603ebaaab2aa342e27ddf191ee0fde138f82698c in / 
# Wed, 13 Sep 2017 14:32:20 GMT
CMD ["/bin/sh"]
# Wed, 13 Sep 2017 19:39:15 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 13 Sep 2017 19:39:15 GMT
ARG CONFIGUREFLAGS=--prefix=/opt/znc --enable-cyrus --enable-perl --enable-python --disable-ipv6
# Wed, 13 Sep 2017 19:39:15 GMT
ARG MAKEFLAGS=
# Wed, 13 Sep 2017 19:39:15 GMT
ENV ZNC_VERSION=1.6.5
# Wed, 13 Sep 2017 19:44:52 GMT
# ARGS: CONFIGUREFLAGS=--prefix=/opt/znc --enable-cyrus --enable-perl --enable-python --disable-ipv6 MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         ca-certificates         cyrus-sasl         icu         su-exec         tini     && apk add --no-cache --virtual build-dependencies         build-base         curl         cyrus-sasl-dev         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && ../configure ${CONFIGUREFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Wed, 13 Sep 2017 19:44:52 GMT
COPY file:9d7b3114446d239420ea168b9310c1d20e26b75d069079c5742a25823c4c2aab in / 
# Wed, 13 Sep 2017 19:44:52 GMT
COPY file:e0192a282adc7f54a8a1ff4594ead3ef35387b9ac6cad11dc37da9ea1b048a13 in /startup-sequence/ 
# Wed, 13 Sep 2017 19:44:53 GMT
COPY file:378c136273fef23830ba35f7a8a99554baf86a694f5366f4ba9e9bbabcb8ee6a in /startup-sequence/ 
# Wed, 13 Sep 2017 19:44:53 GMT
COPY file:9c43478daa2a1fccaed5a69ad3c74782d9efa3cd18a66d033f2ddf6956451ba5 in /startup-sequence/ 
# Wed, 13 Sep 2017 19:44:53 GMT
COPY file:0aff452a445b305c16e9c2c7fb36e9b027100f93ff8f18f4a9342fb94cc44b9c in /startup-sequence/ 
# Wed, 13 Sep 2017 19:44:53 GMT
VOLUME [/znc-data]
# Wed, 13 Sep 2017 19:44:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:019300c8a437a2d60248f27c206795930626dfe7ddc0323d734143bd5eb131a6`  
		Last Modified: Tue, 27 Jun 2017 18:48:47 GMT  
		Size: 2.0 MB (1970271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca91c7b2bd5f15f9fe5c08928b2232a2db5974f0551709a91e32232677efee6`  
		Last Modified: Wed, 13 Sep 2017 19:45:19 GMT  
		Size: 20.8 MB (20831304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478442f9004d4ac569192574ef3b201048ed6238f7b1ddbaee4606db1ebe5bf1`  
		Last Modified: Wed, 13 Sep 2017 19:45:14 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:392443ca0dfeb81ac5b08177eefabf0e957f382f8f5a2eea6a0460143ab7edbc`  
		Last Modified: Wed, 13 Sep 2017 19:45:14 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e776fe77fdc34153c8b7545bf3cf6058063265f6b2e6fc9844e292600c52dd0`  
		Last Modified: Wed, 13 Sep 2017 19:45:12 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a76141d46c4e015a6d69e08809ef7b671f12be41d6846ce5205cc72f74771c`  
		Last Modified: Wed, 13 Sep 2017 19:45:12 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14b491152b89448c45650b6ead527e5850cf7b8a514799e4576b05e3bb8e49ee`  
		Last Modified: Wed, 13 Sep 2017 19:45:12 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
