## `nats:windowsservercore`

```console
$ docker pull nats@sha256:c167741e28dadb7c33432118460c39d4f18a7a94e5cb0b4e270712f625dc0916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.1715; amd64

### `nats:windowsservercore` - windows version 10.0.14393.1715; amd64

```console
$ docker pull nats@sha256:ad19a49e2afb33f4ee7b89c765c8893fd67aa22c0ce991ef0bc0743b2606dc88
```

-	Docker Version: 17.03.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 GB (5338298989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf55b09c7a37e15214b71a60a9e264bef1f0923d8d4a7b9f5b210a7216e29995`
-	Entrypoint: `["gnatsd"]`
-	Default Command: `["-c","gnatsd.conf"]`

```dockerfile
# Tue, 13 Dec 2016 10:53:31 GMT
RUN Apply image 10.0.14393.0
# Tue, 12 Sep 2017 22:02:46 GMT
RUN Install update 10.0.14393.1715
# Thu, 14 Sep 2017 23:53:50 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 14 Sep 2017 23:53:54 GMT
RUN cmd /S /C #(nop) WORKDIR C:\gnatsd
# Wed, 27 Sep 2017 20:18:35 GMT
RUN cmd /S /C #(nop) COPY file:61c1931f3ccb93e5489015f8e20111fb3b675785d0003458700c148a3daff2df in gnatsd.exe 
# Wed, 27 Sep 2017 20:18:39 GMT
RUN cmd /S /C #(nop) COPY file:8fad70d15db71db30b9945fba2b3d29035a631ee4fe410e797aef6981c2a1879 in gnatsd.conf 
# Wed, 27 Sep 2017 20:18:42 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222/tcp 6222/tcp 8222/tcp
# Wed, 27 Sep 2017 20:18:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["gnatsd"]
# Wed, 27 Sep 2017 20:18:50 GMT
RUN cmd /S /C #(nop)  CMD ["-c" "gnatsd.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:da87b55a9b6358a65462540faeaa97505b0a12e1a2c14f08893589181d32d00d`  
		Size: 1.3 GB (1265822551 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a43ac1bf86a2806f6b3ea678de0556b4d4abefde4ff1daa217d58245966cd792`  
		Last Modified: Thu, 14 Sep 2017 23:54:46 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3817b383ff4bab348ffa960cb525689977711efa1b34d1decef3d69b8ee365fd`  
		Last Modified: Thu, 14 Sep 2017 23:54:46 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874685deea14d4d56b6df7af5edd661d9788c8f484677b67487b5f226117a28a`  
		Last Modified: Wed, 27 Sep 2017 20:19:14 GMT  
		Size: 2.5 MB (2482357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:622fe9b14d31257e9e6d0792901b1bd35b7be485cd24befe415c21049ae77c90`  
		Last Modified: Wed, 27 Sep 2017 20:19:14 GMT  
		Size: 1.9 KB (1915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8622227bd56054114f940b795ae8b50006c0a47d2773243fe69bf04f109787`  
		Last Modified: Wed, 27 Sep 2017 20:19:13 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73d3e7dbd0925e1ecf74ddd4082e650fef15c4141826525776ede5e0f6a0678`  
		Last Modified: Wed, 27 Sep 2017 20:19:14 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1ae5fea6b968218d64a81e367f57641ef2403145c29fce81cc71a6250f4fc5`  
		Last Modified: Wed, 27 Sep 2017 20:19:13 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
