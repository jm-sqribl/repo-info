<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `memcached`

-	[`memcached:1`](#memcached1)
-	[`memcached:1.5`](#memcached15)
-	[`memcached:1.5.2`](#memcached152)
-	[`memcached:1.5.2-alpine`](#memcached152-alpine)
-	[`memcached:1.5-alpine`](#memcached15-alpine)
-	[`memcached:1-alpine`](#memcached1-alpine)
-	[`memcached:alpine`](#memcachedalpine)
-	[`memcached:latest`](#memcachedlatest)

## `memcached:1`

```console
$ docker pull memcached@sha256:70e8f6136bfd18b73c03db481a328efbffe90d020b6a1b46bcca26c7a297071f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `memcached:1` - linux; amd64

```console
$ docker pull memcached@sha256:1a7f4b7378450722e1fac00f3da78203aa9b29a33c3fe64a27154ada65f8c46b
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 MB (25255674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed85c5f97e4a3071fc18ddaa41c6fbc4fe64f9f6e16c15e8b31b38389e91f40a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Sep 2017 08:41:48 GMT
ADD file:2bc9df54d28d9ec75722f6748834a1aea0baf089047e86a541064c282246c300 in / 
# Wed, 13 Sep 2017 08:41:49 GMT
CMD ["bash"]
# Tue, 19 Sep 2017 01:37:55 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Mon, 02 Oct 2017 23:34:17 GMT
ENV MEMCACHED_VERSION=1.5.2
# Mon, 02 Oct 2017 23:34:17 GMT
ENV MEMCACHED_SHA1=5d6c85fe15b5e575a563ec1bbeb01020e0132958
# Mon, 02 Oct 2017 23:37:42 GMT
RUN set -x 		&& buildDeps=' 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libsasl2-dev 		make 		perl 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark manual 		libevent-2.0-5 		libsasl2-2 	&& apt-get purge -y --auto-remove $buildDeps 		&& memcached -V
# Mon, 02 Oct 2017 23:37:42 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Mon, 02 Oct 2017 23:37:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 02 Oct 2017 23:37:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Oct 2017 23:37:43 GMT
USER [memcache]
# Mon, 02 Oct 2017 23:37:43 GMT
EXPOSE 11211/tcp
# Mon, 02 Oct 2017 23:37:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:afeb2bfd31c0760573e7262de6ae67a84da0e0a1c3e8157bbddd41a501b18a5c`  
		Last Modified: Thu, 07 Sep 2017 23:21:35 GMT  
		Size: 22.5 MB (22488057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2071de9f4eeec05d24d79982d276e34b21a0eb47d684e8a0f6ff216920f9dbd4`  
		Last Modified: Tue, 19 Sep 2017 01:45:07 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:801d526779aa5e4db381451fee28dddaf024b196b4e47e650e0a9dab5be352f6`  
		Last Modified: Mon, 02 Oct 2017 23:41:29 GMT  
		Size: 2.8 MB (2765454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1e66690632d0cc88a2f5f9831610c92124dcb7d380f3440e45b514f9030540`  
		Last Modified: Mon, 02 Oct 2017 23:41:28 GMT  
		Size: 296.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8235e6c84810a2b4c784bda57cd75121ab29a9db450008525d7d025813d615b9`  
		Last Modified: Mon, 02 Oct 2017 23:41:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; arm variant v7

```console
$ docker pull memcached@sha256:45117fc1ab5b256104f1a7da099e8dedfee8b0632ca63b5c0b1940b4c171761c
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.8 MB (21849606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa094160687b7a04b422d5236b2a1b3a5f55f3461564d84fe7005508db21fdc2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 27 Sep 2017 04:14:53 GMT
ADD file:c64f62f8baccded9d94037c0935c477d3dd18839a9c4e565679657d4c9df92c8 in / 
# Wed, 27 Sep 2017 04:14:53 GMT
CMD ["bash"]
# Thu, 28 Sep 2017 17:33:00 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Tue, 03 Oct 2017 04:58:40 GMT
ENV MEMCACHED_VERSION=1.5.2
# Tue, 03 Oct 2017 04:58:41 GMT
ENV MEMCACHED_SHA1=5d6c85fe15b5e575a563ec1bbeb01020e0132958
# Tue, 03 Oct 2017 05:09:21 GMT
RUN set -x 		&& buildDeps=' 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libsasl2-dev 		make 		perl 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark manual 		libevent-2.0-5 		libsasl2-2 	&& apt-get purge -y --auto-remove $buildDeps 		&& memcached -V
# Tue, 03 Oct 2017 05:09:22 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Tue, 03 Oct 2017 05:09:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 03 Oct 2017 05:09:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Oct 2017 05:09:28 GMT
USER [memcache]
# Tue, 03 Oct 2017 05:09:28 GMT
EXPOSE 11211/tcp
# Tue, 03 Oct 2017 05:09:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f6b0b1de175bfd1f4139472dafaeed39d43c5c14f6f48f113c9053f9b7837ddf`  
		Last Modified: Wed, 27 Sep 2017 04:20:52 GMT  
		Size: 19.3 MB (19276815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f5ecc5bf4596151966ea59e07f6ad9872eea9f0425d607ad70cc9f8098735d`  
		Last Modified: Thu, 28 Sep 2017 18:04:32 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec9465bec05809fbab31cd4def5bdd9eaeaffa172b78595641978d6cec7132d7`  
		Last Modified: Tue, 03 Oct 2017 05:09:53 GMT  
		Size: 2.6 MB (2570630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95b2e3141b98b19f4a9686a2b3b62c01b11022c89f6c794235606b33a1a590c2`  
		Last Modified: Tue, 03 Oct 2017 05:09:48 GMT  
		Size: 297.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d8bbdd412eae144399fb049bd999c8897ee07ffc72311e44077de4e43a274c`  
		Last Modified: Tue, 03 Oct 2017 05:09:48 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:ca66586f1ab5c5447946aa59801e147be829e6335bb5ad3af626201b23acb110
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 MB (22966658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0db14e99e7f68b4de82b214f77333a9e62cda1d5622c220873170a06299e6a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Sep 2017 17:29:09 GMT
ADD file:16391f421551b998f1ff496c48dc67f34dd2003077158fd1af78a898ea367e1d in / 
# Fri, 08 Sep 2017 17:29:10 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 21:28:53 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Tue, 03 Oct 2017 02:47:39 GMT
ENV MEMCACHED_VERSION=1.5.2
# Tue, 03 Oct 2017 02:47:39 GMT
ENV MEMCACHED_SHA1=5d6c85fe15b5e575a563ec1bbeb01020e0132958
# Tue, 03 Oct 2017 02:52:55 GMT
RUN set -x 		&& buildDeps=' 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libsasl2-dev 		make 		perl 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark manual 		libevent-2.0-5 		libsasl2-2 	&& apt-get purge -y --auto-remove $buildDeps 		&& memcached -V
# Tue, 03 Oct 2017 02:52:56 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Tue, 03 Oct 2017 02:52:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 03 Oct 2017 02:52:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Oct 2017 02:52:58 GMT
USER [memcache]
# Tue, 03 Oct 2017 02:52:59 GMT
EXPOSE 11211/tcp
# Tue, 03 Oct 2017 02:52:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0bd6dbb95c7a219839ea8345519110bbccc30c113a72119bbd92c7fe2a3f1e78`  
		Last Modified: Fri, 08 Sep 2017 17:43:38 GMT  
		Size: 20.3 MB (20337273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6665fa1f2e9808b2c4b49d3e92a04338a3e5dbe26dcf2902b5fbb42db9a8221a`  
		Last Modified: Fri, 08 Sep 2017 21:35:34 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d34c0041837ca9b08e74f897f629b5ce97270f9901f7db73b645e218274b02e`  
		Last Modified: Tue, 03 Oct 2017 02:53:27 GMT  
		Size: 2.6 MB (2627226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525ee33bdf80f9245b2a3527d578353460bc159dad068bd1e0ec792c6affbaae`  
		Last Modified: Tue, 03 Oct 2017 02:53:25 GMT  
		Size: 294.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5d789c03941afc108cef42254d041beb203b409220bc34cd631eef2ab503be`  
		Last Modified: Tue, 03 Oct 2017 02:53:25 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:343d8ae081ca1106c325d6cf0a19c3c2acc340270ec19812eea1f2d1f3cbe9f3
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 MB (25490680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c42934e8960fce51082f73a170eed1d762d8fcc84d657c18a05671009236d67e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Sep 2017 00:34:22 GMT
ADD file:1422f50e4e998477f6c3b2fcee6853da10eb8bca7926ec70e494ff485f6284d7 in / 
# Fri, 08 Sep 2017 00:34:22 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 01:18:55 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Tue, 03 Oct 2017 00:33:25 GMT
ENV MEMCACHED_VERSION=1.5.2
# Tue, 03 Oct 2017 00:33:28 GMT
ENV MEMCACHED_SHA1=5d6c85fe15b5e575a563ec1bbeb01020e0132958
# Tue, 03 Oct 2017 00:45:44 GMT
RUN set -x 		&& buildDeps=' 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libsasl2-dev 		make 		perl 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark manual 		libevent-2.0-5 		libsasl2-2 	&& apt-get purge -y --auto-remove $buildDeps 		&& memcached -V
# Tue, 03 Oct 2017 00:45:47 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Tue, 03 Oct 2017 00:45:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 03 Oct 2017 00:45:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Oct 2017 00:45:57 GMT
USER [memcache]
# Tue, 03 Oct 2017 00:45:59 GMT
EXPOSE 11211/tcp
# Tue, 03 Oct 2017 00:46:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7ff7f6fdf12a09feca6f75b5d90b860059bdccf4185a9dab7c2c5b9e6e90123a`  
		Last Modified: Fri, 08 Sep 2017 00:41:42 GMT  
		Size: 22.7 MB (22746060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1a3601d5bf8b21acd6372ae2e68d3aff208607075ac8ddcc4bbb996536673c`  
		Last Modified: Fri, 08 Sep 2017 01:22:42 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddfd59f2c72998bac21ef7ff3276fd6303cff7d7b07c7b2d1d0cf06098aef552`  
		Last Modified: Tue, 03 Oct 2017 00:46:16 GMT  
		Size: 2.7 MB (2742459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1efc5ab41850a9bc0069e6acf3055cd6300c5104b7128cdb08e97e7bb7439940`  
		Last Modified: Tue, 03 Oct 2017 00:46:15 GMT  
		Size: 298.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b0682fdbd5b9156c013ad0865f56422b00ddd745ec9c0c66770cd06e18b9e5`  
		Last Modified: Tue, 03 Oct 2017 00:46:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; s390x

```console
$ docker pull memcached@sha256:dec16560e75f8919ffff35bf442e5408afbf9c54862ab84503ad72ca798ab171
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25137947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bb3ed29f5a6f058f29a7c8983723edb4d73460e7ad7c7e7712e0a205ed67696`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Sep 2017 05:23:00 GMT
ADD file:9b074cf37adfa815e3a6b300f8652eb77a06cfeea3f74fd021795cff318ca2ce in / 
# Fri, 08 Sep 2017 05:23:00 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 06:14:47 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Tue, 03 Oct 2017 17:33:26 GMT
ENV MEMCACHED_VERSION=1.5.2
# Tue, 03 Oct 2017 17:33:27 GMT
ENV MEMCACHED_SHA1=5d6c85fe15b5e575a563ec1bbeb01020e0132958
# Tue, 03 Oct 2017 17:37:12 GMT
RUN set -x 		&& buildDeps=' 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libsasl2-dev 		make 		perl 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark manual 		libevent-2.0-5 		libsasl2-2 	&& apt-get purge -y --auto-remove $buildDeps 		&& memcached -V
# Tue, 03 Oct 2017 17:37:13 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Tue, 03 Oct 2017 17:37:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 03 Oct 2017 17:37:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Oct 2017 17:37:14 GMT
USER [memcache]
# Tue, 03 Oct 2017 17:37:14 GMT
EXPOSE 11211/tcp
# Tue, 03 Oct 2017 17:37:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a3a3449ff754d3a7e8f189d020e507ff2cb0fd172b4240ca2d1d78e2d65d544`  
		Last Modified: Fri, 08 Sep 2017 05:27:12 GMT  
		Size: 22.3 MB (22338151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224b6ce1a0dc831e8b9f4e624f804d0284ddee9b709f63c77ad96a08b244d884`  
		Last Modified: Fri, 08 Sep 2017 06:18:24 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e3b6b53bafc260659b45815f23269d235963995672bb68e5702405e5434fbc`  
		Last Modified: Tue, 03 Oct 2017 17:37:23 GMT  
		Size: 2.8 MB (2797638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270326384f346a86137654a3e86c3514352aa2fe2f70d1f873331b595f887547`  
		Last Modified: Tue, 03 Oct 2017 17:37:23 GMT  
		Size: 297.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8428e5eed7f1348d7537eac0cfd1aed1d7937ef003ff16a597b5999a5c941a28`  
		Last Modified: Tue, 03 Oct 2017 17:37:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1.5`

```console
$ docker pull memcached@sha256:70e8f6136bfd18b73c03db481a328efbffe90d020b6a1b46bcca26c7a297071f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `memcached:1.5` - linux; amd64

```console
$ docker pull memcached@sha256:1a7f4b7378450722e1fac00f3da78203aa9b29a33c3fe64a27154ada65f8c46b
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 MB (25255674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed85c5f97e4a3071fc18ddaa41c6fbc4fe64f9f6e16c15e8b31b38389e91f40a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Sep 2017 08:41:48 GMT
ADD file:2bc9df54d28d9ec75722f6748834a1aea0baf089047e86a541064c282246c300 in / 
# Wed, 13 Sep 2017 08:41:49 GMT
CMD ["bash"]
# Tue, 19 Sep 2017 01:37:55 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Mon, 02 Oct 2017 23:34:17 GMT
ENV MEMCACHED_VERSION=1.5.2
# Mon, 02 Oct 2017 23:34:17 GMT
ENV MEMCACHED_SHA1=5d6c85fe15b5e575a563ec1bbeb01020e0132958
# Mon, 02 Oct 2017 23:37:42 GMT
RUN set -x 		&& buildDeps=' 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libsasl2-dev 		make 		perl 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark manual 		libevent-2.0-5 		libsasl2-2 	&& apt-get purge -y --auto-remove $buildDeps 		&& memcached -V
# Mon, 02 Oct 2017 23:37:42 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Mon, 02 Oct 2017 23:37:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 02 Oct 2017 23:37:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Oct 2017 23:37:43 GMT
USER [memcache]
# Mon, 02 Oct 2017 23:37:43 GMT
EXPOSE 11211/tcp
# Mon, 02 Oct 2017 23:37:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:afeb2bfd31c0760573e7262de6ae67a84da0e0a1c3e8157bbddd41a501b18a5c`  
		Last Modified: Thu, 07 Sep 2017 23:21:35 GMT  
		Size: 22.5 MB (22488057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2071de9f4eeec05d24d79982d276e34b21a0eb47d684e8a0f6ff216920f9dbd4`  
		Last Modified: Tue, 19 Sep 2017 01:45:07 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:801d526779aa5e4db381451fee28dddaf024b196b4e47e650e0a9dab5be352f6`  
		Last Modified: Mon, 02 Oct 2017 23:41:29 GMT  
		Size: 2.8 MB (2765454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1e66690632d0cc88a2f5f9831610c92124dcb7d380f3440e45b514f9030540`  
		Last Modified: Mon, 02 Oct 2017 23:41:28 GMT  
		Size: 296.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8235e6c84810a2b4c784bda57cd75121ab29a9db450008525d7d025813d615b9`  
		Last Modified: Mon, 02 Oct 2017 23:41:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.5` - linux; arm variant v7

```console
$ docker pull memcached@sha256:45117fc1ab5b256104f1a7da099e8dedfee8b0632ca63b5c0b1940b4c171761c
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.8 MB (21849606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa094160687b7a04b422d5236b2a1b3a5f55f3461564d84fe7005508db21fdc2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 27 Sep 2017 04:14:53 GMT
ADD file:c64f62f8baccded9d94037c0935c477d3dd18839a9c4e565679657d4c9df92c8 in / 
# Wed, 27 Sep 2017 04:14:53 GMT
CMD ["bash"]
# Thu, 28 Sep 2017 17:33:00 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Tue, 03 Oct 2017 04:58:40 GMT
ENV MEMCACHED_VERSION=1.5.2
# Tue, 03 Oct 2017 04:58:41 GMT
ENV MEMCACHED_SHA1=5d6c85fe15b5e575a563ec1bbeb01020e0132958
# Tue, 03 Oct 2017 05:09:21 GMT
RUN set -x 		&& buildDeps=' 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libsasl2-dev 		make 		perl 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark manual 		libevent-2.0-5 		libsasl2-2 	&& apt-get purge -y --auto-remove $buildDeps 		&& memcached -V
# Tue, 03 Oct 2017 05:09:22 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Tue, 03 Oct 2017 05:09:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 03 Oct 2017 05:09:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Oct 2017 05:09:28 GMT
USER [memcache]
# Tue, 03 Oct 2017 05:09:28 GMT
EXPOSE 11211/tcp
# Tue, 03 Oct 2017 05:09:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f6b0b1de175bfd1f4139472dafaeed39d43c5c14f6f48f113c9053f9b7837ddf`  
		Last Modified: Wed, 27 Sep 2017 04:20:52 GMT  
		Size: 19.3 MB (19276815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f5ecc5bf4596151966ea59e07f6ad9872eea9f0425d607ad70cc9f8098735d`  
		Last Modified: Thu, 28 Sep 2017 18:04:32 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec9465bec05809fbab31cd4def5bdd9eaeaffa172b78595641978d6cec7132d7`  
		Last Modified: Tue, 03 Oct 2017 05:09:53 GMT  
		Size: 2.6 MB (2570630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95b2e3141b98b19f4a9686a2b3b62c01b11022c89f6c794235606b33a1a590c2`  
		Last Modified: Tue, 03 Oct 2017 05:09:48 GMT  
		Size: 297.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d8bbdd412eae144399fb049bd999c8897ee07ffc72311e44077de4e43a274c`  
		Last Modified: Tue, 03 Oct 2017 05:09:48 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.5` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:ca66586f1ab5c5447946aa59801e147be829e6335bb5ad3af626201b23acb110
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 MB (22966658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0db14e99e7f68b4de82b214f77333a9e62cda1d5622c220873170a06299e6a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Sep 2017 17:29:09 GMT
ADD file:16391f421551b998f1ff496c48dc67f34dd2003077158fd1af78a898ea367e1d in / 
# Fri, 08 Sep 2017 17:29:10 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 21:28:53 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Tue, 03 Oct 2017 02:47:39 GMT
ENV MEMCACHED_VERSION=1.5.2
# Tue, 03 Oct 2017 02:47:39 GMT
ENV MEMCACHED_SHA1=5d6c85fe15b5e575a563ec1bbeb01020e0132958
# Tue, 03 Oct 2017 02:52:55 GMT
RUN set -x 		&& buildDeps=' 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libsasl2-dev 		make 		perl 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark manual 		libevent-2.0-5 		libsasl2-2 	&& apt-get purge -y --auto-remove $buildDeps 		&& memcached -V
# Tue, 03 Oct 2017 02:52:56 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Tue, 03 Oct 2017 02:52:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 03 Oct 2017 02:52:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Oct 2017 02:52:58 GMT
USER [memcache]
# Tue, 03 Oct 2017 02:52:59 GMT
EXPOSE 11211/tcp
# Tue, 03 Oct 2017 02:52:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0bd6dbb95c7a219839ea8345519110bbccc30c113a72119bbd92c7fe2a3f1e78`  
		Last Modified: Fri, 08 Sep 2017 17:43:38 GMT  
		Size: 20.3 MB (20337273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6665fa1f2e9808b2c4b49d3e92a04338a3e5dbe26dcf2902b5fbb42db9a8221a`  
		Last Modified: Fri, 08 Sep 2017 21:35:34 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d34c0041837ca9b08e74f897f629b5ce97270f9901f7db73b645e218274b02e`  
		Last Modified: Tue, 03 Oct 2017 02:53:27 GMT  
		Size: 2.6 MB (2627226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525ee33bdf80f9245b2a3527d578353460bc159dad068bd1e0ec792c6affbaae`  
		Last Modified: Tue, 03 Oct 2017 02:53:25 GMT  
		Size: 294.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5d789c03941afc108cef42254d041beb203b409220bc34cd631eef2ab503be`  
		Last Modified: Tue, 03 Oct 2017 02:53:25 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.5` - linux; ppc64le

```console
$ docker pull memcached@sha256:343d8ae081ca1106c325d6cf0a19c3c2acc340270ec19812eea1f2d1f3cbe9f3
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 MB (25490680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c42934e8960fce51082f73a170eed1d762d8fcc84d657c18a05671009236d67e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Sep 2017 00:34:22 GMT
ADD file:1422f50e4e998477f6c3b2fcee6853da10eb8bca7926ec70e494ff485f6284d7 in / 
# Fri, 08 Sep 2017 00:34:22 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 01:18:55 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Tue, 03 Oct 2017 00:33:25 GMT
ENV MEMCACHED_VERSION=1.5.2
# Tue, 03 Oct 2017 00:33:28 GMT
ENV MEMCACHED_SHA1=5d6c85fe15b5e575a563ec1bbeb01020e0132958
# Tue, 03 Oct 2017 00:45:44 GMT
RUN set -x 		&& buildDeps=' 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libsasl2-dev 		make 		perl 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark manual 		libevent-2.0-5 		libsasl2-2 	&& apt-get purge -y --auto-remove $buildDeps 		&& memcached -V
# Tue, 03 Oct 2017 00:45:47 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Tue, 03 Oct 2017 00:45:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 03 Oct 2017 00:45:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Oct 2017 00:45:57 GMT
USER [memcache]
# Tue, 03 Oct 2017 00:45:59 GMT
EXPOSE 11211/tcp
# Tue, 03 Oct 2017 00:46:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7ff7f6fdf12a09feca6f75b5d90b860059bdccf4185a9dab7c2c5b9e6e90123a`  
		Last Modified: Fri, 08 Sep 2017 00:41:42 GMT  
		Size: 22.7 MB (22746060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1a3601d5bf8b21acd6372ae2e68d3aff208607075ac8ddcc4bbb996536673c`  
		Last Modified: Fri, 08 Sep 2017 01:22:42 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddfd59f2c72998bac21ef7ff3276fd6303cff7d7b07c7b2d1d0cf06098aef552`  
		Last Modified: Tue, 03 Oct 2017 00:46:16 GMT  
		Size: 2.7 MB (2742459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1efc5ab41850a9bc0069e6acf3055cd6300c5104b7128cdb08e97e7bb7439940`  
		Last Modified: Tue, 03 Oct 2017 00:46:15 GMT  
		Size: 298.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b0682fdbd5b9156c013ad0865f56422b00ddd745ec9c0c66770cd06e18b9e5`  
		Last Modified: Tue, 03 Oct 2017 00:46:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.5` - linux; s390x

```console
$ docker pull memcached@sha256:dec16560e75f8919ffff35bf442e5408afbf9c54862ab84503ad72ca798ab171
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25137947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bb3ed29f5a6f058f29a7c8983723edb4d73460e7ad7c7e7712e0a205ed67696`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Sep 2017 05:23:00 GMT
ADD file:9b074cf37adfa815e3a6b300f8652eb77a06cfeea3f74fd021795cff318ca2ce in / 
# Fri, 08 Sep 2017 05:23:00 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 06:14:47 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Tue, 03 Oct 2017 17:33:26 GMT
ENV MEMCACHED_VERSION=1.5.2
# Tue, 03 Oct 2017 17:33:27 GMT
ENV MEMCACHED_SHA1=5d6c85fe15b5e575a563ec1bbeb01020e0132958
# Tue, 03 Oct 2017 17:37:12 GMT
RUN set -x 		&& buildDeps=' 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libsasl2-dev 		make 		perl 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark manual 		libevent-2.0-5 		libsasl2-2 	&& apt-get purge -y --auto-remove $buildDeps 		&& memcached -V
# Tue, 03 Oct 2017 17:37:13 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Tue, 03 Oct 2017 17:37:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 03 Oct 2017 17:37:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Oct 2017 17:37:14 GMT
USER [memcache]
# Tue, 03 Oct 2017 17:37:14 GMT
EXPOSE 11211/tcp
# Tue, 03 Oct 2017 17:37:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a3a3449ff754d3a7e8f189d020e507ff2cb0fd172b4240ca2d1d78e2d65d544`  
		Last Modified: Fri, 08 Sep 2017 05:27:12 GMT  
		Size: 22.3 MB (22338151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224b6ce1a0dc831e8b9f4e624f804d0284ddee9b709f63c77ad96a08b244d884`  
		Last Modified: Fri, 08 Sep 2017 06:18:24 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e3b6b53bafc260659b45815f23269d235963995672bb68e5702405e5434fbc`  
		Last Modified: Tue, 03 Oct 2017 17:37:23 GMT  
		Size: 2.8 MB (2797638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270326384f346a86137654a3e86c3514352aa2fe2f70d1f873331b595f887547`  
		Last Modified: Tue, 03 Oct 2017 17:37:23 GMT  
		Size: 297.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8428e5eed7f1348d7537eac0cfd1aed1d7937ef003ff16a597b5999a5c941a28`  
		Last Modified: Tue, 03 Oct 2017 17:37:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1.5.2`

```console
$ docker pull memcached@sha256:70e8f6136bfd18b73c03db481a328efbffe90d020b6a1b46bcca26c7a297071f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `memcached:1.5.2` - linux; amd64

```console
$ docker pull memcached@sha256:1a7f4b7378450722e1fac00f3da78203aa9b29a33c3fe64a27154ada65f8c46b
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 MB (25255674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed85c5f97e4a3071fc18ddaa41c6fbc4fe64f9f6e16c15e8b31b38389e91f40a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Sep 2017 08:41:48 GMT
ADD file:2bc9df54d28d9ec75722f6748834a1aea0baf089047e86a541064c282246c300 in / 
# Wed, 13 Sep 2017 08:41:49 GMT
CMD ["bash"]
# Tue, 19 Sep 2017 01:37:55 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Mon, 02 Oct 2017 23:34:17 GMT
ENV MEMCACHED_VERSION=1.5.2
# Mon, 02 Oct 2017 23:34:17 GMT
ENV MEMCACHED_SHA1=5d6c85fe15b5e575a563ec1bbeb01020e0132958
# Mon, 02 Oct 2017 23:37:42 GMT
RUN set -x 		&& buildDeps=' 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libsasl2-dev 		make 		perl 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark manual 		libevent-2.0-5 		libsasl2-2 	&& apt-get purge -y --auto-remove $buildDeps 		&& memcached -V
# Mon, 02 Oct 2017 23:37:42 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Mon, 02 Oct 2017 23:37:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 02 Oct 2017 23:37:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Oct 2017 23:37:43 GMT
USER [memcache]
# Mon, 02 Oct 2017 23:37:43 GMT
EXPOSE 11211/tcp
# Mon, 02 Oct 2017 23:37:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:afeb2bfd31c0760573e7262de6ae67a84da0e0a1c3e8157bbddd41a501b18a5c`  
		Last Modified: Thu, 07 Sep 2017 23:21:35 GMT  
		Size: 22.5 MB (22488057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2071de9f4eeec05d24d79982d276e34b21a0eb47d684e8a0f6ff216920f9dbd4`  
		Last Modified: Tue, 19 Sep 2017 01:45:07 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:801d526779aa5e4db381451fee28dddaf024b196b4e47e650e0a9dab5be352f6`  
		Last Modified: Mon, 02 Oct 2017 23:41:29 GMT  
		Size: 2.8 MB (2765454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1e66690632d0cc88a2f5f9831610c92124dcb7d380f3440e45b514f9030540`  
		Last Modified: Mon, 02 Oct 2017 23:41:28 GMT  
		Size: 296.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8235e6c84810a2b4c784bda57cd75121ab29a9db450008525d7d025813d615b9`  
		Last Modified: Mon, 02 Oct 2017 23:41:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.5.2` - linux; arm variant v7

```console
$ docker pull memcached@sha256:45117fc1ab5b256104f1a7da099e8dedfee8b0632ca63b5c0b1940b4c171761c
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.8 MB (21849606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa094160687b7a04b422d5236b2a1b3a5f55f3461564d84fe7005508db21fdc2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 27 Sep 2017 04:14:53 GMT
ADD file:c64f62f8baccded9d94037c0935c477d3dd18839a9c4e565679657d4c9df92c8 in / 
# Wed, 27 Sep 2017 04:14:53 GMT
CMD ["bash"]
# Thu, 28 Sep 2017 17:33:00 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Tue, 03 Oct 2017 04:58:40 GMT
ENV MEMCACHED_VERSION=1.5.2
# Tue, 03 Oct 2017 04:58:41 GMT
ENV MEMCACHED_SHA1=5d6c85fe15b5e575a563ec1bbeb01020e0132958
# Tue, 03 Oct 2017 05:09:21 GMT
RUN set -x 		&& buildDeps=' 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libsasl2-dev 		make 		perl 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark manual 		libevent-2.0-5 		libsasl2-2 	&& apt-get purge -y --auto-remove $buildDeps 		&& memcached -V
# Tue, 03 Oct 2017 05:09:22 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Tue, 03 Oct 2017 05:09:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 03 Oct 2017 05:09:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Oct 2017 05:09:28 GMT
USER [memcache]
# Tue, 03 Oct 2017 05:09:28 GMT
EXPOSE 11211/tcp
# Tue, 03 Oct 2017 05:09:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f6b0b1de175bfd1f4139472dafaeed39d43c5c14f6f48f113c9053f9b7837ddf`  
		Last Modified: Wed, 27 Sep 2017 04:20:52 GMT  
		Size: 19.3 MB (19276815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f5ecc5bf4596151966ea59e07f6ad9872eea9f0425d607ad70cc9f8098735d`  
		Last Modified: Thu, 28 Sep 2017 18:04:32 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec9465bec05809fbab31cd4def5bdd9eaeaffa172b78595641978d6cec7132d7`  
		Last Modified: Tue, 03 Oct 2017 05:09:53 GMT  
		Size: 2.6 MB (2570630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95b2e3141b98b19f4a9686a2b3b62c01b11022c89f6c794235606b33a1a590c2`  
		Last Modified: Tue, 03 Oct 2017 05:09:48 GMT  
		Size: 297.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d8bbdd412eae144399fb049bd999c8897ee07ffc72311e44077de4e43a274c`  
		Last Modified: Tue, 03 Oct 2017 05:09:48 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.5.2` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:ca66586f1ab5c5447946aa59801e147be829e6335bb5ad3af626201b23acb110
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 MB (22966658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0db14e99e7f68b4de82b214f77333a9e62cda1d5622c220873170a06299e6a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Sep 2017 17:29:09 GMT
ADD file:16391f421551b998f1ff496c48dc67f34dd2003077158fd1af78a898ea367e1d in / 
# Fri, 08 Sep 2017 17:29:10 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 21:28:53 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Tue, 03 Oct 2017 02:47:39 GMT
ENV MEMCACHED_VERSION=1.5.2
# Tue, 03 Oct 2017 02:47:39 GMT
ENV MEMCACHED_SHA1=5d6c85fe15b5e575a563ec1bbeb01020e0132958
# Tue, 03 Oct 2017 02:52:55 GMT
RUN set -x 		&& buildDeps=' 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libsasl2-dev 		make 		perl 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark manual 		libevent-2.0-5 		libsasl2-2 	&& apt-get purge -y --auto-remove $buildDeps 		&& memcached -V
# Tue, 03 Oct 2017 02:52:56 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Tue, 03 Oct 2017 02:52:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 03 Oct 2017 02:52:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Oct 2017 02:52:58 GMT
USER [memcache]
# Tue, 03 Oct 2017 02:52:59 GMT
EXPOSE 11211/tcp
# Tue, 03 Oct 2017 02:52:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0bd6dbb95c7a219839ea8345519110bbccc30c113a72119bbd92c7fe2a3f1e78`  
		Last Modified: Fri, 08 Sep 2017 17:43:38 GMT  
		Size: 20.3 MB (20337273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6665fa1f2e9808b2c4b49d3e92a04338a3e5dbe26dcf2902b5fbb42db9a8221a`  
		Last Modified: Fri, 08 Sep 2017 21:35:34 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d34c0041837ca9b08e74f897f629b5ce97270f9901f7db73b645e218274b02e`  
		Last Modified: Tue, 03 Oct 2017 02:53:27 GMT  
		Size: 2.6 MB (2627226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525ee33bdf80f9245b2a3527d578353460bc159dad068bd1e0ec792c6affbaae`  
		Last Modified: Tue, 03 Oct 2017 02:53:25 GMT  
		Size: 294.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5d789c03941afc108cef42254d041beb203b409220bc34cd631eef2ab503be`  
		Last Modified: Tue, 03 Oct 2017 02:53:25 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.5.2` - linux; ppc64le

```console
$ docker pull memcached@sha256:343d8ae081ca1106c325d6cf0a19c3c2acc340270ec19812eea1f2d1f3cbe9f3
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 MB (25490680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c42934e8960fce51082f73a170eed1d762d8fcc84d657c18a05671009236d67e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Sep 2017 00:34:22 GMT
ADD file:1422f50e4e998477f6c3b2fcee6853da10eb8bca7926ec70e494ff485f6284d7 in / 
# Fri, 08 Sep 2017 00:34:22 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 01:18:55 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Tue, 03 Oct 2017 00:33:25 GMT
ENV MEMCACHED_VERSION=1.5.2
# Tue, 03 Oct 2017 00:33:28 GMT
ENV MEMCACHED_SHA1=5d6c85fe15b5e575a563ec1bbeb01020e0132958
# Tue, 03 Oct 2017 00:45:44 GMT
RUN set -x 		&& buildDeps=' 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libsasl2-dev 		make 		perl 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark manual 		libevent-2.0-5 		libsasl2-2 	&& apt-get purge -y --auto-remove $buildDeps 		&& memcached -V
# Tue, 03 Oct 2017 00:45:47 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Tue, 03 Oct 2017 00:45:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 03 Oct 2017 00:45:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Oct 2017 00:45:57 GMT
USER [memcache]
# Tue, 03 Oct 2017 00:45:59 GMT
EXPOSE 11211/tcp
# Tue, 03 Oct 2017 00:46:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7ff7f6fdf12a09feca6f75b5d90b860059bdccf4185a9dab7c2c5b9e6e90123a`  
		Last Modified: Fri, 08 Sep 2017 00:41:42 GMT  
		Size: 22.7 MB (22746060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1a3601d5bf8b21acd6372ae2e68d3aff208607075ac8ddcc4bbb996536673c`  
		Last Modified: Fri, 08 Sep 2017 01:22:42 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddfd59f2c72998bac21ef7ff3276fd6303cff7d7b07c7b2d1d0cf06098aef552`  
		Last Modified: Tue, 03 Oct 2017 00:46:16 GMT  
		Size: 2.7 MB (2742459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1efc5ab41850a9bc0069e6acf3055cd6300c5104b7128cdb08e97e7bb7439940`  
		Last Modified: Tue, 03 Oct 2017 00:46:15 GMT  
		Size: 298.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b0682fdbd5b9156c013ad0865f56422b00ddd745ec9c0c66770cd06e18b9e5`  
		Last Modified: Tue, 03 Oct 2017 00:46:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.5.2` - linux; s390x

```console
$ docker pull memcached@sha256:dec16560e75f8919ffff35bf442e5408afbf9c54862ab84503ad72ca798ab171
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25137947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bb3ed29f5a6f058f29a7c8983723edb4d73460e7ad7c7e7712e0a205ed67696`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Sep 2017 05:23:00 GMT
ADD file:9b074cf37adfa815e3a6b300f8652eb77a06cfeea3f74fd021795cff318ca2ce in / 
# Fri, 08 Sep 2017 05:23:00 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 06:14:47 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Tue, 03 Oct 2017 17:33:26 GMT
ENV MEMCACHED_VERSION=1.5.2
# Tue, 03 Oct 2017 17:33:27 GMT
ENV MEMCACHED_SHA1=5d6c85fe15b5e575a563ec1bbeb01020e0132958
# Tue, 03 Oct 2017 17:37:12 GMT
RUN set -x 		&& buildDeps=' 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libsasl2-dev 		make 		perl 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark manual 		libevent-2.0-5 		libsasl2-2 	&& apt-get purge -y --auto-remove $buildDeps 		&& memcached -V
# Tue, 03 Oct 2017 17:37:13 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Tue, 03 Oct 2017 17:37:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 03 Oct 2017 17:37:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Oct 2017 17:37:14 GMT
USER [memcache]
# Tue, 03 Oct 2017 17:37:14 GMT
EXPOSE 11211/tcp
# Tue, 03 Oct 2017 17:37:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a3a3449ff754d3a7e8f189d020e507ff2cb0fd172b4240ca2d1d78e2d65d544`  
		Last Modified: Fri, 08 Sep 2017 05:27:12 GMT  
		Size: 22.3 MB (22338151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224b6ce1a0dc831e8b9f4e624f804d0284ddee9b709f63c77ad96a08b244d884`  
		Last Modified: Fri, 08 Sep 2017 06:18:24 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e3b6b53bafc260659b45815f23269d235963995672bb68e5702405e5434fbc`  
		Last Modified: Tue, 03 Oct 2017 17:37:23 GMT  
		Size: 2.8 MB (2797638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270326384f346a86137654a3e86c3514352aa2fe2f70d1f873331b595f887547`  
		Last Modified: Tue, 03 Oct 2017 17:37:23 GMT  
		Size: 297.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8428e5eed7f1348d7537eac0cfd1aed1d7937ef003ff16a597b5999a5c941a28`  
		Last Modified: Tue, 03 Oct 2017 17:37:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1.5.2-alpine`

```console
$ docker pull memcached@sha256:a3ba0e45d31ce60450a7579e914bf900e6ff65baa5c200e5c52fbc9c3078e587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `memcached:1.5.2-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:e9e671f5411bc07354fe6e1806c5686527a743ca97ddc4e42877027ca71ebbcb
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3725518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebfb8def40f93f4a05a53be25cb633d4c1cd206d51478880509f2b2868960fdf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Sep 2017 14:32:25 GMT
ADD file:4583e12bf5caec40b861a3409f2a1624c3f3556cc457edb99c9707f00e779e45 in / 
# Wed, 13 Sep 2017 14:32:26 GMT
CMD ["/bin/sh"]
# Tue, 19 Sep 2017 01:41:38 GMT
RUN adduser -D memcache
# Mon, 02 Oct 2017 23:37:58 GMT
ENV MEMCACHED_VERSION=1.5.2
# Mon, 02 Oct 2017 23:37:58 GMT
ENV MEMCACHED_SHA1=5d6c85fe15b5e575a563ec1bbeb01020e0132958
# Mon, 02 Oct 2017 23:41:10 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		libressl 		linux-headers 		make 		perl 		perl-utils 		tar 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --virtual .memcached-rundeps $runDeps 	&& apk del .build-deps 		&& memcached -V
# Mon, 02 Oct 2017 23:41:10 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Mon, 02 Oct 2017 23:41:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 02 Oct 2017 23:41:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Oct 2017 23:41:11 GMT
USER [memcache]
# Mon, 02 Oct 2017 23:41:11 GMT
EXPOSE 11211/tcp
# Mon, 02 Oct 2017 23:41:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:88286f41530e93dffd4b964e1db22ce4939fffa4a4c665dab8591fbab03d4926`  
		Last Modified: Tue, 27 Jun 2017 18:49:37 GMT  
		Size: 2.0 MB (1990402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5342366c11be2dc0ad25a1e84eedb96da23a1d63c55378df80d256b737b91664`  
		Last Modified: Tue, 19 Sep 2017 01:45:30 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df2e26817956fadfaea406fe860115c6de076483607c8799fab2077e5f1e0916`  
		Last Modified: Mon, 02 Oct 2017 23:41:56 GMT  
		Size: 1.7 MB (1733467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa96d76da4bfd4db47a5d2a04e6e87f5f5ec9111b0cb2b0099422f4f21f77e10`  
		Last Modified: Mon, 02 Oct 2017 23:41:55 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d641f7cd319b96a7e84fea23fbdc38e2a964f1f17a6b81c3bbfba286e7cd90c9`  
		Last Modified: Mon, 02 Oct 2017 23:41:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1.5-alpine`

```console
$ docker pull memcached@sha256:a3ba0e45d31ce60450a7579e914bf900e6ff65baa5c200e5c52fbc9c3078e587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `memcached:1.5-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:e9e671f5411bc07354fe6e1806c5686527a743ca97ddc4e42877027ca71ebbcb
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3725518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebfb8def40f93f4a05a53be25cb633d4c1cd206d51478880509f2b2868960fdf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Sep 2017 14:32:25 GMT
ADD file:4583e12bf5caec40b861a3409f2a1624c3f3556cc457edb99c9707f00e779e45 in / 
# Wed, 13 Sep 2017 14:32:26 GMT
CMD ["/bin/sh"]
# Tue, 19 Sep 2017 01:41:38 GMT
RUN adduser -D memcache
# Mon, 02 Oct 2017 23:37:58 GMT
ENV MEMCACHED_VERSION=1.5.2
# Mon, 02 Oct 2017 23:37:58 GMT
ENV MEMCACHED_SHA1=5d6c85fe15b5e575a563ec1bbeb01020e0132958
# Mon, 02 Oct 2017 23:41:10 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		libressl 		linux-headers 		make 		perl 		perl-utils 		tar 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --virtual .memcached-rundeps $runDeps 	&& apk del .build-deps 		&& memcached -V
# Mon, 02 Oct 2017 23:41:10 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Mon, 02 Oct 2017 23:41:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 02 Oct 2017 23:41:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Oct 2017 23:41:11 GMT
USER [memcache]
# Mon, 02 Oct 2017 23:41:11 GMT
EXPOSE 11211/tcp
# Mon, 02 Oct 2017 23:41:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:88286f41530e93dffd4b964e1db22ce4939fffa4a4c665dab8591fbab03d4926`  
		Last Modified: Tue, 27 Jun 2017 18:49:37 GMT  
		Size: 2.0 MB (1990402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5342366c11be2dc0ad25a1e84eedb96da23a1d63c55378df80d256b737b91664`  
		Last Modified: Tue, 19 Sep 2017 01:45:30 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df2e26817956fadfaea406fe860115c6de076483607c8799fab2077e5f1e0916`  
		Last Modified: Mon, 02 Oct 2017 23:41:56 GMT  
		Size: 1.7 MB (1733467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa96d76da4bfd4db47a5d2a04e6e87f5f5ec9111b0cb2b0099422f4f21f77e10`  
		Last Modified: Mon, 02 Oct 2017 23:41:55 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d641f7cd319b96a7e84fea23fbdc38e2a964f1f17a6b81c3bbfba286e7cd90c9`  
		Last Modified: Mon, 02 Oct 2017 23:41:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:a3ba0e45d31ce60450a7579e914bf900e6ff65baa5c200e5c52fbc9c3078e587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `memcached:1-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:e9e671f5411bc07354fe6e1806c5686527a743ca97ddc4e42877027ca71ebbcb
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3725518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebfb8def40f93f4a05a53be25cb633d4c1cd206d51478880509f2b2868960fdf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Sep 2017 14:32:25 GMT
ADD file:4583e12bf5caec40b861a3409f2a1624c3f3556cc457edb99c9707f00e779e45 in / 
# Wed, 13 Sep 2017 14:32:26 GMT
CMD ["/bin/sh"]
# Tue, 19 Sep 2017 01:41:38 GMT
RUN adduser -D memcache
# Mon, 02 Oct 2017 23:37:58 GMT
ENV MEMCACHED_VERSION=1.5.2
# Mon, 02 Oct 2017 23:37:58 GMT
ENV MEMCACHED_SHA1=5d6c85fe15b5e575a563ec1bbeb01020e0132958
# Mon, 02 Oct 2017 23:41:10 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		libressl 		linux-headers 		make 		perl 		perl-utils 		tar 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --virtual .memcached-rundeps $runDeps 	&& apk del .build-deps 		&& memcached -V
# Mon, 02 Oct 2017 23:41:10 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Mon, 02 Oct 2017 23:41:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 02 Oct 2017 23:41:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Oct 2017 23:41:11 GMT
USER [memcache]
# Mon, 02 Oct 2017 23:41:11 GMT
EXPOSE 11211/tcp
# Mon, 02 Oct 2017 23:41:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:88286f41530e93dffd4b964e1db22ce4939fffa4a4c665dab8591fbab03d4926`  
		Last Modified: Tue, 27 Jun 2017 18:49:37 GMT  
		Size: 2.0 MB (1990402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5342366c11be2dc0ad25a1e84eedb96da23a1d63c55378df80d256b737b91664`  
		Last Modified: Tue, 19 Sep 2017 01:45:30 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df2e26817956fadfaea406fe860115c6de076483607c8799fab2077e5f1e0916`  
		Last Modified: Mon, 02 Oct 2017 23:41:56 GMT  
		Size: 1.7 MB (1733467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa96d76da4bfd4db47a5d2a04e6e87f5f5ec9111b0cb2b0099422f4f21f77e10`  
		Last Modified: Mon, 02 Oct 2017 23:41:55 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d641f7cd319b96a7e84fea23fbdc38e2a964f1f17a6b81c3bbfba286e7cd90c9`  
		Last Modified: Mon, 02 Oct 2017 23:41:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:alpine`

```console
$ docker pull memcached@sha256:a3ba0e45d31ce60450a7579e914bf900e6ff65baa5c200e5c52fbc9c3078e587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `memcached:alpine` - linux; amd64

```console
$ docker pull memcached@sha256:e9e671f5411bc07354fe6e1806c5686527a743ca97ddc4e42877027ca71ebbcb
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3725518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebfb8def40f93f4a05a53be25cb633d4c1cd206d51478880509f2b2868960fdf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Sep 2017 14:32:25 GMT
ADD file:4583e12bf5caec40b861a3409f2a1624c3f3556cc457edb99c9707f00e779e45 in / 
# Wed, 13 Sep 2017 14:32:26 GMT
CMD ["/bin/sh"]
# Tue, 19 Sep 2017 01:41:38 GMT
RUN adduser -D memcache
# Mon, 02 Oct 2017 23:37:58 GMT
ENV MEMCACHED_VERSION=1.5.2
# Mon, 02 Oct 2017 23:37:58 GMT
ENV MEMCACHED_SHA1=5d6c85fe15b5e575a563ec1bbeb01020e0132958
# Mon, 02 Oct 2017 23:41:10 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		libressl 		linux-headers 		make 		perl 		perl-utils 		tar 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --virtual .memcached-rundeps $runDeps 	&& apk del .build-deps 		&& memcached -V
# Mon, 02 Oct 2017 23:41:10 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Mon, 02 Oct 2017 23:41:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 02 Oct 2017 23:41:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Oct 2017 23:41:11 GMT
USER [memcache]
# Mon, 02 Oct 2017 23:41:11 GMT
EXPOSE 11211/tcp
# Mon, 02 Oct 2017 23:41:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:88286f41530e93dffd4b964e1db22ce4939fffa4a4c665dab8591fbab03d4926`  
		Last Modified: Tue, 27 Jun 2017 18:49:37 GMT  
		Size: 2.0 MB (1990402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5342366c11be2dc0ad25a1e84eedb96da23a1d63c55378df80d256b737b91664`  
		Last Modified: Tue, 19 Sep 2017 01:45:30 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df2e26817956fadfaea406fe860115c6de076483607c8799fab2077e5f1e0916`  
		Last Modified: Mon, 02 Oct 2017 23:41:56 GMT  
		Size: 1.7 MB (1733467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa96d76da4bfd4db47a5d2a04e6e87f5f5ec9111b0cb2b0099422f4f21f77e10`  
		Last Modified: Mon, 02 Oct 2017 23:41:55 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d641f7cd319b96a7e84fea23fbdc38e2a964f1f17a6b81c3bbfba286e7cd90c9`  
		Last Modified: Mon, 02 Oct 2017 23:41:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:latest`

```console
$ docker pull memcached@sha256:70e8f6136bfd18b73c03db481a328efbffe90d020b6a1b46bcca26c7a297071f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `memcached:latest` - linux; amd64

```console
$ docker pull memcached@sha256:1a7f4b7378450722e1fac00f3da78203aa9b29a33c3fe64a27154ada65f8c46b
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 MB (25255674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed85c5f97e4a3071fc18ddaa41c6fbc4fe64f9f6e16c15e8b31b38389e91f40a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Sep 2017 08:41:48 GMT
ADD file:2bc9df54d28d9ec75722f6748834a1aea0baf089047e86a541064c282246c300 in / 
# Wed, 13 Sep 2017 08:41:49 GMT
CMD ["bash"]
# Tue, 19 Sep 2017 01:37:55 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Mon, 02 Oct 2017 23:34:17 GMT
ENV MEMCACHED_VERSION=1.5.2
# Mon, 02 Oct 2017 23:34:17 GMT
ENV MEMCACHED_SHA1=5d6c85fe15b5e575a563ec1bbeb01020e0132958
# Mon, 02 Oct 2017 23:37:42 GMT
RUN set -x 		&& buildDeps=' 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libsasl2-dev 		make 		perl 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark manual 		libevent-2.0-5 		libsasl2-2 	&& apt-get purge -y --auto-remove $buildDeps 		&& memcached -V
# Mon, 02 Oct 2017 23:37:42 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Mon, 02 Oct 2017 23:37:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 02 Oct 2017 23:37:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Oct 2017 23:37:43 GMT
USER [memcache]
# Mon, 02 Oct 2017 23:37:43 GMT
EXPOSE 11211/tcp
# Mon, 02 Oct 2017 23:37:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:afeb2bfd31c0760573e7262de6ae67a84da0e0a1c3e8157bbddd41a501b18a5c`  
		Last Modified: Thu, 07 Sep 2017 23:21:35 GMT  
		Size: 22.5 MB (22488057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2071de9f4eeec05d24d79982d276e34b21a0eb47d684e8a0f6ff216920f9dbd4`  
		Last Modified: Tue, 19 Sep 2017 01:45:07 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:801d526779aa5e4db381451fee28dddaf024b196b4e47e650e0a9dab5be352f6`  
		Last Modified: Mon, 02 Oct 2017 23:41:29 GMT  
		Size: 2.8 MB (2765454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1e66690632d0cc88a2f5f9831610c92124dcb7d380f3440e45b514f9030540`  
		Last Modified: Mon, 02 Oct 2017 23:41:28 GMT  
		Size: 296.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8235e6c84810a2b4c784bda57cd75121ab29a9db450008525d7d025813d615b9`  
		Last Modified: Mon, 02 Oct 2017 23:41:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; arm variant v7

```console
$ docker pull memcached@sha256:45117fc1ab5b256104f1a7da099e8dedfee8b0632ca63b5c0b1940b4c171761c
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.8 MB (21849606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa094160687b7a04b422d5236b2a1b3a5f55f3461564d84fe7005508db21fdc2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 27 Sep 2017 04:14:53 GMT
ADD file:c64f62f8baccded9d94037c0935c477d3dd18839a9c4e565679657d4c9df92c8 in / 
# Wed, 27 Sep 2017 04:14:53 GMT
CMD ["bash"]
# Thu, 28 Sep 2017 17:33:00 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Tue, 03 Oct 2017 04:58:40 GMT
ENV MEMCACHED_VERSION=1.5.2
# Tue, 03 Oct 2017 04:58:41 GMT
ENV MEMCACHED_SHA1=5d6c85fe15b5e575a563ec1bbeb01020e0132958
# Tue, 03 Oct 2017 05:09:21 GMT
RUN set -x 		&& buildDeps=' 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libsasl2-dev 		make 		perl 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark manual 		libevent-2.0-5 		libsasl2-2 	&& apt-get purge -y --auto-remove $buildDeps 		&& memcached -V
# Tue, 03 Oct 2017 05:09:22 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Tue, 03 Oct 2017 05:09:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 03 Oct 2017 05:09:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Oct 2017 05:09:28 GMT
USER [memcache]
# Tue, 03 Oct 2017 05:09:28 GMT
EXPOSE 11211/tcp
# Tue, 03 Oct 2017 05:09:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f6b0b1de175bfd1f4139472dafaeed39d43c5c14f6f48f113c9053f9b7837ddf`  
		Last Modified: Wed, 27 Sep 2017 04:20:52 GMT  
		Size: 19.3 MB (19276815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f5ecc5bf4596151966ea59e07f6ad9872eea9f0425d607ad70cc9f8098735d`  
		Last Modified: Thu, 28 Sep 2017 18:04:32 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec9465bec05809fbab31cd4def5bdd9eaeaffa172b78595641978d6cec7132d7`  
		Last Modified: Tue, 03 Oct 2017 05:09:53 GMT  
		Size: 2.6 MB (2570630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95b2e3141b98b19f4a9686a2b3b62c01b11022c89f6c794235606b33a1a590c2`  
		Last Modified: Tue, 03 Oct 2017 05:09:48 GMT  
		Size: 297.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d8bbdd412eae144399fb049bd999c8897ee07ffc72311e44077de4e43a274c`  
		Last Modified: Tue, 03 Oct 2017 05:09:48 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:ca66586f1ab5c5447946aa59801e147be829e6335bb5ad3af626201b23acb110
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 MB (22966658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0db14e99e7f68b4de82b214f77333a9e62cda1d5622c220873170a06299e6a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Sep 2017 17:29:09 GMT
ADD file:16391f421551b998f1ff496c48dc67f34dd2003077158fd1af78a898ea367e1d in / 
# Fri, 08 Sep 2017 17:29:10 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 21:28:53 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Tue, 03 Oct 2017 02:47:39 GMT
ENV MEMCACHED_VERSION=1.5.2
# Tue, 03 Oct 2017 02:47:39 GMT
ENV MEMCACHED_SHA1=5d6c85fe15b5e575a563ec1bbeb01020e0132958
# Tue, 03 Oct 2017 02:52:55 GMT
RUN set -x 		&& buildDeps=' 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libsasl2-dev 		make 		perl 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark manual 		libevent-2.0-5 		libsasl2-2 	&& apt-get purge -y --auto-remove $buildDeps 		&& memcached -V
# Tue, 03 Oct 2017 02:52:56 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Tue, 03 Oct 2017 02:52:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 03 Oct 2017 02:52:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Oct 2017 02:52:58 GMT
USER [memcache]
# Tue, 03 Oct 2017 02:52:59 GMT
EXPOSE 11211/tcp
# Tue, 03 Oct 2017 02:52:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0bd6dbb95c7a219839ea8345519110bbccc30c113a72119bbd92c7fe2a3f1e78`  
		Last Modified: Fri, 08 Sep 2017 17:43:38 GMT  
		Size: 20.3 MB (20337273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6665fa1f2e9808b2c4b49d3e92a04338a3e5dbe26dcf2902b5fbb42db9a8221a`  
		Last Modified: Fri, 08 Sep 2017 21:35:34 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d34c0041837ca9b08e74f897f629b5ce97270f9901f7db73b645e218274b02e`  
		Last Modified: Tue, 03 Oct 2017 02:53:27 GMT  
		Size: 2.6 MB (2627226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525ee33bdf80f9245b2a3527d578353460bc159dad068bd1e0ec792c6affbaae`  
		Last Modified: Tue, 03 Oct 2017 02:53:25 GMT  
		Size: 294.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5d789c03941afc108cef42254d041beb203b409220bc34cd631eef2ab503be`  
		Last Modified: Tue, 03 Oct 2017 02:53:25 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:343d8ae081ca1106c325d6cf0a19c3c2acc340270ec19812eea1f2d1f3cbe9f3
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 MB (25490680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c42934e8960fce51082f73a170eed1d762d8fcc84d657c18a05671009236d67e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Sep 2017 00:34:22 GMT
ADD file:1422f50e4e998477f6c3b2fcee6853da10eb8bca7926ec70e494ff485f6284d7 in / 
# Fri, 08 Sep 2017 00:34:22 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 01:18:55 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Tue, 03 Oct 2017 00:33:25 GMT
ENV MEMCACHED_VERSION=1.5.2
# Tue, 03 Oct 2017 00:33:28 GMT
ENV MEMCACHED_SHA1=5d6c85fe15b5e575a563ec1bbeb01020e0132958
# Tue, 03 Oct 2017 00:45:44 GMT
RUN set -x 		&& buildDeps=' 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libsasl2-dev 		make 		perl 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark manual 		libevent-2.0-5 		libsasl2-2 	&& apt-get purge -y --auto-remove $buildDeps 		&& memcached -V
# Tue, 03 Oct 2017 00:45:47 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Tue, 03 Oct 2017 00:45:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 03 Oct 2017 00:45:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Oct 2017 00:45:57 GMT
USER [memcache]
# Tue, 03 Oct 2017 00:45:59 GMT
EXPOSE 11211/tcp
# Tue, 03 Oct 2017 00:46:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7ff7f6fdf12a09feca6f75b5d90b860059bdccf4185a9dab7c2c5b9e6e90123a`  
		Last Modified: Fri, 08 Sep 2017 00:41:42 GMT  
		Size: 22.7 MB (22746060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1a3601d5bf8b21acd6372ae2e68d3aff208607075ac8ddcc4bbb996536673c`  
		Last Modified: Fri, 08 Sep 2017 01:22:42 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddfd59f2c72998bac21ef7ff3276fd6303cff7d7b07c7b2d1d0cf06098aef552`  
		Last Modified: Tue, 03 Oct 2017 00:46:16 GMT  
		Size: 2.7 MB (2742459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1efc5ab41850a9bc0069e6acf3055cd6300c5104b7128cdb08e97e7bb7439940`  
		Last Modified: Tue, 03 Oct 2017 00:46:15 GMT  
		Size: 298.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b0682fdbd5b9156c013ad0865f56422b00ddd745ec9c0c66770cd06e18b9e5`  
		Last Modified: Tue, 03 Oct 2017 00:46:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:dec16560e75f8919ffff35bf442e5408afbf9c54862ab84503ad72ca798ab171
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25137947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bb3ed29f5a6f058f29a7c8983723edb4d73460e7ad7c7e7712e0a205ed67696`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Sep 2017 05:23:00 GMT
ADD file:9b074cf37adfa815e3a6b300f8652eb77a06cfeea3f74fd021795cff318ca2ce in / 
# Fri, 08 Sep 2017 05:23:00 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 06:14:47 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Tue, 03 Oct 2017 17:33:26 GMT
ENV MEMCACHED_VERSION=1.5.2
# Tue, 03 Oct 2017 17:33:27 GMT
ENV MEMCACHED_SHA1=5d6c85fe15b5e575a563ec1bbeb01020e0132958
# Tue, 03 Oct 2017 17:37:12 GMT
RUN set -x 		&& buildDeps=' 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libsasl2-dev 		make 		perl 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark manual 		libevent-2.0-5 		libsasl2-2 	&& apt-get purge -y --auto-remove $buildDeps 		&& memcached -V
# Tue, 03 Oct 2017 17:37:13 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Tue, 03 Oct 2017 17:37:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 03 Oct 2017 17:37:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Oct 2017 17:37:14 GMT
USER [memcache]
# Tue, 03 Oct 2017 17:37:14 GMT
EXPOSE 11211/tcp
# Tue, 03 Oct 2017 17:37:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a3a3449ff754d3a7e8f189d020e507ff2cb0fd172b4240ca2d1d78e2d65d544`  
		Last Modified: Fri, 08 Sep 2017 05:27:12 GMT  
		Size: 22.3 MB (22338151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224b6ce1a0dc831e8b9f4e624f804d0284ddee9b709f63c77ad96a08b244d884`  
		Last Modified: Fri, 08 Sep 2017 06:18:24 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e3b6b53bafc260659b45815f23269d235963995672bb68e5702405e5434fbc`  
		Last Modified: Tue, 03 Oct 2017 17:37:23 GMT  
		Size: 2.8 MB (2797638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270326384f346a86137654a3e86c3514352aa2fe2f70d1f873331b595f887547`  
		Last Modified: Tue, 03 Oct 2017 17:37:23 GMT  
		Size: 297.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8428e5eed7f1348d7537eac0cfd1aed1d7937ef003ff16a597b5999a5c941a28`  
		Last Modified: Tue, 03 Oct 2017 17:37:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
