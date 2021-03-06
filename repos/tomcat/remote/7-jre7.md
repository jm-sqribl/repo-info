## `tomcat:7-jre7`

```console
$ docker pull tomcat@sha256:b7974d98e78c5b4798de591291aa85059aefb574e294599ceb82ba348473332f
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

### `tomcat:7-jre7` - linux; amd64

```console
$ docker pull tomcat@sha256:d7e9a6256d320699657b5175c53847c620257e4fd2b23bf66e9b0b891755ecf1
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.8 MB (202830572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:492ff197469b9fbc40489c4596e5d19d2675bac8f40142f8595a74c65332ef2f`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 13 Sep 2017 08:40:43 GMT
ADD file:d7333b3e0bc6479d2faed32e06d85f1975e5b23e13e75555aeed0f639770413b in / 
# Wed, 13 Sep 2017 08:40:43 GMT
CMD ["bash"]
# Wed, 13 Sep 2017 12:32:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Sep 2017 12:32:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 Sep 2017 04:14:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 14 Sep 2017 04:14:25 GMT
ENV LANG=C.UTF-8
# Thu, 14 Sep 2017 04:14:26 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 14 Sep 2017 04:14:28 GMT
RUN ln -svT "/usr/lib/jvm/java-7-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Thu, 14 Sep 2017 04:14:28 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Thu, 14 Sep 2017 04:14:28 GMT
ENV JAVA_VERSION=7u151
# Thu, 14 Sep 2017 04:14:28 GMT
ENV JAVA_DEBIAN_VERSION=7u151-2.6.11-1~deb8u1
# Thu, 14 Sep 2017 04:15:48 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-7-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Thu, 14 Sep 2017 06:43:12 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 14 Sep 2017 06:43:12 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Sep 2017 06:43:13 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 14 Sep 2017 06:43:13 GMT
WORKDIR /usr/local/tomcat
# Thu, 14 Sep 2017 06:43:13 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 14 Sep 2017 06:43:13 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 14 Sep 2017 06:43:14 GMT
ENV OPENSSL_VERSION=1.1.0f-3
# Thu, 14 Sep 2017 06:43:14 GMT
RUN set -ex; 	if ! grep -q stretch /etc/apt/sources.list; then 		{ 			echo 'deb http://deb.debian.org/debian stretch main'; 		} > /etc/apt/sources.list.d/stretch.list; 		{ 			echo 'Package: *'; 			echo 'Pin: release n=stretch'; 			echo 'Pin-Priority: -10'; 			echo; 			echo 'Package: openssl libssl*'; 			echo "Pin: version $OPENSSL_VERSION"; 			echo 'Pin-Priority: 990'; 		} > /etc/apt/preferences.d/stretch-openssl; 	fi
# Thu, 14 Sep 2017 06:43:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libapr1 		openssl="$OPENSSL_VERSION" 	&& rm -rf /var/lib/apt/lists/*
# Thu, 14 Sep 2017 06:43:36 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 14 Sep 2017 06:43:44 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 Sep 2017 06:43:44 GMT
ENV TOMCAT_MAJOR=7
# Thu, 14 Sep 2017 06:43:45 GMT
ENV TOMCAT_VERSION=7.0.81
# Thu, 14 Sep 2017 06:43:45 GMT
ENV TOMCAT_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=tomcat/tomcat-7/v7.0.81/bin/apache-tomcat-7.0.81.tar.gz
# Thu, 14 Sep 2017 06:43:45 GMT
ENV TOMCAT_ASC_URL=https://www.apache.org/dist/tomcat/tomcat-7/v7.0.81/bin/apache-tomcat-7.0.81.tar.gz.asc
# Thu, 14 Sep 2017 06:43:45 GMT
ENV TOMCAT_TGZ_FALLBACK_URL=https://archive.apache.org/dist/tomcat/tomcat-7/v7.0.81/bin/apache-tomcat-7.0.81.tar.gz
# Thu, 14 Sep 2017 06:43:45 GMT
ENV TOMCAT_ASC_FALLBACK_URL=https://archive.apache.org/dist/tomcat/tomcat-7/v7.0.81/bin/apache-tomcat-7.0.81.tar.gz.asc
# Thu, 14 Sep 2017 06:47:09 GMT
RUN set -x 		&& { 		wget -O tomcat.tar.gz "$TOMCAT_TGZ_URL" 		|| wget -O tomcat.tar.gz "$TOMCAT_TGZ_FALLBACK_URL" 	; } 	&& { 		wget -O tomcat.tar.gz.asc "$TOMCAT_ASC_URL" 		|| wget -O tomcat.tar.gz.asc "$TOMCAT_ASC_FALLBACK_URL" 	; } 	&& gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz 	&& tar -xvf tomcat.tar.gz --strip-components=1 	&& rm bin/*.bat 	&& rm tomcat.tar.gz* 		&& nativeBuildDir="$(mktemp -d)" 	&& tar -xvf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1 	&& nativeBuildDeps=" 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 		openjdk-${JAVA_VERSION%%[-~bu]*}-jdk=$JAVA_DEBIAN_VERSION 	" 	&& apt-get update && apt-get install -y --no-install-recommends $nativeBuildDeps && rm -rf /var/lib/apt/lists/* 	&& ( 		export CATALINA_HOME="$PWD" 		&& cd "$nativeBuildDir/native" 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		&& ./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$(which apr-1-config)" 			--with-java-home="$(docker-java-home)" 			--with-ssl=yes 		&& make -j "$(nproc)" 		&& make install 	) 	&& apt-get purge -y --auto-remove $nativeBuildDeps 	&& rm -rf "$nativeBuildDir" 	&& rm bin/tomcat-native.tar.gz 	&& find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +
# Thu, 14 Sep 2017 06:47:14 GMT
RUN set -e 	&& nativeLines="$(catalina.sh configtest 2>&1)" 	&& nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')" 	&& nativeLines="$(echo "$nativeLines" | sort -u)" 	&& if ! echo "$nativeLines" | grep 'INFO: Loaded APR based Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 14 Sep 2017 06:47:14 GMT
EXPOSE 8080/tcp
# Thu, 14 Sep 2017 06:47:14 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:aa18ad1a0d334d80981104c599fa8cef9264552a265b1197af11274beba767cf`  
		Last Modified: Thu, 07 Sep 2017 23:11:06 GMT  
		Size: 52.6 MB (52595547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a33158a1367c7c4103c89ae66e8f4fdec4ada6a39d4648cf254b32296d6668`  
		Last Modified: Wed, 13 Sep 2017 12:54:21 GMT  
		Size: 19.3 MB (19263717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:606c0b57feb051ea7df9ecb5091d7c5275047f4baa9b54700350c3f35e4a4f26`  
		Last Modified: Thu, 14 Sep 2017 04:51:25 GMT  
		Size: 795.6 KB (795601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584c35e01c21b7270342137194d0860c0a7a90f65441c6e8a1e0f7571bc84a30`  
		Last Modified: Thu, 14 Sep 2017 04:51:27 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b2c1657fd0e01b54bc8a64a8e8c5470058e23a343328e8ac2379e3d043e6ce`  
		Last Modified: Thu, 14 Sep 2017 04:51:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b4dd65ad29cb149c9ecfc67a1032e7737acfd4c5f696afda2a27483ad9152ae`  
		Last Modified: Thu, 14 Sep 2017 04:51:54 GMT  
		Size: 116.9 MB (116883085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b104da1b89f431f1c2420fba581edcb8a7d659e1d780e40057efac86c48e835`  
		Last Modified: Thu, 14 Sep 2017 06:56:52 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b2bd7746367c81bc8647c11949a2fab762d563ff730f25980272b25960c58f`  
		Last Modified: Thu, 14 Sep 2017 06:56:50 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d521e6b892a5a2c1f039ecd81ae929a1e2546537199c97e23b9e17b28bf40218`  
		Last Modified: Thu, 14 Sep 2017 06:56:51 GMT  
		Size: 3.3 MB (3263295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a553e2265165ec4dd143e90af2fe31accbce8422a704ddf64a804b639f53f1fc`  
		Last Modified: Thu, 14 Sep 2017 06:56:50 GMT  
		Size: 113.8 KB (113845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ac7f352a7ee2368ff8d573a424660609f4dfd3880693bdc3b4a0312390abb0`  
		Last Modified: Thu, 14 Sep 2017 06:56:52 GMT  
		Size: 9.9 MB (9914488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e5814f053db8e374bc50ad71287639df014e1717d72cb0c00f59e146d57cb25`  
		Last Modified: Thu, 14 Sep 2017 06:56:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:7-jre7` - linux; arm variant v5

```console
$ docker pull tomcat@sha256:8f482aca3d12295a3e2b6b66e68ba67f306b9377a5fcc74b61080c84494cd5d3
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179136958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f623dd26040e9226beb063e9da271d667a9b9475e7a3c26134943537b0bc08ff`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 27 Sep 2017 14:24:27 GMT
ADD file:195667b0ccd6dad7d7793044adefb6ab0b4934a95d6383e0e1b09275397bc1e7 in / 
# Wed, 27 Sep 2017 14:24:27 GMT
CMD ["bash"]
# Wed, 27 Sep 2017 14:47:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 27 Sep 2017 14:47:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 27 Sep 2017 15:15:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 27 Sep 2017 15:15:41 GMT
ENV LANG=C.UTF-8
# Wed, 27 Sep 2017 15:15:42 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 27 Sep 2017 15:15:43 GMT
RUN ln -svT "/usr/lib/jvm/java-7-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 27 Sep 2017 15:15:43 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 27 Sep 2017 15:15:43 GMT
ENV JAVA_VERSION=7u151
# Wed, 27 Sep 2017 15:15:43 GMT
ENV JAVA_DEBIAN_VERSION=7u151-2.6.11-1~deb8u1
# Wed, 27 Sep 2017 15:16:52 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-7-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 27 Sep 2017 16:13:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 27 Sep 2017 16:13:14 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Sep 2017 16:13:15 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 27 Sep 2017 16:13:15 GMT
WORKDIR /usr/local/tomcat
# Wed, 27 Sep 2017 16:13:16 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 27 Sep 2017 16:13:16 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 27 Sep 2017 16:13:16 GMT
ENV OPENSSL_VERSION=1.1.0f-3
# Wed, 27 Sep 2017 16:13:17 GMT
RUN set -ex; 	if ! grep -q stretch /etc/apt/sources.list; then 		{ 			echo 'deb http://deb.debian.org/debian stretch main'; 		} > /etc/apt/sources.list.d/stretch.list; 		{ 			echo 'Package: *'; 			echo 'Pin: release n=stretch'; 			echo 'Pin-Priority: -10'; 			echo; 			echo 'Package: openssl libssl*'; 			echo "Pin: version $OPENSSL_VERSION"; 			echo 'Pin-Priority: 990'; 		} > /etc/apt/preferences.d/stretch-openssl; 	fi
# Wed, 27 Sep 2017 16:13:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libapr1 		openssl="$OPENSSL_VERSION" 	&& rm -rf /var/lib/apt/lists/*
# Wed, 27 Sep 2017 16:13:53 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 27 Sep 2017 16:13:58 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Wed, 27 Sep 2017 16:13:58 GMT
ENV TOMCAT_MAJOR=7
# Wed, 27 Sep 2017 16:13:58 GMT
ENV TOMCAT_VERSION=7.0.81
# Wed, 27 Sep 2017 16:13:58 GMT
ENV TOMCAT_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=tomcat/tomcat-7/v7.0.81/bin/apache-tomcat-7.0.81.tar.gz
# Wed, 27 Sep 2017 16:13:59 GMT
ENV TOMCAT_ASC_URL=https://www.apache.org/dist/tomcat/tomcat-7/v7.0.81/bin/apache-tomcat-7.0.81.tar.gz.asc
# Wed, 27 Sep 2017 16:13:59 GMT
ENV TOMCAT_TGZ_FALLBACK_URL=https://archive.apache.org/dist/tomcat/tomcat-7/v7.0.81/bin/apache-tomcat-7.0.81.tar.gz
# Wed, 27 Sep 2017 16:13:59 GMT
ENV TOMCAT_ASC_FALLBACK_URL=https://archive.apache.org/dist/tomcat/tomcat-7/v7.0.81/bin/apache-tomcat-7.0.81.tar.gz.asc
# Wed, 27 Sep 2017 16:14:59 GMT
RUN set -x 		&& { 		wget -O tomcat.tar.gz "$TOMCAT_TGZ_URL" 		|| wget -O tomcat.tar.gz "$TOMCAT_TGZ_FALLBACK_URL" 	; } 	&& { 		wget -O tomcat.tar.gz.asc "$TOMCAT_ASC_URL" 		|| wget -O tomcat.tar.gz.asc "$TOMCAT_ASC_FALLBACK_URL" 	; } 	&& gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz 	&& tar -xvf tomcat.tar.gz --strip-components=1 	&& rm bin/*.bat 	&& rm tomcat.tar.gz* 		&& nativeBuildDir="$(mktemp -d)" 	&& tar -xvf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1 	&& nativeBuildDeps=" 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 		openjdk-${JAVA_VERSION%%[-~bu]*}-jdk=$JAVA_DEBIAN_VERSION 	" 	&& apt-get update && apt-get install -y --no-install-recommends $nativeBuildDeps && rm -rf /var/lib/apt/lists/* 	&& ( 		export CATALINA_HOME="$PWD" 		&& cd "$nativeBuildDir/native" 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		&& ./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$(which apr-1-config)" 			--with-java-home="$(docker-java-home)" 			--with-ssl=yes 		&& make -j "$(nproc)" 		&& make install 	) 	&& apt-get purge -y --auto-remove $nativeBuildDeps 	&& rm -rf "$nativeBuildDir" 	&& rm bin/tomcat-native.tar.gz 	&& find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +
# Wed, 27 Sep 2017 16:15:02 GMT
RUN set -e 	&& nativeLines="$(catalina.sh configtest 2>&1)" 	&& nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')" 	&& nativeLines="$(echo "$nativeLines" | sort -u)" 	&& if ! echo "$nativeLines" | grep 'INFO: Loaded APR based Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 27 Sep 2017 16:15:02 GMT
EXPOSE 8080/tcp
# Wed, 27 Sep 2017 16:15:02 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0000473879860f50b5d7e33d60cdb2bd20eccd2563da6dfab9023b079c54f91b`  
		Last Modified: Wed, 27 Sep 2017 14:28:25 GMT  
		Size: 50.9 MB (50879797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:383dc0c402c2a94402ca03cfa2ec05c87d8e91d968961c72d52a7f47b0823a7f`  
		Last Modified: Wed, 27 Sep 2017 15:01:39 GMT  
		Size: 18.7 MB (18653386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636c71cf23a0e02422b029c67bb652759226bc08a46050db8ca3e34118d2c9d4`  
		Last Modified: Wed, 27 Sep 2017 15:31:09 GMT  
		Size: 788.3 KB (788348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a7695c88a60e744b02ca7c8c5386680ad543bdaeffd652becc698d607be0c72`  
		Last Modified: Wed, 27 Sep 2017 15:31:09 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30af743ef3c6d30e8cdb5029e4001c3752dffeed996d894f384e2e6be1451f90`  
		Last Modified: Wed, 27 Sep 2017 15:31:08 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db5d90ba6727880a1d5d0c51323714da87bf74259cc79069a08866c0b3c6c34`  
		Last Modified: Wed, 27 Sep 2017 15:31:31 GMT  
		Size: 95.9 MB (95855625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ee5d3d8a56ca8dd960e943e18729fb9e6ed076527c2c5baf5cb9862ce1cf6c`  
		Last Modified: Wed, 27 Sep 2017 16:19:29 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1597cf396e4e71f430294f9dce6a88315d92221151fe986b45145ee4c4c0e1e`  
		Last Modified: Wed, 27 Sep 2017 16:19:28 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:416c817b5f1b0de271c008c4061ecc683ba6210567da1927ec7e35ed4d528026`  
		Last Modified: Wed, 27 Sep 2017 16:19:29 GMT  
		Size: 3.0 MB (2978455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b57ea4c82af23f947cf8329ba8054e34ae327d6c0ed8d464d4a5064cd3b2df97`  
		Last Modified: Wed, 27 Sep 2017 16:19:28 GMT  
		Size: 116.0 KB (116029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71e6c03d4d26c98752e35b48e27da240e0a697ebc94d41334fb926875af0a24b`  
		Last Modified: Wed, 27 Sep 2017 16:19:30 GMT  
		Size: 9.9 MB (9864292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ffa38ab29c1161498805454e3a16109fbfe8a895021364d68ab2486aec5e69`  
		Last Modified: Wed, 27 Sep 2017 16:19:28 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:7-jre7` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:e0f7f2caf226c59a87e53c14a7147ec0ea94ab2e76f599efc820f73520dbee84
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.8 MB (184831127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20c8a87f1958050953262889c7febcd90d4e6e094609d03e7dd1f0b59790e5f6`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 27 Sep 2017 04:12:21 GMT
ADD file:ef59ce7fe68882b1b44bc3c4a5e9e465561cb257fb63f8c2b3c247abb012486b in / 
# Wed, 27 Sep 2017 04:12:22 GMT
CMD ["bash"]
# Wed, 27 Sep 2017 04:39:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 27 Sep 2017 04:39:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 27 Sep 2017 05:19:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 27 Sep 2017 05:19:21 GMT
ENV LANG=C.UTF-8
# Wed, 27 Sep 2017 05:19:22 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 27 Sep 2017 05:19:24 GMT
RUN ln -svT "/usr/lib/jvm/java-7-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 27 Sep 2017 05:19:24 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 27 Sep 2017 05:19:24 GMT
ENV JAVA_VERSION=7u151
# Wed, 27 Sep 2017 05:19:25 GMT
ENV JAVA_DEBIAN_VERSION=7u151-2.6.11-1~deb8u1
# Wed, 27 Sep 2017 05:20:47 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-7-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 27 Sep 2017 07:26:28 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 27 Sep 2017 07:26:28 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Sep 2017 07:26:29 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 27 Sep 2017 07:26:31 GMT
WORKDIR /usr/local/tomcat
# Wed, 27 Sep 2017 07:26:31 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 27 Sep 2017 07:26:31 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 27 Sep 2017 07:26:31 GMT
ENV OPENSSL_VERSION=1.1.0f-3
# Wed, 27 Sep 2017 07:26:34 GMT
RUN set -ex; 	if ! grep -q stretch /etc/apt/sources.list; then 		{ 			echo 'deb http://deb.debian.org/debian stretch main'; 		} > /etc/apt/sources.list.d/stretch.list; 		{ 			echo 'Package: *'; 			echo 'Pin: release n=stretch'; 			echo 'Pin-Priority: -10'; 			echo; 			echo 'Package: openssl libssl*'; 			echo "Pin: version $OPENSSL_VERSION"; 			echo 'Pin-Priority: 990'; 		} > /etc/apt/preferences.d/stretch-openssl; 	fi
# Wed, 27 Sep 2017 07:27:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libapr1 		openssl="$OPENSSL_VERSION" 	&& rm -rf /var/lib/apt/lists/*
# Wed, 27 Sep 2017 07:27:10 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 27 Sep 2017 07:27:15 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Wed, 27 Sep 2017 07:27:15 GMT
ENV TOMCAT_MAJOR=7
# Wed, 27 Sep 2017 07:27:15 GMT
ENV TOMCAT_VERSION=7.0.81
# Wed, 27 Sep 2017 07:27:15 GMT
ENV TOMCAT_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=tomcat/tomcat-7/v7.0.81/bin/apache-tomcat-7.0.81.tar.gz
# Wed, 27 Sep 2017 07:27:15 GMT
ENV TOMCAT_ASC_URL=https://www.apache.org/dist/tomcat/tomcat-7/v7.0.81/bin/apache-tomcat-7.0.81.tar.gz.asc
# Wed, 27 Sep 2017 07:27:16 GMT
ENV TOMCAT_TGZ_FALLBACK_URL=https://archive.apache.org/dist/tomcat/tomcat-7/v7.0.81/bin/apache-tomcat-7.0.81.tar.gz
# Wed, 27 Sep 2017 07:27:16 GMT
ENV TOMCAT_ASC_FALLBACK_URL=https://archive.apache.org/dist/tomcat/tomcat-7/v7.0.81/bin/apache-tomcat-7.0.81.tar.gz.asc
# Wed, 27 Sep 2017 07:28:18 GMT
RUN set -x 		&& { 		wget -O tomcat.tar.gz "$TOMCAT_TGZ_URL" 		|| wget -O tomcat.tar.gz "$TOMCAT_TGZ_FALLBACK_URL" 	; } 	&& { 		wget -O tomcat.tar.gz.asc "$TOMCAT_ASC_URL" 		|| wget -O tomcat.tar.gz.asc "$TOMCAT_ASC_FALLBACK_URL" 	; } 	&& gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz 	&& tar -xvf tomcat.tar.gz --strip-components=1 	&& rm bin/*.bat 	&& rm tomcat.tar.gz* 		&& nativeBuildDir="$(mktemp -d)" 	&& tar -xvf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1 	&& nativeBuildDeps=" 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 		openjdk-${JAVA_VERSION%%[-~bu]*}-jdk=$JAVA_DEBIAN_VERSION 	" 	&& apt-get update && apt-get install -y --no-install-recommends $nativeBuildDeps && rm -rf /var/lib/apt/lists/* 	&& ( 		export CATALINA_HOME="$PWD" 		&& cd "$nativeBuildDir/native" 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		&& ./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$(which apr-1-config)" 			--with-java-home="$(docker-java-home)" 			--with-ssl=yes 		&& make -j "$(nproc)" 		&& make install 	) 	&& apt-get purge -y --auto-remove $nativeBuildDeps 	&& rm -rf "$nativeBuildDir" 	&& rm bin/tomcat-native.tar.gz 	&& find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +
# Wed, 27 Sep 2017 07:28:21 GMT
RUN set -e 	&& nativeLines="$(catalina.sh configtest 2>&1)" 	&& nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')" 	&& nativeLines="$(echo "$nativeLines" | sort -u)" 	&& if ! echo "$nativeLines" | grep 'INFO: Loaded APR based Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 27 Sep 2017 07:28:21 GMT
EXPOSE 8080/tcp
# Wed, 27 Sep 2017 07:28:21 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:8c7b63aa62f92f5be1e93e5129c5c99dac397c6d3b5f6c6452bfd0905f6f20be`  
		Last Modified: Wed, 27 Sep 2017 04:17:18 GMT  
		Size: 48.7 MB (48686544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a607bd01ffd678134d1281825ba8fafc069965446932fb3da991e8e6c2d3065d`  
		Last Modified: Wed, 27 Sep 2017 04:58:12 GMT  
		Size: 18.3 MB (18262468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:471f4416b78b04ea9f2c696c8cf2b185f8e140c19484b26d6ba923f8e4f8d39a`  
		Last Modified: Wed, 27 Sep 2017 05:35:15 GMT  
		Size: 763.0 KB (762959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd30762fc0081bbe65b4a1fc76f2eece0404254a02dce19d6d780b1bfd5c042`  
		Last Modified: Wed, 27 Sep 2017 05:35:16 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ffd873da19f0a4486e03412365b191771991f3f1a9ae9c41c8b56e713be1a1`  
		Last Modified: Wed, 27 Sep 2017 05:35:14 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a072022d9431474505ba7eecbd13ba82e7c87a115c846504607840ea5faec61`  
		Last Modified: Wed, 27 Sep 2017 05:36:06 GMT  
		Size: 104.3 MB (104255174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd71665f486d0d8b4b87b3763fc9406c03dad69d97e5968d73baceb2064e9e24`  
		Last Modified: Wed, 27 Sep 2017 07:33:24 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df02a86f8dc7c7312305ddf1619808c11c21cd9e1e8053d673f122bd6ce1d4bd`  
		Last Modified: Wed, 27 Sep 2017 07:33:23 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49573c1648597c4417156e4c1f87badb3b3df6c6302fae4cbb4ba5413e0f2c3`  
		Last Modified: Wed, 27 Sep 2017 07:33:23 GMT  
		Size: 2.9 MB (2893138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7642e8e5cdf174e46e21cf8f8473378ec57b254bc4429c2600c3bd6f5f08b70`  
		Last Modified: Wed, 27 Sep 2017 07:33:23 GMT  
		Size: 116.0 KB (116025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c8ff8114fd32de1a7e012927d3e43720c2b245c7a4bc96d8ffdec0e51c1e95e`  
		Last Modified: Wed, 27 Sep 2017 07:33:25 GMT  
		Size: 9.9 MB (9853789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1121d7cce0c7d151307295fde7d27c48c990433a969a33ebde6717e036b50f9`  
		Last Modified: Wed, 27 Sep 2017 07:33:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:7-jre7` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:cdd47f379baccf769cc6a1c444cc7b445591d1ff3524b9db4f275921db0b93ad
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.4 MB (176449679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbfba1d5d9cbe712a388eb59ab8646c945561afa99cce9ac4eb1fdf0c0696ec7`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 08 Sep 2017 17:23:41 GMT
ADD file:9f576a63a5e03994904e585c35fbeef6a2c96c41d8f696705c033f3ca69b6a2b in / 
# Fri, 08 Sep 2017 17:23:42 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 18:32:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 18:32:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 Sep 2017 22:31:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 14 Sep 2017 22:31:37 GMT
ENV LANG=C.UTF-8
# Thu, 14 Sep 2017 22:31:39 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 14 Sep 2017 22:31:41 GMT
RUN ln -svT "/usr/lib/jvm/java-7-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Thu, 14 Sep 2017 22:31:42 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Thu, 14 Sep 2017 22:31:43 GMT
ENV JAVA_VERSION=7u151
# Thu, 14 Sep 2017 22:31:43 GMT
ENV JAVA_DEBIAN_VERSION=7u151-2.6.11-1~deb8u1
# Thu, 14 Sep 2017 22:38:01 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-7-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Fri, 15 Sep 2017 01:22:54 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 15 Sep 2017 01:22:55 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Sep 2017 01:22:58 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 15 Sep 2017 01:22:59 GMT
WORKDIR /usr/local/tomcat
# Fri, 15 Sep 2017 01:23:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 15 Sep 2017 01:23:01 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 15 Sep 2017 01:23:02 GMT
ENV OPENSSL_VERSION=1.1.0f-3
# Fri, 15 Sep 2017 01:23:07 GMT
RUN set -ex; 	if ! grep -q stretch /etc/apt/sources.list; then 		{ 			echo 'deb http://deb.debian.org/debian stretch main'; 		} > /etc/apt/sources.list.d/stretch.list; 		{ 			echo 'Package: *'; 			echo 'Pin: release n=stretch'; 			echo 'Pin-Priority: -10'; 			echo; 			echo 'Package: openssl libssl*'; 			echo "Pin: version $OPENSSL_VERSION"; 			echo 'Pin-Priority: 990'; 		} > /etc/apt/preferences.d/stretch-openssl; 	fi
# Fri, 15 Sep 2017 01:23:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libapr1 		openssl="$OPENSSL_VERSION" 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Sep 2017 01:24:00 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 15 Sep 2017 01:24:10 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Fri, 15 Sep 2017 01:24:11 GMT
ENV TOMCAT_MAJOR=7
# Fri, 15 Sep 2017 01:24:11 GMT
ENV TOMCAT_VERSION=7.0.81
# Fri, 15 Sep 2017 01:24:12 GMT
ENV TOMCAT_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=tomcat/tomcat-7/v7.0.81/bin/apache-tomcat-7.0.81.tar.gz
# Fri, 15 Sep 2017 01:24:13 GMT
ENV TOMCAT_ASC_URL=https://www.apache.org/dist/tomcat/tomcat-7/v7.0.81/bin/apache-tomcat-7.0.81.tar.gz.asc
# Fri, 15 Sep 2017 01:24:13 GMT
ENV TOMCAT_TGZ_FALLBACK_URL=https://archive.apache.org/dist/tomcat/tomcat-7/v7.0.81/bin/apache-tomcat-7.0.81.tar.gz
# Fri, 15 Sep 2017 01:24:14 GMT
ENV TOMCAT_ASC_FALLBACK_URL=https://archive.apache.org/dist/tomcat/tomcat-7/v7.0.81/bin/apache-tomcat-7.0.81.tar.gz.asc
# Fri, 15 Sep 2017 01:25:54 GMT
RUN set -x 		&& { 		wget -O tomcat.tar.gz "$TOMCAT_TGZ_URL" 		|| wget -O tomcat.tar.gz "$TOMCAT_TGZ_FALLBACK_URL" 	; } 	&& { 		wget -O tomcat.tar.gz.asc "$TOMCAT_ASC_URL" 		|| wget -O tomcat.tar.gz.asc "$TOMCAT_ASC_FALLBACK_URL" 	; } 	&& gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz 	&& tar -xvf tomcat.tar.gz --strip-components=1 	&& rm bin/*.bat 	&& rm tomcat.tar.gz* 		&& nativeBuildDir="$(mktemp -d)" 	&& tar -xvf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1 	&& nativeBuildDeps=" 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 		openjdk-${JAVA_VERSION%%[-~bu]*}-jdk=$JAVA_DEBIAN_VERSION 	" 	&& apt-get update && apt-get install -y --no-install-recommends $nativeBuildDeps && rm -rf /var/lib/apt/lists/* 	&& ( 		export CATALINA_HOME="$PWD" 		&& cd "$nativeBuildDir/native" 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		&& ./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$(which apr-1-config)" 			--with-java-home="$(docker-java-home)" 			--with-ssl=yes 		&& make -j "$(nproc)" 		&& make install 	) 	&& apt-get purge -y --auto-remove $nativeBuildDeps 	&& rm -rf "$nativeBuildDir" 	&& rm bin/tomcat-native.tar.gz 	&& find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +
# Fri, 15 Sep 2017 01:25:57 GMT
RUN set -e 	&& nativeLines="$(catalina.sh configtest 2>&1)" 	&& nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')" 	&& nativeLines="$(echo "$nativeLines" | sort -u)" 	&& if ! echo "$nativeLines" | grep 'INFO: Loaded APR based Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 15 Sep 2017 01:25:58 GMT
EXPOSE 8080/tcp
# Fri, 15 Sep 2017 01:25:58 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e91a355b0d3ff86add037a3f24718b760d8eb3f346f998e5116375ddce9eae19`  
		Last Modified: Fri, 08 Sep 2017 17:34:56 GMT  
		Size: 49.9 MB (49929457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e054bfb02234c6e2b5305981d365c3b31101ec460b0d90df3b099305c03196`  
		Last Modified: Thu, 14 Sep 2017 22:01:15 GMT  
		Size: 18.7 MB (18737603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faca5cf969f88a9b02da68ef94499b29d5bf74180ee76a7ad22a7debc7eb1b9c`  
		Last Modified: Thu, 14 Sep 2017 23:07:16 GMT  
		Size: 789.4 KB (789391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f043a5e1e1c7b9c6f765a3e8aaccfdee8ade3ae34a8459190d507e28033a025a`  
		Last Modified: Thu, 14 Sep 2017 23:07:16 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf53c8c46125cb533bbecd8a785d72381c2bc14f12fa007dc8c45d50a5cbe36`  
		Last Modified: Thu, 14 Sep 2017 23:07:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de485a156ff7b019f79b449c70a43c051d331598da6d8acd77fb2d57557d9467`  
		Last Modified: Thu, 14 Sep 2017 23:07:41 GMT  
		Size: 94.0 MB (94000654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81ecd501cd14114da1c3bd952e6a6bc837311af4d16c4d27b0efd2c04a5520c`  
		Last Modified: Fri, 15 Sep 2017 01:39:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4746f7b26aaad42b1090a3deec1827ced9c5fbc97b941e985bc4ac302a179755`  
		Last Modified: Fri, 15 Sep 2017 01:39:14 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc534705cdea11346f1bf1a9f5bb3036548ae78a8625a75e1612a77a8de5b5f7`  
		Last Modified: Fri, 15 Sep 2017 01:39:14 GMT  
		Size: 3.0 MB (2960272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea68c46286899fae171cd67d49edb036522ced577a0a921fa36622276e8b4868`  
		Last Modified: Fri, 15 Sep 2017 01:39:14 GMT  
		Size: 113.8 KB (113846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c26dfb97c2ff0b7b04e060fd5948f84afaaa63415f27785b3f1d4161b09581`  
		Last Modified: Fri, 15 Sep 2017 01:39:16 GMT  
		Size: 9.9 MB (9917460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e293251008533f6df3768e9e11580a1da392886ec6d5e8869c44bcf907dd5d63`  
		Last Modified: Fri, 15 Sep 2017 01:39:14 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:7-jre7` - linux; 386

```console
$ docker pull tomcat@sha256:9db850fb5a4c5b46ccca640e18c2ba1e19118014adcd6597e43fa955c485ae66
```

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.9 MB (215923290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a39034ff7a9053027ca08d8f3ebd1bf60ef1bd7d3683c4cac5576c3d09c25872`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 08 Sep 2017 13:17:52 GMT
ADD file:e02edf114d3ee3a58b6c6729d41261abc361f69333d3b08c7c730572fd6c1874 in / 
# Fri, 08 Sep 2017 13:17:52 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 13:54:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 13:54:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 09 Sep 2017 14:58:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Sat, 09 Sep 2017 14:58:22 GMT
ENV LANG=C.UTF-8
# Sat, 09 Sep 2017 14:58:23 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Sat, 09 Sep 2017 14:58:24 GMT
RUN ln -svT "/usr/lib/jvm/java-7-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Sat, 09 Sep 2017 14:58:24 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Sat, 09 Sep 2017 14:58:25 GMT
ENV JAVA_VERSION=7u151
# Sat, 09 Sep 2017 14:58:25 GMT
ENV JAVA_DEBIAN_VERSION=7u151-2.6.11-1~deb8u1
# Sat, 09 Sep 2017 15:00:16 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-7-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Sat, 09 Sep 2017 16:38:48 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 09 Sep 2017 16:38:48 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Sep 2017 16:38:49 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 09 Sep 2017 16:38:50 GMT
WORKDIR /usr/local/tomcat
# Sat, 09 Sep 2017 16:38:50 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 09 Sep 2017 16:38:50 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 09 Sep 2017 16:38:50 GMT
ENV OPENSSL_VERSION=1.1.0f-3
# Sat, 09 Sep 2017 16:38:51 GMT
RUN set -ex; 	if ! grep -q stretch /etc/apt/sources.list; then 		{ 			echo 'deb http://deb.debian.org/debian stretch main'; 		} > /etc/apt/sources.list.d/stretch.list; 		{ 			echo 'Package: *'; 			echo 'Pin: release n=stretch'; 			echo 'Pin-Priority: -10'; 			echo; 			echo 'Package: openssl libssl*'; 			echo "Pin: version $OPENSSL_VERSION"; 			echo 'Pin-Priority: 990'; 		} > /etc/apt/preferences.d/stretch-openssl; 	fi
# Sat, 09 Sep 2017 16:39:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libapr1 		openssl="$OPENSSL_VERSION" 	&& rm -rf /var/lib/apt/lists/*
# Sat, 09 Sep 2017 16:39:30 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Sat, 09 Sep 2017 16:39:37 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Sat, 09 Sep 2017 16:39:37 GMT
ENV TOMCAT_MAJOR=7
# Sat, 09 Sep 2017 16:39:37 GMT
ENV TOMCAT_VERSION=7.0.81
# Sat, 09 Sep 2017 16:39:37 GMT
ENV TOMCAT_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=tomcat/tomcat-7/v7.0.81/bin/apache-tomcat-7.0.81.tar.gz
# Sat, 09 Sep 2017 16:39:37 GMT
ENV TOMCAT_ASC_URL=https://www.apache.org/dist/tomcat/tomcat-7/v7.0.81/bin/apache-tomcat-7.0.81.tar.gz.asc
# Sat, 09 Sep 2017 16:39:37 GMT
ENV TOMCAT_TGZ_FALLBACK_URL=https://archive.apache.org/dist/tomcat/tomcat-7/v7.0.81/bin/apache-tomcat-7.0.81.tar.gz
# Sat, 09 Sep 2017 16:39:38 GMT
ENV TOMCAT_ASC_FALLBACK_URL=https://archive.apache.org/dist/tomcat/tomcat-7/v7.0.81/bin/apache-tomcat-7.0.81.tar.gz.asc
# Sat, 09 Sep 2017 16:40:42 GMT
RUN set -x 		&& { 		wget -O tomcat.tar.gz "$TOMCAT_TGZ_URL" 		|| wget -O tomcat.tar.gz "$TOMCAT_TGZ_FALLBACK_URL" 	; } 	&& { 		wget -O tomcat.tar.gz.asc "$TOMCAT_ASC_URL" 		|| wget -O tomcat.tar.gz.asc "$TOMCAT_ASC_FALLBACK_URL" 	; } 	&& gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz 	&& tar -xvf tomcat.tar.gz --strip-components=1 	&& rm bin/*.bat 	&& rm tomcat.tar.gz* 		&& nativeBuildDir="$(mktemp -d)" 	&& tar -xvf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1 	&& nativeBuildDeps=" 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 		openjdk-${JAVA_VERSION%%[-~bu]*}-jdk=$JAVA_DEBIAN_VERSION 	" 	&& apt-get update && apt-get install -y --no-install-recommends $nativeBuildDeps && rm -rf /var/lib/apt/lists/* 	&& ( 		export CATALINA_HOME="$PWD" 		&& cd "$nativeBuildDir/native" 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		&& ./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$(which apr-1-config)" 			--with-java-home="$(docker-java-home)" 			--with-ssl=yes 		&& make -j "$(nproc)" 		&& make install 	) 	&& apt-get purge -y --auto-remove $nativeBuildDeps 	&& rm -rf "$nativeBuildDir" 	&& rm bin/tomcat-native.tar.gz 	&& find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +
# Sat, 09 Sep 2017 16:40:46 GMT
RUN set -e 	&& nativeLines="$(catalina.sh configtest 2>&1)" 	&& nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')" 	&& nativeLines="$(echo "$nativeLines" | sort -u)" 	&& if ! echo "$nativeLines" | grep 'INFO: Loaded APR based Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 09 Sep 2017 16:40:46 GMT
EXPOSE 8080/tcp
# Sat, 09 Sep 2017 16:40:46 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f611f84acffe6a66fad3356eb9101ed9fff54e980701079bbce3ee4826ccd3ae`  
		Last Modified: Fri, 08 Sep 2017 13:22:33 GMT  
		Size: 52.8 MB (52773126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ed51718fa88831e0e4e7d7e02a316d71bc90cca2fb9a38748ac4aebeb93cb6`  
		Last Modified: Sat, 09 Sep 2017 13:59:44 GMT  
		Size: 21.6 MB (21594447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eb4420296f36e7bf08987e529a0d76b095bfc22a558c10611469cccc903eed8`  
		Last Modified: Sat, 09 Sep 2017 15:25:03 GMT  
		Size: 798.6 KB (798611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94034f638cfae0977b58d6b46ba77e90f33369e37dddc08e4b0a4596e8afec2d`  
		Last Modified: Sat, 09 Sep 2017 15:25:03 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76eb68242e2cfa4128fa94189970405dda28003194a04fa5c0df1611085cfda6`  
		Last Modified: Sat, 09 Sep 2017 15:25:03 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484d72516bc1be66f7947a6f0442e56be79bc5751aaf05c7ed1afe24413a2a46`  
		Last Modified: Sat, 09 Sep 2017 15:25:27 GMT  
		Size: 127.6 MB (127587119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d341ca9f187c874a9163c8c9d9d1eebab17b2e217263815180f3b6b832b559`  
		Last Modified: Sat, 09 Sep 2017 16:45:10 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8bc88532a016a215276091030f6c2a9b05e490534b5bf9fb58119a7d1736fc`  
		Last Modified: Sat, 09 Sep 2017 16:45:10 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cdb63fdf112047531c680787b0065688bf30544597ed23e89feec58cd9a1fdf`  
		Last Modified: Sat, 09 Sep 2017 16:45:10 GMT  
		Size: 3.3 MB (3276880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2004d94780243b3cbefe41db68ac7f9d5440259e1647d3d2a88873fb4ce37d9`  
		Last Modified: Sat, 09 Sep 2017 16:45:10 GMT  
		Size: 113.8 KB (113847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15afe8070e68d66cb277f482f5167209b420021f4150f8e6d314b4b827d01a6`  
		Last Modified: Sat, 09 Sep 2017 16:45:11 GMT  
		Size: 9.8 MB (9778269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dae60dd3f15d22c08bebf4c67dffe72cfe2682881311fc69f70f8c9d24e0f06`  
		Last Modified: Sat, 09 Sep 2017 16:45:10 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:7-jre7` - linux; ppc64le

```console
$ docker pull tomcat@sha256:3525655d1538a93b9c4bbd0a1bbb94e4bf9ff60cb01baafa32fc053b0e895689
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.9 MB (180931648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2db2ee3d3996672b20309d4473a518f1b21f9c6a88b0ef69b9bd124829c4dc`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 08 Sep 2017 00:32:21 GMT
ADD file:483b3245941140ac32394a804364a1a9bd5dfdf1b4475238b61068cc7252ac08 in / 
# Fri, 08 Sep 2017 00:32:21 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 01:03:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 01:03:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 15 Sep 2017 00:36:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Sep 2017 00:36:25 GMT
ENV LANG=C.UTF-8
# Fri, 15 Sep 2017 00:36:34 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 15 Sep 2017 00:36:41 GMT
RUN ln -svT "/usr/lib/jvm/java-7-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 15 Sep 2017 00:36:43 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Fri, 15 Sep 2017 00:36:45 GMT
ENV JAVA_VERSION=7u151
# Fri, 15 Sep 2017 00:36:47 GMT
ENV JAVA_DEBIAN_VERSION=7u151-2.6.11-1~deb8u1
# Fri, 15 Sep 2017 00:50:36 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-7-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Fri, 15 Sep 2017 03:10:46 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 15 Sep 2017 03:10:48 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Sep 2017 03:10:53 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 15 Sep 2017 03:10:54 GMT
WORKDIR /usr/local/tomcat
# Fri, 15 Sep 2017 03:10:56 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 15 Sep 2017 03:10:58 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 15 Sep 2017 03:11:00 GMT
ENV OPENSSL_VERSION=1.1.0f-3
# Fri, 15 Sep 2017 03:11:05 GMT
RUN set -ex; 	if ! grep -q stretch /etc/apt/sources.list; then 		{ 			echo 'deb http://deb.debian.org/debian stretch main'; 		} > /etc/apt/sources.list.d/stretch.list; 		{ 			echo 'Package: *'; 			echo 'Pin: release n=stretch'; 			echo 'Pin-Priority: -10'; 			echo; 			echo 'Package: openssl libssl*'; 			echo "Pin: version $OPENSSL_VERSION"; 			echo 'Pin-Priority: 990'; 		} > /etc/apt/preferences.d/stretch-openssl; 	fi
# Fri, 15 Sep 2017 03:11:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libapr1 		openssl="$OPENSSL_VERSION" 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Sep 2017 03:11:57 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 15 Sep 2017 03:12:10 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Fri, 15 Sep 2017 03:12:12 GMT
ENV TOMCAT_MAJOR=7
# Fri, 15 Sep 2017 03:12:13 GMT
ENV TOMCAT_VERSION=7.0.81
# Fri, 15 Sep 2017 03:12:15 GMT
ENV TOMCAT_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=tomcat/tomcat-7/v7.0.81/bin/apache-tomcat-7.0.81.tar.gz
# Fri, 15 Sep 2017 03:12:16 GMT
ENV TOMCAT_ASC_URL=https://www.apache.org/dist/tomcat/tomcat-7/v7.0.81/bin/apache-tomcat-7.0.81.tar.gz.asc
# Fri, 15 Sep 2017 03:12:18 GMT
ENV TOMCAT_TGZ_FALLBACK_URL=https://archive.apache.org/dist/tomcat/tomcat-7/v7.0.81/bin/apache-tomcat-7.0.81.tar.gz
# Fri, 15 Sep 2017 03:12:20 GMT
ENV TOMCAT_ASC_FALLBACK_URL=https://archive.apache.org/dist/tomcat/tomcat-7/v7.0.81/bin/apache-tomcat-7.0.81.tar.gz.asc
# Fri, 15 Sep 2017 03:15:53 GMT
RUN set -x 		&& { 		wget -O tomcat.tar.gz "$TOMCAT_TGZ_URL" 		|| wget -O tomcat.tar.gz "$TOMCAT_TGZ_FALLBACK_URL" 	; } 	&& { 		wget -O tomcat.tar.gz.asc "$TOMCAT_ASC_URL" 		|| wget -O tomcat.tar.gz.asc "$TOMCAT_ASC_FALLBACK_URL" 	; } 	&& gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz 	&& tar -xvf tomcat.tar.gz --strip-components=1 	&& rm bin/*.bat 	&& rm tomcat.tar.gz* 		&& nativeBuildDir="$(mktemp -d)" 	&& tar -xvf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1 	&& nativeBuildDeps=" 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 		openjdk-${JAVA_VERSION%%[-~bu]*}-jdk=$JAVA_DEBIAN_VERSION 	" 	&& apt-get update && apt-get install -y --no-install-recommends $nativeBuildDeps && rm -rf /var/lib/apt/lists/* 	&& ( 		export CATALINA_HOME="$PWD" 		&& cd "$nativeBuildDir/native" 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		&& ./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$(which apr-1-config)" 			--with-java-home="$(docker-java-home)" 			--with-ssl=yes 		&& make -j "$(nproc)" 		&& make install 	) 	&& apt-get purge -y --auto-remove $nativeBuildDeps 	&& rm -rf "$nativeBuildDir" 	&& rm bin/tomcat-native.tar.gz 	&& find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +
# Fri, 15 Sep 2017 03:15:58 GMT
RUN set -e 	&& nativeLines="$(catalina.sh configtest 2>&1)" 	&& nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')" 	&& nativeLines="$(echo "$nativeLines" | sort -u)" 	&& if ! echo "$nativeLines" | grep 'INFO: Loaded APR based Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 15 Sep 2017 03:16:00 GMT
EXPOSE 8080/tcp
# Fri, 15 Sep 2017 03:16:02 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:d4a5434e09b7ac8431060d347d6ef1233ae07514878fb2aff4085bcf441c29f3`  
		Last Modified: Fri, 08 Sep 2017 00:36:52 GMT  
		Size: 51.8 MB (51809570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48596af2c38701f94440e222bf8f3d4b2da85e2982c97ae15186eba523249e0b`  
		Last Modified: Thu, 14 Sep 2017 22:21:02 GMT  
		Size: 19.2 MB (19199596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93aff8e404272e9833703642ba3aa88fed68af07050f24c7709f569d0ac750dc`  
		Last Modified: Fri, 15 Sep 2017 01:44:08 GMT  
		Size: 791.2 KB (791186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47834a4accdc027a0c9c901088dc1f86871788bde1184be049ad9bd7c3e73851`  
		Last Modified: Fri, 15 Sep 2017 01:44:07 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9aee3929de836275f650ebba768390489923f17a18f3a704c24aa5b63b17d7d`  
		Last Modified: Fri, 15 Sep 2017 01:44:07 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d933a6047136f6e6fffa90ce2f3fbe1e16d0a5411b123e2c8b18e5fafa87b823`  
		Last Modified: Fri, 15 Sep 2017 01:44:37 GMT  
		Size: 96.2 MB (96155763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d425780ba1ad23c183405cd2e790e62faa786d0d6348d41724afb5244252bf`  
		Last Modified: Fri, 15 Sep 2017 03:40:06 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b9ad87583610aef96d757f18662495be04a1d2c111bdd6950bfc6d3fe634ebc`  
		Last Modified: Fri, 15 Sep 2017 03:40:03 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83e8f959a70d59a87bcfbb7bc7a1b691a03cda547cae04ba6fc5905d1b781ba8`  
		Last Modified: Fri, 15 Sep 2017 03:40:04 GMT  
		Size: 2.9 MB (2920882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bbd0609c5d75b566ff8905b4604ca40db06dd408d6c81ad3fe5b3069d10c799`  
		Last Modified: Fri, 15 Sep 2017 03:40:04 GMT  
		Size: 113.9 KB (113872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d96aaaca1e2ba5b01c8fd8533999c00c9415d1944880baf6538de9a49e273731`  
		Last Modified: Fri, 15 Sep 2017 03:40:06 GMT  
		Size: 9.9 MB (9939749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada46caff61aab29d00052b96379942d76802bb6d92f92a904c9bb2573d97d4f`  
		Last Modified: Fri, 15 Sep 2017 03:40:03 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:7-jre7` - linux; s390x

```console
$ docker pull tomcat@sha256:6b569363ad3cd2eb26d21b7b8b4e2cebfe3c6b919d4ad9704f4a8cfd01c03e5a
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.9 MB (181894687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8c6046a6158c60a4059978584fff0c6be9bf22f5204f45a47370f7f6598d118`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 08 Sep 2017 05:21:42 GMT
ADD file:996e52a941b7162fafcf761c415142a34a2fc703e21d2f264b824373e9fa4b1e in / 
# Fri, 08 Sep 2017 05:21:43 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 05:48:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 05:48:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 08 Sep 2017 17:29:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 17:29:02 GMT
ENV LANG=C.UTF-8
# Fri, 08 Sep 2017 17:29:03 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 08 Sep 2017 17:29:03 GMT
RUN ln -svT "/usr/lib/jvm/java-7-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 08 Sep 2017 17:29:03 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Fri, 08 Sep 2017 17:29:04 GMT
ENV JAVA_VERSION=7u151
# Fri, 08 Sep 2017 17:29:04 GMT
ENV JAVA_DEBIAN_VERSION=7u151-2.6.11-1~deb8u1
# Sat, 09 Sep 2017 05:39:03 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-7-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Sat, 09 Sep 2017 05:59:37 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 09 Sep 2017 05:59:37 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Sep 2017 05:59:39 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 09 Sep 2017 05:59:39 GMT
WORKDIR /usr/local/tomcat
# Sat, 09 Sep 2017 05:59:39 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 09 Sep 2017 05:59:39 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 09 Sep 2017 05:59:39 GMT
ENV OPENSSL_VERSION=1.1.0f-3
# Sat, 09 Sep 2017 05:59:40 GMT
RUN set -ex; 	if ! grep -q stretch /etc/apt/sources.list; then 		{ 			echo 'deb http://deb.debian.org/debian stretch main'; 		} > /etc/apt/sources.list.d/stretch.list; 		{ 			echo 'Package: *'; 			echo 'Pin: release n=stretch'; 			echo 'Pin-Priority: -10'; 			echo; 			echo 'Package: openssl libssl*'; 			echo "Pin: version $OPENSSL_VERSION"; 			echo 'Pin-Priority: 990'; 		} > /etc/apt/preferences.d/stretch-openssl; 	fi
# Sat, 09 Sep 2017 05:59:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libapr1 		openssl="$OPENSSL_VERSION" 	&& rm -rf /var/lib/apt/lists/*
# Sat, 09 Sep 2017 05:59:54 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Sat, 09 Sep 2017 05:59:58 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Sat, 09 Sep 2017 05:59:59 GMT
ENV TOMCAT_MAJOR=7
# Sat, 09 Sep 2017 05:59:59 GMT
ENV TOMCAT_VERSION=7.0.81
# Sat, 09 Sep 2017 05:59:59 GMT
ENV TOMCAT_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=tomcat/tomcat-7/v7.0.81/bin/apache-tomcat-7.0.81.tar.gz
# Sat, 09 Sep 2017 05:59:59 GMT
ENV TOMCAT_ASC_URL=https://www.apache.org/dist/tomcat/tomcat-7/v7.0.81/bin/apache-tomcat-7.0.81.tar.gz.asc
# Sat, 09 Sep 2017 05:59:59 GMT
ENV TOMCAT_TGZ_FALLBACK_URL=https://archive.apache.org/dist/tomcat/tomcat-7/v7.0.81/bin/apache-tomcat-7.0.81.tar.gz
# Sat, 09 Sep 2017 05:59:59 GMT
ENV TOMCAT_ASC_FALLBACK_URL=https://archive.apache.org/dist/tomcat/tomcat-7/v7.0.81/bin/apache-tomcat-7.0.81.tar.gz.asc
# Sat, 09 Sep 2017 06:00:47 GMT
RUN set -x 		&& { 		wget -O tomcat.tar.gz "$TOMCAT_TGZ_URL" 		|| wget -O tomcat.tar.gz "$TOMCAT_TGZ_FALLBACK_URL" 	; } 	&& { 		wget -O tomcat.tar.gz.asc "$TOMCAT_ASC_URL" 		|| wget -O tomcat.tar.gz.asc "$TOMCAT_ASC_FALLBACK_URL" 	; } 	&& gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz 	&& tar -xvf tomcat.tar.gz --strip-components=1 	&& rm bin/*.bat 	&& rm tomcat.tar.gz* 		&& nativeBuildDir="$(mktemp -d)" 	&& tar -xvf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1 	&& nativeBuildDeps=" 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 		openjdk-${JAVA_VERSION%%[-~bu]*}-jdk=$JAVA_DEBIAN_VERSION 	" 	&& apt-get update && apt-get install -y --no-install-recommends $nativeBuildDeps && rm -rf /var/lib/apt/lists/* 	&& ( 		export CATALINA_HOME="$PWD" 		&& cd "$nativeBuildDir/native" 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		&& ./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$(which apr-1-config)" 			--with-java-home="$(docker-java-home)" 			--with-ssl=yes 		&& make -j "$(nproc)" 		&& make install 	) 	&& apt-get purge -y --auto-remove $nativeBuildDeps 	&& rm -rf "$nativeBuildDir" 	&& rm bin/tomcat-native.tar.gz 	&& find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +
# Sat, 09 Sep 2017 06:00:49 GMT
RUN set -e 	&& nativeLines="$(catalina.sh configtest 2>&1)" 	&& nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')" 	&& nativeLines="$(echo "$nativeLines" | sort -u)" 	&& if ! echo "$nativeLines" | grep 'INFO: Loaded APR based Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 09 Sep 2017 06:00:49 GMT
EXPOSE 8080/tcp
# Sat, 09 Sep 2017 06:00:49 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5f39dbffcd07e3254246d3c2e4b3532c3697ed04f83eadf5433da820098787df`  
		Last Modified: Fri, 08 Sep 2017 05:24:42 GMT  
		Size: 52.8 MB (52788802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5a344275c5d5a12a16990e9ddb7cfb9bc9b793cc51fbf8bf8993426e287c27`  
		Last Modified: Fri, 08 Sep 2017 16:41:52 GMT  
		Size: 19.5 MB (19470373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c084b3ab1af5428f9981ab28f3dd2a8f154f246fb9d9ce2e9e3782792ea6e7`  
		Last Modified: Fri, 08 Sep 2017 17:34:17 GMT  
		Size: 804.2 KB (804244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6057421880039b10c9b7e533d65d4d7e17bf4a8ce08d971a425491d4efb98f39`  
		Last Modified: Fri, 08 Sep 2017 17:34:17 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7677a9187fddb4ecce26b38d362093884ab54cbd74d93eb2fe859fd6db870285`  
		Last Modified: Fri, 08 Sep 2017 17:34:17 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e221891b78d1067cea90f003fa97c1e3c96c3f47ed7510c321eb3130857ae1f`  
		Last Modified: Sat, 09 Sep 2017 05:42:14 GMT  
		Size: 95.7 MB (95680047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a72dd7a800cc7f23b257791f7386b2605c4cc8f44d734138dcb711efd5068c`  
		Last Modified: Sat, 09 Sep 2017 06:03:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e697c96f4cbeece9fb6c50d3ff15dbca13a3e4b9d7e614cfb8d40aaf1385d2`  
		Last Modified: Sat, 09 Sep 2017 06:03:32 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23caffb4636bfcba4572b7367e7fb83c1d1cb6f3e805accf814f69cdbaadbf31`  
		Last Modified: Sat, 09 Sep 2017 06:03:33 GMT  
		Size: 3.0 MB (3005377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b23f633bc45c9b424bfc32768803463ade48b1998ea4ec13b719f1af673f65`  
		Last Modified: Sat, 09 Sep 2017 06:03:32 GMT  
		Size: 113.8 KB (113846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b3d7438ac64c62e761143eb719b6c035a58c4fbe8351825f67ee8e7fcbc52b5`  
		Last Modified: Sat, 09 Sep 2017 06:03:33 GMT  
		Size: 10.0 MB (10031005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e79bcb10f6c4c309c609fc0158c5cbd53a074dc73d58bd6cdfbcc143ab6a5a`  
		Last Modified: Sat, 09 Sep 2017 06:03:34 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
