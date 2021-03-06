## `maven:3-jdk-7-alpine`

```console
$ docker pull maven@sha256:021a11b78f367f78172c2c9f741378a84f8f7bee11490b3bfa061f198d4f73f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `maven:3-jdk-7-alpine` - linux; amd64

```console
$ docker pull maven@sha256:cfb4118487710471d09cbcad7f9b6ce7b96a73d4c68cbaba7de8f07685f8ffeb
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.9 MB (89872322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b95882824442a5c0dce47e31ede3830b5ec454ca71727bffac499933f12ec927`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 13 Sep 2017 14:32:25 GMT
ADD file:4583e12bf5caec40b861a3409f2a1624c3f3556cc457edb99c9707f00e779e45 in / 
# Wed, 13 Sep 2017 14:32:26 GMT
CMD ["/bin/sh"]
# Thu, 14 Sep 2017 04:13:40 GMT
ENV LANG=C.UTF-8
# Thu, 14 Sep 2017 04:13:41 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 14 Sep 2017 04:13:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.7-openjdk
# Thu, 14 Sep 2017 04:13:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.7-openjdk/jre/bin:/usr/lib/jvm/java-1.7-openjdk/bin
# Thu, 14 Sep 2017 04:13:42 GMT
ENV JAVA_VERSION=7u131
# Thu, 14 Sep 2017 04:13:42 GMT
ENV JAVA_ALPINE_VERSION=7.131.2.6.9-r1
# Thu, 14 Sep 2017 04:13:56 GMT
RUN set -x 	&& apk add --no-cache 		openjdk7="$JAVA_ALPINE_VERSION" 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 14 Sep 2017 05:08:05 GMT
RUN apk add --no-cache curl tar bash
# Thu, 14 Sep 2017 05:08:05 GMT
ARG MAVEN_VERSION=3.5.0
# Thu, 14 Sep 2017 05:08:06 GMT
ARG USER_HOME_DIR=/root
# Thu, 14 Sep 2017 05:08:06 GMT
ARG SHA=beb91419245395bd69a4a6edad5ca3ec1a8b64e41457672dc687c173a495f034
# Thu, 14 Sep 2017 05:08:06 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.5.0/binaries
# Thu, 14 Sep 2017 05:08:07 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.5.0/binaries MAVEN_VERSION=3.5.0 SHA=beb91419245395bd69a4a6edad5ca3ec1a8b64e41457672dc687c173a495f034 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha256sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Thu, 14 Sep 2017 05:08:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 14 Sep 2017 05:08:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 14 Sep 2017 05:08:08 GMT
COPY file:e4099db07053a2301f4263d416cab324c1f89ee74c752bebec511d8b59464cb6 in /usr/local/bin/mvn-entrypoint.sh 
# Thu, 14 Sep 2017 05:08:08 GMT
COPY file:b3fc14e8337e0079a4e97eace880b4b7cddc0dc0ea733de80749f78fe1eb089a in /usr/share/maven/ref/ 
# Thu, 14 Sep 2017 05:08:08 GMT
VOLUME [/root/.m2]
# Thu, 14 Sep 2017 05:08:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 14 Sep 2017 05:08:09 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:88286f41530e93dffd4b964e1db22ce4939fffa4a4c665dab8591fbab03d4926`  
		Last Modified: Tue, 27 Jun 2017 18:49:37 GMT  
		Size: 2.0 MB (1990402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720349d0916a74fb5124be4a8a2bf898de431927e1caec15cc956c8a7fb33d14`  
		Last Modified: Thu, 14 Sep 2017 04:50:44 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01693a7d9e2f16c6f1164718f315f8cf99b2ac7c343b7e8a0876d185c5a921cd`  
		Last Modified: Thu, 14 Sep 2017 04:51:00 GMT  
		Size: 77.4 MB (77433926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eafffe074ad64f79741cc882a38cf0146bc8c2e8ce8208d7fc5b930828a4e92c`  
		Last Modified: Thu, 14 Sep 2017 05:11:04 GMT  
		Size: 1.8 MB (1773879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2d8cddbc3e6a614fa563a0370c01da19aca450800c9cdc6291c03836522d6f`  
		Last Modified: Thu, 14 Sep 2017 05:11:04 GMT  
		Size: 8.7 MB (8672784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab285f22e24c23f35761a623647497936d4cedf42a0b8c2d47d83ea66a83c954`  
		Last Modified: Thu, 14 Sep 2017 05:11:03 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa016dae77cac50ae406ddd4cc05db10d3ba978c78f13f6436c78a380ea325e`  
		Last Modified: Thu, 14 Sep 2017 05:11:04 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
