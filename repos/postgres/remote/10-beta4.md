## `postgres:10-beta4`

```console
$ docker pull postgres@sha256:d61f0309971e5649ffe3883493ecb55c1e66d592c649ef6dd194f1374cf2e29f
```

-	Platforms:
	-	linux; amd64

### `postgres:10-beta4` - linux; amd64

-	Docker Version: 17.03.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117643603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3b29315e222789347485c3a903721893e1523310f37c1c46f0e91ca8a7c112`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 24 Jul 2017 16:52:54 GMT
ADD file:ebba725fb97cea45d0b1b35ccc8144e766fcfc9a78530465c23b0c4674b14042 in / 
# Mon, 24 Jul 2017 16:52:55 GMT
CMD ["bash"]
# Wed, 26 Jul 2017 08:44:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jul 2017 08:44:00 GMT
RUN groupadd -r postgres --gid=999 && useradd -r -g postgres --uid=999 postgres
# Wed, 26 Jul 2017 08:44:01 GMT
ENV GOSU_VERSION=1.7
# Wed, 26 Jul 2017 08:44:14 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Wed, 26 Jul 2017 08:44:19 GMT
RUN apt-get update && apt-get install -y locales && rm -rf /var/lib/apt/lists/* 	&& localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Wed, 26 Jul 2017 08:44:19 GMT
ENV LANG=en_US.utf8
# Wed, 26 Jul 2017 08:44:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 26 Jul 2017 08:44:23 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Wed, 26 Jul 2017 08:44:23 GMT
ENV PG_MAJOR=10
# Thu, 31 Aug 2017 18:14:21 GMT
ENV PG_VERSION=10~beta4-1.pgdg90+1
# Thu, 31 Aug 2017 18:14:22 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' $PG_MAJOR > /etc/apt/sources.list.d/pgdg.list
# Thu, 31 Aug 2017 18:14:57 GMT
RUN apt-get update 	&& apt-get install -y postgresql-common 	&& sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf 	&& apt-get install -y 		postgresql-$PG_MAJOR=$PG_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 31 Aug 2017 18:14:58 GMT
RUN mv -v /usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample /usr/share/postgresql/ 	&& ln -sv ../postgresql.conf.sample /usr/share/postgresql/$PG_MAJOR/ 	&& sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample
# Thu, 31 Aug 2017 18:14:59 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 31 Aug 2017 18:15:00 GMT
ENV PATH=/usr/lib/postgresql/10/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Aug 2017 18:15:00 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 31 Aug 2017 18:15:01 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA" # this 777 will be replaced by 700 at runtime (allows semi-arbitrary "--user" values)
# Thu, 31 Aug 2017 18:15:01 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 31 Aug 2017 18:15:02 GMT
COPY file:643bb6306366c6990a8d7cc47297e0080cc2a18a48a305868c51739e9416a044 in /usr/local/bin/ 
# Thu, 31 Aug 2017 18:15:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 31 Aug 2017 18:15:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 31 Aug 2017 18:15:04 GMT
EXPOSE 5432/tcp
# Thu, 31 Aug 2017 18:15:04 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:06b22ddb19134ec8c42aaabd3e2e9f5b378e4e53da4a8960eaaaa86351190af3`  
		Last Modified: Mon, 24 Jul 2017 16:59:30 GMT  
		Size: 45.1 MB (45142935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a89e9890c383465015499306a27143688020b186d8efa289d9e97670b8c60dc`  
		Last Modified: Wed, 26 Jul 2017 08:50:39 GMT  
		Size: 7.0 MB (7029499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ec871acfa2d70642e3044907f4c793fbb34bba761548a6557dcce41e72453c`  
		Last Modified: Wed, 26 Jul 2017 08:50:38 GMT  
		Size: 1.7 KB (1714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9332a355d3d73c1cfbc811504d3ed1cf2c5660ea8736467140cf3c4538c135e6`  
		Last Modified: Wed, 26 Jul 2017 08:50:36 GMT  
		Size: 1.3 MB (1275160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6675a5cbbf42cffc312e240b1a8286b4cadbe7057c730c81df3e4ae90fc2d13`  
		Last Modified: Wed, 26 Jul 2017 08:50:37 GMT  
		Size: 6.6 MB (6577473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30d0e64f9fe2ba9d7ff0aa91cfddadb79abfdc05a9523ac365496f35914b13c9`  
		Last Modified: Wed, 26 Jul 2017 08:50:35 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6df1120c4fd91d1cb826ee3406ebf7a0f03e3277756848e8bd4732271c5ee69`  
		Last Modified: Wed, 26 Jul 2017 08:50:37 GMT  
		Size: 4.5 KB (4470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432a643b24bc3d319344ea92ef16bfb9243f82f921f63f9569b5b5b4b09c7ece`  
		Last Modified: Thu, 31 Aug 2017 18:42:32 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc42ba9851dd1b7cca1555c5b241f104b8627d8be745d700b6eb3f4e3d11e4c`  
		Last Modified: Thu, 31 Aug 2017 18:42:45 GMT  
		Size: 57.6 MB (57602510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff6ef65e5e9b9d1f6efdc26ddf7649055ec8344a4dee47d679084f281d29837`  
		Last Modified: Thu, 31 Aug 2017 18:42:30 GMT  
		Size: 7.3 KB (7292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f7d96d3026d9b53b974458df586f9958fd8b9e203ab27f9273a3f2e09ce3a39`  
		Last Modified: Thu, 31 Aug 2017 18:42:30 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94be7274c8e0136f34e5657cb020433e5aeec4c053cab5b46f630d55c6403665`  
		Last Modified: Thu, 31 Aug 2017 18:42:30 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd0cf3eba78c3c1cc9459a28f335fcb6a86ff47a2f2c07ede79df63ae99599a`  
		Last Modified: Thu, 31 Aug 2017 18:42:30 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a29ff8f69cb52c4d59f9633756b274f21950b77da13e3d93e72f7ead2d366a`  
		Last Modified: Thu, 31 Aug 2017 18:42:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip