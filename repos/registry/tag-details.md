<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `registry`

-	[`registry:2`](#registry2)
-	[`registry:2.5`](#registry25)
-	[`registry:2.5.2`](#registry252)
-	[`registry:2.6`](#registry26)
-	[`registry:2.6.2`](#registry262)
-	[`registry:latest`](#registrylatest)

## `registry:2`

```console
$ docker pull registry@sha256:0f8fe61fa337b8ef02217702ba979b47a7d68717d4628f31592ebff85915f3ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `registry:2` - linux; amd64

```console
$ docker pull registry@sha256:b5d514924c67e0c3e74bc79758e8ef099a293c8f0740b87043d0c348f1c09397
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10659516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28525f9a6e46bd6a033b3a3e5f5f64b28d93698b0a23cdb8d66b43b8d8e6b7c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 13 Sep 2017 14:32:15 GMT
ADD file:89e72bfc19e81624ba6a34bd5cecdf258750dc569ba03e17e3f4a286b1526461 in / 
# Wed, 13 Sep 2017 14:32:15 GMT
CMD ["/bin/sh"]
# Tue, 19 Sep 2017 07:25:41 GMT
RUN set -ex     && apk add --no-cache ca-certificates apache2-utils
# Tue, 19 Sep 2017 07:25:41 GMT
COPY file:b99d4fe47ad1addf0e8f244236e05177f3bfe9eb3ddd59f08b67b2612d77c621 in /bin/registry 
# Tue, 19 Sep 2017 07:25:42 GMT
COPY file:6c4758d509045dc45381fa2df2e7ffcc661afcaa29805c75f8f1976f2b016db8 in /etc/docker/registry/config.yml 
# Tue, 19 Sep 2017 07:25:42 GMT
VOLUME [/var/lib/registry]
# Tue, 19 Sep 2017 07:25:42 GMT
EXPOSE 5000/tcp
# Tue, 19 Sep 2017 07:25:42 GMT
COPY file:7b57f7ab1a8cf85c00768560fffc926543a60c9c9f7a2b172767dcc9a3203394 in /entrypoint.sh 
# Tue, 19 Sep 2017 07:25:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Sep 2017 07:25:43 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:90f4dba627d65ea3223761bcfe54e726337a919fe98117ef107914f91be657c9`  
		Last Modified: Tue, 27 Jun 2017 18:47:56 GMT  
		Size: 2.4 MB (2385007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e11d7b4f5e8e125dd203edcc6d7ba0d42e090b29584ba55a882e1cf4ddf4a1`  
		Last Modified: Tue, 19 Sep 2017 07:25:58 GMT  
		Size: 2.0 MB (2008548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f032f3c8932b01f4b7231e43f17dbd4bed7d6fcc5567959ae1aebcff675c904`  
		Last Modified: Tue, 19 Sep 2017 07:26:00 GMT  
		Size: 6.3 MB (6265373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425585e7aedb57b8e7a9974bd8995e7d91ee5beaf596c8eb46c28384fe14a5d8`  
		Last Modified: Tue, 19 Sep 2017 07:25:58 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45f535a83d27374934dcde157f5916195bdde43519d9c4e027d696b1f8742cd`  
		Last Modified: Tue, 19 Sep 2017 07:25:58 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `registry:2.5`

```console
$ docker pull registry@sha256:9a81c5445ea6f2559a430b1f0fae61ef906ed2ddb953c1b49bc5fee9af5c6480
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `registry:2.5` - linux; amd64

```console
$ docker pull registry@sha256:ad3ebae5732a16f44c19d6767bb502dac35120494e80bca784db00b9ac7ca6e8
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11185822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7cdb18beaf8ca7944007c31a97f63e351714ecc78fc2cbf719a5a5b9c52e835`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 13 Sep 2017 14:32:15 GMT
ADD file:89e72bfc19e81624ba6a34bd5cecdf258750dc569ba03e17e3f4a286b1526461 in / 
# Wed, 13 Sep 2017 14:32:15 GMT
CMD ["/bin/sh"]
# Tue, 19 Sep 2017 07:25:41 GMT
RUN set -ex     && apk add --no-cache ca-certificates apache2-utils
# Tue, 19 Sep 2017 07:25:48 GMT
COPY file:364dadf6b930d66cd0070df853eb93466796bc507fdba9bcba04e82476f55687 in /bin/registry 
# Tue, 19 Sep 2017 07:25:49 GMT
COPY file:6c4758d509045dc45381fa2df2e7ffcc661afcaa29805c75f8f1976f2b016db8 in /etc/docker/registry/config.yml 
# Tue, 19 Sep 2017 07:25:49 GMT
VOLUME [/var/lib/registry]
# Tue, 19 Sep 2017 07:25:49 GMT
EXPOSE 5000/tcp
# Tue, 19 Sep 2017 07:25:49 GMT
COPY file:7b57f7ab1a8cf85c00768560fffc926543a60c9c9f7a2b172767dcc9a3203394 in /entrypoint.sh 
# Tue, 19 Sep 2017 07:25:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Sep 2017 07:25:50 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:90f4dba627d65ea3223761bcfe54e726337a919fe98117ef107914f91be657c9`  
		Last Modified: Tue, 27 Jun 2017 18:47:56 GMT  
		Size: 2.4 MB (2385007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e11d7b4f5e8e125dd203edcc6d7ba0d42e090b29584ba55a882e1cf4ddf4a1`  
		Last Modified: Tue, 19 Sep 2017 07:25:58 GMT  
		Size: 2.0 MB (2008548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90640e092c9a632063e66648a75b9f0bc57e833429255f8512d820bf6adf933`  
		Last Modified: Tue, 19 Sep 2017 07:26:26 GMT  
		Size: 6.8 MB (6791683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b401ff2e3d73fe1a1082bc8820342bcda6f4b65caaf2f7bf4ff341c769de3b`  
		Last Modified: Tue, 19 Sep 2017 07:26:24 GMT  
		Size: 370.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:183fd265e5657eed2f1da2df6ac1d5ec70fea4cfe05d685f0ab3df75e328704b`  
		Last Modified: Tue, 19 Sep 2017 07:26:24 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `registry:2.5.2`

```console
$ docker pull registry@sha256:9a81c5445ea6f2559a430b1f0fae61ef906ed2ddb953c1b49bc5fee9af5c6480
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `registry:2.5.2` - linux; amd64

```console
$ docker pull registry@sha256:ad3ebae5732a16f44c19d6767bb502dac35120494e80bca784db00b9ac7ca6e8
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11185822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7cdb18beaf8ca7944007c31a97f63e351714ecc78fc2cbf719a5a5b9c52e835`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 13 Sep 2017 14:32:15 GMT
ADD file:89e72bfc19e81624ba6a34bd5cecdf258750dc569ba03e17e3f4a286b1526461 in / 
# Wed, 13 Sep 2017 14:32:15 GMT
CMD ["/bin/sh"]
# Tue, 19 Sep 2017 07:25:41 GMT
RUN set -ex     && apk add --no-cache ca-certificates apache2-utils
# Tue, 19 Sep 2017 07:25:48 GMT
COPY file:364dadf6b930d66cd0070df853eb93466796bc507fdba9bcba04e82476f55687 in /bin/registry 
# Tue, 19 Sep 2017 07:25:49 GMT
COPY file:6c4758d509045dc45381fa2df2e7ffcc661afcaa29805c75f8f1976f2b016db8 in /etc/docker/registry/config.yml 
# Tue, 19 Sep 2017 07:25:49 GMT
VOLUME [/var/lib/registry]
# Tue, 19 Sep 2017 07:25:49 GMT
EXPOSE 5000/tcp
# Tue, 19 Sep 2017 07:25:49 GMT
COPY file:7b57f7ab1a8cf85c00768560fffc926543a60c9c9f7a2b172767dcc9a3203394 in /entrypoint.sh 
# Tue, 19 Sep 2017 07:25:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Sep 2017 07:25:50 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:90f4dba627d65ea3223761bcfe54e726337a919fe98117ef107914f91be657c9`  
		Last Modified: Tue, 27 Jun 2017 18:47:56 GMT  
		Size: 2.4 MB (2385007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e11d7b4f5e8e125dd203edcc6d7ba0d42e090b29584ba55a882e1cf4ddf4a1`  
		Last Modified: Tue, 19 Sep 2017 07:25:58 GMT  
		Size: 2.0 MB (2008548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90640e092c9a632063e66648a75b9f0bc57e833429255f8512d820bf6adf933`  
		Last Modified: Tue, 19 Sep 2017 07:26:26 GMT  
		Size: 6.8 MB (6791683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b401ff2e3d73fe1a1082bc8820342bcda6f4b65caaf2f7bf4ff341c769de3b`  
		Last Modified: Tue, 19 Sep 2017 07:26:24 GMT  
		Size: 370.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:183fd265e5657eed2f1da2df6ac1d5ec70fea4cfe05d685f0ab3df75e328704b`  
		Last Modified: Tue, 19 Sep 2017 07:26:24 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `registry:2.6`

```console
$ docker pull registry@sha256:0f8fe61fa337b8ef02217702ba979b47a7d68717d4628f31592ebff85915f3ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `registry:2.6` - linux; amd64

```console
$ docker pull registry@sha256:b5d514924c67e0c3e74bc79758e8ef099a293c8f0740b87043d0c348f1c09397
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10659516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28525f9a6e46bd6a033b3a3e5f5f64b28d93698b0a23cdb8d66b43b8d8e6b7c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 13 Sep 2017 14:32:15 GMT
ADD file:89e72bfc19e81624ba6a34bd5cecdf258750dc569ba03e17e3f4a286b1526461 in / 
# Wed, 13 Sep 2017 14:32:15 GMT
CMD ["/bin/sh"]
# Tue, 19 Sep 2017 07:25:41 GMT
RUN set -ex     && apk add --no-cache ca-certificates apache2-utils
# Tue, 19 Sep 2017 07:25:41 GMT
COPY file:b99d4fe47ad1addf0e8f244236e05177f3bfe9eb3ddd59f08b67b2612d77c621 in /bin/registry 
# Tue, 19 Sep 2017 07:25:42 GMT
COPY file:6c4758d509045dc45381fa2df2e7ffcc661afcaa29805c75f8f1976f2b016db8 in /etc/docker/registry/config.yml 
# Tue, 19 Sep 2017 07:25:42 GMT
VOLUME [/var/lib/registry]
# Tue, 19 Sep 2017 07:25:42 GMT
EXPOSE 5000/tcp
# Tue, 19 Sep 2017 07:25:42 GMT
COPY file:7b57f7ab1a8cf85c00768560fffc926543a60c9c9f7a2b172767dcc9a3203394 in /entrypoint.sh 
# Tue, 19 Sep 2017 07:25:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Sep 2017 07:25:43 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:90f4dba627d65ea3223761bcfe54e726337a919fe98117ef107914f91be657c9`  
		Last Modified: Tue, 27 Jun 2017 18:47:56 GMT  
		Size: 2.4 MB (2385007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e11d7b4f5e8e125dd203edcc6d7ba0d42e090b29584ba55a882e1cf4ddf4a1`  
		Last Modified: Tue, 19 Sep 2017 07:25:58 GMT  
		Size: 2.0 MB (2008548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f032f3c8932b01f4b7231e43f17dbd4bed7d6fcc5567959ae1aebcff675c904`  
		Last Modified: Tue, 19 Sep 2017 07:26:00 GMT  
		Size: 6.3 MB (6265373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425585e7aedb57b8e7a9974bd8995e7d91ee5beaf596c8eb46c28384fe14a5d8`  
		Last Modified: Tue, 19 Sep 2017 07:25:58 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45f535a83d27374934dcde157f5916195bdde43519d9c4e027d696b1f8742cd`  
		Last Modified: Tue, 19 Sep 2017 07:25:58 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `registry:2.6.2`

```console
$ docker pull registry@sha256:0f8fe61fa337b8ef02217702ba979b47a7d68717d4628f31592ebff85915f3ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `registry:2.6.2` - linux; amd64

```console
$ docker pull registry@sha256:b5d514924c67e0c3e74bc79758e8ef099a293c8f0740b87043d0c348f1c09397
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10659516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28525f9a6e46bd6a033b3a3e5f5f64b28d93698b0a23cdb8d66b43b8d8e6b7c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 13 Sep 2017 14:32:15 GMT
ADD file:89e72bfc19e81624ba6a34bd5cecdf258750dc569ba03e17e3f4a286b1526461 in / 
# Wed, 13 Sep 2017 14:32:15 GMT
CMD ["/bin/sh"]
# Tue, 19 Sep 2017 07:25:41 GMT
RUN set -ex     && apk add --no-cache ca-certificates apache2-utils
# Tue, 19 Sep 2017 07:25:41 GMT
COPY file:b99d4fe47ad1addf0e8f244236e05177f3bfe9eb3ddd59f08b67b2612d77c621 in /bin/registry 
# Tue, 19 Sep 2017 07:25:42 GMT
COPY file:6c4758d509045dc45381fa2df2e7ffcc661afcaa29805c75f8f1976f2b016db8 in /etc/docker/registry/config.yml 
# Tue, 19 Sep 2017 07:25:42 GMT
VOLUME [/var/lib/registry]
# Tue, 19 Sep 2017 07:25:42 GMT
EXPOSE 5000/tcp
# Tue, 19 Sep 2017 07:25:42 GMT
COPY file:7b57f7ab1a8cf85c00768560fffc926543a60c9c9f7a2b172767dcc9a3203394 in /entrypoint.sh 
# Tue, 19 Sep 2017 07:25:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Sep 2017 07:25:43 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:90f4dba627d65ea3223761bcfe54e726337a919fe98117ef107914f91be657c9`  
		Last Modified: Tue, 27 Jun 2017 18:47:56 GMT  
		Size: 2.4 MB (2385007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e11d7b4f5e8e125dd203edcc6d7ba0d42e090b29584ba55a882e1cf4ddf4a1`  
		Last Modified: Tue, 19 Sep 2017 07:25:58 GMT  
		Size: 2.0 MB (2008548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f032f3c8932b01f4b7231e43f17dbd4bed7d6fcc5567959ae1aebcff675c904`  
		Last Modified: Tue, 19 Sep 2017 07:26:00 GMT  
		Size: 6.3 MB (6265373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425585e7aedb57b8e7a9974bd8995e7d91ee5beaf596c8eb46c28384fe14a5d8`  
		Last Modified: Tue, 19 Sep 2017 07:25:58 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45f535a83d27374934dcde157f5916195bdde43519d9c4e027d696b1f8742cd`  
		Last Modified: Tue, 19 Sep 2017 07:25:58 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `registry:latest`

```console
$ docker pull registry@sha256:0f8fe61fa337b8ef02217702ba979b47a7d68717d4628f31592ebff85915f3ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `registry:latest` - linux; amd64

```console
$ docker pull registry@sha256:b5d514924c67e0c3e74bc79758e8ef099a293c8f0740b87043d0c348f1c09397
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10659516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28525f9a6e46bd6a033b3a3e5f5f64b28d93698b0a23cdb8d66b43b8d8e6b7c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 13 Sep 2017 14:32:15 GMT
ADD file:89e72bfc19e81624ba6a34bd5cecdf258750dc569ba03e17e3f4a286b1526461 in / 
# Wed, 13 Sep 2017 14:32:15 GMT
CMD ["/bin/sh"]
# Tue, 19 Sep 2017 07:25:41 GMT
RUN set -ex     && apk add --no-cache ca-certificates apache2-utils
# Tue, 19 Sep 2017 07:25:41 GMT
COPY file:b99d4fe47ad1addf0e8f244236e05177f3bfe9eb3ddd59f08b67b2612d77c621 in /bin/registry 
# Tue, 19 Sep 2017 07:25:42 GMT
COPY file:6c4758d509045dc45381fa2df2e7ffcc661afcaa29805c75f8f1976f2b016db8 in /etc/docker/registry/config.yml 
# Tue, 19 Sep 2017 07:25:42 GMT
VOLUME [/var/lib/registry]
# Tue, 19 Sep 2017 07:25:42 GMT
EXPOSE 5000/tcp
# Tue, 19 Sep 2017 07:25:42 GMT
COPY file:7b57f7ab1a8cf85c00768560fffc926543a60c9c9f7a2b172767dcc9a3203394 in /entrypoint.sh 
# Tue, 19 Sep 2017 07:25:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Sep 2017 07:25:43 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:90f4dba627d65ea3223761bcfe54e726337a919fe98117ef107914f91be657c9`  
		Last Modified: Tue, 27 Jun 2017 18:47:56 GMT  
		Size: 2.4 MB (2385007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e11d7b4f5e8e125dd203edcc6d7ba0d42e090b29584ba55a882e1cf4ddf4a1`  
		Last Modified: Tue, 19 Sep 2017 07:25:58 GMT  
		Size: 2.0 MB (2008548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f032f3c8932b01f4b7231e43f17dbd4bed7d6fcc5567959ae1aebcff675c904`  
		Last Modified: Tue, 19 Sep 2017 07:26:00 GMT  
		Size: 6.3 MB (6265373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425585e7aedb57b8e7a9974bd8995e7d91ee5beaf596c8eb46c28384fe14a5d8`  
		Last Modified: Tue, 19 Sep 2017 07:25:58 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45f535a83d27374934dcde157f5916195bdde43519d9c4e027d696b1f8742cd`  
		Last Modified: Tue, 19 Sep 2017 07:25:58 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
