## `debian:rc-buggy`

```console
$ docker pull debian@sha256:760c35121fc92f3e1282bff3ae07d495d53c466db11fb2de1126dd69aefd46d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `debian:rc-buggy` - linux; amd64

```console
$ docker pull debian@sha256:598457c893927a87a6974d59c37584709c19ce32ee788b1bb4d17933506e657e
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47754082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:649de8b6696634867ef024213f78497e0362f3764c886569737a8097239b1ea7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 Sep 2017 08:41:20 GMT
ADD file:24ed5f5bb68abbeda1e34de4caa7be426978141c1664a5238107589d4038b5b0 in / 
# Wed, 13 Sep 2017 08:41:21 GMT
CMD ["bash"]
# Wed, 13 Sep 2017 08:42:24 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:82350343a6fef2218dcf962145f0ad627975bdd80329deb9ba552d2f787b0383`  
		Last Modified: Thu, 07 Sep 2017 23:14:32 GMT  
		Size: 47.8 MB (47753859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f77423dd25b61f32fbc4219d6f4e39721b3bb1ef93e257485082badb008ea17`  
		Last Modified: Wed, 13 Sep 2017 08:45:14 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v5

```console
$ docker pull debian@sha256:1c8a8eda677f68e9e7975285095d5bba489061e4652505e84151d4a64c642d80
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46234325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d0c7e4fad826ed4db931ccb32d63f216728be02043a0fa1467a57b1f691f79`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 27 Sep 2017 14:25:35 GMT
ADD file:fb7d9ba902b3a4eacc8db6bb7743fe86476c3f26a619da43c04ee6ad3d633f68 in / 
# Wed, 27 Sep 2017 14:25:35 GMT
CMD ["bash"]
# Wed, 27 Sep 2017 14:27:26 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:d447b204d1715dbc31a6b6b7599eea164973e66a347eddd3dfbbf065b3c842b5`  
		Last Modified: Wed, 27 Sep 2017 14:30:12 GMT  
		Size: 46.2 MB (46234099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdba2febd9f7a7914bcbb9dc59ed72545762d7071498c3198e591b2165a16576`  
		Last Modified: Wed, 27 Sep 2017 14:33:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:144b9231dba2c299e4fcbcc837d22203ff45a10ddbdf4b29c738cb5be5ff3ece
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44754317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:184f0b373e67df61c2a2be1c8c977bc4b0588dc95f6335da6810c20e8d2ee6d7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 27 Sep 2017 04:13:47 GMT
ADD file:ff855341f2178170e860c70b1fd4438ad7df8c19fa9f4cb32b259cbcf6f641fa in / 
# Wed, 27 Sep 2017 04:13:47 GMT
CMD ["bash"]
# Wed, 27 Sep 2017 04:16:16 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:243b557ca4232dfba33281e059dc489793fb140673f16a68fb1ec9b67034c773`  
		Last Modified: Wed, 27 Sep 2017 04:19:16 GMT  
		Size: 44.8 MB (44754088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36408752200609224ec6d64d6d90cfc490670fe52cc78602b0054ee9adebe06`  
		Last Modified: Wed, 27 Sep 2017 04:22:49 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:02b5b3f1fe4874a4590c9c3ba4ed7d1ecf67a92ae03bc2e4dae7fb930272335a
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45456233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34bb42cba235b65b4d1d6f2a1a37f0b72322376aa6dfda534c01cd226a682007`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Sep 2017 17:26:13 GMT
ADD file:07d58ee9d0f6dd60b5363a18ab4766f32f94d4aaed3a1d6d4ff5a2d274f030c2 in / 
# Fri, 08 Sep 2017 17:26:15 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 17:31:45 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:40921cc3e39e34244dca67570f52afe382187c080dd1ffbb5a684332f50dfb0b`  
		Last Modified: Fri, 08 Sep 2017 17:38:43 GMT  
		Size: 45.5 MB (45456006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f3ba3ede83f5472ea2561e8ba8f335bf9d264dd5ef62317bde0d7042ce4bba`  
		Last Modified: Fri, 08 Sep 2017 17:38:16 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:c19a6bc1bafa396790d9f6ec1254989d3eb04b5d75eb178687f3a431ca07ff83
```

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48547942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38f51751378aad2f3d2c5356378921eaffd7971851b199ec59134313b219ac03`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Sep 2017 13:19:03 GMT
ADD file:e914d804cd8b6c794db616b0d7ff276be932d6365650fc16027e8f884ff5751a in / 
# Fri, 08 Sep 2017 13:19:03 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 13:21:07 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:cc453eea7829cd3ac47b9e8510e4c25eef45f737546dec6b7dc2cacc93f2f875`  
		Last Modified: Fri, 08 Sep 2017 13:25:22 GMT  
		Size: 48.5 MB (48547718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0001018d2d891123439f7e932cde5790b1d751cd147754986d95ed85acb46b2e`  
		Last Modified: Fri, 08 Sep 2017 13:25:10 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:d77dc2b6013adb258e7893f90799142a15210d069bff0242552a33feed43bd65
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48412248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22f3036c2dd8a2a0c49041c37adebbf08667caae7baa5ae19c3570defb7d16c7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Sep 2017 00:33:20 GMT
ADD file:819bded9731f1d65e9cc04b2c7f43a197ec4be8692da4708af0f87e7426351f3 in / 
# Fri, 08 Sep 2017 00:33:21 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 00:35:14 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:2fab6b5610875e8a6c33bc4d56c825f356289185b055082d589665968ef0900c`  
		Last Modified: Fri, 08 Sep 2017 00:38:59 GMT  
		Size: 48.4 MB (48412021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f3c8e1c149b6439f350c1e8c1f1c395e239b01061a72f91915577c57e01e56`  
		Last Modified: Fri, 08 Sep 2017 00:38:47 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:2cd18b230609066b587fb0f3eff0237ffe9cef0778341b52b11ccbe5864f2feb
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47521325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ef570b8c47a8c596c1b4e6c4d19ae1eb69ac75f173732fdca7f054f5d876017`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Sep 2017 05:22:21 GMT
ADD file:21fffbf13a9dfb5037f5c17e01b497b8a6e81448b0258d6d12a130e07a751566 in / 
# Fri, 08 Sep 2017 05:22:22 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 05:23:33 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:1c56ecd59b527c3f7815101ee47b3e1e3bbf73f1ecef57fcb4d9d726a847f94d`  
		Last Modified: Fri, 08 Sep 2017 05:25:49 GMT  
		Size: 47.5 MB (47521100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c2b7b2f0f9f13a8e883bf60315e9c8a778e8efae77ff481043ed8688ec013c5`  
		Last Modified: Fri, 08 Sep 2017 05:25:41 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
