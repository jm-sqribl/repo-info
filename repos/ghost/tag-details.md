<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ghost`

-	[`ghost:0`](#ghost0)
-	[`ghost:0.11`](#ghost011)
-	[`ghost:0.11.11`](#ghost01111)
-	[`ghost:0.11.11-alpine`](#ghost01111-alpine)
-	[`ghost:0.11-alpine`](#ghost011-alpine)
-	[`ghost:0-alpine`](#ghost0-alpine)
-	[`ghost:1`](#ghost1)
-	[`ghost:1.10`](#ghost110)
-	[`ghost:1.10.0`](#ghost1100)
-	[`ghost:1.10.0-alpine`](#ghost1100-alpine)
-	[`ghost:1.10-alpine`](#ghost110-alpine)
-	[`ghost:1-alpine`](#ghost1-alpine)
-	[`ghost:alpine`](#ghostalpine)
-	[`ghost:latest`](#ghostlatest)

## `ghost:0`

```console
$ docker pull ghost@sha256:0608eecda5c28c266f8e9a76f344b2bb052d4ddc856900fef999709c432f6a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ghost:0` - linux; amd64

```console
$ docker pull ghost@sha256:511818d093b3345ca0dedcaea215bd20fc5c7b549f7ebad6f7586bbdf4a7dba1
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.3 MB (113269805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d82d3afe087e6b88bab7d4d737896ef68ffa64ebd741cee1c31ddd8448c44ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["npm","start"]`

```dockerfile
# Wed, 13 Sep 2017 08:40:43 GMT
ADD file:d7333b3e0bc6479d2faed32e06d85f1975e5b23e13e75555aeed0f639770413b in / 
# Wed, 13 Sep 2017 08:40:43 GMT
CMD ["bash"]
# Wed, 13 Sep 2017 12:32:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Sep 2017 12:32:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Sep 2017 20:23:45 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 13 Sep 2017 20:23:48 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done
# Wed, 13 Sep 2017 20:23:48 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Wed, 13 Sep 2017 20:38:03 GMT
ENV NODE_VERSION=6.11.3
# Wed, 13 Sep 2017 20:38:26 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Wed, 13 Sep 2017 20:38:26 GMT
ENV YARN_VERSION=0.27.5
# Wed, 13 Sep 2017 20:38:30 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Wed, 13 Sep 2017 20:38:30 GMT
CMD ["node"]
# Wed, 13 Sep 2017 21:14:57 GMT
RUN groupadd user && useradd --create-home --home-dir /home/user -g user user
# Wed, 13 Sep 2017 21:14:58 GMT
ENV GOSU_VERSION=1.10
# Wed, 13 Sep 2017 21:15:03 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Wed, 13 Sep 2017 21:15:03 GMT
ENV GHOST_SOURCE=/usr/src/ghost
# Wed, 13 Sep 2017 21:15:03 GMT
WORKDIR /usr/src/ghost
# Wed, 13 Sep 2017 21:15:03 GMT
ENV GHOST_VERSION=0.11.11
# Wed, 13 Sep 2017 21:16:24 GMT
RUN set -ex; 		buildDeps=' 		g++ 		gcc 		libc6-dev 		make 		python 		unzip 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O ghost.zip "https://github.com/TryGhost/Ghost/releases/download/${GHOST_VERSION}/Ghost-${GHOST_VERSION}.zip"; 	unzip ghost.zip; 		npm install --production; 		apt-get purge -y --auto-remove $buildDeps; 		rm ghost.zip; 	npm cache clean; 	rm -rf /tmp/npm*
# Wed, 13 Sep 2017 21:16:25 GMT
ENV GHOST_CONTENT=/var/lib/ghost
# Wed, 13 Sep 2017 21:16:25 GMT
RUN mkdir -p "$GHOST_CONTENT" 	&& chown -R user:user "$GHOST_CONTENT" 	&& ln -s "$GHOST_CONTENT/config.js" "$GHOST_SOURCE/config.js"
# Wed, 13 Sep 2017 21:16:26 GMT
VOLUME [/var/lib/ghost]
# Wed, 13 Sep 2017 21:16:26 GMT
COPY file:9cace68ea99d0317c469464495249094669747893a60585016756f169051a609 in /usr/local/bin/ 
# Wed, 13 Sep 2017 21:16:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 13 Sep 2017 21:16:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Sep 2017 21:16:27 GMT
EXPOSE 2368/tcp
# Wed, 13 Sep 2017 21:16:28 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:aa18ad1a0d334d80981104c599fa8cef9264552a265b1197af11274beba767cf`  
		Last Modified: Thu, 07 Sep 2017 23:11:06 GMT  
		Size: 52.6 MB (52595547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a33158a1367c7c4103c89ae66e8f4fdec4ada6a39d4648cf254b32296d6668`  
		Last Modified: Wed, 13 Sep 2017 12:54:21 GMT  
		Size: 19.3 MB (19263717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e2ecbdc66945a5816aa0d37501c34fe6ae76d1664a47cd366604f68a557052`  
		Last Modified: Wed, 13 Sep 2017 20:49:04 GMT  
		Size: 4.4 KB (4406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba36da051a26db65f69c7538041ed3bf4d545ba973e1763029ba67ea44b99ef`  
		Last Modified: Wed, 13 Sep 2017 20:49:04 GMT  
		Size: 119.2 KB (119152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83260829fd758c7ed96bf6b66af7a83c16afb34bd20fea7c30627caa474c19e0`  
		Last Modified: Wed, 13 Sep 2017 20:51:45 GMT  
		Size: 14.7 MB (14718405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7459ed23b0dbcdf1adf35d3c09d1104dfce1711690a871cb7fea376fdeea9176`  
		Last Modified: Wed, 13 Sep 2017 20:51:40 GMT  
		Size: 938.5 KB (938460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9f22cda90b85cccd1b353e17d922de5a934c06671035eae326e98223a1de5f`  
		Last Modified: Wed, 13 Sep 2017 21:20:36 GMT  
		Size: 4.4 KB (4449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41cb7f523c5ff8fbd286d75e12d93a0968d671681d8a6956832b0b8a6919b27`  
		Last Modified: Wed, 13 Sep 2017 21:20:35 GMT  
		Size: 500.7 KB (500671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d19cc9ab0833c7f84bdf167c388b98e749852126eb766a5e3b6b647961651d6`  
		Last Modified: Wed, 13 Sep 2017 21:20:33 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7dcbf3a9813073bb7c6a29dccd5bbcfbc19e403194cb33a651c685ce59d51b9`  
		Last Modified: Wed, 13 Sep 2017 21:20:48 GMT  
		Size: 25.1 MB (25123887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01261b2c97b70e0bfc042b0c9003de82f0cb5d0d0eb4ad2f128c99a229e14140`  
		Last Modified: Wed, 13 Sep 2017 21:20:32 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:040b3b274e1dec0d310497e1cb05a227e48e32d052e32735eacd83d0047196b3`  
		Last Modified: Wed, 13 Sep 2017 21:20:33 GMT  
		Size: 630.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3ddb09f03c511d88db3d400b3cea499a39bd59e2e89e2a9787551887fe8acb`  
		Last Modified: Wed, 13 Sep 2017 21:20:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:0` - linux; arm variant v7

```console
$ docker pull ghost@sha256:f5dc803a573bbcf641027bb6acb3c2564a33ec49dd8d124ec9c87154b197790e
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.6 MB (113620036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:220af54d11cf29e1cfbae4e22ff80c8d4e6f8219529be7ae25c3fdb893aed398`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["npm","start"]`

```dockerfile
# Wed, 27 Sep 2017 04:12:21 GMT
ADD file:ef59ce7fe68882b1b44bc3c4a5e9e465561cb257fb63f8c2b3c247abb012486b in / 
# Wed, 27 Sep 2017 04:12:22 GMT
CMD ["bash"]
# Wed, 27 Sep 2017 04:39:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 27 Sep 2017 04:39:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 27 Sep 2017 07:03:35 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 27 Sep 2017 07:07:47 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done
# Wed, 27 Sep 2017 07:07:48 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Wed, 27 Sep 2017 07:17:28 GMT
ENV NODE_VERSION=6.11.3
# Wed, 27 Sep 2017 07:18:06 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Wed, 27 Sep 2017 07:18:08 GMT
ENV YARN_VERSION=0.27.5
# Wed, 27 Sep 2017 07:18:10 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Wed, 27 Sep 2017 07:18:10 GMT
CMD ["node"]
# Wed, 27 Sep 2017 08:01:43 GMT
RUN groupadd user && useradd --create-home --home-dir /home/user -g user user
# Wed, 27 Sep 2017 08:01:43 GMT
ENV GOSU_VERSION=1.10
# Wed, 27 Sep 2017 08:01:45 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Wed, 27 Sep 2017 08:01:46 GMT
ENV GHOST_SOURCE=/usr/src/ghost
# Wed, 27 Sep 2017 08:01:46 GMT
WORKDIR /usr/src/ghost
# Wed, 27 Sep 2017 08:01:46 GMT
ENV GHOST_VERSION=0.11.11
# Wed, 27 Sep 2017 08:05:02 GMT
RUN set -ex; 		buildDeps=' 		g++ 		gcc 		libc6-dev 		make 		python 		unzip 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O ghost.zip "https://github.com/TryGhost/Ghost/releases/download/${GHOST_VERSION}/Ghost-${GHOST_VERSION}.zip"; 	unzip ghost.zip; 		npm install --production; 		apt-get purge -y --auto-remove $buildDeps; 		rm ghost.zip; 	npm cache clean; 	rm -rf /tmp/npm*
# Wed, 27 Sep 2017 08:05:03 GMT
ENV GHOST_CONTENT=/var/lib/ghost
# Wed, 27 Sep 2017 08:05:04 GMT
RUN mkdir -p "$GHOST_CONTENT" 	&& chown -R user:user "$GHOST_CONTENT" 	&& ln -s "$GHOST_CONTENT/config.js" "$GHOST_SOURCE/config.js"
# Wed, 27 Sep 2017 08:05:05 GMT
VOLUME [/var/lib/ghost]
# Wed, 27 Sep 2017 08:05:06 GMT
COPY file:9cace68ea99d0317c469464495249094669747893a60585016756f169051a609 in /usr/local/bin/ 
# Wed, 27 Sep 2017 08:05:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 27 Sep 2017 08:05:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Sep 2017 08:05:07 GMT
EXPOSE 2368/tcp
# Wed, 27 Sep 2017 08:05:08 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:8c7b63aa62f92f5be1e93e5129c5c99dac397c6d3b5f6c6452bfd0905f6f20be`  
		Last Modified: Wed, 27 Sep 2017 04:17:18 GMT  
		Size: 48.7 MB (48686544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a607bd01ffd678134d1281825ba8fafc069965446932fb3da991e8e6c2d3065d`  
		Last Modified: Wed, 27 Sep 2017 04:58:12 GMT  
		Size: 18.3 MB (18262468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7733b25f61410d8e74ee676e195c358ac6519ef39f1a92f3cd11c5f8ca2048`  
		Last Modified: Wed, 27 Sep 2017 07:20:36 GMT  
		Size: 4.4 KB (4420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553903f3bafddd9019242ebd76c10ae0ba04207db8e960c84758e8762b1c4cca`  
		Last Modified: Wed, 27 Sep 2017 07:20:36 GMT  
		Size: 119.2 KB (119190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34bc7bac012caabb127f3461274a9a4cb95bde62751a07df9eb243be1e2877ad`  
		Last Modified: Wed, 27 Sep 2017 07:22:00 GMT  
		Size: 13.9 MB (13877719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c31b00c4993376f813ed323a451b7444b0f176979418ff061aa095b002377bc0`  
		Last Modified: Wed, 27 Sep 2017 07:21:55 GMT  
		Size: 940.2 KB (940161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37537787dded5775d1180812048b91700f5982da8ba1f428c0f2981544a7083d`  
		Last Modified: Wed, 27 Sep 2017 08:06:18 GMT  
		Size: 4.5 KB (4469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e765804f3106a1b91e6c0aa2780c949136a0a36cf7ef8c92d4f760043918efc`  
		Last Modified: Wed, 27 Sep 2017 08:06:19 GMT  
		Size: 475.3 KB (475271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a9491fb3d3b05124cb0ce6c5ceaaec73865863082b87de90f0d3c51c1052fb1`  
		Last Modified: Wed, 27 Sep 2017 08:06:17 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2d66f8d6952b18181012a923a68e15d973f38eafdda3fb0a9319a1b855e1c1`  
		Last Modified: Wed, 27 Sep 2017 08:06:32 GMT  
		Size: 31.2 MB (31248627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6590702ed8de1bb6bac96f9145e5fc8a0f66853255485b11374804adf310e1b0`  
		Last Modified: Wed, 27 Sep 2017 08:06:18 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f029b0c10ea0cf5fbaba441701c26ae405e0fb7327f877f5293d0a4f85e070`  
		Last Modified: Wed, 27 Sep 2017 08:06:17 GMT  
		Size: 627.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579cf0eb08c79b744cff566d460b94bd9aa469fca496d123ce46e20b6d3ead96`  
		Last Modified: Wed, 27 Sep 2017 08:06:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:0` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:1a55aedead29d8caf9fff136dd539dd07d58139577df0f77a991ea03f5e06da0
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.7 MB (116725227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eb0891026cfcb61955f4003c5dcb3fc261d8d589b773667556d528a1bbe9574`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["npm","start"]`

```dockerfile
# Fri, 08 Sep 2017 17:23:41 GMT
ADD file:9f576a63a5e03994904e585c35fbeef6a2c96c41d8f696705c033f3ca69b6a2b in / 
# Fri, 08 Sep 2017 17:23:42 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 18:32:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 18:32:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 Sep 2017 23:16:17 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 14 Sep 2017 23:16:22 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done
# Thu, 14 Sep 2017 23:16:24 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Thu, 14 Sep 2017 23:18:55 GMT
ENV NODE_VERSION=6.11.3
# Thu, 14 Sep 2017 23:19:28 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Thu, 14 Sep 2017 23:19:29 GMT
ENV YARN_VERSION=0.27.5
# Thu, 14 Sep 2017 23:19:35 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Thu, 14 Sep 2017 23:19:37 GMT
CMD ["node"]
# Fri, 15 Sep 2017 02:27:03 GMT
RUN groupadd user && useradd --create-home --home-dir /home/user -g user user
# Fri, 15 Sep 2017 02:27:04 GMT
ENV GOSU_VERSION=1.10
# Fri, 15 Sep 2017 02:27:11 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Fri, 15 Sep 2017 02:27:13 GMT
ENV GHOST_SOURCE=/usr/src/ghost
# Fri, 15 Sep 2017 02:27:14 GMT
WORKDIR /usr/src/ghost
# Fri, 15 Sep 2017 02:27:15 GMT
ENV GHOST_VERSION=0.11.11
# Fri, 15 Sep 2017 02:35:16 GMT
RUN set -ex; 		buildDeps=' 		g++ 		gcc 		libc6-dev 		make 		python 		unzip 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O ghost.zip "https://github.com/TryGhost/Ghost/releases/download/${GHOST_VERSION}/Ghost-${GHOST_VERSION}.zip"; 	unzip ghost.zip; 		npm install --production; 		apt-get purge -y --auto-remove $buildDeps; 		rm ghost.zip; 	npm cache clean; 	rm -rf /tmp/npm*
# Fri, 15 Sep 2017 02:35:18 GMT
ENV GHOST_CONTENT=/var/lib/ghost
# Fri, 15 Sep 2017 02:35:20 GMT
RUN mkdir -p "$GHOST_CONTENT" 	&& chown -R user:user "$GHOST_CONTENT" 	&& ln -s "$GHOST_CONTENT/config.js" "$GHOST_SOURCE/config.js"
# Fri, 15 Sep 2017 02:35:20 GMT
VOLUME [/var/lib/ghost]
# Fri, 15 Sep 2017 02:35:21 GMT
COPY file:9cace68ea99d0317c469464495249094669747893a60585016756f169051a609 in /usr/local/bin/ 
# Fri, 15 Sep 2017 02:35:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 15 Sep 2017 02:35:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Sep 2017 02:35:24 GMT
EXPOSE 2368/tcp
# Fri, 15 Sep 2017 02:35:25 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:e91a355b0d3ff86add037a3f24718b760d8eb3f346f998e5116375ddce9eae19`  
		Last Modified: Fri, 08 Sep 2017 17:34:56 GMT  
		Size: 49.9 MB (49929457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e054bfb02234c6e2b5305981d365c3b31101ec460b0d90df3b099305c03196`  
		Last Modified: Thu, 14 Sep 2017 22:01:15 GMT  
		Size: 18.7 MB (18737603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68cbb48bf959f44cbc4806f42587333e86631edab819261ca51eba1da6fcd637`  
		Last Modified: Thu, 14 Sep 2017 23:24:36 GMT  
		Size: 4.4 KB (4417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e961bd22aace0af8a10a14a5d6282014bdb3cf7c4d5b42e16a0dd45e4cd06dac`  
		Last Modified: Thu, 14 Sep 2017 23:24:36 GMT  
		Size: 119.2 KB (119150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:280e0b3e39cb221ce8de69ec6e8d5e99fd9761fc3a6d37cbd9086ad72d3b41dc`  
		Last Modified: Thu, 14 Sep 2017 23:27:52 GMT  
		Size: 14.7 MB (14707206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e714752cefed2ff3be3734c49f1a880303ff6290d0705230e5f486a0a0bbe756`  
		Last Modified: Thu, 14 Sep 2017 23:27:45 GMT  
		Size: 940.1 KB (940132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73726fc42bfd83fa52c0278ba63ea9ac32229bbc0dce11e97911eb243a502b7d`  
		Last Modified: Fri, 15 Sep 2017 02:37:26 GMT  
		Size: 4.5 KB (4470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a404ee6743342ba49df4730735f43adce0cad4a59f0efa2f933c9000f11ef1bc`  
		Last Modified: Fri, 15 Sep 2017 02:37:26 GMT  
		Size: 468.7 KB (468701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199a30b04158d900b32b6a01ae1eed0b4ab70c91358d2ea1b7516b8d95eebeab`  
		Last Modified: Fri, 15 Sep 2017 02:37:23 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ff3e008f9c5fc283f06b985e850020efe124193f084224f2f23e0b443bb55b`  
		Last Modified: Fri, 15 Sep 2017 02:37:43 GMT  
		Size: 31.8 MB (31812987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba9d9e2d563bae9f4b25081e999b9f6b45410ca7d3d125a57e4e87c3021f9c3`  
		Last Modified: Fri, 15 Sep 2017 02:37:23 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e50b0b8be229b3bfbb8870da1f7d1b5e01735d2b8b0f55112199f8fe6afab7bc`  
		Last Modified: Fri, 15 Sep 2017 02:37:23 GMT  
		Size: 627.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0e6c52495f660412aa883da2946898c623b13051daa29cc4c410da90f5b03f`  
		Last Modified: Fri, 15 Sep 2017 02:37:23 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:0` - linux; ppc64le

```console
$ docker pull ghost@sha256:1005f1627225f360a522fcee9a8a0840235d9ec71060e199b0c85e58a6ffe1bd
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.3 MB (119302332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16ae52ab21f68a4ee3cd2bd1c27a1ba5475ea4b75d619f35b76469c2860f40eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["npm","start"]`

```dockerfile
# Fri, 08 Sep 2017 00:32:21 GMT
ADD file:483b3245941140ac32394a804364a1a9bd5dfdf1b4475238b61068cc7252ac08 in / 
# Fri, 08 Sep 2017 00:32:21 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 01:03:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 01:03:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 Sep 2017 23:10:48 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 14 Sep 2017 23:11:08 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done
# Thu, 14 Sep 2017 23:11:12 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Thu, 14 Sep 2017 23:15:42 GMT
ENV NODE_VERSION=6.11.3
# Thu, 14 Sep 2017 23:16:32 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Thu, 14 Sep 2017 23:16:41 GMT
ENV YARN_VERSION=0.27.5
# Thu, 14 Sep 2017 23:16:48 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Thu, 14 Sep 2017 23:16:50 GMT
CMD ["node"]
# Fri, 15 Sep 2017 02:26:05 GMT
RUN groupadd user && useradd --create-home --home-dir /home/user -g user user
# Fri, 15 Sep 2017 02:26:08 GMT
ENV GOSU_VERSION=1.10
# Fri, 15 Sep 2017 02:26:16 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Fri, 15 Sep 2017 02:26:18 GMT
ENV GHOST_SOURCE=/usr/src/ghost
# Fri, 15 Sep 2017 02:26:20 GMT
WORKDIR /usr/src/ghost
# Fri, 15 Sep 2017 02:26:22 GMT
ENV GHOST_VERSION=0.11.11
# Fri, 15 Sep 2017 02:31:53 GMT
RUN set -ex; 		buildDeps=' 		g++ 		gcc 		libc6-dev 		make 		python 		unzip 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O ghost.zip "https://github.com/TryGhost/Ghost/releases/download/${GHOST_VERSION}/Ghost-${GHOST_VERSION}.zip"; 	unzip ghost.zip; 		npm install --production; 		apt-get purge -y --auto-remove $buildDeps; 		rm ghost.zip; 	npm cache clean; 	rm -rf /tmp/npm*
# Fri, 15 Sep 2017 02:31:56 GMT
ENV GHOST_CONTENT=/var/lib/ghost
# Fri, 15 Sep 2017 02:32:07 GMT
RUN mkdir -p "$GHOST_CONTENT" 	&& chown -R user:user "$GHOST_CONTENT" 	&& ln -s "$GHOST_CONTENT/config.js" "$GHOST_SOURCE/config.js"
# Fri, 15 Sep 2017 02:32:09 GMT
VOLUME [/var/lib/ghost]
# Fri, 15 Sep 2017 02:32:16 GMT
COPY file:9cace68ea99d0317c469464495249094669747893a60585016756f169051a609 in /usr/local/bin/ 
# Fri, 15 Sep 2017 02:32:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 15 Sep 2017 02:32:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Sep 2017 02:32:30 GMT
EXPOSE 2368/tcp
# Fri, 15 Sep 2017 02:32:32 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:d4a5434e09b7ac8431060d347d6ef1233ae07514878fb2aff4085bcf441c29f3`  
		Last Modified: Fri, 08 Sep 2017 00:36:52 GMT  
		Size: 51.8 MB (51809570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48596af2c38701f94440e222bf8f3d4b2da85e2982c97ae15186eba523249e0b`  
		Last Modified: Thu, 14 Sep 2017 22:21:02 GMT  
		Size: 19.2 MB (19199596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1dc276f5b0bc12cddaf889657d8ed9d7ec3e6add07506308ea49dc52bb6eff`  
		Last Modified: Thu, 14 Sep 2017 23:22:38 GMT  
		Size: 4.4 KB (4444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb57f53562fb9db3e40e7ee479f5526f635b724a0632d9a4d3da2500a44c491d`  
		Last Modified: Thu, 14 Sep 2017 23:22:39 GMT  
		Size: 119.2 KB (119184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f255065ee2535a6b44019881cc1954c1a7f665f6b0c530c618663be94e4a23`  
		Last Modified: Thu, 14 Sep 2017 23:26:37 GMT  
		Size: 14.5 MB (14475182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68be6ded470a2cf42b2ccda178f212a25198e102a4e3249456140252fa22f054`  
		Last Modified: Thu, 14 Sep 2017 23:26:32 GMT  
		Size: 940.2 KB (940157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc22da3eeebe6b135d1888ec1156f28777b348fec7f3c6cdb6a333a8099da0a`  
		Last Modified: Fri, 15 Sep 2017 02:35:06 GMT  
		Size: 4.5 KB (4498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd8f3207ce6955d11deca98a27aaf2de8301a014e0d97af228e465805db5dff`  
		Last Modified: Fri, 15 Sep 2017 02:35:06 GMT  
		Size: 469.8 KB (469848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ade0b0c060ae61440265b252105450eba70bcf2388b5bf58325334e89529f188`  
		Last Modified: Fri, 15 Sep 2017 02:35:03 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5643202e31c71770c2d4639e1179e072282f5c531ee7b8d045b6f8c53eb3aaeb`  
		Last Modified: Fri, 15 Sep 2017 02:35:24 GMT  
		Size: 32.3 MB (32278685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:237f9807dedef02d610dcb1b86f56887011abc35d10ae0969d7a094f32ccdb9a`  
		Last Modified: Fri, 15 Sep 2017 02:35:03 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9e30a9c779f9c54a1fa2dd99fc9fefd824063e9ebefcfb9701eded495d1a3a`  
		Last Modified: Fri, 15 Sep 2017 02:35:03 GMT  
		Size: 628.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6cf6eeed2edebfb236212d609426ac37f4e63c3cc24c25b9bcae333812a4685`  
		Last Modified: Fri, 15 Sep 2017 02:35:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:0` - linux; s390x

```console
$ docker pull ghost@sha256:a57f39121c488a204984d8455dc4a101b516f95a3e8bdfed6394bd44617e9116
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.0 MB (120978548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfda72a7d2c2c07e6cd42304b3101f3117c76802be6300435a19350226b562c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["npm","start"]`

```dockerfile
# Fri, 08 Sep 2017 05:21:42 GMT
ADD file:996e52a941b7162fafcf761c415142a34a2fc703e21d2f264b824373e9fa4b1e in / 
# Fri, 08 Sep 2017 05:21:43 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 05:48:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 05:48:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 08 Sep 2017 17:04:11 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Fri, 08 Sep 2017 17:04:12 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done
# Fri, 08 Sep 2017 17:04:12 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Fri, 08 Sep 2017 17:04:55 GMT
ENV NODE_VERSION=6.11.3
# Fri, 08 Sep 2017 17:05:10 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Fri, 08 Sep 2017 17:05:10 GMT
ENV YARN_VERSION=0.27.5
# Fri, 08 Sep 2017 17:05:11 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Fri, 08 Sep 2017 17:05:12 GMT
CMD ["node"]
# Fri, 08 Sep 2017 18:18:24 GMT
RUN groupadd user && useradd --create-home --home-dir /home/user -g user user
# Fri, 08 Sep 2017 18:18:24 GMT
ENV GOSU_VERSION=1.10
# Fri, 08 Sep 2017 18:18:26 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Fri, 08 Sep 2017 18:18:26 GMT
ENV GHOST_SOURCE=/usr/src/ghost
# Fri, 08 Sep 2017 18:18:26 GMT
WORKDIR /usr/src/ghost
# Fri, 08 Sep 2017 18:18:26 GMT
ENV GHOST_VERSION=0.11.11
# Fri, 08 Sep 2017 18:20:12 GMT
RUN set -ex; 		buildDeps=' 		g++ 		gcc 		libc6-dev 		make 		python 		unzip 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O ghost.zip "https://github.com/TryGhost/Ghost/releases/download/${GHOST_VERSION}/Ghost-${GHOST_VERSION}.zip"; 	unzip ghost.zip; 		npm install --production; 		apt-get purge -y --auto-remove $buildDeps; 		rm ghost.zip; 	npm cache clean; 	rm -rf /tmp/npm*
# Fri, 08 Sep 2017 18:20:13 GMT
ENV GHOST_CONTENT=/var/lib/ghost
# Fri, 08 Sep 2017 18:20:13 GMT
RUN mkdir -p "$GHOST_CONTENT" 	&& chown -R user:user "$GHOST_CONTENT" 	&& ln -s "$GHOST_CONTENT/config.js" "$GHOST_SOURCE/config.js"
# Fri, 08 Sep 2017 18:20:13 GMT
VOLUME [/var/lib/ghost]
# Fri, 08 Sep 2017 18:20:14 GMT
COPY file:9cace68ea99d0317c469464495249094669747893a60585016756f169051a609 in /usr/local/bin/ 
# Fri, 08 Sep 2017 18:20:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 08 Sep 2017 18:20:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Sep 2017 18:20:15 GMT
EXPOSE 2368/tcp
# Fri, 08 Sep 2017 18:20:15 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:5f39dbffcd07e3254246d3c2e4b3532c3697ed04f83eadf5433da820098787df`  
		Last Modified: Fri, 08 Sep 2017 05:24:42 GMT  
		Size: 52.8 MB (52788802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5a344275c5d5a12a16990e9ddb7cfb9bc9b793cc51fbf8bf8993426e287c27`  
		Last Modified: Fri, 08 Sep 2017 16:41:52 GMT  
		Size: 19.5 MB (19470373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c81355314e654fd3d4e1dcbec2f82fffb19b856e65aa403cf7b2d471582658`  
		Last Modified: Fri, 08 Sep 2017 17:05:56 GMT  
		Size: 4.4 KB (4411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9c66bc4cf9f13c8d89cb57f07ce23693a1efcbbbcc32e7e30c5e8e0cefa2c8`  
		Last Modified: Fri, 08 Sep 2017 17:05:56 GMT  
		Size: 119.1 KB (119148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa1121a725f9b59e0fcd0c6226075d97e638b15fdfc40f5e1d57d3a5f3c3f190`  
		Last Modified: Fri, 08 Sep 2017 17:07:00 GMT  
		Size: 14.8 MB (14847789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa31e4823df3a66473b6ca7286cf7a152288b868f3cf1d4df5eb0393f5e81da`  
		Last Modified: Fri, 08 Sep 2017 17:06:56 GMT  
		Size: 938.5 KB (938452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:310ec0c957fa56cf3a91e64a6fd1fb173f1ab96f858b1d33ef0e0b9f0d6d8c54`  
		Last Modified: Fri, 08 Sep 2017 18:21:11 GMT  
		Size: 4.5 KB (4454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dbb5c26fc18f28cbae51ee1a57fde1b4dff26ef099909f735707cdb34590485`  
		Last Modified: Fri, 08 Sep 2017 18:21:11 GMT  
		Size: 486.8 KB (486827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8f8595ea20b8e5e7e0b9cc7c44eaa0f184f031ff8e16feb566226a29704133`  
		Last Modified: Fri, 08 Sep 2017 18:21:10 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d8ea3650b4f6dc874d8a690cffecb6dd26ac8fae1c60e210bfcb931f8ebf2a`  
		Last Modified: Fri, 08 Sep 2017 18:21:19 GMT  
		Size: 32.3 MB (32317190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea6ca33ee71f9b5d3f8463a3bf15bde45487d6bfdef165404f1bbc66c5650241`  
		Last Modified: Fri, 08 Sep 2017 18:21:09 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d601bece71affe0ea8f1bf22c4a94f1ce5f45b2caf38d7eb5b44c5de72543d3`  
		Last Modified: Fri, 08 Sep 2017 18:21:09 GMT  
		Size: 626.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1aaf8edaffa4c98463316ba4768b63b95ebe5aac145d5e8b5b218ed4ab73a54`  
		Last Modified: Fri, 08 Sep 2017 18:21:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:0.11`

```console
$ docker pull ghost@sha256:0608eecda5c28c266f8e9a76f344b2bb052d4ddc856900fef999709c432f6a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ghost:0.11` - linux; amd64

```console
$ docker pull ghost@sha256:511818d093b3345ca0dedcaea215bd20fc5c7b549f7ebad6f7586bbdf4a7dba1
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.3 MB (113269805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d82d3afe087e6b88bab7d4d737896ef68ffa64ebd741cee1c31ddd8448c44ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["npm","start"]`

```dockerfile
# Wed, 13 Sep 2017 08:40:43 GMT
ADD file:d7333b3e0bc6479d2faed32e06d85f1975e5b23e13e75555aeed0f639770413b in / 
# Wed, 13 Sep 2017 08:40:43 GMT
CMD ["bash"]
# Wed, 13 Sep 2017 12:32:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Sep 2017 12:32:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Sep 2017 20:23:45 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 13 Sep 2017 20:23:48 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done
# Wed, 13 Sep 2017 20:23:48 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Wed, 13 Sep 2017 20:38:03 GMT
ENV NODE_VERSION=6.11.3
# Wed, 13 Sep 2017 20:38:26 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Wed, 13 Sep 2017 20:38:26 GMT
ENV YARN_VERSION=0.27.5
# Wed, 13 Sep 2017 20:38:30 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Wed, 13 Sep 2017 20:38:30 GMT
CMD ["node"]
# Wed, 13 Sep 2017 21:14:57 GMT
RUN groupadd user && useradd --create-home --home-dir /home/user -g user user
# Wed, 13 Sep 2017 21:14:58 GMT
ENV GOSU_VERSION=1.10
# Wed, 13 Sep 2017 21:15:03 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Wed, 13 Sep 2017 21:15:03 GMT
ENV GHOST_SOURCE=/usr/src/ghost
# Wed, 13 Sep 2017 21:15:03 GMT
WORKDIR /usr/src/ghost
# Wed, 13 Sep 2017 21:15:03 GMT
ENV GHOST_VERSION=0.11.11
# Wed, 13 Sep 2017 21:16:24 GMT
RUN set -ex; 		buildDeps=' 		g++ 		gcc 		libc6-dev 		make 		python 		unzip 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O ghost.zip "https://github.com/TryGhost/Ghost/releases/download/${GHOST_VERSION}/Ghost-${GHOST_VERSION}.zip"; 	unzip ghost.zip; 		npm install --production; 		apt-get purge -y --auto-remove $buildDeps; 		rm ghost.zip; 	npm cache clean; 	rm -rf /tmp/npm*
# Wed, 13 Sep 2017 21:16:25 GMT
ENV GHOST_CONTENT=/var/lib/ghost
# Wed, 13 Sep 2017 21:16:25 GMT
RUN mkdir -p "$GHOST_CONTENT" 	&& chown -R user:user "$GHOST_CONTENT" 	&& ln -s "$GHOST_CONTENT/config.js" "$GHOST_SOURCE/config.js"
# Wed, 13 Sep 2017 21:16:26 GMT
VOLUME [/var/lib/ghost]
# Wed, 13 Sep 2017 21:16:26 GMT
COPY file:9cace68ea99d0317c469464495249094669747893a60585016756f169051a609 in /usr/local/bin/ 
# Wed, 13 Sep 2017 21:16:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 13 Sep 2017 21:16:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Sep 2017 21:16:27 GMT
EXPOSE 2368/tcp
# Wed, 13 Sep 2017 21:16:28 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:aa18ad1a0d334d80981104c599fa8cef9264552a265b1197af11274beba767cf`  
		Last Modified: Thu, 07 Sep 2017 23:11:06 GMT  
		Size: 52.6 MB (52595547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a33158a1367c7c4103c89ae66e8f4fdec4ada6a39d4648cf254b32296d6668`  
		Last Modified: Wed, 13 Sep 2017 12:54:21 GMT  
		Size: 19.3 MB (19263717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e2ecbdc66945a5816aa0d37501c34fe6ae76d1664a47cd366604f68a557052`  
		Last Modified: Wed, 13 Sep 2017 20:49:04 GMT  
		Size: 4.4 KB (4406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba36da051a26db65f69c7538041ed3bf4d545ba973e1763029ba67ea44b99ef`  
		Last Modified: Wed, 13 Sep 2017 20:49:04 GMT  
		Size: 119.2 KB (119152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83260829fd758c7ed96bf6b66af7a83c16afb34bd20fea7c30627caa474c19e0`  
		Last Modified: Wed, 13 Sep 2017 20:51:45 GMT  
		Size: 14.7 MB (14718405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7459ed23b0dbcdf1adf35d3c09d1104dfce1711690a871cb7fea376fdeea9176`  
		Last Modified: Wed, 13 Sep 2017 20:51:40 GMT  
		Size: 938.5 KB (938460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9f22cda90b85cccd1b353e17d922de5a934c06671035eae326e98223a1de5f`  
		Last Modified: Wed, 13 Sep 2017 21:20:36 GMT  
		Size: 4.4 KB (4449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41cb7f523c5ff8fbd286d75e12d93a0968d671681d8a6956832b0b8a6919b27`  
		Last Modified: Wed, 13 Sep 2017 21:20:35 GMT  
		Size: 500.7 KB (500671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d19cc9ab0833c7f84bdf167c388b98e749852126eb766a5e3b6b647961651d6`  
		Last Modified: Wed, 13 Sep 2017 21:20:33 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7dcbf3a9813073bb7c6a29dccd5bbcfbc19e403194cb33a651c685ce59d51b9`  
		Last Modified: Wed, 13 Sep 2017 21:20:48 GMT  
		Size: 25.1 MB (25123887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01261b2c97b70e0bfc042b0c9003de82f0cb5d0d0eb4ad2f128c99a229e14140`  
		Last Modified: Wed, 13 Sep 2017 21:20:32 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:040b3b274e1dec0d310497e1cb05a227e48e32d052e32735eacd83d0047196b3`  
		Last Modified: Wed, 13 Sep 2017 21:20:33 GMT  
		Size: 630.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3ddb09f03c511d88db3d400b3cea499a39bd59e2e89e2a9787551887fe8acb`  
		Last Modified: Wed, 13 Sep 2017 21:20:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:0.11` - linux; arm variant v7

```console
$ docker pull ghost@sha256:f5dc803a573bbcf641027bb6acb3c2564a33ec49dd8d124ec9c87154b197790e
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.6 MB (113620036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:220af54d11cf29e1cfbae4e22ff80c8d4e6f8219529be7ae25c3fdb893aed398`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["npm","start"]`

```dockerfile
# Wed, 27 Sep 2017 04:12:21 GMT
ADD file:ef59ce7fe68882b1b44bc3c4a5e9e465561cb257fb63f8c2b3c247abb012486b in / 
# Wed, 27 Sep 2017 04:12:22 GMT
CMD ["bash"]
# Wed, 27 Sep 2017 04:39:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 27 Sep 2017 04:39:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 27 Sep 2017 07:03:35 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 27 Sep 2017 07:07:47 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done
# Wed, 27 Sep 2017 07:07:48 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Wed, 27 Sep 2017 07:17:28 GMT
ENV NODE_VERSION=6.11.3
# Wed, 27 Sep 2017 07:18:06 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Wed, 27 Sep 2017 07:18:08 GMT
ENV YARN_VERSION=0.27.5
# Wed, 27 Sep 2017 07:18:10 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Wed, 27 Sep 2017 07:18:10 GMT
CMD ["node"]
# Wed, 27 Sep 2017 08:01:43 GMT
RUN groupadd user && useradd --create-home --home-dir /home/user -g user user
# Wed, 27 Sep 2017 08:01:43 GMT
ENV GOSU_VERSION=1.10
# Wed, 27 Sep 2017 08:01:45 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Wed, 27 Sep 2017 08:01:46 GMT
ENV GHOST_SOURCE=/usr/src/ghost
# Wed, 27 Sep 2017 08:01:46 GMT
WORKDIR /usr/src/ghost
# Wed, 27 Sep 2017 08:01:46 GMT
ENV GHOST_VERSION=0.11.11
# Wed, 27 Sep 2017 08:05:02 GMT
RUN set -ex; 		buildDeps=' 		g++ 		gcc 		libc6-dev 		make 		python 		unzip 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O ghost.zip "https://github.com/TryGhost/Ghost/releases/download/${GHOST_VERSION}/Ghost-${GHOST_VERSION}.zip"; 	unzip ghost.zip; 		npm install --production; 		apt-get purge -y --auto-remove $buildDeps; 		rm ghost.zip; 	npm cache clean; 	rm -rf /tmp/npm*
# Wed, 27 Sep 2017 08:05:03 GMT
ENV GHOST_CONTENT=/var/lib/ghost
# Wed, 27 Sep 2017 08:05:04 GMT
RUN mkdir -p "$GHOST_CONTENT" 	&& chown -R user:user "$GHOST_CONTENT" 	&& ln -s "$GHOST_CONTENT/config.js" "$GHOST_SOURCE/config.js"
# Wed, 27 Sep 2017 08:05:05 GMT
VOLUME [/var/lib/ghost]
# Wed, 27 Sep 2017 08:05:06 GMT
COPY file:9cace68ea99d0317c469464495249094669747893a60585016756f169051a609 in /usr/local/bin/ 
# Wed, 27 Sep 2017 08:05:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 27 Sep 2017 08:05:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Sep 2017 08:05:07 GMT
EXPOSE 2368/tcp
# Wed, 27 Sep 2017 08:05:08 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:8c7b63aa62f92f5be1e93e5129c5c99dac397c6d3b5f6c6452bfd0905f6f20be`  
		Last Modified: Wed, 27 Sep 2017 04:17:18 GMT  
		Size: 48.7 MB (48686544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a607bd01ffd678134d1281825ba8fafc069965446932fb3da991e8e6c2d3065d`  
		Last Modified: Wed, 27 Sep 2017 04:58:12 GMT  
		Size: 18.3 MB (18262468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7733b25f61410d8e74ee676e195c358ac6519ef39f1a92f3cd11c5f8ca2048`  
		Last Modified: Wed, 27 Sep 2017 07:20:36 GMT  
		Size: 4.4 KB (4420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553903f3bafddd9019242ebd76c10ae0ba04207db8e960c84758e8762b1c4cca`  
		Last Modified: Wed, 27 Sep 2017 07:20:36 GMT  
		Size: 119.2 KB (119190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34bc7bac012caabb127f3461274a9a4cb95bde62751a07df9eb243be1e2877ad`  
		Last Modified: Wed, 27 Sep 2017 07:22:00 GMT  
		Size: 13.9 MB (13877719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c31b00c4993376f813ed323a451b7444b0f176979418ff061aa095b002377bc0`  
		Last Modified: Wed, 27 Sep 2017 07:21:55 GMT  
		Size: 940.2 KB (940161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37537787dded5775d1180812048b91700f5982da8ba1f428c0f2981544a7083d`  
		Last Modified: Wed, 27 Sep 2017 08:06:18 GMT  
		Size: 4.5 KB (4469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e765804f3106a1b91e6c0aa2780c949136a0a36cf7ef8c92d4f760043918efc`  
		Last Modified: Wed, 27 Sep 2017 08:06:19 GMT  
		Size: 475.3 KB (475271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a9491fb3d3b05124cb0ce6c5ceaaec73865863082b87de90f0d3c51c1052fb1`  
		Last Modified: Wed, 27 Sep 2017 08:06:17 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2d66f8d6952b18181012a923a68e15d973f38eafdda3fb0a9319a1b855e1c1`  
		Last Modified: Wed, 27 Sep 2017 08:06:32 GMT  
		Size: 31.2 MB (31248627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6590702ed8de1bb6bac96f9145e5fc8a0f66853255485b11374804adf310e1b0`  
		Last Modified: Wed, 27 Sep 2017 08:06:18 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f029b0c10ea0cf5fbaba441701c26ae405e0fb7327f877f5293d0a4f85e070`  
		Last Modified: Wed, 27 Sep 2017 08:06:17 GMT  
		Size: 627.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579cf0eb08c79b744cff566d460b94bd9aa469fca496d123ce46e20b6d3ead96`  
		Last Modified: Wed, 27 Sep 2017 08:06:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:0.11` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:1a55aedead29d8caf9fff136dd539dd07d58139577df0f77a991ea03f5e06da0
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.7 MB (116725227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eb0891026cfcb61955f4003c5dcb3fc261d8d589b773667556d528a1bbe9574`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["npm","start"]`

```dockerfile
# Fri, 08 Sep 2017 17:23:41 GMT
ADD file:9f576a63a5e03994904e585c35fbeef6a2c96c41d8f696705c033f3ca69b6a2b in / 
# Fri, 08 Sep 2017 17:23:42 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 18:32:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 18:32:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 Sep 2017 23:16:17 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 14 Sep 2017 23:16:22 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done
# Thu, 14 Sep 2017 23:16:24 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Thu, 14 Sep 2017 23:18:55 GMT
ENV NODE_VERSION=6.11.3
# Thu, 14 Sep 2017 23:19:28 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Thu, 14 Sep 2017 23:19:29 GMT
ENV YARN_VERSION=0.27.5
# Thu, 14 Sep 2017 23:19:35 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Thu, 14 Sep 2017 23:19:37 GMT
CMD ["node"]
# Fri, 15 Sep 2017 02:27:03 GMT
RUN groupadd user && useradd --create-home --home-dir /home/user -g user user
# Fri, 15 Sep 2017 02:27:04 GMT
ENV GOSU_VERSION=1.10
# Fri, 15 Sep 2017 02:27:11 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Fri, 15 Sep 2017 02:27:13 GMT
ENV GHOST_SOURCE=/usr/src/ghost
# Fri, 15 Sep 2017 02:27:14 GMT
WORKDIR /usr/src/ghost
# Fri, 15 Sep 2017 02:27:15 GMT
ENV GHOST_VERSION=0.11.11
# Fri, 15 Sep 2017 02:35:16 GMT
RUN set -ex; 		buildDeps=' 		g++ 		gcc 		libc6-dev 		make 		python 		unzip 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O ghost.zip "https://github.com/TryGhost/Ghost/releases/download/${GHOST_VERSION}/Ghost-${GHOST_VERSION}.zip"; 	unzip ghost.zip; 		npm install --production; 		apt-get purge -y --auto-remove $buildDeps; 		rm ghost.zip; 	npm cache clean; 	rm -rf /tmp/npm*
# Fri, 15 Sep 2017 02:35:18 GMT
ENV GHOST_CONTENT=/var/lib/ghost
# Fri, 15 Sep 2017 02:35:20 GMT
RUN mkdir -p "$GHOST_CONTENT" 	&& chown -R user:user "$GHOST_CONTENT" 	&& ln -s "$GHOST_CONTENT/config.js" "$GHOST_SOURCE/config.js"
# Fri, 15 Sep 2017 02:35:20 GMT
VOLUME [/var/lib/ghost]
# Fri, 15 Sep 2017 02:35:21 GMT
COPY file:9cace68ea99d0317c469464495249094669747893a60585016756f169051a609 in /usr/local/bin/ 
# Fri, 15 Sep 2017 02:35:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 15 Sep 2017 02:35:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Sep 2017 02:35:24 GMT
EXPOSE 2368/tcp
# Fri, 15 Sep 2017 02:35:25 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:e91a355b0d3ff86add037a3f24718b760d8eb3f346f998e5116375ddce9eae19`  
		Last Modified: Fri, 08 Sep 2017 17:34:56 GMT  
		Size: 49.9 MB (49929457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e054bfb02234c6e2b5305981d365c3b31101ec460b0d90df3b099305c03196`  
		Last Modified: Thu, 14 Sep 2017 22:01:15 GMT  
		Size: 18.7 MB (18737603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68cbb48bf959f44cbc4806f42587333e86631edab819261ca51eba1da6fcd637`  
		Last Modified: Thu, 14 Sep 2017 23:24:36 GMT  
		Size: 4.4 KB (4417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e961bd22aace0af8a10a14a5d6282014bdb3cf7c4d5b42e16a0dd45e4cd06dac`  
		Last Modified: Thu, 14 Sep 2017 23:24:36 GMT  
		Size: 119.2 KB (119150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:280e0b3e39cb221ce8de69ec6e8d5e99fd9761fc3a6d37cbd9086ad72d3b41dc`  
		Last Modified: Thu, 14 Sep 2017 23:27:52 GMT  
		Size: 14.7 MB (14707206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e714752cefed2ff3be3734c49f1a880303ff6290d0705230e5f486a0a0bbe756`  
		Last Modified: Thu, 14 Sep 2017 23:27:45 GMT  
		Size: 940.1 KB (940132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73726fc42bfd83fa52c0278ba63ea9ac32229bbc0dce11e97911eb243a502b7d`  
		Last Modified: Fri, 15 Sep 2017 02:37:26 GMT  
		Size: 4.5 KB (4470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a404ee6743342ba49df4730735f43adce0cad4a59f0efa2f933c9000f11ef1bc`  
		Last Modified: Fri, 15 Sep 2017 02:37:26 GMT  
		Size: 468.7 KB (468701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199a30b04158d900b32b6a01ae1eed0b4ab70c91358d2ea1b7516b8d95eebeab`  
		Last Modified: Fri, 15 Sep 2017 02:37:23 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ff3e008f9c5fc283f06b985e850020efe124193f084224f2f23e0b443bb55b`  
		Last Modified: Fri, 15 Sep 2017 02:37:43 GMT  
		Size: 31.8 MB (31812987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba9d9e2d563bae9f4b25081e999b9f6b45410ca7d3d125a57e4e87c3021f9c3`  
		Last Modified: Fri, 15 Sep 2017 02:37:23 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e50b0b8be229b3bfbb8870da1f7d1b5e01735d2b8b0f55112199f8fe6afab7bc`  
		Last Modified: Fri, 15 Sep 2017 02:37:23 GMT  
		Size: 627.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0e6c52495f660412aa883da2946898c623b13051daa29cc4c410da90f5b03f`  
		Last Modified: Fri, 15 Sep 2017 02:37:23 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:0.11` - linux; ppc64le

```console
$ docker pull ghost@sha256:1005f1627225f360a522fcee9a8a0840235d9ec71060e199b0c85e58a6ffe1bd
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.3 MB (119302332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16ae52ab21f68a4ee3cd2bd1c27a1ba5475ea4b75d619f35b76469c2860f40eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["npm","start"]`

```dockerfile
# Fri, 08 Sep 2017 00:32:21 GMT
ADD file:483b3245941140ac32394a804364a1a9bd5dfdf1b4475238b61068cc7252ac08 in / 
# Fri, 08 Sep 2017 00:32:21 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 01:03:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 01:03:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 Sep 2017 23:10:48 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 14 Sep 2017 23:11:08 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done
# Thu, 14 Sep 2017 23:11:12 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Thu, 14 Sep 2017 23:15:42 GMT
ENV NODE_VERSION=6.11.3
# Thu, 14 Sep 2017 23:16:32 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Thu, 14 Sep 2017 23:16:41 GMT
ENV YARN_VERSION=0.27.5
# Thu, 14 Sep 2017 23:16:48 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Thu, 14 Sep 2017 23:16:50 GMT
CMD ["node"]
# Fri, 15 Sep 2017 02:26:05 GMT
RUN groupadd user && useradd --create-home --home-dir /home/user -g user user
# Fri, 15 Sep 2017 02:26:08 GMT
ENV GOSU_VERSION=1.10
# Fri, 15 Sep 2017 02:26:16 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Fri, 15 Sep 2017 02:26:18 GMT
ENV GHOST_SOURCE=/usr/src/ghost
# Fri, 15 Sep 2017 02:26:20 GMT
WORKDIR /usr/src/ghost
# Fri, 15 Sep 2017 02:26:22 GMT
ENV GHOST_VERSION=0.11.11
# Fri, 15 Sep 2017 02:31:53 GMT
RUN set -ex; 		buildDeps=' 		g++ 		gcc 		libc6-dev 		make 		python 		unzip 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O ghost.zip "https://github.com/TryGhost/Ghost/releases/download/${GHOST_VERSION}/Ghost-${GHOST_VERSION}.zip"; 	unzip ghost.zip; 		npm install --production; 		apt-get purge -y --auto-remove $buildDeps; 		rm ghost.zip; 	npm cache clean; 	rm -rf /tmp/npm*
# Fri, 15 Sep 2017 02:31:56 GMT
ENV GHOST_CONTENT=/var/lib/ghost
# Fri, 15 Sep 2017 02:32:07 GMT
RUN mkdir -p "$GHOST_CONTENT" 	&& chown -R user:user "$GHOST_CONTENT" 	&& ln -s "$GHOST_CONTENT/config.js" "$GHOST_SOURCE/config.js"
# Fri, 15 Sep 2017 02:32:09 GMT
VOLUME [/var/lib/ghost]
# Fri, 15 Sep 2017 02:32:16 GMT
COPY file:9cace68ea99d0317c469464495249094669747893a60585016756f169051a609 in /usr/local/bin/ 
# Fri, 15 Sep 2017 02:32:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 15 Sep 2017 02:32:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Sep 2017 02:32:30 GMT
EXPOSE 2368/tcp
# Fri, 15 Sep 2017 02:32:32 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:d4a5434e09b7ac8431060d347d6ef1233ae07514878fb2aff4085bcf441c29f3`  
		Last Modified: Fri, 08 Sep 2017 00:36:52 GMT  
		Size: 51.8 MB (51809570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48596af2c38701f94440e222bf8f3d4b2da85e2982c97ae15186eba523249e0b`  
		Last Modified: Thu, 14 Sep 2017 22:21:02 GMT  
		Size: 19.2 MB (19199596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1dc276f5b0bc12cddaf889657d8ed9d7ec3e6add07506308ea49dc52bb6eff`  
		Last Modified: Thu, 14 Sep 2017 23:22:38 GMT  
		Size: 4.4 KB (4444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb57f53562fb9db3e40e7ee479f5526f635b724a0632d9a4d3da2500a44c491d`  
		Last Modified: Thu, 14 Sep 2017 23:22:39 GMT  
		Size: 119.2 KB (119184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f255065ee2535a6b44019881cc1954c1a7f665f6b0c530c618663be94e4a23`  
		Last Modified: Thu, 14 Sep 2017 23:26:37 GMT  
		Size: 14.5 MB (14475182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68be6ded470a2cf42b2ccda178f212a25198e102a4e3249456140252fa22f054`  
		Last Modified: Thu, 14 Sep 2017 23:26:32 GMT  
		Size: 940.2 KB (940157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc22da3eeebe6b135d1888ec1156f28777b348fec7f3c6cdb6a333a8099da0a`  
		Last Modified: Fri, 15 Sep 2017 02:35:06 GMT  
		Size: 4.5 KB (4498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd8f3207ce6955d11deca98a27aaf2de8301a014e0d97af228e465805db5dff`  
		Last Modified: Fri, 15 Sep 2017 02:35:06 GMT  
		Size: 469.8 KB (469848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ade0b0c060ae61440265b252105450eba70bcf2388b5bf58325334e89529f188`  
		Last Modified: Fri, 15 Sep 2017 02:35:03 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5643202e31c71770c2d4639e1179e072282f5c531ee7b8d045b6f8c53eb3aaeb`  
		Last Modified: Fri, 15 Sep 2017 02:35:24 GMT  
		Size: 32.3 MB (32278685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:237f9807dedef02d610dcb1b86f56887011abc35d10ae0969d7a094f32ccdb9a`  
		Last Modified: Fri, 15 Sep 2017 02:35:03 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9e30a9c779f9c54a1fa2dd99fc9fefd824063e9ebefcfb9701eded495d1a3a`  
		Last Modified: Fri, 15 Sep 2017 02:35:03 GMT  
		Size: 628.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6cf6eeed2edebfb236212d609426ac37f4e63c3cc24c25b9bcae333812a4685`  
		Last Modified: Fri, 15 Sep 2017 02:35:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:0.11` - linux; s390x

```console
$ docker pull ghost@sha256:a57f39121c488a204984d8455dc4a101b516f95a3e8bdfed6394bd44617e9116
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.0 MB (120978548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfda72a7d2c2c07e6cd42304b3101f3117c76802be6300435a19350226b562c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["npm","start"]`

```dockerfile
# Fri, 08 Sep 2017 05:21:42 GMT
ADD file:996e52a941b7162fafcf761c415142a34a2fc703e21d2f264b824373e9fa4b1e in / 
# Fri, 08 Sep 2017 05:21:43 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 05:48:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 05:48:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 08 Sep 2017 17:04:11 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Fri, 08 Sep 2017 17:04:12 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done
# Fri, 08 Sep 2017 17:04:12 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Fri, 08 Sep 2017 17:04:55 GMT
ENV NODE_VERSION=6.11.3
# Fri, 08 Sep 2017 17:05:10 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Fri, 08 Sep 2017 17:05:10 GMT
ENV YARN_VERSION=0.27.5
# Fri, 08 Sep 2017 17:05:11 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Fri, 08 Sep 2017 17:05:12 GMT
CMD ["node"]
# Fri, 08 Sep 2017 18:18:24 GMT
RUN groupadd user && useradd --create-home --home-dir /home/user -g user user
# Fri, 08 Sep 2017 18:18:24 GMT
ENV GOSU_VERSION=1.10
# Fri, 08 Sep 2017 18:18:26 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Fri, 08 Sep 2017 18:18:26 GMT
ENV GHOST_SOURCE=/usr/src/ghost
# Fri, 08 Sep 2017 18:18:26 GMT
WORKDIR /usr/src/ghost
# Fri, 08 Sep 2017 18:18:26 GMT
ENV GHOST_VERSION=0.11.11
# Fri, 08 Sep 2017 18:20:12 GMT
RUN set -ex; 		buildDeps=' 		g++ 		gcc 		libc6-dev 		make 		python 		unzip 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O ghost.zip "https://github.com/TryGhost/Ghost/releases/download/${GHOST_VERSION}/Ghost-${GHOST_VERSION}.zip"; 	unzip ghost.zip; 		npm install --production; 		apt-get purge -y --auto-remove $buildDeps; 		rm ghost.zip; 	npm cache clean; 	rm -rf /tmp/npm*
# Fri, 08 Sep 2017 18:20:13 GMT
ENV GHOST_CONTENT=/var/lib/ghost
# Fri, 08 Sep 2017 18:20:13 GMT
RUN mkdir -p "$GHOST_CONTENT" 	&& chown -R user:user "$GHOST_CONTENT" 	&& ln -s "$GHOST_CONTENT/config.js" "$GHOST_SOURCE/config.js"
# Fri, 08 Sep 2017 18:20:13 GMT
VOLUME [/var/lib/ghost]
# Fri, 08 Sep 2017 18:20:14 GMT
COPY file:9cace68ea99d0317c469464495249094669747893a60585016756f169051a609 in /usr/local/bin/ 
# Fri, 08 Sep 2017 18:20:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 08 Sep 2017 18:20:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Sep 2017 18:20:15 GMT
EXPOSE 2368/tcp
# Fri, 08 Sep 2017 18:20:15 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:5f39dbffcd07e3254246d3c2e4b3532c3697ed04f83eadf5433da820098787df`  
		Last Modified: Fri, 08 Sep 2017 05:24:42 GMT  
		Size: 52.8 MB (52788802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5a344275c5d5a12a16990e9ddb7cfb9bc9b793cc51fbf8bf8993426e287c27`  
		Last Modified: Fri, 08 Sep 2017 16:41:52 GMT  
		Size: 19.5 MB (19470373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c81355314e654fd3d4e1dcbec2f82fffb19b856e65aa403cf7b2d471582658`  
		Last Modified: Fri, 08 Sep 2017 17:05:56 GMT  
		Size: 4.4 KB (4411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9c66bc4cf9f13c8d89cb57f07ce23693a1efcbbbcc32e7e30c5e8e0cefa2c8`  
		Last Modified: Fri, 08 Sep 2017 17:05:56 GMT  
		Size: 119.1 KB (119148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa1121a725f9b59e0fcd0c6226075d97e638b15fdfc40f5e1d57d3a5f3c3f190`  
		Last Modified: Fri, 08 Sep 2017 17:07:00 GMT  
		Size: 14.8 MB (14847789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa31e4823df3a66473b6ca7286cf7a152288b868f3cf1d4df5eb0393f5e81da`  
		Last Modified: Fri, 08 Sep 2017 17:06:56 GMT  
		Size: 938.5 KB (938452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:310ec0c957fa56cf3a91e64a6fd1fb173f1ab96f858b1d33ef0e0b9f0d6d8c54`  
		Last Modified: Fri, 08 Sep 2017 18:21:11 GMT  
		Size: 4.5 KB (4454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dbb5c26fc18f28cbae51ee1a57fde1b4dff26ef099909f735707cdb34590485`  
		Last Modified: Fri, 08 Sep 2017 18:21:11 GMT  
		Size: 486.8 KB (486827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8f8595ea20b8e5e7e0b9cc7c44eaa0f184f031ff8e16feb566226a29704133`  
		Last Modified: Fri, 08 Sep 2017 18:21:10 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d8ea3650b4f6dc874d8a690cffecb6dd26ac8fae1c60e210bfcb931f8ebf2a`  
		Last Modified: Fri, 08 Sep 2017 18:21:19 GMT  
		Size: 32.3 MB (32317190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea6ca33ee71f9b5d3f8463a3bf15bde45487d6bfdef165404f1bbc66c5650241`  
		Last Modified: Fri, 08 Sep 2017 18:21:09 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d601bece71affe0ea8f1bf22c4a94f1ce5f45b2caf38d7eb5b44c5de72543d3`  
		Last Modified: Fri, 08 Sep 2017 18:21:09 GMT  
		Size: 626.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1aaf8edaffa4c98463316ba4768b63b95ebe5aac145d5e8b5b218ed4ab73a54`  
		Last Modified: Fri, 08 Sep 2017 18:21:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:0.11.11`

```console
$ docker pull ghost@sha256:0608eecda5c28c266f8e9a76f344b2bb052d4ddc856900fef999709c432f6a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ghost:0.11.11` - linux; amd64

```console
$ docker pull ghost@sha256:511818d093b3345ca0dedcaea215bd20fc5c7b549f7ebad6f7586bbdf4a7dba1
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.3 MB (113269805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d82d3afe087e6b88bab7d4d737896ef68ffa64ebd741cee1c31ddd8448c44ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["npm","start"]`

```dockerfile
# Wed, 13 Sep 2017 08:40:43 GMT
ADD file:d7333b3e0bc6479d2faed32e06d85f1975e5b23e13e75555aeed0f639770413b in / 
# Wed, 13 Sep 2017 08:40:43 GMT
CMD ["bash"]
# Wed, 13 Sep 2017 12:32:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Sep 2017 12:32:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Sep 2017 20:23:45 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 13 Sep 2017 20:23:48 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done
# Wed, 13 Sep 2017 20:23:48 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Wed, 13 Sep 2017 20:38:03 GMT
ENV NODE_VERSION=6.11.3
# Wed, 13 Sep 2017 20:38:26 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Wed, 13 Sep 2017 20:38:26 GMT
ENV YARN_VERSION=0.27.5
# Wed, 13 Sep 2017 20:38:30 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Wed, 13 Sep 2017 20:38:30 GMT
CMD ["node"]
# Wed, 13 Sep 2017 21:14:57 GMT
RUN groupadd user && useradd --create-home --home-dir /home/user -g user user
# Wed, 13 Sep 2017 21:14:58 GMT
ENV GOSU_VERSION=1.10
# Wed, 13 Sep 2017 21:15:03 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Wed, 13 Sep 2017 21:15:03 GMT
ENV GHOST_SOURCE=/usr/src/ghost
# Wed, 13 Sep 2017 21:15:03 GMT
WORKDIR /usr/src/ghost
# Wed, 13 Sep 2017 21:15:03 GMT
ENV GHOST_VERSION=0.11.11
# Wed, 13 Sep 2017 21:16:24 GMT
RUN set -ex; 		buildDeps=' 		g++ 		gcc 		libc6-dev 		make 		python 		unzip 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O ghost.zip "https://github.com/TryGhost/Ghost/releases/download/${GHOST_VERSION}/Ghost-${GHOST_VERSION}.zip"; 	unzip ghost.zip; 		npm install --production; 		apt-get purge -y --auto-remove $buildDeps; 		rm ghost.zip; 	npm cache clean; 	rm -rf /tmp/npm*
# Wed, 13 Sep 2017 21:16:25 GMT
ENV GHOST_CONTENT=/var/lib/ghost
# Wed, 13 Sep 2017 21:16:25 GMT
RUN mkdir -p "$GHOST_CONTENT" 	&& chown -R user:user "$GHOST_CONTENT" 	&& ln -s "$GHOST_CONTENT/config.js" "$GHOST_SOURCE/config.js"
# Wed, 13 Sep 2017 21:16:26 GMT
VOLUME [/var/lib/ghost]
# Wed, 13 Sep 2017 21:16:26 GMT
COPY file:9cace68ea99d0317c469464495249094669747893a60585016756f169051a609 in /usr/local/bin/ 
# Wed, 13 Sep 2017 21:16:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 13 Sep 2017 21:16:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Sep 2017 21:16:27 GMT
EXPOSE 2368/tcp
# Wed, 13 Sep 2017 21:16:28 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:aa18ad1a0d334d80981104c599fa8cef9264552a265b1197af11274beba767cf`  
		Last Modified: Thu, 07 Sep 2017 23:11:06 GMT  
		Size: 52.6 MB (52595547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a33158a1367c7c4103c89ae66e8f4fdec4ada6a39d4648cf254b32296d6668`  
		Last Modified: Wed, 13 Sep 2017 12:54:21 GMT  
		Size: 19.3 MB (19263717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e2ecbdc66945a5816aa0d37501c34fe6ae76d1664a47cd366604f68a557052`  
		Last Modified: Wed, 13 Sep 2017 20:49:04 GMT  
		Size: 4.4 KB (4406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba36da051a26db65f69c7538041ed3bf4d545ba973e1763029ba67ea44b99ef`  
		Last Modified: Wed, 13 Sep 2017 20:49:04 GMT  
		Size: 119.2 KB (119152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83260829fd758c7ed96bf6b66af7a83c16afb34bd20fea7c30627caa474c19e0`  
		Last Modified: Wed, 13 Sep 2017 20:51:45 GMT  
		Size: 14.7 MB (14718405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7459ed23b0dbcdf1adf35d3c09d1104dfce1711690a871cb7fea376fdeea9176`  
		Last Modified: Wed, 13 Sep 2017 20:51:40 GMT  
		Size: 938.5 KB (938460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9f22cda90b85cccd1b353e17d922de5a934c06671035eae326e98223a1de5f`  
		Last Modified: Wed, 13 Sep 2017 21:20:36 GMT  
		Size: 4.4 KB (4449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41cb7f523c5ff8fbd286d75e12d93a0968d671681d8a6956832b0b8a6919b27`  
		Last Modified: Wed, 13 Sep 2017 21:20:35 GMT  
		Size: 500.7 KB (500671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d19cc9ab0833c7f84bdf167c388b98e749852126eb766a5e3b6b647961651d6`  
		Last Modified: Wed, 13 Sep 2017 21:20:33 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7dcbf3a9813073bb7c6a29dccd5bbcfbc19e403194cb33a651c685ce59d51b9`  
		Last Modified: Wed, 13 Sep 2017 21:20:48 GMT  
		Size: 25.1 MB (25123887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01261b2c97b70e0bfc042b0c9003de82f0cb5d0d0eb4ad2f128c99a229e14140`  
		Last Modified: Wed, 13 Sep 2017 21:20:32 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:040b3b274e1dec0d310497e1cb05a227e48e32d052e32735eacd83d0047196b3`  
		Last Modified: Wed, 13 Sep 2017 21:20:33 GMT  
		Size: 630.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3ddb09f03c511d88db3d400b3cea499a39bd59e2e89e2a9787551887fe8acb`  
		Last Modified: Wed, 13 Sep 2017 21:20:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:0.11.11` - linux; arm variant v7

```console
$ docker pull ghost@sha256:f5dc803a573bbcf641027bb6acb3c2564a33ec49dd8d124ec9c87154b197790e
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.6 MB (113620036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:220af54d11cf29e1cfbae4e22ff80c8d4e6f8219529be7ae25c3fdb893aed398`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["npm","start"]`

```dockerfile
# Wed, 27 Sep 2017 04:12:21 GMT
ADD file:ef59ce7fe68882b1b44bc3c4a5e9e465561cb257fb63f8c2b3c247abb012486b in / 
# Wed, 27 Sep 2017 04:12:22 GMT
CMD ["bash"]
# Wed, 27 Sep 2017 04:39:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 27 Sep 2017 04:39:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 27 Sep 2017 07:03:35 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 27 Sep 2017 07:07:47 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done
# Wed, 27 Sep 2017 07:07:48 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Wed, 27 Sep 2017 07:17:28 GMT
ENV NODE_VERSION=6.11.3
# Wed, 27 Sep 2017 07:18:06 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Wed, 27 Sep 2017 07:18:08 GMT
ENV YARN_VERSION=0.27.5
# Wed, 27 Sep 2017 07:18:10 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Wed, 27 Sep 2017 07:18:10 GMT
CMD ["node"]
# Wed, 27 Sep 2017 08:01:43 GMT
RUN groupadd user && useradd --create-home --home-dir /home/user -g user user
# Wed, 27 Sep 2017 08:01:43 GMT
ENV GOSU_VERSION=1.10
# Wed, 27 Sep 2017 08:01:45 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Wed, 27 Sep 2017 08:01:46 GMT
ENV GHOST_SOURCE=/usr/src/ghost
# Wed, 27 Sep 2017 08:01:46 GMT
WORKDIR /usr/src/ghost
# Wed, 27 Sep 2017 08:01:46 GMT
ENV GHOST_VERSION=0.11.11
# Wed, 27 Sep 2017 08:05:02 GMT
RUN set -ex; 		buildDeps=' 		g++ 		gcc 		libc6-dev 		make 		python 		unzip 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O ghost.zip "https://github.com/TryGhost/Ghost/releases/download/${GHOST_VERSION}/Ghost-${GHOST_VERSION}.zip"; 	unzip ghost.zip; 		npm install --production; 		apt-get purge -y --auto-remove $buildDeps; 		rm ghost.zip; 	npm cache clean; 	rm -rf /tmp/npm*
# Wed, 27 Sep 2017 08:05:03 GMT
ENV GHOST_CONTENT=/var/lib/ghost
# Wed, 27 Sep 2017 08:05:04 GMT
RUN mkdir -p "$GHOST_CONTENT" 	&& chown -R user:user "$GHOST_CONTENT" 	&& ln -s "$GHOST_CONTENT/config.js" "$GHOST_SOURCE/config.js"
# Wed, 27 Sep 2017 08:05:05 GMT
VOLUME [/var/lib/ghost]
# Wed, 27 Sep 2017 08:05:06 GMT
COPY file:9cace68ea99d0317c469464495249094669747893a60585016756f169051a609 in /usr/local/bin/ 
# Wed, 27 Sep 2017 08:05:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 27 Sep 2017 08:05:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Sep 2017 08:05:07 GMT
EXPOSE 2368/tcp
# Wed, 27 Sep 2017 08:05:08 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:8c7b63aa62f92f5be1e93e5129c5c99dac397c6d3b5f6c6452bfd0905f6f20be`  
		Last Modified: Wed, 27 Sep 2017 04:17:18 GMT  
		Size: 48.7 MB (48686544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a607bd01ffd678134d1281825ba8fafc069965446932fb3da991e8e6c2d3065d`  
		Last Modified: Wed, 27 Sep 2017 04:58:12 GMT  
		Size: 18.3 MB (18262468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7733b25f61410d8e74ee676e195c358ac6519ef39f1a92f3cd11c5f8ca2048`  
		Last Modified: Wed, 27 Sep 2017 07:20:36 GMT  
		Size: 4.4 KB (4420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553903f3bafddd9019242ebd76c10ae0ba04207db8e960c84758e8762b1c4cca`  
		Last Modified: Wed, 27 Sep 2017 07:20:36 GMT  
		Size: 119.2 KB (119190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34bc7bac012caabb127f3461274a9a4cb95bde62751a07df9eb243be1e2877ad`  
		Last Modified: Wed, 27 Sep 2017 07:22:00 GMT  
		Size: 13.9 MB (13877719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c31b00c4993376f813ed323a451b7444b0f176979418ff061aa095b002377bc0`  
		Last Modified: Wed, 27 Sep 2017 07:21:55 GMT  
		Size: 940.2 KB (940161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37537787dded5775d1180812048b91700f5982da8ba1f428c0f2981544a7083d`  
		Last Modified: Wed, 27 Sep 2017 08:06:18 GMT  
		Size: 4.5 KB (4469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e765804f3106a1b91e6c0aa2780c949136a0a36cf7ef8c92d4f760043918efc`  
		Last Modified: Wed, 27 Sep 2017 08:06:19 GMT  
		Size: 475.3 KB (475271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a9491fb3d3b05124cb0ce6c5ceaaec73865863082b87de90f0d3c51c1052fb1`  
		Last Modified: Wed, 27 Sep 2017 08:06:17 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2d66f8d6952b18181012a923a68e15d973f38eafdda3fb0a9319a1b855e1c1`  
		Last Modified: Wed, 27 Sep 2017 08:06:32 GMT  
		Size: 31.2 MB (31248627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6590702ed8de1bb6bac96f9145e5fc8a0f66853255485b11374804adf310e1b0`  
		Last Modified: Wed, 27 Sep 2017 08:06:18 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f029b0c10ea0cf5fbaba441701c26ae405e0fb7327f877f5293d0a4f85e070`  
		Last Modified: Wed, 27 Sep 2017 08:06:17 GMT  
		Size: 627.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579cf0eb08c79b744cff566d460b94bd9aa469fca496d123ce46e20b6d3ead96`  
		Last Modified: Wed, 27 Sep 2017 08:06:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:0.11.11` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:1a55aedead29d8caf9fff136dd539dd07d58139577df0f77a991ea03f5e06da0
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.7 MB (116725227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eb0891026cfcb61955f4003c5dcb3fc261d8d589b773667556d528a1bbe9574`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["npm","start"]`

```dockerfile
# Fri, 08 Sep 2017 17:23:41 GMT
ADD file:9f576a63a5e03994904e585c35fbeef6a2c96c41d8f696705c033f3ca69b6a2b in / 
# Fri, 08 Sep 2017 17:23:42 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 18:32:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 18:32:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 Sep 2017 23:16:17 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 14 Sep 2017 23:16:22 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done
# Thu, 14 Sep 2017 23:16:24 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Thu, 14 Sep 2017 23:18:55 GMT
ENV NODE_VERSION=6.11.3
# Thu, 14 Sep 2017 23:19:28 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Thu, 14 Sep 2017 23:19:29 GMT
ENV YARN_VERSION=0.27.5
# Thu, 14 Sep 2017 23:19:35 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Thu, 14 Sep 2017 23:19:37 GMT
CMD ["node"]
# Fri, 15 Sep 2017 02:27:03 GMT
RUN groupadd user && useradd --create-home --home-dir /home/user -g user user
# Fri, 15 Sep 2017 02:27:04 GMT
ENV GOSU_VERSION=1.10
# Fri, 15 Sep 2017 02:27:11 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Fri, 15 Sep 2017 02:27:13 GMT
ENV GHOST_SOURCE=/usr/src/ghost
# Fri, 15 Sep 2017 02:27:14 GMT
WORKDIR /usr/src/ghost
# Fri, 15 Sep 2017 02:27:15 GMT
ENV GHOST_VERSION=0.11.11
# Fri, 15 Sep 2017 02:35:16 GMT
RUN set -ex; 		buildDeps=' 		g++ 		gcc 		libc6-dev 		make 		python 		unzip 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O ghost.zip "https://github.com/TryGhost/Ghost/releases/download/${GHOST_VERSION}/Ghost-${GHOST_VERSION}.zip"; 	unzip ghost.zip; 		npm install --production; 		apt-get purge -y --auto-remove $buildDeps; 		rm ghost.zip; 	npm cache clean; 	rm -rf /tmp/npm*
# Fri, 15 Sep 2017 02:35:18 GMT
ENV GHOST_CONTENT=/var/lib/ghost
# Fri, 15 Sep 2017 02:35:20 GMT
RUN mkdir -p "$GHOST_CONTENT" 	&& chown -R user:user "$GHOST_CONTENT" 	&& ln -s "$GHOST_CONTENT/config.js" "$GHOST_SOURCE/config.js"
# Fri, 15 Sep 2017 02:35:20 GMT
VOLUME [/var/lib/ghost]
# Fri, 15 Sep 2017 02:35:21 GMT
COPY file:9cace68ea99d0317c469464495249094669747893a60585016756f169051a609 in /usr/local/bin/ 
# Fri, 15 Sep 2017 02:35:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 15 Sep 2017 02:35:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Sep 2017 02:35:24 GMT
EXPOSE 2368/tcp
# Fri, 15 Sep 2017 02:35:25 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:e91a355b0d3ff86add037a3f24718b760d8eb3f346f998e5116375ddce9eae19`  
		Last Modified: Fri, 08 Sep 2017 17:34:56 GMT  
		Size: 49.9 MB (49929457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e054bfb02234c6e2b5305981d365c3b31101ec460b0d90df3b099305c03196`  
		Last Modified: Thu, 14 Sep 2017 22:01:15 GMT  
		Size: 18.7 MB (18737603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68cbb48bf959f44cbc4806f42587333e86631edab819261ca51eba1da6fcd637`  
		Last Modified: Thu, 14 Sep 2017 23:24:36 GMT  
		Size: 4.4 KB (4417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e961bd22aace0af8a10a14a5d6282014bdb3cf7c4d5b42e16a0dd45e4cd06dac`  
		Last Modified: Thu, 14 Sep 2017 23:24:36 GMT  
		Size: 119.2 KB (119150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:280e0b3e39cb221ce8de69ec6e8d5e99fd9761fc3a6d37cbd9086ad72d3b41dc`  
		Last Modified: Thu, 14 Sep 2017 23:27:52 GMT  
		Size: 14.7 MB (14707206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e714752cefed2ff3be3734c49f1a880303ff6290d0705230e5f486a0a0bbe756`  
		Last Modified: Thu, 14 Sep 2017 23:27:45 GMT  
		Size: 940.1 KB (940132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73726fc42bfd83fa52c0278ba63ea9ac32229bbc0dce11e97911eb243a502b7d`  
		Last Modified: Fri, 15 Sep 2017 02:37:26 GMT  
		Size: 4.5 KB (4470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a404ee6743342ba49df4730735f43adce0cad4a59f0efa2f933c9000f11ef1bc`  
		Last Modified: Fri, 15 Sep 2017 02:37:26 GMT  
		Size: 468.7 KB (468701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199a30b04158d900b32b6a01ae1eed0b4ab70c91358d2ea1b7516b8d95eebeab`  
		Last Modified: Fri, 15 Sep 2017 02:37:23 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ff3e008f9c5fc283f06b985e850020efe124193f084224f2f23e0b443bb55b`  
		Last Modified: Fri, 15 Sep 2017 02:37:43 GMT  
		Size: 31.8 MB (31812987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba9d9e2d563bae9f4b25081e999b9f6b45410ca7d3d125a57e4e87c3021f9c3`  
		Last Modified: Fri, 15 Sep 2017 02:37:23 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e50b0b8be229b3bfbb8870da1f7d1b5e01735d2b8b0f55112199f8fe6afab7bc`  
		Last Modified: Fri, 15 Sep 2017 02:37:23 GMT  
		Size: 627.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0e6c52495f660412aa883da2946898c623b13051daa29cc4c410da90f5b03f`  
		Last Modified: Fri, 15 Sep 2017 02:37:23 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:0.11.11` - linux; ppc64le

```console
$ docker pull ghost@sha256:1005f1627225f360a522fcee9a8a0840235d9ec71060e199b0c85e58a6ffe1bd
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.3 MB (119302332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16ae52ab21f68a4ee3cd2bd1c27a1ba5475ea4b75d619f35b76469c2860f40eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["npm","start"]`

```dockerfile
# Fri, 08 Sep 2017 00:32:21 GMT
ADD file:483b3245941140ac32394a804364a1a9bd5dfdf1b4475238b61068cc7252ac08 in / 
# Fri, 08 Sep 2017 00:32:21 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 01:03:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 01:03:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 Sep 2017 23:10:48 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 14 Sep 2017 23:11:08 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done
# Thu, 14 Sep 2017 23:11:12 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Thu, 14 Sep 2017 23:15:42 GMT
ENV NODE_VERSION=6.11.3
# Thu, 14 Sep 2017 23:16:32 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Thu, 14 Sep 2017 23:16:41 GMT
ENV YARN_VERSION=0.27.5
# Thu, 14 Sep 2017 23:16:48 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Thu, 14 Sep 2017 23:16:50 GMT
CMD ["node"]
# Fri, 15 Sep 2017 02:26:05 GMT
RUN groupadd user && useradd --create-home --home-dir /home/user -g user user
# Fri, 15 Sep 2017 02:26:08 GMT
ENV GOSU_VERSION=1.10
# Fri, 15 Sep 2017 02:26:16 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Fri, 15 Sep 2017 02:26:18 GMT
ENV GHOST_SOURCE=/usr/src/ghost
# Fri, 15 Sep 2017 02:26:20 GMT
WORKDIR /usr/src/ghost
# Fri, 15 Sep 2017 02:26:22 GMT
ENV GHOST_VERSION=0.11.11
# Fri, 15 Sep 2017 02:31:53 GMT
RUN set -ex; 		buildDeps=' 		g++ 		gcc 		libc6-dev 		make 		python 		unzip 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O ghost.zip "https://github.com/TryGhost/Ghost/releases/download/${GHOST_VERSION}/Ghost-${GHOST_VERSION}.zip"; 	unzip ghost.zip; 		npm install --production; 		apt-get purge -y --auto-remove $buildDeps; 		rm ghost.zip; 	npm cache clean; 	rm -rf /tmp/npm*
# Fri, 15 Sep 2017 02:31:56 GMT
ENV GHOST_CONTENT=/var/lib/ghost
# Fri, 15 Sep 2017 02:32:07 GMT
RUN mkdir -p "$GHOST_CONTENT" 	&& chown -R user:user "$GHOST_CONTENT" 	&& ln -s "$GHOST_CONTENT/config.js" "$GHOST_SOURCE/config.js"
# Fri, 15 Sep 2017 02:32:09 GMT
VOLUME [/var/lib/ghost]
# Fri, 15 Sep 2017 02:32:16 GMT
COPY file:9cace68ea99d0317c469464495249094669747893a60585016756f169051a609 in /usr/local/bin/ 
# Fri, 15 Sep 2017 02:32:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 15 Sep 2017 02:32:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Sep 2017 02:32:30 GMT
EXPOSE 2368/tcp
# Fri, 15 Sep 2017 02:32:32 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:d4a5434e09b7ac8431060d347d6ef1233ae07514878fb2aff4085bcf441c29f3`  
		Last Modified: Fri, 08 Sep 2017 00:36:52 GMT  
		Size: 51.8 MB (51809570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48596af2c38701f94440e222bf8f3d4b2da85e2982c97ae15186eba523249e0b`  
		Last Modified: Thu, 14 Sep 2017 22:21:02 GMT  
		Size: 19.2 MB (19199596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1dc276f5b0bc12cddaf889657d8ed9d7ec3e6add07506308ea49dc52bb6eff`  
		Last Modified: Thu, 14 Sep 2017 23:22:38 GMT  
		Size: 4.4 KB (4444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb57f53562fb9db3e40e7ee479f5526f635b724a0632d9a4d3da2500a44c491d`  
		Last Modified: Thu, 14 Sep 2017 23:22:39 GMT  
		Size: 119.2 KB (119184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f255065ee2535a6b44019881cc1954c1a7f665f6b0c530c618663be94e4a23`  
		Last Modified: Thu, 14 Sep 2017 23:26:37 GMT  
		Size: 14.5 MB (14475182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68be6ded470a2cf42b2ccda178f212a25198e102a4e3249456140252fa22f054`  
		Last Modified: Thu, 14 Sep 2017 23:26:32 GMT  
		Size: 940.2 KB (940157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc22da3eeebe6b135d1888ec1156f28777b348fec7f3c6cdb6a333a8099da0a`  
		Last Modified: Fri, 15 Sep 2017 02:35:06 GMT  
		Size: 4.5 KB (4498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd8f3207ce6955d11deca98a27aaf2de8301a014e0d97af228e465805db5dff`  
		Last Modified: Fri, 15 Sep 2017 02:35:06 GMT  
		Size: 469.8 KB (469848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ade0b0c060ae61440265b252105450eba70bcf2388b5bf58325334e89529f188`  
		Last Modified: Fri, 15 Sep 2017 02:35:03 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5643202e31c71770c2d4639e1179e072282f5c531ee7b8d045b6f8c53eb3aaeb`  
		Last Modified: Fri, 15 Sep 2017 02:35:24 GMT  
		Size: 32.3 MB (32278685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:237f9807dedef02d610dcb1b86f56887011abc35d10ae0969d7a094f32ccdb9a`  
		Last Modified: Fri, 15 Sep 2017 02:35:03 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9e30a9c779f9c54a1fa2dd99fc9fefd824063e9ebefcfb9701eded495d1a3a`  
		Last Modified: Fri, 15 Sep 2017 02:35:03 GMT  
		Size: 628.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6cf6eeed2edebfb236212d609426ac37f4e63c3cc24c25b9bcae333812a4685`  
		Last Modified: Fri, 15 Sep 2017 02:35:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:0.11.11` - linux; s390x

```console
$ docker pull ghost@sha256:a57f39121c488a204984d8455dc4a101b516f95a3e8bdfed6394bd44617e9116
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.0 MB (120978548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfda72a7d2c2c07e6cd42304b3101f3117c76802be6300435a19350226b562c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["npm","start"]`

```dockerfile
# Fri, 08 Sep 2017 05:21:42 GMT
ADD file:996e52a941b7162fafcf761c415142a34a2fc703e21d2f264b824373e9fa4b1e in / 
# Fri, 08 Sep 2017 05:21:43 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 05:48:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 05:48:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 08 Sep 2017 17:04:11 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Fri, 08 Sep 2017 17:04:12 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done
# Fri, 08 Sep 2017 17:04:12 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Fri, 08 Sep 2017 17:04:55 GMT
ENV NODE_VERSION=6.11.3
# Fri, 08 Sep 2017 17:05:10 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Fri, 08 Sep 2017 17:05:10 GMT
ENV YARN_VERSION=0.27.5
# Fri, 08 Sep 2017 17:05:11 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Fri, 08 Sep 2017 17:05:12 GMT
CMD ["node"]
# Fri, 08 Sep 2017 18:18:24 GMT
RUN groupadd user && useradd --create-home --home-dir /home/user -g user user
# Fri, 08 Sep 2017 18:18:24 GMT
ENV GOSU_VERSION=1.10
# Fri, 08 Sep 2017 18:18:26 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Fri, 08 Sep 2017 18:18:26 GMT
ENV GHOST_SOURCE=/usr/src/ghost
# Fri, 08 Sep 2017 18:18:26 GMT
WORKDIR /usr/src/ghost
# Fri, 08 Sep 2017 18:18:26 GMT
ENV GHOST_VERSION=0.11.11
# Fri, 08 Sep 2017 18:20:12 GMT
RUN set -ex; 		buildDeps=' 		g++ 		gcc 		libc6-dev 		make 		python 		unzip 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O ghost.zip "https://github.com/TryGhost/Ghost/releases/download/${GHOST_VERSION}/Ghost-${GHOST_VERSION}.zip"; 	unzip ghost.zip; 		npm install --production; 		apt-get purge -y --auto-remove $buildDeps; 		rm ghost.zip; 	npm cache clean; 	rm -rf /tmp/npm*
# Fri, 08 Sep 2017 18:20:13 GMT
ENV GHOST_CONTENT=/var/lib/ghost
# Fri, 08 Sep 2017 18:20:13 GMT
RUN mkdir -p "$GHOST_CONTENT" 	&& chown -R user:user "$GHOST_CONTENT" 	&& ln -s "$GHOST_CONTENT/config.js" "$GHOST_SOURCE/config.js"
# Fri, 08 Sep 2017 18:20:13 GMT
VOLUME [/var/lib/ghost]
# Fri, 08 Sep 2017 18:20:14 GMT
COPY file:9cace68ea99d0317c469464495249094669747893a60585016756f169051a609 in /usr/local/bin/ 
# Fri, 08 Sep 2017 18:20:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 08 Sep 2017 18:20:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Sep 2017 18:20:15 GMT
EXPOSE 2368/tcp
# Fri, 08 Sep 2017 18:20:15 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:5f39dbffcd07e3254246d3c2e4b3532c3697ed04f83eadf5433da820098787df`  
		Last Modified: Fri, 08 Sep 2017 05:24:42 GMT  
		Size: 52.8 MB (52788802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5a344275c5d5a12a16990e9ddb7cfb9bc9b793cc51fbf8bf8993426e287c27`  
		Last Modified: Fri, 08 Sep 2017 16:41:52 GMT  
		Size: 19.5 MB (19470373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c81355314e654fd3d4e1dcbec2f82fffb19b856e65aa403cf7b2d471582658`  
		Last Modified: Fri, 08 Sep 2017 17:05:56 GMT  
		Size: 4.4 KB (4411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9c66bc4cf9f13c8d89cb57f07ce23693a1efcbbbcc32e7e30c5e8e0cefa2c8`  
		Last Modified: Fri, 08 Sep 2017 17:05:56 GMT  
		Size: 119.1 KB (119148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa1121a725f9b59e0fcd0c6226075d97e638b15fdfc40f5e1d57d3a5f3c3f190`  
		Last Modified: Fri, 08 Sep 2017 17:07:00 GMT  
		Size: 14.8 MB (14847789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa31e4823df3a66473b6ca7286cf7a152288b868f3cf1d4df5eb0393f5e81da`  
		Last Modified: Fri, 08 Sep 2017 17:06:56 GMT  
		Size: 938.5 KB (938452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:310ec0c957fa56cf3a91e64a6fd1fb173f1ab96f858b1d33ef0e0b9f0d6d8c54`  
		Last Modified: Fri, 08 Sep 2017 18:21:11 GMT  
		Size: 4.5 KB (4454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dbb5c26fc18f28cbae51ee1a57fde1b4dff26ef099909f735707cdb34590485`  
		Last Modified: Fri, 08 Sep 2017 18:21:11 GMT  
		Size: 486.8 KB (486827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8f8595ea20b8e5e7e0b9cc7c44eaa0f184f031ff8e16feb566226a29704133`  
		Last Modified: Fri, 08 Sep 2017 18:21:10 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d8ea3650b4f6dc874d8a690cffecb6dd26ac8fae1c60e210bfcb931f8ebf2a`  
		Last Modified: Fri, 08 Sep 2017 18:21:19 GMT  
		Size: 32.3 MB (32317190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea6ca33ee71f9b5d3f8463a3bf15bde45487d6bfdef165404f1bbc66c5650241`  
		Last Modified: Fri, 08 Sep 2017 18:21:09 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d601bece71affe0ea8f1bf22c4a94f1ce5f45b2caf38d7eb5b44c5de72543d3`  
		Last Modified: Fri, 08 Sep 2017 18:21:09 GMT  
		Size: 626.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1aaf8edaffa4c98463316ba4768b63b95ebe5aac145d5e8b5b218ed4ab73a54`  
		Last Modified: Fri, 08 Sep 2017 18:21:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:0.11.11-alpine`

```console
$ docker pull ghost@sha256:26a691bac954e9b8e07da7346e82d5ea14218361395c16e38793eec63c9957c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `ghost:0.11.11-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:4ad3d7e137160c04def7f214fcae86a03d473a76efc88af5f820bf194bd932f3
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44996427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ae23590f30dcbf59bd5464a61c9d637ebc7ff58820fd39e0aac46f08b9271f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["npm","start"]`

```dockerfile
# Wed, 13 Sep 2017 14:32:15 GMT
ADD file:89e72bfc19e81624ba6a34bd5cecdf258750dc569ba03e17e3f4a286b1526461 in / 
# Wed, 13 Sep 2017 14:32:15 GMT
CMD ["/bin/sh"]
# Wed, 13 Sep 2017 20:24:57 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Wed, 13 Sep 2017 20:24:58 GMT
ENV NODE_VERSION=6.11.3
# Wed, 13 Sep 2017 20:36:42 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         binutils-gold         curl         g++         gcc         gnupg         libgcc         linux-headers         make         python   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN)     && make install     && apk del .build-deps     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt
# Wed, 13 Sep 2017 20:36:42 GMT
ENV YARN_VERSION=0.27.5
# Wed, 13 Sep 2017 20:36:50 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Wed, 13 Sep 2017 20:36:50 GMT
CMD ["node"]
# Wed, 13 Sep 2017 21:13:34 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 13 Sep 2017 21:16:34 GMT
RUN apk add --no-cache 		bash 		tar
# Wed, 13 Sep 2017 21:16:34 GMT
ENV GHOST_SOURCE=/usr/src/ghost
# Wed, 13 Sep 2017 21:16:34 GMT
WORKDIR /usr/src/ghost
# Wed, 13 Sep 2017 21:16:35 GMT
ENV GHOST_VERSION=0.11.11
# Wed, 13 Sep 2017 21:17:23 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		gcc 		make 		openssl 		python 		unzip 	; 		wget -O ghost.zip "https://github.com/TryGhost/Ghost/releases/download/${GHOST_VERSION}/Ghost-${GHOST_VERSION}.zip"; 	unzip ghost.zip; 		npm install --production; 		apk del .build-deps; 		rm ghost.zip; 	npm cache clean; 	rm -rf /tmp/npm*
# Wed, 13 Sep 2017 21:17:23 GMT
ENV GHOST_CONTENT=/var/lib/ghost
# Wed, 13 Sep 2017 21:17:24 GMT
RUN mkdir -p "$GHOST_CONTENT" 	&& chown -R node:node "$GHOST_CONTENT" 	&& ln -s "$GHOST_CONTENT/config.js" "$GHOST_SOURCE/config.js"
# Wed, 13 Sep 2017 21:17:24 GMT
VOLUME [/var/lib/ghost]
# Wed, 13 Sep 2017 21:17:25 GMT
COPY file:2cb0a64ef22301242537372657c5d88304b43153f351a7f2d0d61e05c3dfb29a in /usr/local/bin/ 
# Wed, 13 Sep 2017 21:17:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Sep 2017 21:17:25 GMT
EXPOSE 2368/tcp
# Wed, 13 Sep 2017 21:17:25 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:90f4dba627d65ea3223761bcfe54e726337a919fe98117ef107914f91be657c9`  
		Last Modified: Tue, 27 Jun 2017 18:47:56 GMT  
		Size: 2.4 MB (2385007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c02e9bd0b129afc373209e2498ba6bd7157164b4a96de677a2e1224527558e3d`  
		Last Modified: Wed, 13 Sep 2017 20:51:01 GMT  
		Size: 15.4 MB (15438807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae02bb9be1084245b51165da53a51c16267d437758238436108e38b62ee73c83`  
		Last Modified: Wed, 13 Sep 2017 20:50:56 GMT  
		Size: 945.5 KB (945482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670dd55024c52593c29fd34bf9e31b4442960627d5c074537ddb43b44c801685`  
		Last Modified: Wed, 13 Sep 2017 21:19:03 GMT  
		Size: 8.4 KB (8367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6998b8eab62af074a96f5a68111c04090ff0a876b7a501917024948d84228a`  
		Last Modified: Wed, 13 Sep 2017 21:21:11 GMT  
		Size: 1.3 MB (1336092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae0b83b60255add53275d283becad4dd2c65fbacccb6ba51342326cab98cde9`  
		Last Modified: Wed, 13 Sep 2017 21:21:06 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:940406319f692a95bc97b34410f9ad07b1ac5410b537fedf4bcef9cd1cf19f22`  
		Last Modified: Wed, 13 Sep 2017 21:21:20 GMT  
		Size: 24.9 MB (24881708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d59ebfd1db388965772b75bf1597d45b7d4cd3d8c591934d37ad09b94b5e43d2`  
		Last Modified: Wed, 13 Sep 2017 21:21:07 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:862a533120c862f1a83b05447d226be18d2af33f4860087d080db846d1360a05`  
		Last Modified: Wed, 13 Sep 2017 21:21:06 GMT  
		Size: 609.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:0.11-alpine`

```console
$ docker pull ghost@sha256:26a691bac954e9b8e07da7346e82d5ea14218361395c16e38793eec63c9957c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `ghost:0.11-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:4ad3d7e137160c04def7f214fcae86a03d473a76efc88af5f820bf194bd932f3
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44996427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ae23590f30dcbf59bd5464a61c9d637ebc7ff58820fd39e0aac46f08b9271f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["npm","start"]`

```dockerfile
# Wed, 13 Sep 2017 14:32:15 GMT
ADD file:89e72bfc19e81624ba6a34bd5cecdf258750dc569ba03e17e3f4a286b1526461 in / 
# Wed, 13 Sep 2017 14:32:15 GMT
CMD ["/bin/sh"]
# Wed, 13 Sep 2017 20:24:57 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Wed, 13 Sep 2017 20:24:58 GMT
ENV NODE_VERSION=6.11.3
# Wed, 13 Sep 2017 20:36:42 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         binutils-gold         curl         g++         gcc         gnupg         libgcc         linux-headers         make         python   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN)     && make install     && apk del .build-deps     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt
# Wed, 13 Sep 2017 20:36:42 GMT
ENV YARN_VERSION=0.27.5
# Wed, 13 Sep 2017 20:36:50 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Wed, 13 Sep 2017 20:36:50 GMT
CMD ["node"]
# Wed, 13 Sep 2017 21:13:34 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 13 Sep 2017 21:16:34 GMT
RUN apk add --no-cache 		bash 		tar
# Wed, 13 Sep 2017 21:16:34 GMT
ENV GHOST_SOURCE=/usr/src/ghost
# Wed, 13 Sep 2017 21:16:34 GMT
WORKDIR /usr/src/ghost
# Wed, 13 Sep 2017 21:16:35 GMT
ENV GHOST_VERSION=0.11.11
# Wed, 13 Sep 2017 21:17:23 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		gcc 		make 		openssl 		python 		unzip 	; 		wget -O ghost.zip "https://github.com/TryGhost/Ghost/releases/download/${GHOST_VERSION}/Ghost-${GHOST_VERSION}.zip"; 	unzip ghost.zip; 		npm install --production; 		apk del .build-deps; 		rm ghost.zip; 	npm cache clean; 	rm -rf /tmp/npm*
# Wed, 13 Sep 2017 21:17:23 GMT
ENV GHOST_CONTENT=/var/lib/ghost
# Wed, 13 Sep 2017 21:17:24 GMT
RUN mkdir -p "$GHOST_CONTENT" 	&& chown -R node:node "$GHOST_CONTENT" 	&& ln -s "$GHOST_CONTENT/config.js" "$GHOST_SOURCE/config.js"
# Wed, 13 Sep 2017 21:17:24 GMT
VOLUME [/var/lib/ghost]
# Wed, 13 Sep 2017 21:17:25 GMT
COPY file:2cb0a64ef22301242537372657c5d88304b43153f351a7f2d0d61e05c3dfb29a in /usr/local/bin/ 
# Wed, 13 Sep 2017 21:17:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Sep 2017 21:17:25 GMT
EXPOSE 2368/tcp
# Wed, 13 Sep 2017 21:17:25 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:90f4dba627d65ea3223761bcfe54e726337a919fe98117ef107914f91be657c9`  
		Last Modified: Tue, 27 Jun 2017 18:47:56 GMT  
		Size: 2.4 MB (2385007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c02e9bd0b129afc373209e2498ba6bd7157164b4a96de677a2e1224527558e3d`  
		Last Modified: Wed, 13 Sep 2017 20:51:01 GMT  
		Size: 15.4 MB (15438807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae02bb9be1084245b51165da53a51c16267d437758238436108e38b62ee73c83`  
		Last Modified: Wed, 13 Sep 2017 20:50:56 GMT  
		Size: 945.5 KB (945482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670dd55024c52593c29fd34bf9e31b4442960627d5c074537ddb43b44c801685`  
		Last Modified: Wed, 13 Sep 2017 21:19:03 GMT  
		Size: 8.4 KB (8367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6998b8eab62af074a96f5a68111c04090ff0a876b7a501917024948d84228a`  
		Last Modified: Wed, 13 Sep 2017 21:21:11 GMT  
		Size: 1.3 MB (1336092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae0b83b60255add53275d283becad4dd2c65fbacccb6ba51342326cab98cde9`  
		Last Modified: Wed, 13 Sep 2017 21:21:06 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:940406319f692a95bc97b34410f9ad07b1ac5410b537fedf4bcef9cd1cf19f22`  
		Last Modified: Wed, 13 Sep 2017 21:21:20 GMT  
		Size: 24.9 MB (24881708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d59ebfd1db388965772b75bf1597d45b7d4cd3d8c591934d37ad09b94b5e43d2`  
		Last Modified: Wed, 13 Sep 2017 21:21:07 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:862a533120c862f1a83b05447d226be18d2af33f4860087d080db846d1360a05`  
		Last Modified: Wed, 13 Sep 2017 21:21:06 GMT  
		Size: 609.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:0-alpine`

```console
$ docker pull ghost@sha256:26a691bac954e9b8e07da7346e82d5ea14218361395c16e38793eec63c9957c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `ghost:0-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:4ad3d7e137160c04def7f214fcae86a03d473a76efc88af5f820bf194bd932f3
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44996427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ae23590f30dcbf59bd5464a61c9d637ebc7ff58820fd39e0aac46f08b9271f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["npm","start"]`

```dockerfile
# Wed, 13 Sep 2017 14:32:15 GMT
ADD file:89e72bfc19e81624ba6a34bd5cecdf258750dc569ba03e17e3f4a286b1526461 in / 
# Wed, 13 Sep 2017 14:32:15 GMT
CMD ["/bin/sh"]
# Wed, 13 Sep 2017 20:24:57 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Wed, 13 Sep 2017 20:24:58 GMT
ENV NODE_VERSION=6.11.3
# Wed, 13 Sep 2017 20:36:42 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         binutils-gold         curl         g++         gcc         gnupg         libgcc         linux-headers         make         python   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN)     && make install     && apk del .build-deps     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt
# Wed, 13 Sep 2017 20:36:42 GMT
ENV YARN_VERSION=0.27.5
# Wed, 13 Sep 2017 20:36:50 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Wed, 13 Sep 2017 20:36:50 GMT
CMD ["node"]
# Wed, 13 Sep 2017 21:13:34 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 13 Sep 2017 21:16:34 GMT
RUN apk add --no-cache 		bash 		tar
# Wed, 13 Sep 2017 21:16:34 GMT
ENV GHOST_SOURCE=/usr/src/ghost
# Wed, 13 Sep 2017 21:16:34 GMT
WORKDIR /usr/src/ghost
# Wed, 13 Sep 2017 21:16:35 GMT
ENV GHOST_VERSION=0.11.11
# Wed, 13 Sep 2017 21:17:23 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		gcc 		make 		openssl 		python 		unzip 	; 		wget -O ghost.zip "https://github.com/TryGhost/Ghost/releases/download/${GHOST_VERSION}/Ghost-${GHOST_VERSION}.zip"; 	unzip ghost.zip; 		npm install --production; 		apk del .build-deps; 		rm ghost.zip; 	npm cache clean; 	rm -rf /tmp/npm*
# Wed, 13 Sep 2017 21:17:23 GMT
ENV GHOST_CONTENT=/var/lib/ghost
# Wed, 13 Sep 2017 21:17:24 GMT
RUN mkdir -p "$GHOST_CONTENT" 	&& chown -R node:node "$GHOST_CONTENT" 	&& ln -s "$GHOST_CONTENT/config.js" "$GHOST_SOURCE/config.js"
# Wed, 13 Sep 2017 21:17:24 GMT
VOLUME [/var/lib/ghost]
# Wed, 13 Sep 2017 21:17:25 GMT
COPY file:2cb0a64ef22301242537372657c5d88304b43153f351a7f2d0d61e05c3dfb29a in /usr/local/bin/ 
# Wed, 13 Sep 2017 21:17:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Sep 2017 21:17:25 GMT
EXPOSE 2368/tcp
# Wed, 13 Sep 2017 21:17:25 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:90f4dba627d65ea3223761bcfe54e726337a919fe98117ef107914f91be657c9`  
		Last Modified: Tue, 27 Jun 2017 18:47:56 GMT  
		Size: 2.4 MB (2385007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c02e9bd0b129afc373209e2498ba6bd7157164b4a96de677a2e1224527558e3d`  
		Last Modified: Wed, 13 Sep 2017 20:51:01 GMT  
		Size: 15.4 MB (15438807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae02bb9be1084245b51165da53a51c16267d437758238436108e38b62ee73c83`  
		Last Modified: Wed, 13 Sep 2017 20:50:56 GMT  
		Size: 945.5 KB (945482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670dd55024c52593c29fd34bf9e31b4442960627d5c074537ddb43b44c801685`  
		Last Modified: Wed, 13 Sep 2017 21:19:03 GMT  
		Size: 8.4 KB (8367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6998b8eab62af074a96f5a68111c04090ff0a876b7a501917024948d84228a`  
		Last Modified: Wed, 13 Sep 2017 21:21:11 GMT  
		Size: 1.3 MB (1336092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae0b83b60255add53275d283becad4dd2c65fbacccb6ba51342326cab98cde9`  
		Last Modified: Wed, 13 Sep 2017 21:21:06 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:940406319f692a95bc97b34410f9ad07b1ac5410b537fedf4bcef9cd1cf19f22`  
		Last Modified: Wed, 13 Sep 2017 21:21:20 GMT  
		Size: 24.9 MB (24881708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d59ebfd1db388965772b75bf1597d45b7d4cd3d8c591934d37ad09b94b5e43d2`  
		Last Modified: Wed, 13 Sep 2017 21:21:07 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:862a533120c862f1a83b05447d226be18d2af33f4860087d080db846d1360a05`  
		Last Modified: Wed, 13 Sep 2017 21:21:06 GMT  
		Size: 609.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:1`

```console
$ docker pull ghost@sha256:d446bb82e91ed5d33204c5a9c691d96165fb39ff62789090a15e0e4d5b6beb71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ghost:1` - linux; amd64

```console
$ docker pull ghost@sha256:d44b2a32948ec5ce91c7f50b28a51c35d4b77a831ca5410de669faae1161554d
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.0 MB (216993763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffcb039c6423f48dbd4cbc193990fc3e2dac3f7ce7d4043efb3cab571381de9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 13 Sep 2017 08:40:43 GMT
ADD file:d7333b3e0bc6479d2faed32e06d85f1975e5b23e13e75555aeed0f639770413b in / 
# Wed, 13 Sep 2017 08:40:43 GMT
CMD ["bash"]
# Wed, 13 Sep 2017 12:32:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Sep 2017 12:32:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Sep 2017 20:23:45 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 13 Sep 2017 20:23:48 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done
# Wed, 13 Sep 2017 20:23:48 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Wed, 13 Sep 2017 20:38:03 GMT
ENV NODE_VERSION=6.11.3
# Wed, 13 Sep 2017 20:38:26 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Wed, 13 Sep 2017 20:38:26 GMT
ENV YARN_VERSION=0.27.5
# Wed, 13 Sep 2017 20:38:30 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Wed, 13 Sep 2017 20:38:30 GMT
CMD ["node"]
# Wed, 13 Sep 2017 21:10:30 GMT
ENV GOSU_VERSION=1.10
# Wed, 13 Sep 2017 21:10:35 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Wed, 13 Sep 2017 21:10:35 GMT
ENV NPM_CONFIG_LOGLEVEL=warn
# Wed, 13 Sep 2017 21:10:35 GMT
ENV NODE_ENV=production
# Wed, 13 Sep 2017 21:10:35 GMT
ENV GHOST_CLI_VERSION=1.1.1
# Fri, 29 Sep 2017 22:33:33 GMT
ENV GHOST_VERSION=1.10.0
# Fri, 29 Sep 2017 22:34:08 GMT
RUN npm install -g "ghost-cli@$GHOST_CLI_VERSION" knex-migrator@latest
# Fri, 29 Sep 2017 22:34:09 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 29 Sep 2017 22:34:09 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 29 Sep 2017 22:34:42 GMT
RUN set -ex; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"
# Fri, 29 Sep 2017 22:34:43 GMT
WORKDIR /var/lib/ghost
# Fri, 29 Sep 2017 22:34:44 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 29 Sep 2017 22:34:44 GMT
COPY file:ef6da72f41bc8f60c42fab63c9c2ffdee82253c6dd2110e3d50866e5445df15e in /usr/local/bin 
# Fri, 29 Sep 2017 22:34:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Sep 2017 22:34:44 GMT
EXPOSE 2368/tcp
# Fri, 29 Sep 2017 22:34:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:aa18ad1a0d334d80981104c599fa8cef9264552a265b1197af11274beba767cf`  
		Last Modified: Thu, 07 Sep 2017 23:11:06 GMT  
		Size: 52.6 MB (52595547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a33158a1367c7c4103c89ae66e8f4fdec4ada6a39d4648cf254b32296d6668`  
		Last Modified: Wed, 13 Sep 2017 12:54:21 GMT  
		Size: 19.3 MB (19263717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e2ecbdc66945a5816aa0d37501c34fe6ae76d1664a47cd366604f68a557052`  
		Last Modified: Wed, 13 Sep 2017 20:49:04 GMT  
		Size: 4.4 KB (4406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba36da051a26db65f69c7538041ed3bf4d545ba973e1763029ba67ea44b99ef`  
		Last Modified: Wed, 13 Sep 2017 20:49:04 GMT  
		Size: 119.2 KB (119152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83260829fd758c7ed96bf6b66af7a83c16afb34bd20fea7c30627caa474c19e0`  
		Last Modified: Wed, 13 Sep 2017 20:51:45 GMT  
		Size: 14.7 MB (14718405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7459ed23b0dbcdf1adf35d3c09d1104dfce1711690a871cb7fea376fdeea9176`  
		Last Modified: Wed, 13 Sep 2017 20:51:40 GMT  
		Size: 938.5 KB (938460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed248cbe68e68af79ca31d36052e903e9bce24bac602f71d2d8ee4a9bc3676a1`  
		Last Modified: Wed, 13 Sep 2017 21:17:36 GMT  
		Size: 500.7 KB (500669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d1e6583f2f4dc6499d66c22f938d5d66fced54f990d20271ab036a86fe0cbc`  
		Last Modified: Fri, 29 Sep 2017 22:42:07 GMT  
		Size: 34.4 MB (34373399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3f41a3555b3208a268885077ed506c02f4da1f3b4a815d7028bad80dcea546`  
		Last Modified: Fri, 29 Sep 2017 22:42:32 GMT  
		Size: 94.5 MB (94479434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e58a823622c8980387093b393ee3ec8b406ee36a079cc10da539b0471f4e2a3`  
		Last Modified: Fri, 29 Sep 2017 22:41:36 GMT  
		Size: 574.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:1` - linux; arm variant v7

```console
$ docker pull ghost@sha256:24db28a9250caead11744a7d1944be9a2c36652c03b014abaed2f286fca94def
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.4 MB (201351870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7be5bcccf373c0e3287bbc7b2a27655d28f6662151e103ade060f108074abab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 27 Sep 2017 04:12:21 GMT
ADD file:ef59ce7fe68882b1b44bc3c4a5e9e465561cb257fb63f8c2b3c247abb012486b in / 
# Wed, 27 Sep 2017 04:12:22 GMT
CMD ["bash"]
# Wed, 27 Sep 2017 04:39:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 27 Sep 2017 04:39:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 27 Sep 2017 07:03:35 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 27 Sep 2017 07:07:47 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done
# Wed, 27 Sep 2017 07:07:48 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Wed, 27 Sep 2017 07:17:28 GMT
ENV NODE_VERSION=6.11.3
# Wed, 27 Sep 2017 07:18:06 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Wed, 27 Sep 2017 07:18:08 GMT
ENV YARN_VERSION=0.27.5
# Wed, 27 Sep 2017 07:18:10 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Wed, 27 Sep 2017 07:18:10 GMT
CMD ["node"]
# Wed, 27 Sep 2017 07:58:52 GMT
ENV GOSU_VERSION=1.10
# Wed, 27 Sep 2017 07:58:54 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Wed, 27 Sep 2017 07:58:54 GMT
ENV NPM_CONFIG_LOGLEVEL=warn
# Wed, 27 Sep 2017 07:58:54 GMT
ENV NODE_ENV=production
# Wed, 27 Sep 2017 07:58:54 GMT
ENV GHOST_CLI_VERSION=1.1.1
# Sat, 30 Sep 2017 11:55:22 GMT
ENV GHOST_VERSION=1.10.0
# Sat, 30 Sep 2017 11:56:35 GMT
RUN npm install -g "ghost-cli@$GHOST_CLI_VERSION" knex-migrator@latest
# Sat, 30 Sep 2017 11:56:36 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 30 Sep 2017 11:56:37 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 30 Sep 2017 11:57:49 GMT
RUN set -ex; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"
# Sat, 30 Sep 2017 11:57:52 GMT
WORKDIR /var/lib/ghost
# Sat, 30 Sep 2017 11:57:52 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 30 Sep 2017 11:57:52 GMT
COPY file:ef6da72f41bc8f60c42fab63c9c2ffdee82253c6dd2110e3d50866e5445df15e in /usr/local/bin 
# Sat, 30 Sep 2017 11:57:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 30 Sep 2017 11:57:53 GMT
EXPOSE 2368/tcp
# Sat, 30 Sep 2017 11:57:53 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:8c7b63aa62f92f5be1e93e5129c5c99dac397c6d3b5f6c6452bfd0905f6f20be`  
		Last Modified: Wed, 27 Sep 2017 04:17:18 GMT  
		Size: 48.7 MB (48686544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a607bd01ffd678134d1281825ba8fafc069965446932fb3da991e8e6c2d3065d`  
		Last Modified: Wed, 27 Sep 2017 04:58:12 GMT  
		Size: 18.3 MB (18262468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7733b25f61410d8e74ee676e195c358ac6519ef39f1a92f3cd11c5f8ca2048`  
		Last Modified: Wed, 27 Sep 2017 07:20:36 GMT  
		Size: 4.4 KB (4420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553903f3bafddd9019242ebd76c10ae0ba04207db8e960c84758e8762b1c4cca`  
		Last Modified: Wed, 27 Sep 2017 07:20:36 GMT  
		Size: 119.2 KB (119190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34bc7bac012caabb127f3461274a9a4cb95bde62751a07df9eb243be1e2877ad`  
		Last Modified: Wed, 27 Sep 2017 07:22:00 GMT  
		Size: 13.9 MB (13877719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c31b00c4993376f813ed323a451b7444b0f176979418ff061aa095b002377bc0`  
		Last Modified: Wed, 27 Sep 2017 07:21:55 GMT  
		Size: 940.2 KB (940161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:541588608a9db7c94840b658b4d597ff4903433af8b4e46a3b35d0d48ccfa330`  
		Last Modified: Wed, 27 Sep 2017 08:05:26 GMT  
		Size: 475.3 KB (475267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ee01efe1bc522be8f8abd8080bdd3708e66ec95ede0cb6a5d2e1a5a321caf51`  
		Last Modified: Sat, 30 Sep 2017 11:58:34 GMT  
		Size: 29.2 MB (29169178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d95b75a1bb347fc5d04c4ac95b89a21a27bb397e26275b5c126c561efb0947b`  
		Last Modified: Sat, 30 Sep 2017 11:58:58 GMT  
		Size: 89.8 MB (89816348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4681c19bb16c56ef451982b2084f48ac2ae91f8007c55a3259b7fd168ecc312f`  
		Last Modified: Sat, 30 Sep 2017 11:58:20 GMT  
		Size: 575.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:1` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:4778e6eafd796f96c4e3d279c18fc1a3dd030f32e215c2fe6150198baae84e90
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.9 MB (203937560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ce70e09282f3873bdcf8a71e0562634725e2269efe303c165537c15dabfbbbb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 08 Sep 2017 17:23:41 GMT
ADD file:9f576a63a5e03994904e585c35fbeef6a2c96c41d8f696705c033f3ca69b6a2b in / 
# Fri, 08 Sep 2017 17:23:42 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 18:32:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 18:32:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 Sep 2017 23:16:17 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 14 Sep 2017 23:16:22 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done
# Thu, 14 Sep 2017 23:16:24 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Thu, 14 Sep 2017 23:18:55 GMT
ENV NODE_VERSION=6.11.3
# Thu, 14 Sep 2017 23:19:28 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Thu, 14 Sep 2017 23:19:29 GMT
ENV YARN_VERSION=0.27.5
# Thu, 14 Sep 2017 23:19:35 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Thu, 14 Sep 2017 23:19:37 GMT
CMD ["node"]
# Fri, 15 Sep 2017 02:19:54 GMT
ENV GOSU_VERSION=1.10
# Fri, 15 Sep 2017 02:20:02 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Fri, 15 Sep 2017 02:20:03 GMT
ENV NPM_CONFIG_LOGLEVEL=warn
# Fri, 15 Sep 2017 02:20:04 GMT
ENV NODE_ENV=production
# Fri, 15 Sep 2017 02:20:05 GMT
ENV GHOST_CLI_VERSION=1.1.1
# Sat, 30 Sep 2017 10:41:33 GMT
ENV GHOST_VERSION=1.10.0
# Sat, 30 Sep 2017 10:43:52 GMT
RUN npm install -g "ghost-cli@$GHOST_CLI_VERSION" knex-migrator@latest
# Sat, 30 Sep 2017 10:43:54 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 30 Sep 2017 10:43:55 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 30 Sep 2017 10:45:38 GMT
RUN set -ex; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"
# Sat, 30 Sep 2017 10:45:42 GMT
WORKDIR /var/lib/ghost
# Sat, 30 Sep 2017 10:45:42 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 30 Sep 2017 10:45:43 GMT
COPY file:ef6da72f41bc8f60c42fab63c9c2ffdee82253c6dd2110e3d50866e5445df15e in /usr/local/bin 
# Sat, 30 Sep 2017 10:45:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 30 Sep 2017 10:45:45 GMT
EXPOSE 2368/tcp
# Sat, 30 Sep 2017 10:45:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:e91a355b0d3ff86add037a3f24718b760d8eb3f346f998e5116375ddce9eae19`  
		Last Modified: Fri, 08 Sep 2017 17:34:56 GMT  
		Size: 49.9 MB (49929457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e054bfb02234c6e2b5305981d365c3b31101ec460b0d90df3b099305c03196`  
		Last Modified: Thu, 14 Sep 2017 22:01:15 GMT  
		Size: 18.7 MB (18737603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68cbb48bf959f44cbc4806f42587333e86631edab819261ca51eba1da6fcd637`  
		Last Modified: Thu, 14 Sep 2017 23:24:36 GMT  
		Size: 4.4 KB (4417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e961bd22aace0af8a10a14a5d6282014bdb3cf7c4d5b42e16a0dd45e4cd06dac`  
		Last Modified: Thu, 14 Sep 2017 23:24:36 GMT  
		Size: 119.2 KB (119150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:280e0b3e39cb221ce8de69ec6e8d5e99fd9761fc3a6d37cbd9086ad72d3b41dc`  
		Last Modified: Thu, 14 Sep 2017 23:27:52 GMT  
		Size: 14.7 MB (14707206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e714752cefed2ff3be3734c49f1a880303ff6290d0705230e5f486a0a0bbe756`  
		Last Modified: Thu, 14 Sep 2017 23:27:45 GMT  
		Size: 940.1 KB (940132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de4bc9133bf690ef04927a67017f86cc9e619e51f7cac9262ff9165db6baefc`  
		Last Modified: Fri, 15 Sep 2017 02:35:50 GMT  
		Size: 468.7 KB (468701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d7bd10a95781c324562ce9f74235c7ef17ba5265033caafb028f240912114a`  
		Last Modified: Sat, 30 Sep 2017 10:46:26 GMT  
		Size: 29.2 MB (29168766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82c35004fc2685c10e031b4e39e97503ed72b418850306ead8ad0a25f0112976`  
		Last Modified: Sat, 30 Sep 2017 10:46:48 GMT  
		Size: 89.9 MB (89861555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd20cd50f4050f013e3109e93315f76c9c378d8d8acad7e5140112cacb55f835`  
		Last Modified: Sat, 30 Sep 2017 10:46:11 GMT  
		Size: 573.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:1` - linux; ppc64le

```console
$ docker pull ghost@sha256:5519b5f58af430a845cfb4617430d530fc69b279353a2b41883793c949d79537
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.1 MB (206070261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf606d1107cf8f7551b5f5dff21b1769766e0d07f6e2decbeafacb2446180d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 08 Sep 2017 00:32:21 GMT
ADD file:483b3245941140ac32394a804364a1a9bd5dfdf1b4475238b61068cc7252ac08 in / 
# Fri, 08 Sep 2017 00:32:21 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 01:03:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 01:03:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 Sep 2017 23:10:48 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 14 Sep 2017 23:11:08 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done
# Thu, 14 Sep 2017 23:11:12 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Thu, 14 Sep 2017 23:15:42 GMT
ENV NODE_VERSION=6.11.3
# Thu, 14 Sep 2017 23:16:32 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Thu, 14 Sep 2017 23:16:41 GMT
ENV YARN_VERSION=0.27.5
# Thu, 14 Sep 2017 23:16:48 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Thu, 14 Sep 2017 23:16:50 GMT
CMD ["node"]
# Fri, 15 Sep 2017 02:22:38 GMT
ENV GOSU_VERSION=1.10
# Fri, 15 Sep 2017 02:22:46 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Fri, 15 Sep 2017 02:22:48 GMT
ENV NPM_CONFIG_LOGLEVEL=warn
# Fri, 15 Sep 2017 02:22:52 GMT
ENV NODE_ENV=production
# Fri, 15 Sep 2017 02:22:54 GMT
ENV GHOST_CLI_VERSION=1.1.1
# Sat, 30 Sep 2017 01:26:24 GMT
ENV GHOST_VERSION=1.10.0
# Sat, 30 Sep 2017 01:27:21 GMT
RUN npm install -g "ghost-cli@$GHOST_CLI_VERSION" knex-migrator@latest
# Sat, 30 Sep 2017 01:27:28 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 30 Sep 2017 01:27:30 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 30 Sep 2017 01:28:37 GMT
RUN set -ex; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"
# Sat, 30 Sep 2017 01:28:44 GMT
WORKDIR /var/lib/ghost
# Sat, 30 Sep 2017 01:28:48 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 30 Sep 2017 01:28:50 GMT
COPY file:ef6da72f41bc8f60c42fab63c9c2ffdee82253c6dd2110e3d50866e5445df15e in /usr/local/bin 
# Sat, 30 Sep 2017 01:28:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 30 Sep 2017 01:28:55 GMT
EXPOSE 2368/tcp
# Sat, 30 Sep 2017 01:28:58 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d4a5434e09b7ac8431060d347d6ef1233ae07514878fb2aff4085bcf441c29f3`  
		Last Modified: Fri, 08 Sep 2017 00:36:52 GMT  
		Size: 51.8 MB (51809570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48596af2c38701f94440e222bf8f3d4b2da85e2982c97ae15186eba523249e0b`  
		Last Modified: Thu, 14 Sep 2017 22:21:02 GMT  
		Size: 19.2 MB (19199596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1dc276f5b0bc12cddaf889657d8ed9d7ec3e6add07506308ea49dc52bb6eff`  
		Last Modified: Thu, 14 Sep 2017 23:22:38 GMT  
		Size: 4.4 KB (4444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb57f53562fb9db3e40e7ee479f5526f635b724a0632d9a4d3da2500a44c491d`  
		Last Modified: Thu, 14 Sep 2017 23:22:39 GMT  
		Size: 119.2 KB (119184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f255065ee2535a6b44019881cc1954c1a7f665f6b0c530c618663be94e4a23`  
		Last Modified: Thu, 14 Sep 2017 23:26:37 GMT  
		Size: 14.5 MB (14475182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68be6ded470a2cf42b2ccda178f212a25198e102a4e3249456140252fa22f054`  
		Last Modified: Thu, 14 Sep 2017 23:26:32 GMT  
		Size: 940.2 KB (940157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad1d6527d8ade34c5efd2bd98f7a049a917ff22859c6eaaed4046a2df232d91b`  
		Last Modified: Fri, 15 Sep 2017 02:32:57 GMT  
		Size: 469.9 KB (469852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f814a9bc90f3c846324f0952f0ae962140c6c3eaedd3e91eebd25f20d56bcc06`  
		Last Modified: Sat, 30 Sep 2017 01:29:27 GMT  
		Size: 29.2 MB (29167447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd14b03e56a10a52bb6decdf699c7db5c4446ff682043ec05c46042069ac5e6`  
		Last Modified: Sat, 30 Sep 2017 01:29:45 GMT  
		Size: 89.9 MB (89884255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b4c1125e28a6f6aaf1a9849d51d4724cd2372100162880dc826bfe2cf89a5b`  
		Last Modified: Sat, 30 Sep 2017 01:29:17 GMT  
		Size: 574.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:1` - linux; s390x

```console
$ docker pull ghost@sha256:d64cf4c152b1cab609af105e32edb33313e29d8f13cf68ca7e057d980c2c8cc2
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207664584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce7ab8a934452910b724a2dbbdd3229e252349593a2327814139278d378072c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 08 Sep 2017 05:21:42 GMT
ADD file:996e52a941b7162fafcf761c415142a34a2fc703e21d2f264b824373e9fa4b1e in / 
# Fri, 08 Sep 2017 05:21:43 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 05:48:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 05:48:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 08 Sep 2017 17:04:11 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Fri, 08 Sep 2017 17:04:12 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done
# Fri, 08 Sep 2017 17:04:12 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Fri, 08 Sep 2017 17:04:55 GMT
ENV NODE_VERSION=6.11.3
# Fri, 08 Sep 2017 17:05:10 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Fri, 08 Sep 2017 17:05:10 GMT
ENV YARN_VERSION=0.27.5
# Fri, 08 Sep 2017 17:05:11 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Fri, 08 Sep 2017 17:05:12 GMT
CMD ["node"]
# Fri, 08 Sep 2017 18:17:08 GMT
ENV GOSU_VERSION=1.10
# Fri, 08 Sep 2017 18:17:11 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Fri, 08 Sep 2017 18:17:11 GMT
ENV NPM_CONFIG_LOGLEVEL=warn
# Fri, 08 Sep 2017 18:17:11 GMT
ENV NODE_ENV=production
# Fri, 08 Sep 2017 18:17:11 GMT
ENV GHOST_CLI_VERSION=1.1.1
# Sat, 30 Sep 2017 14:22:24 GMT
ENV GHOST_VERSION=1.10.0
# Sat, 30 Sep 2017 14:23:02 GMT
RUN npm install -g "ghost-cli@$GHOST_CLI_VERSION" knex-migrator@latest
# Sat, 30 Sep 2017 14:23:03 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 30 Sep 2017 14:23:03 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 30 Sep 2017 14:23:33 GMT
RUN set -ex; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"
# Sat, 30 Sep 2017 14:23:35 GMT
WORKDIR /var/lib/ghost
# Sat, 30 Sep 2017 14:23:35 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 30 Sep 2017 14:23:35 GMT
COPY file:ef6da72f41bc8f60c42fab63c9c2ffdee82253c6dd2110e3d50866e5445df15e in /usr/local/bin 
# Sat, 30 Sep 2017 14:23:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 30 Sep 2017 14:23:35 GMT
EXPOSE 2368/tcp
# Sat, 30 Sep 2017 14:23:36 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:5f39dbffcd07e3254246d3c2e4b3532c3697ed04f83eadf5433da820098787df`  
		Last Modified: Fri, 08 Sep 2017 05:24:42 GMT  
		Size: 52.8 MB (52788802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5a344275c5d5a12a16990e9ddb7cfb9bc9b793cc51fbf8bf8993426e287c27`  
		Last Modified: Fri, 08 Sep 2017 16:41:52 GMT  
		Size: 19.5 MB (19470373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c81355314e654fd3d4e1dcbec2f82fffb19b856e65aa403cf7b2d471582658`  
		Last Modified: Fri, 08 Sep 2017 17:05:56 GMT  
		Size: 4.4 KB (4411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9c66bc4cf9f13c8d89cb57f07ce23693a1efcbbbcc32e7e30c5e8e0cefa2c8`  
		Last Modified: Fri, 08 Sep 2017 17:05:56 GMT  
		Size: 119.1 KB (119148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa1121a725f9b59e0fcd0c6226075d97e638b15fdfc40f5e1d57d3a5f3c3f190`  
		Last Modified: Fri, 08 Sep 2017 17:07:00 GMT  
		Size: 14.8 MB (14847789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa31e4823df3a66473b6ca7286cf7a152288b868f3cf1d4df5eb0393f5e81da`  
		Last Modified: Fri, 08 Sep 2017 17:06:56 GMT  
		Size: 938.5 KB (938452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6819f9496d60b6b7dda2b89e7dd5c2a3c3442d0f1270b9f67b3c132f70fbeeb`  
		Last Modified: Fri, 08 Sep 2017 18:20:31 GMT  
		Size: 486.8 KB (486823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a59f71a40f843fc869ea2674c548cd5437531fbfa4cad604ba97432de4c3662`  
		Last Modified: Sat, 30 Sep 2017 14:23:59 GMT  
		Size: 29.2 MB (29166808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0eef1dc513aa74c3750bd41d13dbfd1576d9333340f889213b7d62aaeae7737`  
		Last Modified: Sat, 30 Sep 2017 14:24:10 GMT  
		Size: 89.8 MB (89841405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9fda95fa7073acebbc9f0b203e74fe5e7d92fde0d6097b30ce415370f804ee`  
		Last Modified: Sat, 30 Sep 2017 14:23:52 GMT  
		Size: 573.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:1.10`

```console
$ docker pull ghost@sha256:d446bb82e91ed5d33204c5a9c691d96165fb39ff62789090a15e0e4d5b6beb71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ghost:1.10` - linux; amd64

```console
$ docker pull ghost@sha256:d44b2a32948ec5ce91c7f50b28a51c35d4b77a831ca5410de669faae1161554d
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.0 MB (216993763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffcb039c6423f48dbd4cbc193990fc3e2dac3f7ce7d4043efb3cab571381de9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 13 Sep 2017 08:40:43 GMT
ADD file:d7333b3e0bc6479d2faed32e06d85f1975e5b23e13e75555aeed0f639770413b in / 
# Wed, 13 Sep 2017 08:40:43 GMT
CMD ["bash"]
# Wed, 13 Sep 2017 12:32:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Sep 2017 12:32:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Sep 2017 20:23:45 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 13 Sep 2017 20:23:48 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done
# Wed, 13 Sep 2017 20:23:48 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Wed, 13 Sep 2017 20:38:03 GMT
ENV NODE_VERSION=6.11.3
# Wed, 13 Sep 2017 20:38:26 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Wed, 13 Sep 2017 20:38:26 GMT
ENV YARN_VERSION=0.27.5
# Wed, 13 Sep 2017 20:38:30 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Wed, 13 Sep 2017 20:38:30 GMT
CMD ["node"]
# Wed, 13 Sep 2017 21:10:30 GMT
ENV GOSU_VERSION=1.10
# Wed, 13 Sep 2017 21:10:35 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Wed, 13 Sep 2017 21:10:35 GMT
ENV NPM_CONFIG_LOGLEVEL=warn
# Wed, 13 Sep 2017 21:10:35 GMT
ENV NODE_ENV=production
# Wed, 13 Sep 2017 21:10:35 GMT
ENV GHOST_CLI_VERSION=1.1.1
# Fri, 29 Sep 2017 22:33:33 GMT
ENV GHOST_VERSION=1.10.0
# Fri, 29 Sep 2017 22:34:08 GMT
RUN npm install -g "ghost-cli@$GHOST_CLI_VERSION" knex-migrator@latest
# Fri, 29 Sep 2017 22:34:09 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 29 Sep 2017 22:34:09 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 29 Sep 2017 22:34:42 GMT
RUN set -ex; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"
# Fri, 29 Sep 2017 22:34:43 GMT
WORKDIR /var/lib/ghost
# Fri, 29 Sep 2017 22:34:44 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 29 Sep 2017 22:34:44 GMT
COPY file:ef6da72f41bc8f60c42fab63c9c2ffdee82253c6dd2110e3d50866e5445df15e in /usr/local/bin 
# Fri, 29 Sep 2017 22:34:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Sep 2017 22:34:44 GMT
EXPOSE 2368/tcp
# Fri, 29 Sep 2017 22:34:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:aa18ad1a0d334d80981104c599fa8cef9264552a265b1197af11274beba767cf`  
		Last Modified: Thu, 07 Sep 2017 23:11:06 GMT  
		Size: 52.6 MB (52595547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a33158a1367c7c4103c89ae66e8f4fdec4ada6a39d4648cf254b32296d6668`  
		Last Modified: Wed, 13 Sep 2017 12:54:21 GMT  
		Size: 19.3 MB (19263717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e2ecbdc66945a5816aa0d37501c34fe6ae76d1664a47cd366604f68a557052`  
		Last Modified: Wed, 13 Sep 2017 20:49:04 GMT  
		Size: 4.4 KB (4406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba36da051a26db65f69c7538041ed3bf4d545ba973e1763029ba67ea44b99ef`  
		Last Modified: Wed, 13 Sep 2017 20:49:04 GMT  
		Size: 119.2 KB (119152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83260829fd758c7ed96bf6b66af7a83c16afb34bd20fea7c30627caa474c19e0`  
		Last Modified: Wed, 13 Sep 2017 20:51:45 GMT  
		Size: 14.7 MB (14718405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7459ed23b0dbcdf1adf35d3c09d1104dfce1711690a871cb7fea376fdeea9176`  
		Last Modified: Wed, 13 Sep 2017 20:51:40 GMT  
		Size: 938.5 KB (938460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed248cbe68e68af79ca31d36052e903e9bce24bac602f71d2d8ee4a9bc3676a1`  
		Last Modified: Wed, 13 Sep 2017 21:17:36 GMT  
		Size: 500.7 KB (500669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d1e6583f2f4dc6499d66c22f938d5d66fced54f990d20271ab036a86fe0cbc`  
		Last Modified: Fri, 29 Sep 2017 22:42:07 GMT  
		Size: 34.4 MB (34373399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3f41a3555b3208a268885077ed506c02f4da1f3b4a815d7028bad80dcea546`  
		Last Modified: Fri, 29 Sep 2017 22:42:32 GMT  
		Size: 94.5 MB (94479434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e58a823622c8980387093b393ee3ec8b406ee36a079cc10da539b0471f4e2a3`  
		Last Modified: Fri, 29 Sep 2017 22:41:36 GMT  
		Size: 574.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:1.10` - linux; arm variant v7

```console
$ docker pull ghost@sha256:24db28a9250caead11744a7d1944be9a2c36652c03b014abaed2f286fca94def
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.4 MB (201351870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7be5bcccf373c0e3287bbc7b2a27655d28f6662151e103ade060f108074abab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 27 Sep 2017 04:12:21 GMT
ADD file:ef59ce7fe68882b1b44bc3c4a5e9e465561cb257fb63f8c2b3c247abb012486b in / 
# Wed, 27 Sep 2017 04:12:22 GMT
CMD ["bash"]
# Wed, 27 Sep 2017 04:39:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 27 Sep 2017 04:39:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 27 Sep 2017 07:03:35 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 27 Sep 2017 07:07:47 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done
# Wed, 27 Sep 2017 07:07:48 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Wed, 27 Sep 2017 07:17:28 GMT
ENV NODE_VERSION=6.11.3
# Wed, 27 Sep 2017 07:18:06 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Wed, 27 Sep 2017 07:18:08 GMT
ENV YARN_VERSION=0.27.5
# Wed, 27 Sep 2017 07:18:10 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Wed, 27 Sep 2017 07:18:10 GMT
CMD ["node"]
# Wed, 27 Sep 2017 07:58:52 GMT
ENV GOSU_VERSION=1.10
# Wed, 27 Sep 2017 07:58:54 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Wed, 27 Sep 2017 07:58:54 GMT
ENV NPM_CONFIG_LOGLEVEL=warn
# Wed, 27 Sep 2017 07:58:54 GMT
ENV NODE_ENV=production
# Wed, 27 Sep 2017 07:58:54 GMT
ENV GHOST_CLI_VERSION=1.1.1
# Sat, 30 Sep 2017 11:55:22 GMT
ENV GHOST_VERSION=1.10.0
# Sat, 30 Sep 2017 11:56:35 GMT
RUN npm install -g "ghost-cli@$GHOST_CLI_VERSION" knex-migrator@latest
# Sat, 30 Sep 2017 11:56:36 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 30 Sep 2017 11:56:37 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 30 Sep 2017 11:57:49 GMT
RUN set -ex; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"
# Sat, 30 Sep 2017 11:57:52 GMT
WORKDIR /var/lib/ghost
# Sat, 30 Sep 2017 11:57:52 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 30 Sep 2017 11:57:52 GMT
COPY file:ef6da72f41bc8f60c42fab63c9c2ffdee82253c6dd2110e3d50866e5445df15e in /usr/local/bin 
# Sat, 30 Sep 2017 11:57:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 30 Sep 2017 11:57:53 GMT
EXPOSE 2368/tcp
# Sat, 30 Sep 2017 11:57:53 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:8c7b63aa62f92f5be1e93e5129c5c99dac397c6d3b5f6c6452bfd0905f6f20be`  
		Last Modified: Wed, 27 Sep 2017 04:17:18 GMT  
		Size: 48.7 MB (48686544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a607bd01ffd678134d1281825ba8fafc069965446932fb3da991e8e6c2d3065d`  
		Last Modified: Wed, 27 Sep 2017 04:58:12 GMT  
		Size: 18.3 MB (18262468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7733b25f61410d8e74ee676e195c358ac6519ef39f1a92f3cd11c5f8ca2048`  
		Last Modified: Wed, 27 Sep 2017 07:20:36 GMT  
		Size: 4.4 KB (4420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553903f3bafddd9019242ebd76c10ae0ba04207db8e960c84758e8762b1c4cca`  
		Last Modified: Wed, 27 Sep 2017 07:20:36 GMT  
		Size: 119.2 KB (119190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34bc7bac012caabb127f3461274a9a4cb95bde62751a07df9eb243be1e2877ad`  
		Last Modified: Wed, 27 Sep 2017 07:22:00 GMT  
		Size: 13.9 MB (13877719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c31b00c4993376f813ed323a451b7444b0f176979418ff061aa095b002377bc0`  
		Last Modified: Wed, 27 Sep 2017 07:21:55 GMT  
		Size: 940.2 KB (940161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:541588608a9db7c94840b658b4d597ff4903433af8b4e46a3b35d0d48ccfa330`  
		Last Modified: Wed, 27 Sep 2017 08:05:26 GMT  
		Size: 475.3 KB (475267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ee01efe1bc522be8f8abd8080bdd3708e66ec95ede0cb6a5d2e1a5a321caf51`  
		Last Modified: Sat, 30 Sep 2017 11:58:34 GMT  
		Size: 29.2 MB (29169178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d95b75a1bb347fc5d04c4ac95b89a21a27bb397e26275b5c126c561efb0947b`  
		Last Modified: Sat, 30 Sep 2017 11:58:58 GMT  
		Size: 89.8 MB (89816348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4681c19bb16c56ef451982b2084f48ac2ae91f8007c55a3259b7fd168ecc312f`  
		Last Modified: Sat, 30 Sep 2017 11:58:20 GMT  
		Size: 575.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:1.10` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:4778e6eafd796f96c4e3d279c18fc1a3dd030f32e215c2fe6150198baae84e90
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.9 MB (203937560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ce70e09282f3873bdcf8a71e0562634725e2269efe303c165537c15dabfbbbb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 08 Sep 2017 17:23:41 GMT
ADD file:9f576a63a5e03994904e585c35fbeef6a2c96c41d8f696705c033f3ca69b6a2b in / 
# Fri, 08 Sep 2017 17:23:42 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 18:32:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 18:32:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 Sep 2017 23:16:17 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 14 Sep 2017 23:16:22 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done
# Thu, 14 Sep 2017 23:16:24 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Thu, 14 Sep 2017 23:18:55 GMT
ENV NODE_VERSION=6.11.3
# Thu, 14 Sep 2017 23:19:28 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Thu, 14 Sep 2017 23:19:29 GMT
ENV YARN_VERSION=0.27.5
# Thu, 14 Sep 2017 23:19:35 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Thu, 14 Sep 2017 23:19:37 GMT
CMD ["node"]
# Fri, 15 Sep 2017 02:19:54 GMT
ENV GOSU_VERSION=1.10
# Fri, 15 Sep 2017 02:20:02 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Fri, 15 Sep 2017 02:20:03 GMT
ENV NPM_CONFIG_LOGLEVEL=warn
# Fri, 15 Sep 2017 02:20:04 GMT
ENV NODE_ENV=production
# Fri, 15 Sep 2017 02:20:05 GMT
ENV GHOST_CLI_VERSION=1.1.1
# Sat, 30 Sep 2017 10:41:33 GMT
ENV GHOST_VERSION=1.10.0
# Sat, 30 Sep 2017 10:43:52 GMT
RUN npm install -g "ghost-cli@$GHOST_CLI_VERSION" knex-migrator@latest
# Sat, 30 Sep 2017 10:43:54 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 30 Sep 2017 10:43:55 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 30 Sep 2017 10:45:38 GMT
RUN set -ex; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"
# Sat, 30 Sep 2017 10:45:42 GMT
WORKDIR /var/lib/ghost
# Sat, 30 Sep 2017 10:45:42 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 30 Sep 2017 10:45:43 GMT
COPY file:ef6da72f41bc8f60c42fab63c9c2ffdee82253c6dd2110e3d50866e5445df15e in /usr/local/bin 
# Sat, 30 Sep 2017 10:45:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 30 Sep 2017 10:45:45 GMT
EXPOSE 2368/tcp
# Sat, 30 Sep 2017 10:45:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:e91a355b0d3ff86add037a3f24718b760d8eb3f346f998e5116375ddce9eae19`  
		Last Modified: Fri, 08 Sep 2017 17:34:56 GMT  
		Size: 49.9 MB (49929457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e054bfb02234c6e2b5305981d365c3b31101ec460b0d90df3b099305c03196`  
		Last Modified: Thu, 14 Sep 2017 22:01:15 GMT  
		Size: 18.7 MB (18737603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68cbb48bf959f44cbc4806f42587333e86631edab819261ca51eba1da6fcd637`  
		Last Modified: Thu, 14 Sep 2017 23:24:36 GMT  
		Size: 4.4 KB (4417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e961bd22aace0af8a10a14a5d6282014bdb3cf7c4d5b42e16a0dd45e4cd06dac`  
		Last Modified: Thu, 14 Sep 2017 23:24:36 GMT  
		Size: 119.2 KB (119150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:280e0b3e39cb221ce8de69ec6e8d5e99fd9761fc3a6d37cbd9086ad72d3b41dc`  
		Last Modified: Thu, 14 Sep 2017 23:27:52 GMT  
		Size: 14.7 MB (14707206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e714752cefed2ff3be3734c49f1a880303ff6290d0705230e5f486a0a0bbe756`  
		Last Modified: Thu, 14 Sep 2017 23:27:45 GMT  
		Size: 940.1 KB (940132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de4bc9133bf690ef04927a67017f86cc9e619e51f7cac9262ff9165db6baefc`  
		Last Modified: Fri, 15 Sep 2017 02:35:50 GMT  
		Size: 468.7 KB (468701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d7bd10a95781c324562ce9f74235c7ef17ba5265033caafb028f240912114a`  
		Last Modified: Sat, 30 Sep 2017 10:46:26 GMT  
		Size: 29.2 MB (29168766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82c35004fc2685c10e031b4e39e97503ed72b418850306ead8ad0a25f0112976`  
		Last Modified: Sat, 30 Sep 2017 10:46:48 GMT  
		Size: 89.9 MB (89861555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd20cd50f4050f013e3109e93315f76c9c378d8d8acad7e5140112cacb55f835`  
		Last Modified: Sat, 30 Sep 2017 10:46:11 GMT  
		Size: 573.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:1.10` - linux; ppc64le

```console
$ docker pull ghost@sha256:5519b5f58af430a845cfb4617430d530fc69b279353a2b41883793c949d79537
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.1 MB (206070261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf606d1107cf8f7551b5f5dff21b1769766e0d07f6e2decbeafacb2446180d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 08 Sep 2017 00:32:21 GMT
ADD file:483b3245941140ac32394a804364a1a9bd5dfdf1b4475238b61068cc7252ac08 in / 
# Fri, 08 Sep 2017 00:32:21 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 01:03:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 01:03:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 Sep 2017 23:10:48 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 14 Sep 2017 23:11:08 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done
# Thu, 14 Sep 2017 23:11:12 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Thu, 14 Sep 2017 23:15:42 GMT
ENV NODE_VERSION=6.11.3
# Thu, 14 Sep 2017 23:16:32 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Thu, 14 Sep 2017 23:16:41 GMT
ENV YARN_VERSION=0.27.5
# Thu, 14 Sep 2017 23:16:48 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Thu, 14 Sep 2017 23:16:50 GMT
CMD ["node"]
# Fri, 15 Sep 2017 02:22:38 GMT
ENV GOSU_VERSION=1.10
# Fri, 15 Sep 2017 02:22:46 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Fri, 15 Sep 2017 02:22:48 GMT
ENV NPM_CONFIG_LOGLEVEL=warn
# Fri, 15 Sep 2017 02:22:52 GMT
ENV NODE_ENV=production
# Fri, 15 Sep 2017 02:22:54 GMT
ENV GHOST_CLI_VERSION=1.1.1
# Sat, 30 Sep 2017 01:26:24 GMT
ENV GHOST_VERSION=1.10.0
# Sat, 30 Sep 2017 01:27:21 GMT
RUN npm install -g "ghost-cli@$GHOST_CLI_VERSION" knex-migrator@latest
# Sat, 30 Sep 2017 01:27:28 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 30 Sep 2017 01:27:30 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 30 Sep 2017 01:28:37 GMT
RUN set -ex; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"
# Sat, 30 Sep 2017 01:28:44 GMT
WORKDIR /var/lib/ghost
# Sat, 30 Sep 2017 01:28:48 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 30 Sep 2017 01:28:50 GMT
COPY file:ef6da72f41bc8f60c42fab63c9c2ffdee82253c6dd2110e3d50866e5445df15e in /usr/local/bin 
# Sat, 30 Sep 2017 01:28:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 30 Sep 2017 01:28:55 GMT
EXPOSE 2368/tcp
# Sat, 30 Sep 2017 01:28:58 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d4a5434e09b7ac8431060d347d6ef1233ae07514878fb2aff4085bcf441c29f3`  
		Last Modified: Fri, 08 Sep 2017 00:36:52 GMT  
		Size: 51.8 MB (51809570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48596af2c38701f94440e222bf8f3d4b2da85e2982c97ae15186eba523249e0b`  
		Last Modified: Thu, 14 Sep 2017 22:21:02 GMT  
		Size: 19.2 MB (19199596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1dc276f5b0bc12cddaf889657d8ed9d7ec3e6add07506308ea49dc52bb6eff`  
		Last Modified: Thu, 14 Sep 2017 23:22:38 GMT  
		Size: 4.4 KB (4444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb57f53562fb9db3e40e7ee479f5526f635b724a0632d9a4d3da2500a44c491d`  
		Last Modified: Thu, 14 Sep 2017 23:22:39 GMT  
		Size: 119.2 KB (119184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f255065ee2535a6b44019881cc1954c1a7f665f6b0c530c618663be94e4a23`  
		Last Modified: Thu, 14 Sep 2017 23:26:37 GMT  
		Size: 14.5 MB (14475182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68be6ded470a2cf42b2ccda178f212a25198e102a4e3249456140252fa22f054`  
		Last Modified: Thu, 14 Sep 2017 23:26:32 GMT  
		Size: 940.2 KB (940157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad1d6527d8ade34c5efd2bd98f7a049a917ff22859c6eaaed4046a2df232d91b`  
		Last Modified: Fri, 15 Sep 2017 02:32:57 GMT  
		Size: 469.9 KB (469852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f814a9bc90f3c846324f0952f0ae962140c6c3eaedd3e91eebd25f20d56bcc06`  
		Last Modified: Sat, 30 Sep 2017 01:29:27 GMT  
		Size: 29.2 MB (29167447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd14b03e56a10a52bb6decdf699c7db5c4446ff682043ec05c46042069ac5e6`  
		Last Modified: Sat, 30 Sep 2017 01:29:45 GMT  
		Size: 89.9 MB (89884255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b4c1125e28a6f6aaf1a9849d51d4724cd2372100162880dc826bfe2cf89a5b`  
		Last Modified: Sat, 30 Sep 2017 01:29:17 GMT  
		Size: 574.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:1.10` - linux; s390x

```console
$ docker pull ghost@sha256:d64cf4c152b1cab609af105e32edb33313e29d8f13cf68ca7e057d980c2c8cc2
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207664584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce7ab8a934452910b724a2dbbdd3229e252349593a2327814139278d378072c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 08 Sep 2017 05:21:42 GMT
ADD file:996e52a941b7162fafcf761c415142a34a2fc703e21d2f264b824373e9fa4b1e in / 
# Fri, 08 Sep 2017 05:21:43 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 05:48:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 05:48:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 08 Sep 2017 17:04:11 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Fri, 08 Sep 2017 17:04:12 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done
# Fri, 08 Sep 2017 17:04:12 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Fri, 08 Sep 2017 17:04:55 GMT
ENV NODE_VERSION=6.11.3
# Fri, 08 Sep 2017 17:05:10 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Fri, 08 Sep 2017 17:05:10 GMT
ENV YARN_VERSION=0.27.5
# Fri, 08 Sep 2017 17:05:11 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Fri, 08 Sep 2017 17:05:12 GMT
CMD ["node"]
# Fri, 08 Sep 2017 18:17:08 GMT
ENV GOSU_VERSION=1.10
# Fri, 08 Sep 2017 18:17:11 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Fri, 08 Sep 2017 18:17:11 GMT
ENV NPM_CONFIG_LOGLEVEL=warn
# Fri, 08 Sep 2017 18:17:11 GMT
ENV NODE_ENV=production
# Fri, 08 Sep 2017 18:17:11 GMT
ENV GHOST_CLI_VERSION=1.1.1
# Sat, 30 Sep 2017 14:22:24 GMT
ENV GHOST_VERSION=1.10.0
# Sat, 30 Sep 2017 14:23:02 GMT
RUN npm install -g "ghost-cli@$GHOST_CLI_VERSION" knex-migrator@latest
# Sat, 30 Sep 2017 14:23:03 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 30 Sep 2017 14:23:03 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 30 Sep 2017 14:23:33 GMT
RUN set -ex; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"
# Sat, 30 Sep 2017 14:23:35 GMT
WORKDIR /var/lib/ghost
# Sat, 30 Sep 2017 14:23:35 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 30 Sep 2017 14:23:35 GMT
COPY file:ef6da72f41bc8f60c42fab63c9c2ffdee82253c6dd2110e3d50866e5445df15e in /usr/local/bin 
# Sat, 30 Sep 2017 14:23:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 30 Sep 2017 14:23:35 GMT
EXPOSE 2368/tcp
# Sat, 30 Sep 2017 14:23:36 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:5f39dbffcd07e3254246d3c2e4b3532c3697ed04f83eadf5433da820098787df`  
		Last Modified: Fri, 08 Sep 2017 05:24:42 GMT  
		Size: 52.8 MB (52788802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5a344275c5d5a12a16990e9ddb7cfb9bc9b793cc51fbf8bf8993426e287c27`  
		Last Modified: Fri, 08 Sep 2017 16:41:52 GMT  
		Size: 19.5 MB (19470373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c81355314e654fd3d4e1dcbec2f82fffb19b856e65aa403cf7b2d471582658`  
		Last Modified: Fri, 08 Sep 2017 17:05:56 GMT  
		Size: 4.4 KB (4411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9c66bc4cf9f13c8d89cb57f07ce23693a1efcbbbcc32e7e30c5e8e0cefa2c8`  
		Last Modified: Fri, 08 Sep 2017 17:05:56 GMT  
		Size: 119.1 KB (119148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa1121a725f9b59e0fcd0c6226075d97e638b15fdfc40f5e1d57d3a5f3c3f190`  
		Last Modified: Fri, 08 Sep 2017 17:07:00 GMT  
		Size: 14.8 MB (14847789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa31e4823df3a66473b6ca7286cf7a152288b868f3cf1d4df5eb0393f5e81da`  
		Last Modified: Fri, 08 Sep 2017 17:06:56 GMT  
		Size: 938.5 KB (938452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6819f9496d60b6b7dda2b89e7dd5c2a3c3442d0f1270b9f67b3c132f70fbeeb`  
		Last Modified: Fri, 08 Sep 2017 18:20:31 GMT  
		Size: 486.8 KB (486823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a59f71a40f843fc869ea2674c548cd5437531fbfa4cad604ba97432de4c3662`  
		Last Modified: Sat, 30 Sep 2017 14:23:59 GMT  
		Size: 29.2 MB (29166808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0eef1dc513aa74c3750bd41d13dbfd1576d9333340f889213b7d62aaeae7737`  
		Last Modified: Sat, 30 Sep 2017 14:24:10 GMT  
		Size: 89.8 MB (89841405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9fda95fa7073acebbc9f0b203e74fe5e7d92fde0d6097b30ce415370f804ee`  
		Last Modified: Sat, 30 Sep 2017 14:23:52 GMT  
		Size: 573.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:1.10.0`

```console
$ docker pull ghost@sha256:d446bb82e91ed5d33204c5a9c691d96165fb39ff62789090a15e0e4d5b6beb71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ghost:1.10.0` - linux; amd64

```console
$ docker pull ghost@sha256:d44b2a32948ec5ce91c7f50b28a51c35d4b77a831ca5410de669faae1161554d
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.0 MB (216993763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffcb039c6423f48dbd4cbc193990fc3e2dac3f7ce7d4043efb3cab571381de9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 13 Sep 2017 08:40:43 GMT
ADD file:d7333b3e0bc6479d2faed32e06d85f1975e5b23e13e75555aeed0f639770413b in / 
# Wed, 13 Sep 2017 08:40:43 GMT
CMD ["bash"]
# Wed, 13 Sep 2017 12:32:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Sep 2017 12:32:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Sep 2017 20:23:45 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 13 Sep 2017 20:23:48 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done
# Wed, 13 Sep 2017 20:23:48 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Wed, 13 Sep 2017 20:38:03 GMT
ENV NODE_VERSION=6.11.3
# Wed, 13 Sep 2017 20:38:26 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Wed, 13 Sep 2017 20:38:26 GMT
ENV YARN_VERSION=0.27.5
# Wed, 13 Sep 2017 20:38:30 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Wed, 13 Sep 2017 20:38:30 GMT
CMD ["node"]
# Wed, 13 Sep 2017 21:10:30 GMT
ENV GOSU_VERSION=1.10
# Wed, 13 Sep 2017 21:10:35 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Wed, 13 Sep 2017 21:10:35 GMT
ENV NPM_CONFIG_LOGLEVEL=warn
# Wed, 13 Sep 2017 21:10:35 GMT
ENV NODE_ENV=production
# Wed, 13 Sep 2017 21:10:35 GMT
ENV GHOST_CLI_VERSION=1.1.1
# Fri, 29 Sep 2017 22:33:33 GMT
ENV GHOST_VERSION=1.10.0
# Fri, 29 Sep 2017 22:34:08 GMT
RUN npm install -g "ghost-cli@$GHOST_CLI_VERSION" knex-migrator@latest
# Fri, 29 Sep 2017 22:34:09 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 29 Sep 2017 22:34:09 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 29 Sep 2017 22:34:42 GMT
RUN set -ex; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"
# Fri, 29 Sep 2017 22:34:43 GMT
WORKDIR /var/lib/ghost
# Fri, 29 Sep 2017 22:34:44 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 29 Sep 2017 22:34:44 GMT
COPY file:ef6da72f41bc8f60c42fab63c9c2ffdee82253c6dd2110e3d50866e5445df15e in /usr/local/bin 
# Fri, 29 Sep 2017 22:34:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Sep 2017 22:34:44 GMT
EXPOSE 2368/tcp
# Fri, 29 Sep 2017 22:34:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:aa18ad1a0d334d80981104c599fa8cef9264552a265b1197af11274beba767cf`  
		Last Modified: Thu, 07 Sep 2017 23:11:06 GMT  
		Size: 52.6 MB (52595547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a33158a1367c7c4103c89ae66e8f4fdec4ada6a39d4648cf254b32296d6668`  
		Last Modified: Wed, 13 Sep 2017 12:54:21 GMT  
		Size: 19.3 MB (19263717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e2ecbdc66945a5816aa0d37501c34fe6ae76d1664a47cd366604f68a557052`  
		Last Modified: Wed, 13 Sep 2017 20:49:04 GMT  
		Size: 4.4 KB (4406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba36da051a26db65f69c7538041ed3bf4d545ba973e1763029ba67ea44b99ef`  
		Last Modified: Wed, 13 Sep 2017 20:49:04 GMT  
		Size: 119.2 KB (119152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83260829fd758c7ed96bf6b66af7a83c16afb34bd20fea7c30627caa474c19e0`  
		Last Modified: Wed, 13 Sep 2017 20:51:45 GMT  
		Size: 14.7 MB (14718405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7459ed23b0dbcdf1adf35d3c09d1104dfce1711690a871cb7fea376fdeea9176`  
		Last Modified: Wed, 13 Sep 2017 20:51:40 GMT  
		Size: 938.5 KB (938460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed248cbe68e68af79ca31d36052e903e9bce24bac602f71d2d8ee4a9bc3676a1`  
		Last Modified: Wed, 13 Sep 2017 21:17:36 GMT  
		Size: 500.7 KB (500669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d1e6583f2f4dc6499d66c22f938d5d66fced54f990d20271ab036a86fe0cbc`  
		Last Modified: Fri, 29 Sep 2017 22:42:07 GMT  
		Size: 34.4 MB (34373399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3f41a3555b3208a268885077ed506c02f4da1f3b4a815d7028bad80dcea546`  
		Last Modified: Fri, 29 Sep 2017 22:42:32 GMT  
		Size: 94.5 MB (94479434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e58a823622c8980387093b393ee3ec8b406ee36a079cc10da539b0471f4e2a3`  
		Last Modified: Fri, 29 Sep 2017 22:41:36 GMT  
		Size: 574.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:1.10.0` - linux; arm variant v7

```console
$ docker pull ghost@sha256:24db28a9250caead11744a7d1944be9a2c36652c03b014abaed2f286fca94def
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.4 MB (201351870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7be5bcccf373c0e3287bbc7b2a27655d28f6662151e103ade060f108074abab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 27 Sep 2017 04:12:21 GMT
ADD file:ef59ce7fe68882b1b44bc3c4a5e9e465561cb257fb63f8c2b3c247abb012486b in / 
# Wed, 27 Sep 2017 04:12:22 GMT
CMD ["bash"]
# Wed, 27 Sep 2017 04:39:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 27 Sep 2017 04:39:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 27 Sep 2017 07:03:35 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 27 Sep 2017 07:07:47 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done
# Wed, 27 Sep 2017 07:07:48 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Wed, 27 Sep 2017 07:17:28 GMT
ENV NODE_VERSION=6.11.3
# Wed, 27 Sep 2017 07:18:06 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Wed, 27 Sep 2017 07:18:08 GMT
ENV YARN_VERSION=0.27.5
# Wed, 27 Sep 2017 07:18:10 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Wed, 27 Sep 2017 07:18:10 GMT
CMD ["node"]
# Wed, 27 Sep 2017 07:58:52 GMT
ENV GOSU_VERSION=1.10
# Wed, 27 Sep 2017 07:58:54 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Wed, 27 Sep 2017 07:58:54 GMT
ENV NPM_CONFIG_LOGLEVEL=warn
# Wed, 27 Sep 2017 07:58:54 GMT
ENV NODE_ENV=production
# Wed, 27 Sep 2017 07:58:54 GMT
ENV GHOST_CLI_VERSION=1.1.1
# Sat, 30 Sep 2017 11:55:22 GMT
ENV GHOST_VERSION=1.10.0
# Sat, 30 Sep 2017 11:56:35 GMT
RUN npm install -g "ghost-cli@$GHOST_CLI_VERSION" knex-migrator@latest
# Sat, 30 Sep 2017 11:56:36 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 30 Sep 2017 11:56:37 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 30 Sep 2017 11:57:49 GMT
RUN set -ex; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"
# Sat, 30 Sep 2017 11:57:52 GMT
WORKDIR /var/lib/ghost
# Sat, 30 Sep 2017 11:57:52 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 30 Sep 2017 11:57:52 GMT
COPY file:ef6da72f41bc8f60c42fab63c9c2ffdee82253c6dd2110e3d50866e5445df15e in /usr/local/bin 
# Sat, 30 Sep 2017 11:57:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 30 Sep 2017 11:57:53 GMT
EXPOSE 2368/tcp
# Sat, 30 Sep 2017 11:57:53 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:8c7b63aa62f92f5be1e93e5129c5c99dac397c6d3b5f6c6452bfd0905f6f20be`  
		Last Modified: Wed, 27 Sep 2017 04:17:18 GMT  
		Size: 48.7 MB (48686544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a607bd01ffd678134d1281825ba8fafc069965446932fb3da991e8e6c2d3065d`  
		Last Modified: Wed, 27 Sep 2017 04:58:12 GMT  
		Size: 18.3 MB (18262468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7733b25f61410d8e74ee676e195c358ac6519ef39f1a92f3cd11c5f8ca2048`  
		Last Modified: Wed, 27 Sep 2017 07:20:36 GMT  
		Size: 4.4 KB (4420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553903f3bafddd9019242ebd76c10ae0ba04207db8e960c84758e8762b1c4cca`  
		Last Modified: Wed, 27 Sep 2017 07:20:36 GMT  
		Size: 119.2 KB (119190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34bc7bac012caabb127f3461274a9a4cb95bde62751a07df9eb243be1e2877ad`  
		Last Modified: Wed, 27 Sep 2017 07:22:00 GMT  
		Size: 13.9 MB (13877719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c31b00c4993376f813ed323a451b7444b0f176979418ff061aa095b002377bc0`  
		Last Modified: Wed, 27 Sep 2017 07:21:55 GMT  
		Size: 940.2 KB (940161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:541588608a9db7c94840b658b4d597ff4903433af8b4e46a3b35d0d48ccfa330`  
		Last Modified: Wed, 27 Sep 2017 08:05:26 GMT  
		Size: 475.3 KB (475267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ee01efe1bc522be8f8abd8080bdd3708e66ec95ede0cb6a5d2e1a5a321caf51`  
		Last Modified: Sat, 30 Sep 2017 11:58:34 GMT  
		Size: 29.2 MB (29169178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d95b75a1bb347fc5d04c4ac95b89a21a27bb397e26275b5c126c561efb0947b`  
		Last Modified: Sat, 30 Sep 2017 11:58:58 GMT  
		Size: 89.8 MB (89816348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4681c19bb16c56ef451982b2084f48ac2ae91f8007c55a3259b7fd168ecc312f`  
		Last Modified: Sat, 30 Sep 2017 11:58:20 GMT  
		Size: 575.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:1.10.0` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:4778e6eafd796f96c4e3d279c18fc1a3dd030f32e215c2fe6150198baae84e90
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.9 MB (203937560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ce70e09282f3873bdcf8a71e0562634725e2269efe303c165537c15dabfbbbb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 08 Sep 2017 17:23:41 GMT
ADD file:9f576a63a5e03994904e585c35fbeef6a2c96c41d8f696705c033f3ca69b6a2b in / 
# Fri, 08 Sep 2017 17:23:42 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 18:32:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 18:32:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 Sep 2017 23:16:17 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 14 Sep 2017 23:16:22 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done
# Thu, 14 Sep 2017 23:16:24 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Thu, 14 Sep 2017 23:18:55 GMT
ENV NODE_VERSION=6.11.3
# Thu, 14 Sep 2017 23:19:28 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Thu, 14 Sep 2017 23:19:29 GMT
ENV YARN_VERSION=0.27.5
# Thu, 14 Sep 2017 23:19:35 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Thu, 14 Sep 2017 23:19:37 GMT
CMD ["node"]
# Fri, 15 Sep 2017 02:19:54 GMT
ENV GOSU_VERSION=1.10
# Fri, 15 Sep 2017 02:20:02 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Fri, 15 Sep 2017 02:20:03 GMT
ENV NPM_CONFIG_LOGLEVEL=warn
# Fri, 15 Sep 2017 02:20:04 GMT
ENV NODE_ENV=production
# Fri, 15 Sep 2017 02:20:05 GMT
ENV GHOST_CLI_VERSION=1.1.1
# Sat, 30 Sep 2017 10:41:33 GMT
ENV GHOST_VERSION=1.10.0
# Sat, 30 Sep 2017 10:43:52 GMT
RUN npm install -g "ghost-cli@$GHOST_CLI_VERSION" knex-migrator@latest
# Sat, 30 Sep 2017 10:43:54 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 30 Sep 2017 10:43:55 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 30 Sep 2017 10:45:38 GMT
RUN set -ex; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"
# Sat, 30 Sep 2017 10:45:42 GMT
WORKDIR /var/lib/ghost
# Sat, 30 Sep 2017 10:45:42 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 30 Sep 2017 10:45:43 GMT
COPY file:ef6da72f41bc8f60c42fab63c9c2ffdee82253c6dd2110e3d50866e5445df15e in /usr/local/bin 
# Sat, 30 Sep 2017 10:45:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 30 Sep 2017 10:45:45 GMT
EXPOSE 2368/tcp
# Sat, 30 Sep 2017 10:45:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:e91a355b0d3ff86add037a3f24718b760d8eb3f346f998e5116375ddce9eae19`  
		Last Modified: Fri, 08 Sep 2017 17:34:56 GMT  
		Size: 49.9 MB (49929457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e054bfb02234c6e2b5305981d365c3b31101ec460b0d90df3b099305c03196`  
		Last Modified: Thu, 14 Sep 2017 22:01:15 GMT  
		Size: 18.7 MB (18737603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68cbb48bf959f44cbc4806f42587333e86631edab819261ca51eba1da6fcd637`  
		Last Modified: Thu, 14 Sep 2017 23:24:36 GMT  
		Size: 4.4 KB (4417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e961bd22aace0af8a10a14a5d6282014bdb3cf7c4d5b42e16a0dd45e4cd06dac`  
		Last Modified: Thu, 14 Sep 2017 23:24:36 GMT  
		Size: 119.2 KB (119150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:280e0b3e39cb221ce8de69ec6e8d5e99fd9761fc3a6d37cbd9086ad72d3b41dc`  
		Last Modified: Thu, 14 Sep 2017 23:27:52 GMT  
		Size: 14.7 MB (14707206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e714752cefed2ff3be3734c49f1a880303ff6290d0705230e5f486a0a0bbe756`  
		Last Modified: Thu, 14 Sep 2017 23:27:45 GMT  
		Size: 940.1 KB (940132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de4bc9133bf690ef04927a67017f86cc9e619e51f7cac9262ff9165db6baefc`  
		Last Modified: Fri, 15 Sep 2017 02:35:50 GMT  
		Size: 468.7 KB (468701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d7bd10a95781c324562ce9f74235c7ef17ba5265033caafb028f240912114a`  
		Last Modified: Sat, 30 Sep 2017 10:46:26 GMT  
		Size: 29.2 MB (29168766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82c35004fc2685c10e031b4e39e97503ed72b418850306ead8ad0a25f0112976`  
		Last Modified: Sat, 30 Sep 2017 10:46:48 GMT  
		Size: 89.9 MB (89861555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd20cd50f4050f013e3109e93315f76c9c378d8d8acad7e5140112cacb55f835`  
		Last Modified: Sat, 30 Sep 2017 10:46:11 GMT  
		Size: 573.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:1.10.0` - linux; ppc64le

```console
$ docker pull ghost@sha256:5519b5f58af430a845cfb4617430d530fc69b279353a2b41883793c949d79537
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.1 MB (206070261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf606d1107cf8f7551b5f5dff21b1769766e0d07f6e2decbeafacb2446180d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 08 Sep 2017 00:32:21 GMT
ADD file:483b3245941140ac32394a804364a1a9bd5dfdf1b4475238b61068cc7252ac08 in / 
# Fri, 08 Sep 2017 00:32:21 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 01:03:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 01:03:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 Sep 2017 23:10:48 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 14 Sep 2017 23:11:08 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done
# Thu, 14 Sep 2017 23:11:12 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Thu, 14 Sep 2017 23:15:42 GMT
ENV NODE_VERSION=6.11.3
# Thu, 14 Sep 2017 23:16:32 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Thu, 14 Sep 2017 23:16:41 GMT
ENV YARN_VERSION=0.27.5
# Thu, 14 Sep 2017 23:16:48 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Thu, 14 Sep 2017 23:16:50 GMT
CMD ["node"]
# Fri, 15 Sep 2017 02:22:38 GMT
ENV GOSU_VERSION=1.10
# Fri, 15 Sep 2017 02:22:46 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Fri, 15 Sep 2017 02:22:48 GMT
ENV NPM_CONFIG_LOGLEVEL=warn
# Fri, 15 Sep 2017 02:22:52 GMT
ENV NODE_ENV=production
# Fri, 15 Sep 2017 02:22:54 GMT
ENV GHOST_CLI_VERSION=1.1.1
# Sat, 30 Sep 2017 01:26:24 GMT
ENV GHOST_VERSION=1.10.0
# Sat, 30 Sep 2017 01:27:21 GMT
RUN npm install -g "ghost-cli@$GHOST_CLI_VERSION" knex-migrator@latest
# Sat, 30 Sep 2017 01:27:28 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 30 Sep 2017 01:27:30 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 30 Sep 2017 01:28:37 GMT
RUN set -ex; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"
# Sat, 30 Sep 2017 01:28:44 GMT
WORKDIR /var/lib/ghost
# Sat, 30 Sep 2017 01:28:48 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 30 Sep 2017 01:28:50 GMT
COPY file:ef6da72f41bc8f60c42fab63c9c2ffdee82253c6dd2110e3d50866e5445df15e in /usr/local/bin 
# Sat, 30 Sep 2017 01:28:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 30 Sep 2017 01:28:55 GMT
EXPOSE 2368/tcp
# Sat, 30 Sep 2017 01:28:58 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d4a5434e09b7ac8431060d347d6ef1233ae07514878fb2aff4085bcf441c29f3`  
		Last Modified: Fri, 08 Sep 2017 00:36:52 GMT  
		Size: 51.8 MB (51809570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48596af2c38701f94440e222bf8f3d4b2da85e2982c97ae15186eba523249e0b`  
		Last Modified: Thu, 14 Sep 2017 22:21:02 GMT  
		Size: 19.2 MB (19199596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1dc276f5b0bc12cddaf889657d8ed9d7ec3e6add07506308ea49dc52bb6eff`  
		Last Modified: Thu, 14 Sep 2017 23:22:38 GMT  
		Size: 4.4 KB (4444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb57f53562fb9db3e40e7ee479f5526f635b724a0632d9a4d3da2500a44c491d`  
		Last Modified: Thu, 14 Sep 2017 23:22:39 GMT  
		Size: 119.2 KB (119184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f255065ee2535a6b44019881cc1954c1a7f665f6b0c530c618663be94e4a23`  
		Last Modified: Thu, 14 Sep 2017 23:26:37 GMT  
		Size: 14.5 MB (14475182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68be6ded470a2cf42b2ccda178f212a25198e102a4e3249456140252fa22f054`  
		Last Modified: Thu, 14 Sep 2017 23:26:32 GMT  
		Size: 940.2 KB (940157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad1d6527d8ade34c5efd2bd98f7a049a917ff22859c6eaaed4046a2df232d91b`  
		Last Modified: Fri, 15 Sep 2017 02:32:57 GMT  
		Size: 469.9 KB (469852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f814a9bc90f3c846324f0952f0ae962140c6c3eaedd3e91eebd25f20d56bcc06`  
		Last Modified: Sat, 30 Sep 2017 01:29:27 GMT  
		Size: 29.2 MB (29167447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd14b03e56a10a52bb6decdf699c7db5c4446ff682043ec05c46042069ac5e6`  
		Last Modified: Sat, 30 Sep 2017 01:29:45 GMT  
		Size: 89.9 MB (89884255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b4c1125e28a6f6aaf1a9849d51d4724cd2372100162880dc826bfe2cf89a5b`  
		Last Modified: Sat, 30 Sep 2017 01:29:17 GMT  
		Size: 574.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:1.10.0` - linux; s390x

```console
$ docker pull ghost@sha256:d64cf4c152b1cab609af105e32edb33313e29d8f13cf68ca7e057d980c2c8cc2
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207664584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce7ab8a934452910b724a2dbbdd3229e252349593a2327814139278d378072c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 08 Sep 2017 05:21:42 GMT
ADD file:996e52a941b7162fafcf761c415142a34a2fc703e21d2f264b824373e9fa4b1e in / 
# Fri, 08 Sep 2017 05:21:43 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 05:48:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 05:48:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 08 Sep 2017 17:04:11 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Fri, 08 Sep 2017 17:04:12 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done
# Fri, 08 Sep 2017 17:04:12 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Fri, 08 Sep 2017 17:04:55 GMT
ENV NODE_VERSION=6.11.3
# Fri, 08 Sep 2017 17:05:10 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Fri, 08 Sep 2017 17:05:10 GMT
ENV YARN_VERSION=0.27.5
# Fri, 08 Sep 2017 17:05:11 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Fri, 08 Sep 2017 17:05:12 GMT
CMD ["node"]
# Fri, 08 Sep 2017 18:17:08 GMT
ENV GOSU_VERSION=1.10
# Fri, 08 Sep 2017 18:17:11 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Fri, 08 Sep 2017 18:17:11 GMT
ENV NPM_CONFIG_LOGLEVEL=warn
# Fri, 08 Sep 2017 18:17:11 GMT
ENV NODE_ENV=production
# Fri, 08 Sep 2017 18:17:11 GMT
ENV GHOST_CLI_VERSION=1.1.1
# Sat, 30 Sep 2017 14:22:24 GMT
ENV GHOST_VERSION=1.10.0
# Sat, 30 Sep 2017 14:23:02 GMT
RUN npm install -g "ghost-cli@$GHOST_CLI_VERSION" knex-migrator@latest
# Sat, 30 Sep 2017 14:23:03 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 30 Sep 2017 14:23:03 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 30 Sep 2017 14:23:33 GMT
RUN set -ex; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"
# Sat, 30 Sep 2017 14:23:35 GMT
WORKDIR /var/lib/ghost
# Sat, 30 Sep 2017 14:23:35 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 30 Sep 2017 14:23:35 GMT
COPY file:ef6da72f41bc8f60c42fab63c9c2ffdee82253c6dd2110e3d50866e5445df15e in /usr/local/bin 
# Sat, 30 Sep 2017 14:23:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 30 Sep 2017 14:23:35 GMT
EXPOSE 2368/tcp
# Sat, 30 Sep 2017 14:23:36 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:5f39dbffcd07e3254246d3c2e4b3532c3697ed04f83eadf5433da820098787df`  
		Last Modified: Fri, 08 Sep 2017 05:24:42 GMT  
		Size: 52.8 MB (52788802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5a344275c5d5a12a16990e9ddb7cfb9bc9b793cc51fbf8bf8993426e287c27`  
		Last Modified: Fri, 08 Sep 2017 16:41:52 GMT  
		Size: 19.5 MB (19470373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c81355314e654fd3d4e1dcbec2f82fffb19b856e65aa403cf7b2d471582658`  
		Last Modified: Fri, 08 Sep 2017 17:05:56 GMT  
		Size: 4.4 KB (4411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9c66bc4cf9f13c8d89cb57f07ce23693a1efcbbbcc32e7e30c5e8e0cefa2c8`  
		Last Modified: Fri, 08 Sep 2017 17:05:56 GMT  
		Size: 119.1 KB (119148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa1121a725f9b59e0fcd0c6226075d97e638b15fdfc40f5e1d57d3a5f3c3f190`  
		Last Modified: Fri, 08 Sep 2017 17:07:00 GMT  
		Size: 14.8 MB (14847789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa31e4823df3a66473b6ca7286cf7a152288b868f3cf1d4df5eb0393f5e81da`  
		Last Modified: Fri, 08 Sep 2017 17:06:56 GMT  
		Size: 938.5 KB (938452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6819f9496d60b6b7dda2b89e7dd5c2a3c3442d0f1270b9f67b3c132f70fbeeb`  
		Last Modified: Fri, 08 Sep 2017 18:20:31 GMT  
		Size: 486.8 KB (486823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a59f71a40f843fc869ea2674c548cd5437531fbfa4cad604ba97432de4c3662`  
		Last Modified: Sat, 30 Sep 2017 14:23:59 GMT  
		Size: 29.2 MB (29166808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0eef1dc513aa74c3750bd41d13dbfd1576d9333340f889213b7d62aaeae7737`  
		Last Modified: Sat, 30 Sep 2017 14:24:10 GMT  
		Size: 89.8 MB (89841405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9fda95fa7073acebbc9f0b203e74fe5e7d92fde0d6097b30ce415370f804ee`  
		Last Modified: Sat, 30 Sep 2017 14:23:52 GMT  
		Size: 573.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:1.10.0-alpine`

```console
$ docker pull ghost@sha256:b7c4fcb9e78518ea85fcba80969f445301b38f76833a6668eb268da7b6e7f3a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `ghost:1.10.0-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:80cc0530d07e3d8e03453e71f31ef1342d82e075c35de047da4ca655d16ed7b3
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148723683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:125d9b4f2bcd666d226ddf7738a52a2e3478d5978409812c8e03b30123b7c5aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 13 Sep 2017 14:32:15 GMT
ADD file:89e72bfc19e81624ba6a34bd5cecdf258750dc569ba03e17e3f4a286b1526461 in / 
# Wed, 13 Sep 2017 14:32:15 GMT
CMD ["/bin/sh"]
# Wed, 13 Sep 2017 20:24:57 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Wed, 13 Sep 2017 20:24:58 GMT
ENV NODE_VERSION=6.11.3
# Wed, 13 Sep 2017 20:36:42 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         binutils-gold         curl         g++         gcc         gnupg         libgcc         linux-headers         make         python   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN)     && make install     && apk del .build-deps     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt
# Wed, 13 Sep 2017 20:36:42 GMT
ENV YARN_VERSION=0.27.5
# Wed, 13 Sep 2017 20:36:50 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Wed, 13 Sep 2017 20:36:50 GMT
CMD ["node"]
# Wed, 13 Sep 2017 21:13:34 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 13 Sep 2017 21:13:38 GMT
RUN apk add --no-cache 		bash
# Wed, 13 Sep 2017 21:13:39 GMT
ENV NPM_CONFIG_LOGLEVEL=warn
# Wed, 13 Sep 2017 21:13:39 GMT
ENV NODE_ENV=production
# Wed, 13 Sep 2017 21:13:40 GMT
ENV GHOST_CLI_VERSION=1.1.1
# Fri, 29 Sep 2017 22:38:06 GMT
ENV GHOST_VERSION=1.10.0
# Fri, 29 Sep 2017 22:38:44 GMT
RUN npm install -g "ghost-cli@$GHOST_CLI_VERSION" knex-migrator@latest
# Fri, 29 Sep 2017 22:38:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 29 Sep 2017 22:38:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 29 Sep 2017 22:39:18 GMT
RUN set -ex; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"
# Fri, 29 Sep 2017 22:39:19 GMT
WORKDIR /var/lib/ghost
# Fri, 29 Sep 2017 22:39:19 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 29 Sep 2017 22:39:19 GMT
COPY file:fe4f8ce065580d78daf2ea3ae3ab9174f3edd7740df8b95889926dc1cdfe77b0 in /usr/local/bin 
# Fri, 29 Sep 2017 22:39:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Sep 2017 22:39:20 GMT
EXPOSE 2368/tcp
# Fri, 29 Sep 2017 22:39:20 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:90f4dba627d65ea3223761bcfe54e726337a919fe98117ef107914f91be657c9`  
		Last Modified: Tue, 27 Jun 2017 18:47:56 GMT  
		Size: 2.4 MB (2385007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c02e9bd0b129afc373209e2498ba6bd7157164b4a96de677a2e1224527558e3d`  
		Last Modified: Wed, 13 Sep 2017 20:51:01 GMT  
		Size: 15.4 MB (15438807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae02bb9be1084245b51165da53a51c16267d437758238436108e38b62ee73c83`  
		Last Modified: Wed, 13 Sep 2017 20:50:56 GMT  
		Size: 945.5 KB (945482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670dd55024c52593c29fd34bf9e31b4442960627d5c074537ddb43b44c801685`  
		Last Modified: Wed, 13 Sep 2017 21:19:03 GMT  
		Size: 8.4 KB (8367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28bea52f21d15abf9efa81d6d421474f05454334c0b6f6d271b714f31d813ba4`  
		Last Modified: Wed, 13 Sep 2017 21:19:06 GMT  
		Size: 1.1 MB (1095613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9c2681f66adc3c8d26aa113921eeebea088307d02a9daaccd90525bf120630`  
		Last Modified: Fri, 29 Sep 2017 22:43:35 GMT  
		Size: 34.4 MB (34373107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77932bf3c0a49a1869f04c91c580e6ee178d0995c7025278e9fcc0bc6dad6a1`  
		Last Modified: Fri, 29 Sep 2017 22:43:54 GMT  
		Size: 94.5 MB (94476740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:785d252b4a267634c87200cf08c7c95793f401311c07d24ff262f244eae1bd44`  
		Last Modified: Fri, 29 Sep 2017 22:43:02 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:1.10-alpine`

```console
$ docker pull ghost@sha256:b7c4fcb9e78518ea85fcba80969f445301b38f76833a6668eb268da7b6e7f3a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `ghost:1.10-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:80cc0530d07e3d8e03453e71f31ef1342d82e075c35de047da4ca655d16ed7b3
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148723683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:125d9b4f2bcd666d226ddf7738a52a2e3478d5978409812c8e03b30123b7c5aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 13 Sep 2017 14:32:15 GMT
ADD file:89e72bfc19e81624ba6a34bd5cecdf258750dc569ba03e17e3f4a286b1526461 in / 
# Wed, 13 Sep 2017 14:32:15 GMT
CMD ["/bin/sh"]
# Wed, 13 Sep 2017 20:24:57 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Wed, 13 Sep 2017 20:24:58 GMT
ENV NODE_VERSION=6.11.3
# Wed, 13 Sep 2017 20:36:42 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         binutils-gold         curl         g++         gcc         gnupg         libgcc         linux-headers         make         python   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN)     && make install     && apk del .build-deps     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt
# Wed, 13 Sep 2017 20:36:42 GMT
ENV YARN_VERSION=0.27.5
# Wed, 13 Sep 2017 20:36:50 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Wed, 13 Sep 2017 20:36:50 GMT
CMD ["node"]
# Wed, 13 Sep 2017 21:13:34 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 13 Sep 2017 21:13:38 GMT
RUN apk add --no-cache 		bash
# Wed, 13 Sep 2017 21:13:39 GMT
ENV NPM_CONFIG_LOGLEVEL=warn
# Wed, 13 Sep 2017 21:13:39 GMT
ENV NODE_ENV=production
# Wed, 13 Sep 2017 21:13:40 GMT
ENV GHOST_CLI_VERSION=1.1.1
# Fri, 29 Sep 2017 22:38:06 GMT
ENV GHOST_VERSION=1.10.0
# Fri, 29 Sep 2017 22:38:44 GMT
RUN npm install -g "ghost-cli@$GHOST_CLI_VERSION" knex-migrator@latest
# Fri, 29 Sep 2017 22:38:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 29 Sep 2017 22:38:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 29 Sep 2017 22:39:18 GMT
RUN set -ex; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"
# Fri, 29 Sep 2017 22:39:19 GMT
WORKDIR /var/lib/ghost
# Fri, 29 Sep 2017 22:39:19 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 29 Sep 2017 22:39:19 GMT
COPY file:fe4f8ce065580d78daf2ea3ae3ab9174f3edd7740df8b95889926dc1cdfe77b0 in /usr/local/bin 
# Fri, 29 Sep 2017 22:39:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Sep 2017 22:39:20 GMT
EXPOSE 2368/tcp
# Fri, 29 Sep 2017 22:39:20 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:90f4dba627d65ea3223761bcfe54e726337a919fe98117ef107914f91be657c9`  
		Last Modified: Tue, 27 Jun 2017 18:47:56 GMT  
		Size: 2.4 MB (2385007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c02e9bd0b129afc373209e2498ba6bd7157164b4a96de677a2e1224527558e3d`  
		Last Modified: Wed, 13 Sep 2017 20:51:01 GMT  
		Size: 15.4 MB (15438807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae02bb9be1084245b51165da53a51c16267d437758238436108e38b62ee73c83`  
		Last Modified: Wed, 13 Sep 2017 20:50:56 GMT  
		Size: 945.5 KB (945482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670dd55024c52593c29fd34bf9e31b4442960627d5c074537ddb43b44c801685`  
		Last Modified: Wed, 13 Sep 2017 21:19:03 GMT  
		Size: 8.4 KB (8367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28bea52f21d15abf9efa81d6d421474f05454334c0b6f6d271b714f31d813ba4`  
		Last Modified: Wed, 13 Sep 2017 21:19:06 GMT  
		Size: 1.1 MB (1095613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9c2681f66adc3c8d26aa113921eeebea088307d02a9daaccd90525bf120630`  
		Last Modified: Fri, 29 Sep 2017 22:43:35 GMT  
		Size: 34.4 MB (34373107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77932bf3c0a49a1869f04c91c580e6ee178d0995c7025278e9fcc0bc6dad6a1`  
		Last Modified: Fri, 29 Sep 2017 22:43:54 GMT  
		Size: 94.5 MB (94476740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:785d252b4a267634c87200cf08c7c95793f401311c07d24ff262f244eae1bd44`  
		Last Modified: Fri, 29 Sep 2017 22:43:02 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:1-alpine`

```console
$ docker pull ghost@sha256:b7c4fcb9e78518ea85fcba80969f445301b38f76833a6668eb268da7b6e7f3a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `ghost:1-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:80cc0530d07e3d8e03453e71f31ef1342d82e075c35de047da4ca655d16ed7b3
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148723683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:125d9b4f2bcd666d226ddf7738a52a2e3478d5978409812c8e03b30123b7c5aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 13 Sep 2017 14:32:15 GMT
ADD file:89e72bfc19e81624ba6a34bd5cecdf258750dc569ba03e17e3f4a286b1526461 in / 
# Wed, 13 Sep 2017 14:32:15 GMT
CMD ["/bin/sh"]
# Wed, 13 Sep 2017 20:24:57 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Wed, 13 Sep 2017 20:24:58 GMT
ENV NODE_VERSION=6.11.3
# Wed, 13 Sep 2017 20:36:42 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         binutils-gold         curl         g++         gcc         gnupg         libgcc         linux-headers         make         python   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN)     && make install     && apk del .build-deps     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt
# Wed, 13 Sep 2017 20:36:42 GMT
ENV YARN_VERSION=0.27.5
# Wed, 13 Sep 2017 20:36:50 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Wed, 13 Sep 2017 20:36:50 GMT
CMD ["node"]
# Wed, 13 Sep 2017 21:13:34 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 13 Sep 2017 21:13:38 GMT
RUN apk add --no-cache 		bash
# Wed, 13 Sep 2017 21:13:39 GMT
ENV NPM_CONFIG_LOGLEVEL=warn
# Wed, 13 Sep 2017 21:13:39 GMT
ENV NODE_ENV=production
# Wed, 13 Sep 2017 21:13:40 GMT
ENV GHOST_CLI_VERSION=1.1.1
# Fri, 29 Sep 2017 22:38:06 GMT
ENV GHOST_VERSION=1.10.0
# Fri, 29 Sep 2017 22:38:44 GMT
RUN npm install -g "ghost-cli@$GHOST_CLI_VERSION" knex-migrator@latest
# Fri, 29 Sep 2017 22:38:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 29 Sep 2017 22:38:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 29 Sep 2017 22:39:18 GMT
RUN set -ex; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"
# Fri, 29 Sep 2017 22:39:19 GMT
WORKDIR /var/lib/ghost
# Fri, 29 Sep 2017 22:39:19 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 29 Sep 2017 22:39:19 GMT
COPY file:fe4f8ce065580d78daf2ea3ae3ab9174f3edd7740df8b95889926dc1cdfe77b0 in /usr/local/bin 
# Fri, 29 Sep 2017 22:39:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Sep 2017 22:39:20 GMT
EXPOSE 2368/tcp
# Fri, 29 Sep 2017 22:39:20 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:90f4dba627d65ea3223761bcfe54e726337a919fe98117ef107914f91be657c9`  
		Last Modified: Tue, 27 Jun 2017 18:47:56 GMT  
		Size: 2.4 MB (2385007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c02e9bd0b129afc373209e2498ba6bd7157164b4a96de677a2e1224527558e3d`  
		Last Modified: Wed, 13 Sep 2017 20:51:01 GMT  
		Size: 15.4 MB (15438807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae02bb9be1084245b51165da53a51c16267d437758238436108e38b62ee73c83`  
		Last Modified: Wed, 13 Sep 2017 20:50:56 GMT  
		Size: 945.5 KB (945482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670dd55024c52593c29fd34bf9e31b4442960627d5c074537ddb43b44c801685`  
		Last Modified: Wed, 13 Sep 2017 21:19:03 GMT  
		Size: 8.4 KB (8367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28bea52f21d15abf9efa81d6d421474f05454334c0b6f6d271b714f31d813ba4`  
		Last Modified: Wed, 13 Sep 2017 21:19:06 GMT  
		Size: 1.1 MB (1095613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9c2681f66adc3c8d26aa113921eeebea088307d02a9daaccd90525bf120630`  
		Last Modified: Fri, 29 Sep 2017 22:43:35 GMT  
		Size: 34.4 MB (34373107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77932bf3c0a49a1869f04c91c580e6ee178d0995c7025278e9fcc0bc6dad6a1`  
		Last Modified: Fri, 29 Sep 2017 22:43:54 GMT  
		Size: 94.5 MB (94476740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:785d252b4a267634c87200cf08c7c95793f401311c07d24ff262f244eae1bd44`  
		Last Modified: Fri, 29 Sep 2017 22:43:02 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:alpine`

```console
$ docker pull ghost@sha256:b7c4fcb9e78518ea85fcba80969f445301b38f76833a6668eb268da7b6e7f3a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `ghost:alpine` - linux; amd64

```console
$ docker pull ghost@sha256:80cc0530d07e3d8e03453e71f31ef1342d82e075c35de047da4ca655d16ed7b3
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148723683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:125d9b4f2bcd666d226ddf7738a52a2e3478d5978409812c8e03b30123b7c5aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 13 Sep 2017 14:32:15 GMT
ADD file:89e72bfc19e81624ba6a34bd5cecdf258750dc569ba03e17e3f4a286b1526461 in / 
# Wed, 13 Sep 2017 14:32:15 GMT
CMD ["/bin/sh"]
# Wed, 13 Sep 2017 20:24:57 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Wed, 13 Sep 2017 20:24:58 GMT
ENV NODE_VERSION=6.11.3
# Wed, 13 Sep 2017 20:36:42 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         binutils-gold         curl         g++         gcc         gnupg         libgcc         linux-headers         make         python   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN)     && make install     && apk del .build-deps     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt
# Wed, 13 Sep 2017 20:36:42 GMT
ENV YARN_VERSION=0.27.5
# Wed, 13 Sep 2017 20:36:50 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Wed, 13 Sep 2017 20:36:50 GMT
CMD ["node"]
# Wed, 13 Sep 2017 21:13:34 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 13 Sep 2017 21:13:38 GMT
RUN apk add --no-cache 		bash
# Wed, 13 Sep 2017 21:13:39 GMT
ENV NPM_CONFIG_LOGLEVEL=warn
# Wed, 13 Sep 2017 21:13:39 GMT
ENV NODE_ENV=production
# Wed, 13 Sep 2017 21:13:40 GMT
ENV GHOST_CLI_VERSION=1.1.1
# Fri, 29 Sep 2017 22:38:06 GMT
ENV GHOST_VERSION=1.10.0
# Fri, 29 Sep 2017 22:38:44 GMT
RUN npm install -g "ghost-cli@$GHOST_CLI_VERSION" knex-migrator@latest
# Fri, 29 Sep 2017 22:38:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 29 Sep 2017 22:38:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 29 Sep 2017 22:39:18 GMT
RUN set -ex; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"
# Fri, 29 Sep 2017 22:39:19 GMT
WORKDIR /var/lib/ghost
# Fri, 29 Sep 2017 22:39:19 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 29 Sep 2017 22:39:19 GMT
COPY file:fe4f8ce065580d78daf2ea3ae3ab9174f3edd7740df8b95889926dc1cdfe77b0 in /usr/local/bin 
# Fri, 29 Sep 2017 22:39:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Sep 2017 22:39:20 GMT
EXPOSE 2368/tcp
# Fri, 29 Sep 2017 22:39:20 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:90f4dba627d65ea3223761bcfe54e726337a919fe98117ef107914f91be657c9`  
		Last Modified: Tue, 27 Jun 2017 18:47:56 GMT  
		Size: 2.4 MB (2385007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c02e9bd0b129afc373209e2498ba6bd7157164b4a96de677a2e1224527558e3d`  
		Last Modified: Wed, 13 Sep 2017 20:51:01 GMT  
		Size: 15.4 MB (15438807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae02bb9be1084245b51165da53a51c16267d437758238436108e38b62ee73c83`  
		Last Modified: Wed, 13 Sep 2017 20:50:56 GMT  
		Size: 945.5 KB (945482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670dd55024c52593c29fd34bf9e31b4442960627d5c074537ddb43b44c801685`  
		Last Modified: Wed, 13 Sep 2017 21:19:03 GMT  
		Size: 8.4 KB (8367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28bea52f21d15abf9efa81d6d421474f05454334c0b6f6d271b714f31d813ba4`  
		Last Modified: Wed, 13 Sep 2017 21:19:06 GMT  
		Size: 1.1 MB (1095613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9c2681f66adc3c8d26aa113921eeebea088307d02a9daaccd90525bf120630`  
		Last Modified: Fri, 29 Sep 2017 22:43:35 GMT  
		Size: 34.4 MB (34373107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77932bf3c0a49a1869f04c91c580e6ee178d0995c7025278e9fcc0bc6dad6a1`  
		Last Modified: Fri, 29 Sep 2017 22:43:54 GMT  
		Size: 94.5 MB (94476740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:785d252b4a267634c87200cf08c7c95793f401311c07d24ff262f244eae1bd44`  
		Last Modified: Fri, 29 Sep 2017 22:43:02 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:latest`

```console
$ docker pull ghost@sha256:d446bb82e91ed5d33204c5a9c691d96165fb39ff62789090a15e0e4d5b6beb71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ghost:latest` - linux; amd64

```console
$ docker pull ghost@sha256:d44b2a32948ec5ce91c7f50b28a51c35d4b77a831ca5410de669faae1161554d
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.0 MB (216993763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffcb039c6423f48dbd4cbc193990fc3e2dac3f7ce7d4043efb3cab571381de9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 13 Sep 2017 08:40:43 GMT
ADD file:d7333b3e0bc6479d2faed32e06d85f1975e5b23e13e75555aeed0f639770413b in / 
# Wed, 13 Sep 2017 08:40:43 GMT
CMD ["bash"]
# Wed, 13 Sep 2017 12:32:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Sep 2017 12:32:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Sep 2017 20:23:45 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 13 Sep 2017 20:23:48 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done
# Wed, 13 Sep 2017 20:23:48 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Wed, 13 Sep 2017 20:38:03 GMT
ENV NODE_VERSION=6.11.3
# Wed, 13 Sep 2017 20:38:26 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Wed, 13 Sep 2017 20:38:26 GMT
ENV YARN_VERSION=0.27.5
# Wed, 13 Sep 2017 20:38:30 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Wed, 13 Sep 2017 20:38:30 GMT
CMD ["node"]
# Wed, 13 Sep 2017 21:10:30 GMT
ENV GOSU_VERSION=1.10
# Wed, 13 Sep 2017 21:10:35 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Wed, 13 Sep 2017 21:10:35 GMT
ENV NPM_CONFIG_LOGLEVEL=warn
# Wed, 13 Sep 2017 21:10:35 GMT
ENV NODE_ENV=production
# Wed, 13 Sep 2017 21:10:35 GMT
ENV GHOST_CLI_VERSION=1.1.1
# Fri, 29 Sep 2017 22:33:33 GMT
ENV GHOST_VERSION=1.10.0
# Fri, 29 Sep 2017 22:34:08 GMT
RUN npm install -g "ghost-cli@$GHOST_CLI_VERSION" knex-migrator@latest
# Fri, 29 Sep 2017 22:34:09 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 29 Sep 2017 22:34:09 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 29 Sep 2017 22:34:42 GMT
RUN set -ex; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"
# Fri, 29 Sep 2017 22:34:43 GMT
WORKDIR /var/lib/ghost
# Fri, 29 Sep 2017 22:34:44 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 29 Sep 2017 22:34:44 GMT
COPY file:ef6da72f41bc8f60c42fab63c9c2ffdee82253c6dd2110e3d50866e5445df15e in /usr/local/bin 
# Fri, 29 Sep 2017 22:34:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Sep 2017 22:34:44 GMT
EXPOSE 2368/tcp
# Fri, 29 Sep 2017 22:34:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:aa18ad1a0d334d80981104c599fa8cef9264552a265b1197af11274beba767cf`  
		Last Modified: Thu, 07 Sep 2017 23:11:06 GMT  
		Size: 52.6 MB (52595547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a33158a1367c7c4103c89ae66e8f4fdec4ada6a39d4648cf254b32296d6668`  
		Last Modified: Wed, 13 Sep 2017 12:54:21 GMT  
		Size: 19.3 MB (19263717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e2ecbdc66945a5816aa0d37501c34fe6ae76d1664a47cd366604f68a557052`  
		Last Modified: Wed, 13 Sep 2017 20:49:04 GMT  
		Size: 4.4 KB (4406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba36da051a26db65f69c7538041ed3bf4d545ba973e1763029ba67ea44b99ef`  
		Last Modified: Wed, 13 Sep 2017 20:49:04 GMT  
		Size: 119.2 KB (119152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83260829fd758c7ed96bf6b66af7a83c16afb34bd20fea7c30627caa474c19e0`  
		Last Modified: Wed, 13 Sep 2017 20:51:45 GMT  
		Size: 14.7 MB (14718405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7459ed23b0dbcdf1adf35d3c09d1104dfce1711690a871cb7fea376fdeea9176`  
		Last Modified: Wed, 13 Sep 2017 20:51:40 GMT  
		Size: 938.5 KB (938460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed248cbe68e68af79ca31d36052e903e9bce24bac602f71d2d8ee4a9bc3676a1`  
		Last Modified: Wed, 13 Sep 2017 21:17:36 GMT  
		Size: 500.7 KB (500669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d1e6583f2f4dc6499d66c22f938d5d66fced54f990d20271ab036a86fe0cbc`  
		Last Modified: Fri, 29 Sep 2017 22:42:07 GMT  
		Size: 34.4 MB (34373399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3f41a3555b3208a268885077ed506c02f4da1f3b4a815d7028bad80dcea546`  
		Last Modified: Fri, 29 Sep 2017 22:42:32 GMT  
		Size: 94.5 MB (94479434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e58a823622c8980387093b393ee3ec8b406ee36a079cc10da539b0471f4e2a3`  
		Last Modified: Fri, 29 Sep 2017 22:41:36 GMT  
		Size: 574.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:latest` - linux; arm variant v7

```console
$ docker pull ghost@sha256:24db28a9250caead11744a7d1944be9a2c36652c03b014abaed2f286fca94def
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.4 MB (201351870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7be5bcccf373c0e3287bbc7b2a27655d28f6662151e103ade060f108074abab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 27 Sep 2017 04:12:21 GMT
ADD file:ef59ce7fe68882b1b44bc3c4a5e9e465561cb257fb63f8c2b3c247abb012486b in / 
# Wed, 27 Sep 2017 04:12:22 GMT
CMD ["bash"]
# Wed, 27 Sep 2017 04:39:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 27 Sep 2017 04:39:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 27 Sep 2017 07:03:35 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 27 Sep 2017 07:07:47 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done
# Wed, 27 Sep 2017 07:07:48 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Wed, 27 Sep 2017 07:17:28 GMT
ENV NODE_VERSION=6.11.3
# Wed, 27 Sep 2017 07:18:06 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Wed, 27 Sep 2017 07:18:08 GMT
ENV YARN_VERSION=0.27.5
# Wed, 27 Sep 2017 07:18:10 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Wed, 27 Sep 2017 07:18:10 GMT
CMD ["node"]
# Wed, 27 Sep 2017 07:58:52 GMT
ENV GOSU_VERSION=1.10
# Wed, 27 Sep 2017 07:58:54 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Wed, 27 Sep 2017 07:58:54 GMT
ENV NPM_CONFIG_LOGLEVEL=warn
# Wed, 27 Sep 2017 07:58:54 GMT
ENV NODE_ENV=production
# Wed, 27 Sep 2017 07:58:54 GMT
ENV GHOST_CLI_VERSION=1.1.1
# Sat, 30 Sep 2017 11:55:22 GMT
ENV GHOST_VERSION=1.10.0
# Sat, 30 Sep 2017 11:56:35 GMT
RUN npm install -g "ghost-cli@$GHOST_CLI_VERSION" knex-migrator@latest
# Sat, 30 Sep 2017 11:56:36 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 30 Sep 2017 11:56:37 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 30 Sep 2017 11:57:49 GMT
RUN set -ex; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"
# Sat, 30 Sep 2017 11:57:52 GMT
WORKDIR /var/lib/ghost
# Sat, 30 Sep 2017 11:57:52 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 30 Sep 2017 11:57:52 GMT
COPY file:ef6da72f41bc8f60c42fab63c9c2ffdee82253c6dd2110e3d50866e5445df15e in /usr/local/bin 
# Sat, 30 Sep 2017 11:57:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 30 Sep 2017 11:57:53 GMT
EXPOSE 2368/tcp
# Sat, 30 Sep 2017 11:57:53 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:8c7b63aa62f92f5be1e93e5129c5c99dac397c6d3b5f6c6452bfd0905f6f20be`  
		Last Modified: Wed, 27 Sep 2017 04:17:18 GMT  
		Size: 48.7 MB (48686544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a607bd01ffd678134d1281825ba8fafc069965446932fb3da991e8e6c2d3065d`  
		Last Modified: Wed, 27 Sep 2017 04:58:12 GMT  
		Size: 18.3 MB (18262468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7733b25f61410d8e74ee676e195c358ac6519ef39f1a92f3cd11c5f8ca2048`  
		Last Modified: Wed, 27 Sep 2017 07:20:36 GMT  
		Size: 4.4 KB (4420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553903f3bafddd9019242ebd76c10ae0ba04207db8e960c84758e8762b1c4cca`  
		Last Modified: Wed, 27 Sep 2017 07:20:36 GMT  
		Size: 119.2 KB (119190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34bc7bac012caabb127f3461274a9a4cb95bde62751a07df9eb243be1e2877ad`  
		Last Modified: Wed, 27 Sep 2017 07:22:00 GMT  
		Size: 13.9 MB (13877719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c31b00c4993376f813ed323a451b7444b0f176979418ff061aa095b002377bc0`  
		Last Modified: Wed, 27 Sep 2017 07:21:55 GMT  
		Size: 940.2 KB (940161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:541588608a9db7c94840b658b4d597ff4903433af8b4e46a3b35d0d48ccfa330`  
		Last Modified: Wed, 27 Sep 2017 08:05:26 GMT  
		Size: 475.3 KB (475267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ee01efe1bc522be8f8abd8080bdd3708e66ec95ede0cb6a5d2e1a5a321caf51`  
		Last Modified: Sat, 30 Sep 2017 11:58:34 GMT  
		Size: 29.2 MB (29169178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d95b75a1bb347fc5d04c4ac95b89a21a27bb397e26275b5c126c561efb0947b`  
		Last Modified: Sat, 30 Sep 2017 11:58:58 GMT  
		Size: 89.8 MB (89816348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4681c19bb16c56ef451982b2084f48ac2ae91f8007c55a3259b7fd168ecc312f`  
		Last Modified: Sat, 30 Sep 2017 11:58:20 GMT  
		Size: 575.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:latest` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:4778e6eafd796f96c4e3d279c18fc1a3dd030f32e215c2fe6150198baae84e90
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.9 MB (203937560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ce70e09282f3873bdcf8a71e0562634725e2269efe303c165537c15dabfbbbb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 08 Sep 2017 17:23:41 GMT
ADD file:9f576a63a5e03994904e585c35fbeef6a2c96c41d8f696705c033f3ca69b6a2b in / 
# Fri, 08 Sep 2017 17:23:42 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 18:32:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 18:32:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 Sep 2017 23:16:17 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 14 Sep 2017 23:16:22 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done
# Thu, 14 Sep 2017 23:16:24 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Thu, 14 Sep 2017 23:18:55 GMT
ENV NODE_VERSION=6.11.3
# Thu, 14 Sep 2017 23:19:28 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Thu, 14 Sep 2017 23:19:29 GMT
ENV YARN_VERSION=0.27.5
# Thu, 14 Sep 2017 23:19:35 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Thu, 14 Sep 2017 23:19:37 GMT
CMD ["node"]
# Fri, 15 Sep 2017 02:19:54 GMT
ENV GOSU_VERSION=1.10
# Fri, 15 Sep 2017 02:20:02 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Fri, 15 Sep 2017 02:20:03 GMT
ENV NPM_CONFIG_LOGLEVEL=warn
# Fri, 15 Sep 2017 02:20:04 GMT
ENV NODE_ENV=production
# Fri, 15 Sep 2017 02:20:05 GMT
ENV GHOST_CLI_VERSION=1.1.1
# Sat, 30 Sep 2017 10:41:33 GMT
ENV GHOST_VERSION=1.10.0
# Sat, 30 Sep 2017 10:43:52 GMT
RUN npm install -g "ghost-cli@$GHOST_CLI_VERSION" knex-migrator@latest
# Sat, 30 Sep 2017 10:43:54 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 30 Sep 2017 10:43:55 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 30 Sep 2017 10:45:38 GMT
RUN set -ex; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"
# Sat, 30 Sep 2017 10:45:42 GMT
WORKDIR /var/lib/ghost
# Sat, 30 Sep 2017 10:45:42 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 30 Sep 2017 10:45:43 GMT
COPY file:ef6da72f41bc8f60c42fab63c9c2ffdee82253c6dd2110e3d50866e5445df15e in /usr/local/bin 
# Sat, 30 Sep 2017 10:45:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 30 Sep 2017 10:45:45 GMT
EXPOSE 2368/tcp
# Sat, 30 Sep 2017 10:45:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:e91a355b0d3ff86add037a3f24718b760d8eb3f346f998e5116375ddce9eae19`  
		Last Modified: Fri, 08 Sep 2017 17:34:56 GMT  
		Size: 49.9 MB (49929457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e054bfb02234c6e2b5305981d365c3b31101ec460b0d90df3b099305c03196`  
		Last Modified: Thu, 14 Sep 2017 22:01:15 GMT  
		Size: 18.7 MB (18737603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68cbb48bf959f44cbc4806f42587333e86631edab819261ca51eba1da6fcd637`  
		Last Modified: Thu, 14 Sep 2017 23:24:36 GMT  
		Size: 4.4 KB (4417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e961bd22aace0af8a10a14a5d6282014bdb3cf7c4d5b42e16a0dd45e4cd06dac`  
		Last Modified: Thu, 14 Sep 2017 23:24:36 GMT  
		Size: 119.2 KB (119150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:280e0b3e39cb221ce8de69ec6e8d5e99fd9761fc3a6d37cbd9086ad72d3b41dc`  
		Last Modified: Thu, 14 Sep 2017 23:27:52 GMT  
		Size: 14.7 MB (14707206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e714752cefed2ff3be3734c49f1a880303ff6290d0705230e5f486a0a0bbe756`  
		Last Modified: Thu, 14 Sep 2017 23:27:45 GMT  
		Size: 940.1 KB (940132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de4bc9133bf690ef04927a67017f86cc9e619e51f7cac9262ff9165db6baefc`  
		Last Modified: Fri, 15 Sep 2017 02:35:50 GMT  
		Size: 468.7 KB (468701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d7bd10a95781c324562ce9f74235c7ef17ba5265033caafb028f240912114a`  
		Last Modified: Sat, 30 Sep 2017 10:46:26 GMT  
		Size: 29.2 MB (29168766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82c35004fc2685c10e031b4e39e97503ed72b418850306ead8ad0a25f0112976`  
		Last Modified: Sat, 30 Sep 2017 10:46:48 GMT  
		Size: 89.9 MB (89861555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd20cd50f4050f013e3109e93315f76c9c378d8d8acad7e5140112cacb55f835`  
		Last Modified: Sat, 30 Sep 2017 10:46:11 GMT  
		Size: 573.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:latest` - linux; ppc64le

```console
$ docker pull ghost@sha256:5519b5f58af430a845cfb4617430d530fc69b279353a2b41883793c949d79537
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.1 MB (206070261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf606d1107cf8f7551b5f5dff21b1769766e0d07f6e2decbeafacb2446180d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 08 Sep 2017 00:32:21 GMT
ADD file:483b3245941140ac32394a804364a1a9bd5dfdf1b4475238b61068cc7252ac08 in / 
# Fri, 08 Sep 2017 00:32:21 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 01:03:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 01:03:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 Sep 2017 23:10:48 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 14 Sep 2017 23:11:08 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done
# Thu, 14 Sep 2017 23:11:12 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Thu, 14 Sep 2017 23:15:42 GMT
ENV NODE_VERSION=6.11.3
# Thu, 14 Sep 2017 23:16:32 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Thu, 14 Sep 2017 23:16:41 GMT
ENV YARN_VERSION=0.27.5
# Thu, 14 Sep 2017 23:16:48 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Thu, 14 Sep 2017 23:16:50 GMT
CMD ["node"]
# Fri, 15 Sep 2017 02:22:38 GMT
ENV GOSU_VERSION=1.10
# Fri, 15 Sep 2017 02:22:46 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Fri, 15 Sep 2017 02:22:48 GMT
ENV NPM_CONFIG_LOGLEVEL=warn
# Fri, 15 Sep 2017 02:22:52 GMT
ENV NODE_ENV=production
# Fri, 15 Sep 2017 02:22:54 GMT
ENV GHOST_CLI_VERSION=1.1.1
# Sat, 30 Sep 2017 01:26:24 GMT
ENV GHOST_VERSION=1.10.0
# Sat, 30 Sep 2017 01:27:21 GMT
RUN npm install -g "ghost-cli@$GHOST_CLI_VERSION" knex-migrator@latest
# Sat, 30 Sep 2017 01:27:28 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 30 Sep 2017 01:27:30 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 30 Sep 2017 01:28:37 GMT
RUN set -ex; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"
# Sat, 30 Sep 2017 01:28:44 GMT
WORKDIR /var/lib/ghost
# Sat, 30 Sep 2017 01:28:48 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 30 Sep 2017 01:28:50 GMT
COPY file:ef6da72f41bc8f60c42fab63c9c2ffdee82253c6dd2110e3d50866e5445df15e in /usr/local/bin 
# Sat, 30 Sep 2017 01:28:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 30 Sep 2017 01:28:55 GMT
EXPOSE 2368/tcp
# Sat, 30 Sep 2017 01:28:58 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d4a5434e09b7ac8431060d347d6ef1233ae07514878fb2aff4085bcf441c29f3`  
		Last Modified: Fri, 08 Sep 2017 00:36:52 GMT  
		Size: 51.8 MB (51809570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48596af2c38701f94440e222bf8f3d4b2da85e2982c97ae15186eba523249e0b`  
		Last Modified: Thu, 14 Sep 2017 22:21:02 GMT  
		Size: 19.2 MB (19199596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1dc276f5b0bc12cddaf889657d8ed9d7ec3e6add07506308ea49dc52bb6eff`  
		Last Modified: Thu, 14 Sep 2017 23:22:38 GMT  
		Size: 4.4 KB (4444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb57f53562fb9db3e40e7ee479f5526f635b724a0632d9a4d3da2500a44c491d`  
		Last Modified: Thu, 14 Sep 2017 23:22:39 GMT  
		Size: 119.2 KB (119184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f255065ee2535a6b44019881cc1954c1a7f665f6b0c530c618663be94e4a23`  
		Last Modified: Thu, 14 Sep 2017 23:26:37 GMT  
		Size: 14.5 MB (14475182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68be6ded470a2cf42b2ccda178f212a25198e102a4e3249456140252fa22f054`  
		Last Modified: Thu, 14 Sep 2017 23:26:32 GMT  
		Size: 940.2 KB (940157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad1d6527d8ade34c5efd2bd98f7a049a917ff22859c6eaaed4046a2df232d91b`  
		Last Modified: Fri, 15 Sep 2017 02:32:57 GMT  
		Size: 469.9 KB (469852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f814a9bc90f3c846324f0952f0ae962140c6c3eaedd3e91eebd25f20d56bcc06`  
		Last Modified: Sat, 30 Sep 2017 01:29:27 GMT  
		Size: 29.2 MB (29167447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd14b03e56a10a52bb6decdf699c7db5c4446ff682043ec05c46042069ac5e6`  
		Last Modified: Sat, 30 Sep 2017 01:29:45 GMT  
		Size: 89.9 MB (89884255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b4c1125e28a6f6aaf1a9849d51d4724cd2372100162880dc826bfe2cf89a5b`  
		Last Modified: Sat, 30 Sep 2017 01:29:17 GMT  
		Size: 574.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:latest` - linux; s390x

```console
$ docker pull ghost@sha256:d64cf4c152b1cab609af105e32edb33313e29d8f13cf68ca7e057d980c2c8cc2
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207664584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce7ab8a934452910b724a2dbbdd3229e252349593a2327814139278d378072c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 08 Sep 2017 05:21:42 GMT
ADD file:996e52a941b7162fafcf761c415142a34a2fc703e21d2f264b824373e9fa4b1e in / 
# Fri, 08 Sep 2017 05:21:43 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 05:48:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 05:48:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 08 Sep 2017 17:04:11 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Fri, 08 Sep 2017 17:04:12 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done
# Fri, 08 Sep 2017 17:04:12 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Fri, 08 Sep 2017 17:04:55 GMT
ENV NODE_VERSION=6.11.3
# Fri, 08 Sep 2017 17:05:10 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Fri, 08 Sep 2017 17:05:10 GMT
ENV YARN_VERSION=0.27.5
# Fri, 08 Sep 2017 17:05:11 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Fri, 08 Sep 2017 17:05:12 GMT
CMD ["node"]
# Fri, 08 Sep 2017 18:17:08 GMT
ENV GOSU_VERSION=1.10
# Fri, 08 Sep 2017 18:17:11 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Fri, 08 Sep 2017 18:17:11 GMT
ENV NPM_CONFIG_LOGLEVEL=warn
# Fri, 08 Sep 2017 18:17:11 GMT
ENV NODE_ENV=production
# Fri, 08 Sep 2017 18:17:11 GMT
ENV GHOST_CLI_VERSION=1.1.1
# Sat, 30 Sep 2017 14:22:24 GMT
ENV GHOST_VERSION=1.10.0
# Sat, 30 Sep 2017 14:23:02 GMT
RUN npm install -g "ghost-cli@$GHOST_CLI_VERSION" knex-migrator@latest
# Sat, 30 Sep 2017 14:23:03 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 30 Sep 2017 14:23:03 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 30 Sep 2017 14:23:33 GMT
RUN set -ex; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"
# Sat, 30 Sep 2017 14:23:35 GMT
WORKDIR /var/lib/ghost
# Sat, 30 Sep 2017 14:23:35 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 30 Sep 2017 14:23:35 GMT
COPY file:ef6da72f41bc8f60c42fab63c9c2ffdee82253c6dd2110e3d50866e5445df15e in /usr/local/bin 
# Sat, 30 Sep 2017 14:23:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 30 Sep 2017 14:23:35 GMT
EXPOSE 2368/tcp
# Sat, 30 Sep 2017 14:23:36 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:5f39dbffcd07e3254246d3c2e4b3532c3697ed04f83eadf5433da820098787df`  
		Last Modified: Fri, 08 Sep 2017 05:24:42 GMT  
		Size: 52.8 MB (52788802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5a344275c5d5a12a16990e9ddb7cfb9bc9b793cc51fbf8bf8993426e287c27`  
		Last Modified: Fri, 08 Sep 2017 16:41:52 GMT  
		Size: 19.5 MB (19470373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c81355314e654fd3d4e1dcbec2f82fffb19b856e65aa403cf7b2d471582658`  
		Last Modified: Fri, 08 Sep 2017 17:05:56 GMT  
		Size: 4.4 KB (4411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9c66bc4cf9f13c8d89cb57f07ce23693a1efcbbbcc32e7e30c5e8e0cefa2c8`  
		Last Modified: Fri, 08 Sep 2017 17:05:56 GMT  
		Size: 119.1 KB (119148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa1121a725f9b59e0fcd0c6226075d97e638b15fdfc40f5e1d57d3a5f3c3f190`  
		Last Modified: Fri, 08 Sep 2017 17:07:00 GMT  
		Size: 14.8 MB (14847789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa31e4823df3a66473b6ca7286cf7a152288b868f3cf1d4df5eb0393f5e81da`  
		Last Modified: Fri, 08 Sep 2017 17:06:56 GMT  
		Size: 938.5 KB (938452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6819f9496d60b6b7dda2b89e7dd5c2a3c3442d0f1270b9f67b3c132f70fbeeb`  
		Last Modified: Fri, 08 Sep 2017 18:20:31 GMT  
		Size: 486.8 KB (486823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a59f71a40f843fc869ea2674c548cd5437531fbfa4cad604ba97432de4c3662`  
		Last Modified: Sat, 30 Sep 2017 14:23:59 GMT  
		Size: 29.2 MB (29166808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0eef1dc513aa74c3750bd41d13dbfd1576d9333340f889213b7d62aaeae7737`  
		Last Modified: Sat, 30 Sep 2017 14:24:10 GMT  
		Size: 89.8 MB (89841405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9fda95fa7073acebbc9f0b203e74fe5e7d92fde0d6097b30ce415370f804ee`  
		Last Modified: Sat, 30 Sep 2017 14:23:52 GMT  
		Size: 573.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
