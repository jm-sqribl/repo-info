## `traefik:alpine`

```console
$ docker pull traefik@sha256:882bd8f818de9437be8d8bf6c6eeddaa03f43ed92173c2bf2cb1017c8007c65b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `traefik:alpine` - linux; amd64

```console
$ docker pull traefik@sha256:2ee454e68fe274a1e6daf103bb051082179ebf449c24c3010da921a91dfa1e38
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15335648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d95023f9ce9e4b655a9b7cd61a94dfa1a17b21038b83fdb87859a6e0c1b15a5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 13 Sep 2017 14:32:25 GMT
ADD file:4583e12bf5caec40b861a3409f2a1624c3f3556cc457edb99c9707f00e779e45 in / 
# Wed, 13 Sep 2017 14:32:26 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2017 19:35:45 GMT
RUN apk --no-cache add ca-certificates
# Mon, 18 Sep 2017 19:36:14 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	apk add --no-cache --virtual .fetch-deps libressl; 	wget -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.3.8/traefik_linux-$arch"; 	apk del .fetch-deps; 	chmod +x /usr/local/bin/traefik
# Mon, 18 Sep 2017 19:36:15 GMT
COPY file:41f5bd1ea0a61e819b7d8c5489c305d4f2798046917dd6b6695318f555981727 in / 
# Mon, 18 Sep 2017 19:36:15 GMT
EXPOSE 80/tcp
# Mon, 18 Sep 2017 19:36:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Sep 2017 19:36:15 GMT
CMD ["traefik"]
# Mon, 18 Sep 2017 19:36:15 GMT
LABEL org.label-schema.vendor=Containous org.label-schema.url=https://traefik.io org.label-schema.name=Traefik org.label-schema.description=A modern reverse-proxy org.label-schema.version=v1.3.8 org.label-schema.docker.schema-version=1.0
```

-	Layers:
	-	`sha256:88286f41530e93dffd4b964e1db22ce4939fffa4a4c665dab8591fbab03d4926`  
		Last Modified: Tue, 27 Jun 2017 18:49:37 GMT  
		Size: 2.0 MB (1990402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690da7be984deafe90a6af23d8afd106994491a9c83c7914b48b31d056b063ca`  
		Last Modified: Mon, 18 Sep 2017 19:37:01 GMT  
		Size: 351.4 KB (351350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf4bd1966dd6bd12b2296c6d77fef149b96e6739897310350c2ace52dd5135b`  
		Last Modified: Mon, 18 Sep 2017 19:37:35 GMT  
		Size: 13.0 MB (12993555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fe078b14dae64bede97a388b2b38920330f351c95f75e9929dcae559ecf950`  
		Last Modified: Mon, 18 Sep 2017 19:37:32 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
