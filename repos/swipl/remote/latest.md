## `swipl:latest`

```console
$ docker pull swipl@sha256:cbfcf6976a86c76d73906ca10928ef9c32288ffdb1d5e91f17baf3ae9b202551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `swipl:latest` - linux; amd64

```console
$ docker pull swipl@sha256:c4ffbdfe11b0412e98d8f00c4b3353c1e0077b55a5bcadb4a668abb252390751
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50985431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22f2f02024c1cb4bde7b88320138b2b9f32b914ee6b4456ec2a1b627c8804a33`
-	Default Command: `["swipl"]`

```dockerfile
# Wed, 13 Sep 2017 08:41:48 GMT
ADD file:2bc9df54d28d9ec75722f6748834a1aea0baf089047e86a541064c282246c300 in / 
# Wed, 13 Sep 2017 08:41:49 GMT
CMD ["bash"]
# Wed, 13 Sep 2017 21:28:38 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Wed, 13 Sep 2017 21:28:51 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libarchive13     libgmp10     libossp-uuid16     libssl1.1     libdb5.3     libpcre3     libedit2     libgeos-c1v5     libspatialindex4v5     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient18 &&     rm -rf /var/lib/apt/lists/*
# Mon, 02 Oct 2017 17:57:09 GMT
RUN SWIPL_VER=7.7.0 &&     SWIPL_CHECKSUM=a1f603302fee12bfc390272ca76381401f5483c3a5521d391265404af58fdfcb &&     BUILD_DEPS='make gcc wget libarchive-dev libgmp-dev libossp-uuid-dev libpcre3-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev libgeos-dev libspatialindex-dev unixodbc-dev' &&     apt-get update && apt-get install -y --no-install-recommends $BUILD_DEPS &&     mkdir /tmp/src &&     cd /tmp/src &&     wget http://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz &&     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM &&     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM &&     tar -xzf swipl-$SWIPL_VER.tar.gz &&     cd swipl-$SWIPL_VER &&     cp build.templ build &&     sed -i '/PREFIX=$HOME/c\PREFIX=/swipl' build &&     sed -i '/# export DISABLE_PKGS/c\export DISABLE_PKGS="jpl xpce"' build &&     sed -i '/# export EXTRA_PKGS/c\export EXTRA_PKGS="db space"' build &&     chmod u+x build && ./build &&     apt-get purge -y --auto-remove $BUILD_DEPS &&     cd /usr/bin && rm -rf /tmp/src && ln -s /swipl/bin/swipl swipl && rm -rf /var/lib/apt/lists/*
# Mon, 02 Oct 2017 17:57:09 GMT
ENV LANG=C.UTF-8
# Mon, 02 Oct 2017 17:57:10 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:afeb2bfd31c0760573e7262de6ae67a84da0e0a1c3e8157bbddd41a501b18a5c`  
		Last Modified: Thu, 07 Sep 2017 23:21:35 GMT  
		Size: 22.5 MB (22488057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67aa1f6eaa9c07a4bbe9bff22dcf3000f0a8361615de82ffbe8d4db9afea29d8`  
		Last Modified: Wed, 13 Sep 2017 21:30:39 GMT  
		Size: 22.0 MB (22014782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88891ad82967cb952a5db1f1f2888b507925f2943defbd3a5f9d621cf83445a5`  
		Last Modified: Mon, 02 Oct 2017 17:57:29 GMT  
		Size: 6.5 MB (6482592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
