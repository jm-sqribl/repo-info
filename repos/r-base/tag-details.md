<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `r-base`

-	[`r-base:3.4.2`](#r-base342)
-	[`r-base:latest`](#r-baselatest)

## `r-base:3.4.2`

```console
$ docker pull r-base@sha256:70af7ae787c64bcd023fa5aa295a844c6bd734e5f32d272bbdf67c33ef9cbffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `r-base:3.4.2` - linux; amd64

```console
$ docker pull r-base@sha256:e0bcf9843b2a4850b4d213428af4243111d2c8d3f862bf3936277f32b44c0f4c
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.3 MB (273282835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe0f785fb7132f9155f539a3306eb032929e54b3fcfe9c96e7bf8695d28eb879`
-	Default Command: `["R"]`

```dockerfile
# Wed, 13 Sep 2017 08:41:54 GMT
ADD file:ba27ed06ab0b41115fcba163ee91adb3ef91d5198bc0a998aefab339543c6129 in / 
# Wed, 13 Sep 2017 08:41:54 GMT
CMD ["bash"]
# Wed, 13 Sep 2017 16:46:52 GMT
MAINTAINER "Carl Boettiger and Dirk Eddelbuettel" rocker-maintainers@eddelbuettel.com
# Wed, 13 Sep 2017 16:46:54 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Wed, 13 Sep 2017 16:47:10 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Sep 2017 16:47:12 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 13 Sep 2017 16:47:12 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 13 Sep 2017 16:47:12 GMT
ENV LANG=en_US.UTF-8
# Wed, 13 Sep 2017 16:47:13 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list 	&& echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default
# Mon, 02 Oct 2017 17:43:23 GMT
ENV R_BASE_VERSION=3.4.2
# Mon, 02 Oct 2017 17:45:27 GMT
RUN apt-get update 	&& apt-get install -t unstable -y --no-install-recommends 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}* 		r-base-dev=${R_BASE_VERSION}* 		r-recommended=${R_BASE_VERSION}*         && echo 'options(repos = c(CRAN = "https://cran.rstudio.com/"), download.file.method = "libcurl")' >> /etc/R/Rprofile.site         && echo 'source("/etc/R/Rprofile.site")' >> /etc/littler.r 	&& ln -s /usr/share/doc/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/share/doc/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/share/doc/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/share/doc/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Mon, 02 Oct 2017 17:45:28 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:45d1abe0cfa1c1a4b0ad226ed84808e071967e832f41514b00435d5a6c67d39d`  
		Last Modified: Mon, 11 Sep 2017 10:13:27 GMT  
		Size: 47.5 MB (47547409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa13897e3390656be0d64aa9d06329b240ab0f2b3bd45503aa6b13e976d6567`  
		Last Modified: Wed, 13 Sep 2017 16:49:37 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:659455c278d07c79bf0551ffc26809aa9ad8570739829f8b7366f4bedb0caf59`  
		Last Modified: Wed, 13 Sep 2017 16:49:42 GMT  
		Size: 23.4 MB (23363494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bdf9a91ef1ef587aa2e0996c90574612034d6d8e74ae980e02f606f81e98811`  
		Last Modified: Wed, 13 Sep 2017 16:49:37 GMT  
		Size: 425.9 KB (425869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:844ff4896fb8913f25b983b65495e0ac0166a588ca2620313c709377f79214dc`  
		Last Modified: Wed, 13 Sep 2017 16:49:37 GMT  
		Size: 294.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a9a6e4714c196a68e4be405a0ccf75c1fa4cb7a613a482c8b73456950f34bd5`  
		Last Modified: Mon, 02 Oct 2017 17:46:03 GMT  
		Size: 201.9 MB (201943925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `r-base:latest`

```console
$ docker pull r-base@sha256:70af7ae787c64bcd023fa5aa295a844c6bd734e5f32d272bbdf67c33ef9cbffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `r-base:latest` - linux; amd64

```console
$ docker pull r-base@sha256:e0bcf9843b2a4850b4d213428af4243111d2c8d3f862bf3936277f32b44c0f4c
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.3 MB (273282835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe0f785fb7132f9155f539a3306eb032929e54b3fcfe9c96e7bf8695d28eb879`
-	Default Command: `["R"]`

```dockerfile
# Wed, 13 Sep 2017 08:41:54 GMT
ADD file:ba27ed06ab0b41115fcba163ee91adb3ef91d5198bc0a998aefab339543c6129 in / 
# Wed, 13 Sep 2017 08:41:54 GMT
CMD ["bash"]
# Wed, 13 Sep 2017 16:46:52 GMT
MAINTAINER "Carl Boettiger and Dirk Eddelbuettel" rocker-maintainers@eddelbuettel.com
# Wed, 13 Sep 2017 16:46:54 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Wed, 13 Sep 2017 16:47:10 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Sep 2017 16:47:12 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 13 Sep 2017 16:47:12 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 13 Sep 2017 16:47:12 GMT
ENV LANG=en_US.UTF-8
# Wed, 13 Sep 2017 16:47:13 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list 	&& echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default
# Mon, 02 Oct 2017 17:43:23 GMT
ENV R_BASE_VERSION=3.4.2
# Mon, 02 Oct 2017 17:45:27 GMT
RUN apt-get update 	&& apt-get install -t unstable -y --no-install-recommends 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}* 		r-base-dev=${R_BASE_VERSION}* 		r-recommended=${R_BASE_VERSION}*         && echo 'options(repos = c(CRAN = "https://cran.rstudio.com/"), download.file.method = "libcurl")' >> /etc/R/Rprofile.site         && echo 'source("/etc/R/Rprofile.site")' >> /etc/littler.r 	&& ln -s /usr/share/doc/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/share/doc/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/share/doc/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/share/doc/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Mon, 02 Oct 2017 17:45:28 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:45d1abe0cfa1c1a4b0ad226ed84808e071967e832f41514b00435d5a6c67d39d`  
		Last Modified: Mon, 11 Sep 2017 10:13:27 GMT  
		Size: 47.5 MB (47547409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa13897e3390656be0d64aa9d06329b240ab0f2b3bd45503aa6b13e976d6567`  
		Last Modified: Wed, 13 Sep 2017 16:49:37 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:659455c278d07c79bf0551ffc26809aa9ad8570739829f8b7366f4bedb0caf59`  
		Last Modified: Wed, 13 Sep 2017 16:49:42 GMT  
		Size: 23.4 MB (23363494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bdf9a91ef1ef587aa2e0996c90574612034d6d8e74ae980e02f606f81e98811`  
		Last Modified: Wed, 13 Sep 2017 16:49:37 GMT  
		Size: 425.9 KB (425869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:844ff4896fb8913f25b983b65495e0ac0166a588ca2620313c709377f79214dc`  
		Last Modified: Wed, 13 Sep 2017 16:49:37 GMT  
		Size: 294.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a9a6e4714c196a68e4be405a0ccf75c1fa4cb7a613a482c8b73456950f34bd5`  
		Last Modified: Mon, 02 Oct 2017 17:46:03 GMT  
		Size: 201.9 MB (201943925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
