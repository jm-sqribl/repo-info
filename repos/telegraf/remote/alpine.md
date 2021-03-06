## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:47f64870817d225720bdd3a6e6c21d9fe2ba09ee59d1f19ee4444836b67e1dba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:9702dff7b000474b3f6dd1e3b126f649a976d964230f235a5d7d39d4744bcdcb
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12614100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:086ce6353001aa041d3b8e7d8312c08962ad5e6d9107fdbbb3e6f877f2dc5fed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 13 Sep 2017 14:32:20 GMT
ADD file:9d67752278c0e5a1298cd2d6603ebaaab2aa342e27ddf191ee0fde138f82698c in / 
# Wed, 13 Sep 2017 14:32:20 GMT
CMD ["/bin/sh"]
# Wed, 13 Sep 2017 15:12:34 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 14 Sep 2017 00:38:16 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools &&     update-ca-certificates
# Wed, 27 Sep 2017 17:02:51 GMT
ENV TELEGRAF_VERSION=1.4.1
# Wed, 27 Sep 2017 17:03:08 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget -q https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget -q https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/telegraf.conf /etc/telegraf/ &&     chmod +x /usr/src/telegraf*/* &&     cp -a /usr/src/telegraf*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 27 Sep 2017 17:03:12 GMT
EXPOSE 8092/udp 8094/tcp 8125/udp
# Wed, 27 Sep 2017 17:03:12 GMT
COPY file:43e6828e001b57ab465cff8dfd3d30830289afe7ca5944b61641956bfe38cd1c in /entrypoint.sh 
# Wed, 27 Sep 2017 17:03:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Sep 2017 17:03:12 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:019300c8a437a2d60248f27c206795930626dfe7ddc0323d734143bd5eb131a6`  
		Last Modified: Tue, 27 Jun 2017 18:48:47 GMT  
		Size: 2.0 MB (1970271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f86ea3a05bc091d3d70e7de3d61d06e961eaeb967c4e0c6060196f0dcdc42f`  
		Last Modified: Wed, 13 Sep 2017 15:14:01 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:533d12625f92f18763be93f4384313958baa2423c942b99b5f0194914c66f724`  
		Last Modified: Thu, 14 Sep 2017 00:39:13 GMT  
		Size: 1.8 MB (1771344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:869fbd2f91dfbe6aeee0343a4b801ad162049588673205321dbaab53d81bcd17`  
		Last Modified: Wed, 27 Sep 2017 17:03:54 GMT  
		Size: 8.9 MB (8872146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8395da71da1dc72d9b20c5d791cdca6f116cdf88bf82bac4515a38152fdd1214`  
		Last Modified: Wed, 27 Sep 2017 17:03:53 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
