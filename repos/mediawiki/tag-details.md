<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mediawiki`

-	[`mediawiki:1.27`](#mediawiki127)
-	[`mediawiki:1.27.3`](#mediawiki1273)
-	[`mediawiki:1.28`](#mediawiki128)
-	[`mediawiki:1.28.2`](#mediawiki1282)
-	[`mediawiki:1.29`](#mediawiki129)
-	[`mediawiki:1.29.1`](#mediawiki1291)
-	[`mediawiki:latest`](#mediawikilatest)
-	[`mediawiki:legacy`](#mediawikilegacy)
-	[`mediawiki:lts`](#mediawikilts)
-	[`mediawiki:stable`](#mediawikistable)

## `mediawiki:1.27`

```console
$ docker pull mediawiki@sha256:9df58ec967985038a57df791286826e2569a714f00b7289478ff1c790ce7000b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mediawiki:1.27` - linux; amd64

```console
$ docker pull mediawiki@sha256:51a38d067566c19a0d3dae17be86e2bc7590e885d9c896bd0f0c09b8481cbb9d
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.4 MB (245375379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af897575138a24b57dd6b6a96cef4d53694f17f3d826491acaca6373538fe3f5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 13 Sep 2017 08:40:43 GMT
ADD file:d7333b3e0bc6479d2faed32e06d85f1975e5b23e13e75555aeed0f639770413b in / 
# Wed, 13 Sep 2017 08:40:43 GMT
CMD ["bash"]
# Thu, 14 Sep 2017 23:57:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		libpcre3-dev 		make 		pkg-config 		re2c
# Thu, 14 Sep 2017 23:58:23 GMT
RUN apt-get update && apt-get install -y 		$PHPIZE_DEPS 		ca-certificates 		curl 		libedit2 		libsqlite3-0 		libxml2 		xz-utils 	--no-install-recommends && rm -r /var/lib/apt/lists/*
# Thu, 14 Sep 2017 23:58:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Sep 2017 23:58:24 GMT
RUN mkdir -p $PHP_INI_DIR/conf.d
# Fri, 15 Sep 2017 00:08:17 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		apache2 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Sep 2017 00:08:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 15 Sep 2017 00:08:18 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 15 Sep 2017 00:08:18 GMT
RUN set -ex 		&& sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS" 		&& . "$APACHE_ENVVARS" 	&& for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		/var/www/html 	; do 		rm -rvf "$dir" 		&& mkdir -p "$dir" 		&& chown -R "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 	done
# Fri, 15 Sep 2017 00:08:19 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 15 Sep 2017 00:08:19 GMT
RUN set -ex 	&& . "$APACHE_ENVVARS" 	&& ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log" 	&& ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log" 	&& ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"
# Fri, 15 Sep 2017 00:08:20 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 15 Sep 2017 00:08:20 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 15 Sep 2017 00:08:20 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2
# Fri, 15 Sep 2017 00:08:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 15 Sep 2017 00:08:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 15 Sep 2017 00:08:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Fri, 15 Sep 2017 00:39:01 GMT
ENV GPG_KEYS=1A4E8B7277C42E53DBA9C7B9BCAA30EA9C0D5763 6E4F6AB321FDC07F2C332E3AC2BF0BC433CFC8B3
# Fri, 29 Sep 2017 00:45:54 GMT
ENV PHP_VERSION=7.0.24
# Fri, 29 Sep 2017 00:45:54 GMT
ENV PHP_URL=https://secure.php.net/get/php-7.0.24.tar.xz/from/this/mirror PHP_ASC_URL=https://secure.php.net/get/php-7.0.24.tar.xz.asc/from/this/mirror
# Fri, 29 Sep 2017 00:45:55 GMT
ENV PHP_SHA256=4dba7aa365193c9229f89f1975fad4c01135d29922a338ffb4a27e840d6f1c98 PHP_MD5=
# Fri, 29 Sep 2017 00:46:19 GMT
RUN set -xe; 		fetchDeps=' 		wget 	'; 	if ! command -v gpg > /dev/null; then 		fetchDeps="$fetchDeps 			dirmngr 			gnupg2 		"; 	fi; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		wget -O php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		wget -O php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps
# Fri, 29 Sep 2017 00:46:19 GMT
COPY file:207c686e3fed4f71f8a7b245d8dcae9c9048d276a326d82b553c12a90af0c0ca in /usr/local/bin/ 
# Fri, 29 Sep 2017 00:48:50 GMT
RUN set -xe 	&& buildDeps=" 		$PHP_EXTRA_BUILD_DEPS 		libcurl4-openssl-dev 		libedit-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	" 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	&& docker-php-source extract 	&& cd /usr/src/php 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)" 	&& if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi 	&& ./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--disable-cgi 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pcre-regex=/usr 		--with-libdir="lib/$debMultiarch" 				$PHP_EXTRA_CONFIGURE_ARGS 	&& make -j "$(nproc)" 	&& make install 	&& { find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; } 	&& make clean 	&& cd / 	&& docker-php-source delete 		&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $buildDeps 		&& pecl update-channels 	&& rm -rf /tmp/pear ~/.pearrc
# Fri, 29 Sep 2017 00:48:50 GMT
COPY multi:dbabcc0b81566a75f49e7faa9ca5f96cd22a515b80ee7ea1e34fceceee3f9c2a in /usr/local/bin/ 
# Fri, 29 Sep 2017 00:48:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 29 Sep 2017 00:48:51 GMT
COPY file:24613ecbb1ce6a09f683b0753da9c26a1af07547326e8a02f6eec80ad6f2774a in /usr/local/bin/ 
# Fri, 29 Sep 2017 00:48:51 GMT
WORKDIR /var/www/html
# Fri, 29 Sep 2017 00:48:51 GMT
EXPOSE 80/tcp
# Fri, 29 Sep 2017 00:48:51 GMT
CMD ["apache2-foreground"]
# Fri, 29 Sep 2017 01:43:32 GMT
RUN apt-get update && apt-get install -y 		git 		imagemagick 		libicu-dev 	--no-install-recommends && rm -r /var/lib/apt/lists/*
# Fri, 29 Sep 2017 01:44:43 GMT
RUN docker-php-ext-install mbstring mysqli opcache intl
# Fri, 29 Sep 2017 01:46:04 GMT
RUN pecl channel-update pecl.php.net 	&& pecl install apcu-5.1.8 	&& docker-php-ext-enable apcu
# Fri, 29 Sep 2017 01:46:05 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 		echo 'opcache.enable_cli=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 29 Sep 2017 01:46:05 GMT
RUN mkdir -p /var/www/data 	&& chown -R www-data:www-data /var/www/data
# Fri, 29 Sep 2017 01:49:44 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.27
# Fri, 29 Sep 2017 01:49:44 GMT
ENV MEDIAWIKI_BRANCH=REL1_27
# Fri, 29 Sep 2017 01:49:44 GMT
ENV MEDIAWIKI_VERSION=1.27.3
# Fri, 29 Sep 2017 01:49:44 GMT
ENV MEDIAWIKI_SHA512=bc6228342b589a3acb0f5623b9ef45982d7aab032ff322aaf7bda7ac3ee16a7732b8013698d8f509da4310bbb65c12a73b7bbe4612d5e0e3d93965199efdc8eb
# Fri, 29 Sep 2017 01:49:50 GMT
RUN curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz 	&& echo "${MEDIAWIKI_SHA512} *mediawiki.tar.gz" | sha512sum -c - 	&& tar -xz --strip-components=1 -f mediawiki.tar.gz 	&& rm mediawiki.tar.gz 	&& chown -R www-data:www-data extensions skins cache images
```

-	Layers:
	-	`sha256:aa18ad1a0d334d80981104c599fa8cef9264552a265b1197af11274beba767cf`  
		Last Modified: Thu, 07 Sep 2017 23:11:06 GMT  
		Size: 52.6 MB (52595547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d5f85af454812aec1820ce0e52e003b81e4569823e2da5b0cccb58e31b136f`  
		Last Modified: Fri, 15 Sep 2017 01:34:31 GMT  
		Size: 82.5 MB (82495988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca642e7826b9552669a262d36f5488e3a478c2f9f97a98db37b203194ea6248`  
		Last Modified: Fri, 15 Sep 2017 01:34:12 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3638d91a90398e9b21e86d5f58ce592dcef089e461ed52559ddcc99d1021c04b`  
		Last Modified: Fri, 15 Sep 2017 01:35:48 GMT  
		Size: 3.0 MB (3012522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3646a95ab6778f36ca28c448f0217a571157bd80a83faa94284a046540d9b90e`  
		Last Modified: Fri, 15 Sep 2017 01:35:46 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628b8373e193144e4047261fde47c3b10881e013cc4730690c28281e30f340d4`  
		Last Modified: Fri, 15 Sep 2017 01:35:45 GMT  
		Size: 431.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24a2b2280edf466db78ea09cb8f23295781c7472f63e5ee7ebd5302e6ef3c45`  
		Last Modified: Fri, 15 Sep 2017 01:35:45 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f968b84cbbbc7f23c623c4ae9ad247431a59a370333ec20de8191284b4838b54`  
		Last Modified: Fri, 15 Sep 2017 01:35:44 GMT  
		Size: 485.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eba9b5fa4872bbe2b17063876e02d94e27ed76aaae378ff06f4fb5fabe92cca`  
		Last Modified: Fri, 29 Sep 2017 01:22:29 GMT  
		Size: 12.3 MB (12314249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0234067d12410685389f8fb0c6baa2ad79e2258de03ee29c0880902e4fb9d5e0`  
		Last Modified: Fri, 29 Sep 2017 01:22:27 GMT  
		Size: 502.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b85a2b999ef3bb1a50a67119cf987b7731cb7b0c1db3b4e40cad13de362b2b7a`  
		Last Modified: Fri, 29 Sep 2017 01:22:34 GMT  
		Size: 13.2 MB (13212054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d31395fe2313a4fde865b2d1f5309793fb4115b44960bc26a7b3b98e288c6ca`  
		Last Modified: Fri, 29 Sep 2017 01:22:28 GMT  
		Size: 2.2 KB (2180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cff026afe51f89f948e975c0e3d1eaa0b96d81c64131c518e03067fdded35f4`  
		Last Modified: Fri, 29 Sep 2017 01:22:27 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98fe309fb9f48e5ef6e9b0fb75f556ad442242b6564bc9a195c0940f5fa24e07`  
		Last Modified: Fri, 29 Sep 2017 01:50:17 GMT  
		Size: 48.1 MB (48128140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b595c41b7857b1df5a2deb28ee4bd4dfaad5394f4d3c6c01b75813dd5e77bb3`  
		Last Modified: Fri, 29 Sep 2017 01:50:04 GMT  
		Size: 1.4 MB (1396887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcfdff861639f786eaee6312b7d55a7a6dc5701f9127cd6dda7bd439772f8d87`  
		Last Modified: Fri, 29 Sep 2017 01:50:04 GMT  
		Size: 324.7 KB (324705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e042b08e2f1c8ab292b65a02ae566d8102407fdc6b9b7b37a85497059d63612`  
		Last Modified: Fri, 29 Sep 2017 01:50:04 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f56197b8593bfc486b67dc5e0145ea549653a73d2fb64be3622c1aca733aaef`  
		Last Modified: Fri, 29 Sep 2017 01:50:04 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c3e1b3f0ce55a9e4ed949938077f5668b285d3329740b9766bb93b31dc34a46`  
		Last Modified: Fri, 29 Sep 2017 01:50:55 GMT  
		Size: 31.9 MB (31888632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mediawiki:1.27.3`

```console
$ docker pull mediawiki@sha256:9df58ec967985038a57df791286826e2569a714f00b7289478ff1c790ce7000b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mediawiki:1.27.3` - linux; amd64

```console
$ docker pull mediawiki@sha256:51a38d067566c19a0d3dae17be86e2bc7590e885d9c896bd0f0c09b8481cbb9d
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.4 MB (245375379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af897575138a24b57dd6b6a96cef4d53694f17f3d826491acaca6373538fe3f5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 13 Sep 2017 08:40:43 GMT
ADD file:d7333b3e0bc6479d2faed32e06d85f1975e5b23e13e75555aeed0f639770413b in / 
# Wed, 13 Sep 2017 08:40:43 GMT
CMD ["bash"]
# Thu, 14 Sep 2017 23:57:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		libpcre3-dev 		make 		pkg-config 		re2c
# Thu, 14 Sep 2017 23:58:23 GMT
RUN apt-get update && apt-get install -y 		$PHPIZE_DEPS 		ca-certificates 		curl 		libedit2 		libsqlite3-0 		libxml2 		xz-utils 	--no-install-recommends && rm -r /var/lib/apt/lists/*
# Thu, 14 Sep 2017 23:58:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Sep 2017 23:58:24 GMT
RUN mkdir -p $PHP_INI_DIR/conf.d
# Fri, 15 Sep 2017 00:08:17 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		apache2 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Sep 2017 00:08:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 15 Sep 2017 00:08:18 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 15 Sep 2017 00:08:18 GMT
RUN set -ex 		&& sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS" 		&& . "$APACHE_ENVVARS" 	&& for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		/var/www/html 	; do 		rm -rvf "$dir" 		&& mkdir -p "$dir" 		&& chown -R "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 	done
# Fri, 15 Sep 2017 00:08:19 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 15 Sep 2017 00:08:19 GMT
RUN set -ex 	&& . "$APACHE_ENVVARS" 	&& ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log" 	&& ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log" 	&& ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"
# Fri, 15 Sep 2017 00:08:20 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 15 Sep 2017 00:08:20 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 15 Sep 2017 00:08:20 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2
# Fri, 15 Sep 2017 00:08:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 15 Sep 2017 00:08:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 15 Sep 2017 00:08:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Fri, 15 Sep 2017 00:39:01 GMT
ENV GPG_KEYS=1A4E8B7277C42E53DBA9C7B9BCAA30EA9C0D5763 6E4F6AB321FDC07F2C332E3AC2BF0BC433CFC8B3
# Fri, 29 Sep 2017 00:45:54 GMT
ENV PHP_VERSION=7.0.24
# Fri, 29 Sep 2017 00:45:54 GMT
ENV PHP_URL=https://secure.php.net/get/php-7.0.24.tar.xz/from/this/mirror PHP_ASC_URL=https://secure.php.net/get/php-7.0.24.tar.xz.asc/from/this/mirror
# Fri, 29 Sep 2017 00:45:55 GMT
ENV PHP_SHA256=4dba7aa365193c9229f89f1975fad4c01135d29922a338ffb4a27e840d6f1c98 PHP_MD5=
# Fri, 29 Sep 2017 00:46:19 GMT
RUN set -xe; 		fetchDeps=' 		wget 	'; 	if ! command -v gpg > /dev/null; then 		fetchDeps="$fetchDeps 			dirmngr 			gnupg2 		"; 	fi; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		wget -O php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		wget -O php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps
# Fri, 29 Sep 2017 00:46:19 GMT
COPY file:207c686e3fed4f71f8a7b245d8dcae9c9048d276a326d82b553c12a90af0c0ca in /usr/local/bin/ 
# Fri, 29 Sep 2017 00:48:50 GMT
RUN set -xe 	&& buildDeps=" 		$PHP_EXTRA_BUILD_DEPS 		libcurl4-openssl-dev 		libedit-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	" 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	&& docker-php-source extract 	&& cd /usr/src/php 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)" 	&& if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi 	&& ./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--disable-cgi 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pcre-regex=/usr 		--with-libdir="lib/$debMultiarch" 				$PHP_EXTRA_CONFIGURE_ARGS 	&& make -j "$(nproc)" 	&& make install 	&& { find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; } 	&& make clean 	&& cd / 	&& docker-php-source delete 		&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $buildDeps 		&& pecl update-channels 	&& rm -rf /tmp/pear ~/.pearrc
# Fri, 29 Sep 2017 00:48:50 GMT
COPY multi:dbabcc0b81566a75f49e7faa9ca5f96cd22a515b80ee7ea1e34fceceee3f9c2a in /usr/local/bin/ 
# Fri, 29 Sep 2017 00:48:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 29 Sep 2017 00:48:51 GMT
COPY file:24613ecbb1ce6a09f683b0753da9c26a1af07547326e8a02f6eec80ad6f2774a in /usr/local/bin/ 
# Fri, 29 Sep 2017 00:48:51 GMT
WORKDIR /var/www/html
# Fri, 29 Sep 2017 00:48:51 GMT
EXPOSE 80/tcp
# Fri, 29 Sep 2017 00:48:51 GMT
CMD ["apache2-foreground"]
# Fri, 29 Sep 2017 01:43:32 GMT
RUN apt-get update && apt-get install -y 		git 		imagemagick 		libicu-dev 	--no-install-recommends && rm -r /var/lib/apt/lists/*
# Fri, 29 Sep 2017 01:44:43 GMT
RUN docker-php-ext-install mbstring mysqli opcache intl
# Fri, 29 Sep 2017 01:46:04 GMT
RUN pecl channel-update pecl.php.net 	&& pecl install apcu-5.1.8 	&& docker-php-ext-enable apcu
# Fri, 29 Sep 2017 01:46:05 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 		echo 'opcache.enable_cli=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 29 Sep 2017 01:46:05 GMT
RUN mkdir -p /var/www/data 	&& chown -R www-data:www-data /var/www/data
# Fri, 29 Sep 2017 01:49:44 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.27
# Fri, 29 Sep 2017 01:49:44 GMT
ENV MEDIAWIKI_BRANCH=REL1_27
# Fri, 29 Sep 2017 01:49:44 GMT
ENV MEDIAWIKI_VERSION=1.27.3
# Fri, 29 Sep 2017 01:49:44 GMT
ENV MEDIAWIKI_SHA512=bc6228342b589a3acb0f5623b9ef45982d7aab032ff322aaf7bda7ac3ee16a7732b8013698d8f509da4310bbb65c12a73b7bbe4612d5e0e3d93965199efdc8eb
# Fri, 29 Sep 2017 01:49:50 GMT
RUN curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz 	&& echo "${MEDIAWIKI_SHA512} *mediawiki.tar.gz" | sha512sum -c - 	&& tar -xz --strip-components=1 -f mediawiki.tar.gz 	&& rm mediawiki.tar.gz 	&& chown -R www-data:www-data extensions skins cache images
```

-	Layers:
	-	`sha256:aa18ad1a0d334d80981104c599fa8cef9264552a265b1197af11274beba767cf`  
		Last Modified: Thu, 07 Sep 2017 23:11:06 GMT  
		Size: 52.6 MB (52595547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d5f85af454812aec1820ce0e52e003b81e4569823e2da5b0cccb58e31b136f`  
		Last Modified: Fri, 15 Sep 2017 01:34:31 GMT  
		Size: 82.5 MB (82495988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca642e7826b9552669a262d36f5488e3a478c2f9f97a98db37b203194ea6248`  
		Last Modified: Fri, 15 Sep 2017 01:34:12 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3638d91a90398e9b21e86d5f58ce592dcef089e461ed52559ddcc99d1021c04b`  
		Last Modified: Fri, 15 Sep 2017 01:35:48 GMT  
		Size: 3.0 MB (3012522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3646a95ab6778f36ca28c448f0217a571157bd80a83faa94284a046540d9b90e`  
		Last Modified: Fri, 15 Sep 2017 01:35:46 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628b8373e193144e4047261fde47c3b10881e013cc4730690c28281e30f340d4`  
		Last Modified: Fri, 15 Sep 2017 01:35:45 GMT  
		Size: 431.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24a2b2280edf466db78ea09cb8f23295781c7472f63e5ee7ebd5302e6ef3c45`  
		Last Modified: Fri, 15 Sep 2017 01:35:45 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f968b84cbbbc7f23c623c4ae9ad247431a59a370333ec20de8191284b4838b54`  
		Last Modified: Fri, 15 Sep 2017 01:35:44 GMT  
		Size: 485.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eba9b5fa4872bbe2b17063876e02d94e27ed76aaae378ff06f4fb5fabe92cca`  
		Last Modified: Fri, 29 Sep 2017 01:22:29 GMT  
		Size: 12.3 MB (12314249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0234067d12410685389f8fb0c6baa2ad79e2258de03ee29c0880902e4fb9d5e0`  
		Last Modified: Fri, 29 Sep 2017 01:22:27 GMT  
		Size: 502.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b85a2b999ef3bb1a50a67119cf987b7731cb7b0c1db3b4e40cad13de362b2b7a`  
		Last Modified: Fri, 29 Sep 2017 01:22:34 GMT  
		Size: 13.2 MB (13212054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d31395fe2313a4fde865b2d1f5309793fb4115b44960bc26a7b3b98e288c6ca`  
		Last Modified: Fri, 29 Sep 2017 01:22:28 GMT  
		Size: 2.2 KB (2180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cff026afe51f89f948e975c0e3d1eaa0b96d81c64131c518e03067fdded35f4`  
		Last Modified: Fri, 29 Sep 2017 01:22:27 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98fe309fb9f48e5ef6e9b0fb75f556ad442242b6564bc9a195c0940f5fa24e07`  
		Last Modified: Fri, 29 Sep 2017 01:50:17 GMT  
		Size: 48.1 MB (48128140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b595c41b7857b1df5a2deb28ee4bd4dfaad5394f4d3c6c01b75813dd5e77bb3`  
		Last Modified: Fri, 29 Sep 2017 01:50:04 GMT  
		Size: 1.4 MB (1396887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcfdff861639f786eaee6312b7d55a7a6dc5701f9127cd6dda7bd439772f8d87`  
		Last Modified: Fri, 29 Sep 2017 01:50:04 GMT  
		Size: 324.7 KB (324705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e042b08e2f1c8ab292b65a02ae566d8102407fdc6b9b7b37a85497059d63612`  
		Last Modified: Fri, 29 Sep 2017 01:50:04 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f56197b8593bfc486b67dc5e0145ea549653a73d2fb64be3622c1aca733aaef`  
		Last Modified: Fri, 29 Sep 2017 01:50:04 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c3e1b3f0ce55a9e4ed949938077f5668b285d3329740b9766bb93b31dc34a46`  
		Last Modified: Fri, 29 Sep 2017 01:50:55 GMT  
		Size: 31.9 MB (31888632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mediawiki:1.28`

```console
$ docker pull mediawiki@sha256:a31e1f83e8aef40487f9ae07afc7c6ba793921efbb9d488a23b4722e6d3ac5e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mediawiki:1.28` - linux; amd64

```console
$ docker pull mediawiki@sha256:af783c50af7ea56e7e50d3fffb0076f754ab29b31b1f422b4b810f8b9fc1099a
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.9 MB (246864575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852e1be5b054ce20547f5fdffc6256eb5c56dc10e7e19d6ad67186fafb23f17e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 13 Sep 2017 08:40:43 GMT
ADD file:d7333b3e0bc6479d2faed32e06d85f1975e5b23e13e75555aeed0f639770413b in / 
# Wed, 13 Sep 2017 08:40:43 GMT
CMD ["bash"]
# Thu, 14 Sep 2017 23:57:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		libpcre3-dev 		make 		pkg-config 		re2c
# Thu, 14 Sep 2017 23:58:23 GMT
RUN apt-get update && apt-get install -y 		$PHPIZE_DEPS 		ca-certificates 		curl 		libedit2 		libsqlite3-0 		libxml2 		xz-utils 	--no-install-recommends && rm -r /var/lib/apt/lists/*
# Thu, 14 Sep 2017 23:58:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Sep 2017 23:58:24 GMT
RUN mkdir -p $PHP_INI_DIR/conf.d
# Fri, 15 Sep 2017 00:08:17 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		apache2 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Sep 2017 00:08:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 15 Sep 2017 00:08:18 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 15 Sep 2017 00:08:18 GMT
RUN set -ex 		&& sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS" 		&& . "$APACHE_ENVVARS" 	&& for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		/var/www/html 	; do 		rm -rvf "$dir" 		&& mkdir -p "$dir" 		&& chown -R "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 	done
# Fri, 15 Sep 2017 00:08:19 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 15 Sep 2017 00:08:19 GMT
RUN set -ex 	&& . "$APACHE_ENVVARS" 	&& ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log" 	&& ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log" 	&& ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"
# Fri, 15 Sep 2017 00:08:20 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 15 Sep 2017 00:08:20 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 15 Sep 2017 00:08:20 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2
# Fri, 15 Sep 2017 00:08:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 15 Sep 2017 00:08:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 15 Sep 2017 00:08:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Fri, 15 Sep 2017 00:39:01 GMT
ENV GPG_KEYS=1A4E8B7277C42E53DBA9C7B9BCAA30EA9C0D5763 6E4F6AB321FDC07F2C332E3AC2BF0BC433CFC8B3
# Fri, 29 Sep 2017 00:45:54 GMT
ENV PHP_VERSION=7.0.24
# Fri, 29 Sep 2017 00:45:54 GMT
ENV PHP_URL=https://secure.php.net/get/php-7.0.24.tar.xz/from/this/mirror PHP_ASC_URL=https://secure.php.net/get/php-7.0.24.tar.xz.asc/from/this/mirror
# Fri, 29 Sep 2017 00:45:55 GMT
ENV PHP_SHA256=4dba7aa365193c9229f89f1975fad4c01135d29922a338ffb4a27e840d6f1c98 PHP_MD5=
# Fri, 29 Sep 2017 00:46:19 GMT
RUN set -xe; 		fetchDeps=' 		wget 	'; 	if ! command -v gpg > /dev/null; then 		fetchDeps="$fetchDeps 			dirmngr 			gnupg2 		"; 	fi; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		wget -O php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		wget -O php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps
# Fri, 29 Sep 2017 00:46:19 GMT
COPY file:207c686e3fed4f71f8a7b245d8dcae9c9048d276a326d82b553c12a90af0c0ca in /usr/local/bin/ 
# Fri, 29 Sep 2017 00:48:50 GMT
RUN set -xe 	&& buildDeps=" 		$PHP_EXTRA_BUILD_DEPS 		libcurl4-openssl-dev 		libedit-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	" 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	&& docker-php-source extract 	&& cd /usr/src/php 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)" 	&& if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi 	&& ./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--disable-cgi 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pcre-regex=/usr 		--with-libdir="lib/$debMultiarch" 				$PHP_EXTRA_CONFIGURE_ARGS 	&& make -j "$(nproc)" 	&& make install 	&& { find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; } 	&& make clean 	&& cd / 	&& docker-php-source delete 		&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $buildDeps 		&& pecl update-channels 	&& rm -rf /tmp/pear ~/.pearrc
# Fri, 29 Sep 2017 00:48:50 GMT
COPY multi:dbabcc0b81566a75f49e7faa9ca5f96cd22a515b80ee7ea1e34fceceee3f9c2a in /usr/local/bin/ 
# Fri, 29 Sep 2017 00:48:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 29 Sep 2017 00:48:51 GMT
COPY file:24613ecbb1ce6a09f683b0753da9c26a1af07547326e8a02f6eec80ad6f2774a in /usr/local/bin/ 
# Fri, 29 Sep 2017 00:48:51 GMT
WORKDIR /var/www/html
# Fri, 29 Sep 2017 00:48:51 GMT
EXPOSE 80/tcp
# Fri, 29 Sep 2017 00:48:51 GMT
CMD ["apache2-foreground"]
# Fri, 29 Sep 2017 01:43:32 GMT
RUN apt-get update && apt-get install -y 		git 		imagemagick 		libicu-dev 	--no-install-recommends && rm -r /var/lib/apt/lists/*
# Fri, 29 Sep 2017 01:44:43 GMT
RUN docker-php-ext-install mbstring mysqli opcache intl
# Fri, 29 Sep 2017 01:46:04 GMT
RUN pecl channel-update pecl.php.net 	&& pecl install apcu-5.1.8 	&& docker-php-ext-enable apcu
# Fri, 29 Sep 2017 01:46:05 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 		echo 'opcache.enable_cli=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 29 Sep 2017 01:46:05 GMT
RUN mkdir -p /var/www/data 	&& chown -R www-data:www-data /var/www/data
# Fri, 29 Sep 2017 01:46:05 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.28
# Fri, 29 Sep 2017 01:46:06 GMT
ENV MEDIAWIKI_BRANCH=REL1_28
# Fri, 29 Sep 2017 01:46:06 GMT
ENV MEDIAWIKI_VERSION=1.28.2
# Fri, 29 Sep 2017 01:46:06 GMT
ENV MEDIAWIKI_SHA512=049fa132f17efa43c9cf380fdd85b117b959c8b70fd48f0c8e0dec8a770e3f3405fe272df006ba1fe47fa339b2eb4030ac21edc01295232219eeecdfebee08ce
# Fri, 29 Sep 2017 01:46:12 GMT
RUN curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz 	&& echo "${MEDIAWIKI_SHA512} *mediawiki.tar.gz" | sha512sum -c - 	&& tar -xz --strip-components=1 -f mediawiki.tar.gz 	&& rm mediawiki.tar.gz 	&& chown -R www-data:www-data extensions skins cache images
```

-	Layers:
	-	`sha256:aa18ad1a0d334d80981104c599fa8cef9264552a265b1197af11274beba767cf`  
		Last Modified: Thu, 07 Sep 2017 23:11:06 GMT  
		Size: 52.6 MB (52595547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d5f85af454812aec1820ce0e52e003b81e4569823e2da5b0cccb58e31b136f`  
		Last Modified: Fri, 15 Sep 2017 01:34:31 GMT  
		Size: 82.5 MB (82495988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca642e7826b9552669a262d36f5488e3a478c2f9f97a98db37b203194ea6248`  
		Last Modified: Fri, 15 Sep 2017 01:34:12 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3638d91a90398e9b21e86d5f58ce592dcef089e461ed52559ddcc99d1021c04b`  
		Last Modified: Fri, 15 Sep 2017 01:35:48 GMT  
		Size: 3.0 MB (3012522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3646a95ab6778f36ca28c448f0217a571157bd80a83faa94284a046540d9b90e`  
		Last Modified: Fri, 15 Sep 2017 01:35:46 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628b8373e193144e4047261fde47c3b10881e013cc4730690c28281e30f340d4`  
		Last Modified: Fri, 15 Sep 2017 01:35:45 GMT  
		Size: 431.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24a2b2280edf466db78ea09cb8f23295781c7472f63e5ee7ebd5302e6ef3c45`  
		Last Modified: Fri, 15 Sep 2017 01:35:45 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f968b84cbbbc7f23c623c4ae9ad247431a59a370333ec20de8191284b4838b54`  
		Last Modified: Fri, 15 Sep 2017 01:35:44 GMT  
		Size: 485.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eba9b5fa4872bbe2b17063876e02d94e27ed76aaae378ff06f4fb5fabe92cca`  
		Last Modified: Fri, 29 Sep 2017 01:22:29 GMT  
		Size: 12.3 MB (12314249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0234067d12410685389f8fb0c6baa2ad79e2258de03ee29c0880902e4fb9d5e0`  
		Last Modified: Fri, 29 Sep 2017 01:22:27 GMT  
		Size: 502.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b85a2b999ef3bb1a50a67119cf987b7731cb7b0c1db3b4e40cad13de362b2b7a`  
		Last Modified: Fri, 29 Sep 2017 01:22:34 GMT  
		Size: 13.2 MB (13212054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d31395fe2313a4fde865b2d1f5309793fb4115b44960bc26a7b3b98e288c6ca`  
		Last Modified: Fri, 29 Sep 2017 01:22:28 GMT  
		Size: 2.2 KB (2180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cff026afe51f89f948e975c0e3d1eaa0b96d81c64131c518e03067fdded35f4`  
		Last Modified: Fri, 29 Sep 2017 01:22:27 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98fe309fb9f48e5ef6e9b0fb75f556ad442242b6564bc9a195c0940f5fa24e07`  
		Last Modified: Fri, 29 Sep 2017 01:50:17 GMT  
		Size: 48.1 MB (48128140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b595c41b7857b1df5a2deb28ee4bd4dfaad5394f4d3c6c01b75813dd5e77bb3`  
		Last Modified: Fri, 29 Sep 2017 01:50:04 GMT  
		Size: 1.4 MB (1396887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcfdff861639f786eaee6312b7d55a7a6dc5701f9127cd6dda7bd439772f8d87`  
		Last Modified: Fri, 29 Sep 2017 01:50:04 GMT  
		Size: 324.7 KB (324705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e042b08e2f1c8ab292b65a02ae566d8102407fdc6b9b7b37a85497059d63612`  
		Last Modified: Fri, 29 Sep 2017 01:50:04 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f56197b8593bfc486b67dc5e0145ea549653a73d2fb64be3622c1aca733aaef`  
		Last Modified: Fri, 29 Sep 2017 01:50:04 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d46df421b14bd633693323e773e0a5b225397fb12fff5aab59ac499a17ecac4`  
		Last Modified: Fri, 29 Sep 2017 01:50:14 GMT  
		Size: 33.4 MB (33377828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mediawiki:1.28.2`

```console
$ docker pull mediawiki@sha256:a31e1f83e8aef40487f9ae07afc7c6ba793921efbb9d488a23b4722e6d3ac5e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mediawiki:1.28.2` - linux; amd64

```console
$ docker pull mediawiki@sha256:af783c50af7ea56e7e50d3fffb0076f754ab29b31b1f422b4b810f8b9fc1099a
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.9 MB (246864575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852e1be5b054ce20547f5fdffc6256eb5c56dc10e7e19d6ad67186fafb23f17e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 13 Sep 2017 08:40:43 GMT
ADD file:d7333b3e0bc6479d2faed32e06d85f1975e5b23e13e75555aeed0f639770413b in / 
# Wed, 13 Sep 2017 08:40:43 GMT
CMD ["bash"]
# Thu, 14 Sep 2017 23:57:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		libpcre3-dev 		make 		pkg-config 		re2c
# Thu, 14 Sep 2017 23:58:23 GMT
RUN apt-get update && apt-get install -y 		$PHPIZE_DEPS 		ca-certificates 		curl 		libedit2 		libsqlite3-0 		libxml2 		xz-utils 	--no-install-recommends && rm -r /var/lib/apt/lists/*
# Thu, 14 Sep 2017 23:58:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Sep 2017 23:58:24 GMT
RUN mkdir -p $PHP_INI_DIR/conf.d
# Fri, 15 Sep 2017 00:08:17 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		apache2 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Sep 2017 00:08:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 15 Sep 2017 00:08:18 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 15 Sep 2017 00:08:18 GMT
RUN set -ex 		&& sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS" 		&& . "$APACHE_ENVVARS" 	&& for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		/var/www/html 	; do 		rm -rvf "$dir" 		&& mkdir -p "$dir" 		&& chown -R "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 	done
# Fri, 15 Sep 2017 00:08:19 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 15 Sep 2017 00:08:19 GMT
RUN set -ex 	&& . "$APACHE_ENVVARS" 	&& ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log" 	&& ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log" 	&& ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"
# Fri, 15 Sep 2017 00:08:20 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 15 Sep 2017 00:08:20 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 15 Sep 2017 00:08:20 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2
# Fri, 15 Sep 2017 00:08:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 15 Sep 2017 00:08:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 15 Sep 2017 00:08:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Fri, 15 Sep 2017 00:39:01 GMT
ENV GPG_KEYS=1A4E8B7277C42E53DBA9C7B9BCAA30EA9C0D5763 6E4F6AB321FDC07F2C332E3AC2BF0BC433CFC8B3
# Fri, 29 Sep 2017 00:45:54 GMT
ENV PHP_VERSION=7.0.24
# Fri, 29 Sep 2017 00:45:54 GMT
ENV PHP_URL=https://secure.php.net/get/php-7.0.24.tar.xz/from/this/mirror PHP_ASC_URL=https://secure.php.net/get/php-7.0.24.tar.xz.asc/from/this/mirror
# Fri, 29 Sep 2017 00:45:55 GMT
ENV PHP_SHA256=4dba7aa365193c9229f89f1975fad4c01135d29922a338ffb4a27e840d6f1c98 PHP_MD5=
# Fri, 29 Sep 2017 00:46:19 GMT
RUN set -xe; 		fetchDeps=' 		wget 	'; 	if ! command -v gpg > /dev/null; then 		fetchDeps="$fetchDeps 			dirmngr 			gnupg2 		"; 	fi; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		wget -O php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		wget -O php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps
# Fri, 29 Sep 2017 00:46:19 GMT
COPY file:207c686e3fed4f71f8a7b245d8dcae9c9048d276a326d82b553c12a90af0c0ca in /usr/local/bin/ 
# Fri, 29 Sep 2017 00:48:50 GMT
RUN set -xe 	&& buildDeps=" 		$PHP_EXTRA_BUILD_DEPS 		libcurl4-openssl-dev 		libedit-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	" 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	&& docker-php-source extract 	&& cd /usr/src/php 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)" 	&& if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi 	&& ./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--disable-cgi 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pcre-regex=/usr 		--with-libdir="lib/$debMultiarch" 				$PHP_EXTRA_CONFIGURE_ARGS 	&& make -j "$(nproc)" 	&& make install 	&& { find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; } 	&& make clean 	&& cd / 	&& docker-php-source delete 		&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $buildDeps 		&& pecl update-channels 	&& rm -rf /tmp/pear ~/.pearrc
# Fri, 29 Sep 2017 00:48:50 GMT
COPY multi:dbabcc0b81566a75f49e7faa9ca5f96cd22a515b80ee7ea1e34fceceee3f9c2a in /usr/local/bin/ 
# Fri, 29 Sep 2017 00:48:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 29 Sep 2017 00:48:51 GMT
COPY file:24613ecbb1ce6a09f683b0753da9c26a1af07547326e8a02f6eec80ad6f2774a in /usr/local/bin/ 
# Fri, 29 Sep 2017 00:48:51 GMT
WORKDIR /var/www/html
# Fri, 29 Sep 2017 00:48:51 GMT
EXPOSE 80/tcp
# Fri, 29 Sep 2017 00:48:51 GMT
CMD ["apache2-foreground"]
# Fri, 29 Sep 2017 01:43:32 GMT
RUN apt-get update && apt-get install -y 		git 		imagemagick 		libicu-dev 	--no-install-recommends && rm -r /var/lib/apt/lists/*
# Fri, 29 Sep 2017 01:44:43 GMT
RUN docker-php-ext-install mbstring mysqli opcache intl
# Fri, 29 Sep 2017 01:46:04 GMT
RUN pecl channel-update pecl.php.net 	&& pecl install apcu-5.1.8 	&& docker-php-ext-enable apcu
# Fri, 29 Sep 2017 01:46:05 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 		echo 'opcache.enable_cli=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 29 Sep 2017 01:46:05 GMT
RUN mkdir -p /var/www/data 	&& chown -R www-data:www-data /var/www/data
# Fri, 29 Sep 2017 01:46:05 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.28
# Fri, 29 Sep 2017 01:46:06 GMT
ENV MEDIAWIKI_BRANCH=REL1_28
# Fri, 29 Sep 2017 01:46:06 GMT
ENV MEDIAWIKI_VERSION=1.28.2
# Fri, 29 Sep 2017 01:46:06 GMT
ENV MEDIAWIKI_SHA512=049fa132f17efa43c9cf380fdd85b117b959c8b70fd48f0c8e0dec8a770e3f3405fe272df006ba1fe47fa339b2eb4030ac21edc01295232219eeecdfebee08ce
# Fri, 29 Sep 2017 01:46:12 GMT
RUN curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz 	&& echo "${MEDIAWIKI_SHA512} *mediawiki.tar.gz" | sha512sum -c - 	&& tar -xz --strip-components=1 -f mediawiki.tar.gz 	&& rm mediawiki.tar.gz 	&& chown -R www-data:www-data extensions skins cache images
```

-	Layers:
	-	`sha256:aa18ad1a0d334d80981104c599fa8cef9264552a265b1197af11274beba767cf`  
		Last Modified: Thu, 07 Sep 2017 23:11:06 GMT  
		Size: 52.6 MB (52595547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d5f85af454812aec1820ce0e52e003b81e4569823e2da5b0cccb58e31b136f`  
		Last Modified: Fri, 15 Sep 2017 01:34:31 GMT  
		Size: 82.5 MB (82495988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca642e7826b9552669a262d36f5488e3a478c2f9f97a98db37b203194ea6248`  
		Last Modified: Fri, 15 Sep 2017 01:34:12 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3638d91a90398e9b21e86d5f58ce592dcef089e461ed52559ddcc99d1021c04b`  
		Last Modified: Fri, 15 Sep 2017 01:35:48 GMT  
		Size: 3.0 MB (3012522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3646a95ab6778f36ca28c448f0217a571157bd80a83faa94284a046540d9b90e`  
		Last Modified: Fri, 15 Sep 2017 01:35:46 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628b8373e193144e4047261fde47c3b10881e013cc4730690c28281e30f340d4`  
		Last Modified: Fri, 15 Sep 2017 01:35:45 GMT  
		Size: 431.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24a2b2280edf466db78ea09cb8f23295781c7472f63e5ee7ebd5302e6ef3c45`  
		Last Modified: Fri, 15 Sep 2017 01:35:45 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f968b84cbbbc7f23c623c4ae9ad247431a59a370333ec20de8191284b4838b54`  
		Last Modified: Fri, 15 Sep 2017 01:35:44 GMT  
		Size: 485.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eba9b5fa4872bbe2b17063876e02d94e27ed76aaae378ff06f4fb5fabe92cca`  
		Last Modified: Fri, 29 Sep 2017 01:22:29 GMT  
		Size: 12.3 MB (12314249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0234067d12410685389f8fb0c6baa2ad79e2258de03ee29c0880902e4fb9d5e0`  
		Last Modified: Fri, 29 Sep 2017 01:22:27 GMT  
		Size: 502.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b85a2b999ef3bb1a50a67119cf987b7731cb7b0c1db3b4e40cad13de362b2b7a`  
		Last Modified: Fri, 29 Sep 2017 01:22:34 GMT  
		Size: 13.2 MB (13212054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d31395fe2313a4fde865b2d1f5309793fb4115b44960bc26a7b3b98e288c6ca`  
		Last Modified: Fri, 29 Sep 2017 01:22:28 GMT  
		Size: 2.2 KB (2180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cff026afe51f89f948e975c0e3d1eaa0b96d81c64131c518e03067fdded35f4`  
		Last Modified: Fri, 29 Sep 2017 01:22:27 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98fe309fb9f48e5ef6e9b0fb75f556ad442242b6564bc9a195c0940f5fa24e07`  
		Last Modified: Fri, 29 Sep 2017 01:50:17 GMT  
		Size: 48.1 MB (48128140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b595c41b7857b1df5a2deb28ee4bd4dfaad5394f4d3c6c01b75813dd5e77bb3`  
		Last Modified: Fri, 29 Sep 2017 01:50:04 GMT  
		Size: 1.4 MB (1396887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcfdff861639f786eaee6312b7d55a7a6dc5701f9127cd6dda7bd439772f8d87`  
		Last Modified: Fri, 29 Sep 2017 01:50:04 GMT  
		Size: 324.7 KB (324705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e042b08e2f1c8ab292b65a02ae566d8102407fdc6b9b7b37a85497059d63612`  
		Last Modified: Fri, 29 Sep 2017 01:50:04 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f56197b8593bfc486b67dc5e0145ea549653a73d2fb64be3622c1aca733aaef`  
		Last Modified: Fri, 29 Sep 2017 01:50:04 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d46df421b14bd633693323e773e0a5b225397fb12fff5aab59ac499a17ecac4`  
		Last Modified: Fri, 29 Sep 2017 01:50:14 GMT  
		Size: 33.4 MB (33377828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mediawiki:1.29`

```console
$ docker pull mediawiki@sha256:3b6cab8092ecec8a6953fff8f50bd6a87374f20438cf5b338f37b72caffd93f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mediawiki:1.29` - linux; amd64

```console
$ docker pull mediawiki@sha256:daa6ce0d7ef73aeefe8133804d66ebc1cb6c32a4d4ea8ac2442cf08ebf8401c6
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 MB (254305964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5726e4f5ce4772c9e7c75bc83330ebe18d044c4cf77c900197699ceff591369`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 13 Sep 2017 08:40:43 GMT
ADD file:d7333b3e0bc6479d2faed32e06d85f1975e5b23e13e75555aeed0f639770413b in / 
# Wed, 13 Sep 2017 08:40:43 GMT
CMD ["bash"]
# Thu, 14 Sep 2017 23:57:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		libpcre3-dev 		make 		pkg-config 		re2c
# Thu, 14 Sep 2017 23:58:23 GMT
RUN apt-get update && apt-get install -y 		$PHPIZE_DEPS 		ca-certificates 		curl 		libedit2 		libsqlite3-0 		libxml2 		xz-utils 	--no-install-recommends && rm -r /var/lib/apt/lists/*
# Thu, 14 Sep 2017 23:58:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Sep 2017 23:58:24 GMT
RUN mkdir -p $PHP_INI_DIR/conf.d
# Fri, 15 Sep 2017 00:08:17 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		apache2 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Sep 2017 00:08:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 15 Sep 2017 00:08:18 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 15 Sep 2017 00:08:18 GMT
RUN set -ex 		&& sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS" 		&& . "$APACHE_ENVVARS" 	&& for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		/var/www/html 	; do 		rm -rvf "$dir" 		&& mkdir -p "$dir" 		&& chown -R "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 	done
# Fri, 15 Sep 2017 00:08:19 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 15 Sep 2017 00:08:19 GMT
RUN set -ex 	&& . "$APACHE_ENVVARS" 	&& ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log" 	&& ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log" 	&& ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"
# Fri, 15 Sep 2017 00:08:20 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 15 Sep 2017 00:08:20 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 15 Sep 2017 00:08:20 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2
# Fri, 15 Sep 2017 00:08:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 15 Sep 2017 00:08:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 15 Sep 2017 00:08:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Fri, 15 Sep 2017 00:08:21 GMT
ENV GPG_KEYS=A917B1ECDA84AEC2B568FED6F50ABC807BD5DCD0 528995BFEDFBA7191D46839EF9BA0ADA31CBD89E
# Fri, 29 Sep 2017 23:07:28 GMT
ENV PHP_VERSION=7.1.10
# Fri, 29 Sep 2017 23:07:28 GMT
ENV PHP_URL=https://secure.php.net/get/php-7.1.10.tar.xz/from/this/mirror PHP_ASC_URL=https://secure.php.net/get/php-7.1.10.tar.xz.asc/from/this/mirror
# Fri, 29 Sep 2017 23:07:28 GMT
ENV PHP_SHA256=2b8efa771a2ead0bb3ae67b530ca505b5b286adc873cca9ce97a6e1d6815c50b PHP_MD5=
# Fri, 29 Sep 2017 23:07:50 GMT
RUN set -xe; 		fetchDeps=' 		wget 	'; 	if ! command -v gpg > /dev/null; then 		fetchDeps="$fetchDeps 			dirmngr 			gnupg2 		"; 	fi; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		wget -O php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		wget -O php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps
# Fri, 29 Sep 2017 23:07:50 GMT
COPY file:207c686e3fed4f71f8a7b245d8dcae9c9048d276a326d82b553c12a90af0c0ca in /usr/local/bin/ 
# Fri, 29 Sep 2017 23:10:26 GMT
RUN set -xe 	&& buildDeps=" 		$PHP_EXTRA_BUILD_DEPS 		libcurl4-openssl-dev 		libedit-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	" 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	&& docker-php-source extract 	&& cd /usr/src/php 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)" 	&& if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi 	&& ./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--disable-cgi 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pcre-regex=/usr 		--with-libdir="lib/$debMultiarch" 				$PHP_EXTRA_CONFIGURE_ARGS 	&& make -j "$(nproc)" 	&& make install 	&& { find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; } 	&& make clean 	&& cd / 	&& docker-php-source delete 		&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $buildDeps 		&& pecl update-channels 	&& rm -rf /tmp/pear ~/.pearrc
# Fri, 29 Sep 2017 23:10:27 GMT
COPY multi:dbabcc0b81566a75f49e7faa9ca5f96cd22a515b80ee7ea1e34fceceee3f9c2a in /usr/local/bin/ 
# Fri, 29 Sep 2017 23:10:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 29 Sep 2017 23:10:27 GMT
COPY file:24613ecbb1ce6a09f683b0753da9c26a1af07547326e8a02f6eec80ad6f2774a in /usr/local/bin/ 
# Fri, 29 Sep 2017 23:10:27 GMT
WORKDIR /var/www/html
# Fri, 29 Sep 2017 23:10:28 GMT
EXPOSE 80/tcp
# Fri, 29 Sep 2017 23:10:28 GMT
CMD ["apache2-foreground"]
# Sat, 30 Sep 2017 00:36:54 GMT
RUN apt-get update && apt-get install -y 		git 		imagemagick 		libicu-dev 	--no-install-recommends && rm -r /var/lib/apt/lists/*
# Sat, 30 Sep 2017 00:38:11 GMT
RUN docker-php-ext-install mbstring mysqli opcache intl
# Sat, 30 Sep 2017 00:38:23 GMT
RUN pecl channel-update pecl.php.net 	&& pecl install apcu-5.1.8 	&& docker-php-ext-enable apcu
# Sat, 30 Sep 2017 00:38:23 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 		echo 'opcache.enable_cli=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sat, 30 Sep 2017 00:38:24 GMT
RUN mkdir -p /var/www/data 	&& chown -R www-data:www-data /var/www/data
# Sat, 30 Sep 2017 00:38:24 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.29
# Sat, 30 Sep 2017 00:38:25 GMT
ENV MEDIAWIKI_BRANCH=REL1_29
# Sat, 30 Sep 2017 00:38:25 GMT
ENV MEDIAWIKI_VERSION=1.29.1
# Sat, 30 Sep 2017 00:38:25 GMT
ENV MEDIAWIKI_SHA512=c4e04c4fb665c3d8299f3e03e608904aaf0e06381240c7259813eb670c3e32cde919353dd19993250cf49be81d604ac5f6d468bc563116a4b268e5011d34119f
# Sat, 30 Sep 2017 00:38:31 GMT
RUN curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz 	&& echo "${MEDIAWIKI_SHA512} *mediawiki.tar.gz" | sha512sum -c - 	&& tar -xz --strip-components=1 -f mediawiki.tar.gz 	&& rm mediawiki.tar.gz 	&& chown -R www-data:www-data extensions skins cache images
```

-	Layers:
	-	`sha256:aa18ad1a0d334d80981104c599fa8cef9264552a265b1197af11274beba767cf`  
		Last Modified: Thu, 07 Sep 2017 23:11:06 GMT  
		Size: 52.6 MB (52595547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d5f85af454812aec1820ce0e52e003b81e4569823e2da5b0cccb58e31b136f`  
		Last Modified: Fri, 15 Sep 2017 01:34:31 GMT  
		Size: 82.5 MB (82495988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca642e7826b9552669a262d36f5488e3a478c2f9f97a98db37b203194ea6248`  
		Last Modified: Fri, 15 Sep 2017 01:34:12 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3638d91a90398e9b21e86d5f58ce592dcef089e461ed52559ddcc99d1021c04b`  
		Last Modified: Fri, 15 Sep 2017 01:35:48 GMT  
		Size: 3.0 MB (3012522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3646a95ab6778f36ca28c448f0217a571157bd80a83faa94284a046540d9b90e`  
		Last Modified: Fri, 15 Sep 2017 01:35:46 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628b8373e193144e4047261fde47c3b10881e013cc4730690c28281e30f340d4`  
		Last Modified: Fri, 15 Sep 2017 01:35:45 GMT  
		Size: 431.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24a2b2280edf466db78ea09cb8f23295781c7472f63e5ee7ebd5302e6ef3c45`  
		Last Modified: Fri, 15 Sep 2017 01:35:45 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f968b84cbbbc7f23c623c4ae9ad247431a59a370333ec20de8191284b4838b54`  
		Last Modified: Fri, 15 Sep 2017 01:35:44 GMT  
		Size: 485.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77afd73ce87d8a835726d0c9b72b750bad785a6cda38015d6aa383c0cfe519c`  
		Last Modified: Fri, 29 Sep 2017 23:43:38 GMT  
		Size: 12.5 MB (12520223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863afbb954365f5f975093a2eb7094211798ef1c2bda6945449a78969af9bc94`  
		Last Modified: Fri, 29 Sep 2017 23:43:37 GMT  
		Size: 501.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f381536e9279732352befaf4f534e8ba6f937e97c061e96e83e4bd1b7e3005`  
		Last Modified: Fri, 29 Sep 2017 23:43:40 GMT  
		Size: 13.5 MB (13521858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e96e9b4935a1b0dbaadd56fd518ad6dd0fb7fbb5bdc9d308ac91d5cbe365f22`  
		Last Modified: Fri, 29 Sep 2017 23:43:37 GMT  
		Size: 2.2 KB (2183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca94deb9c4dfde50548223713993b67299f97259943b49e9a6cfca6aa89e7116`  
		Last Modified: Fri, 29 Sep 2017 23:43:37 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1531a42b8fbad2ddcbf0a3bb4fce32136c8f9d4d12f6d42315a7fcdfe097991a`  
		Last Modified: Sat, 30 Sep 2017 00:43:32 GMT  
		Size: 48.1 MB (48128251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67a47f465ce0894770fe71aed42434aa04555179cb78bee240bd72aa57b21d3b`  
		Last Modified: Sat, 30 Sep 2017 00:43:19 GMT  
		Size: 1.5 MB (1490066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aacf27acbcf759713ab885124351e83a55666bc5e0c78f5972b4f7806f31cb63`  
		Last Modified: Sat, 30 Sep 2017 00:43:19 GMT  
		Size: 326.1 KB (326080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ef81a00ec595c6233d071a07d5f23c7279e50c206451fca533a8101195e8c5`  
		Last Modified: Sat, 30 Sep 2017 00:43:18 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608e37947697643dea39232439f0aa981786281393e269c6416276acc784c3fb`  
		Last Modified: Sat, 30 Sep 2017 00:43:18 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e9113eba113d2dd2fbaae853604bcabec1c3950f6dac585d99ecb47c36e837`  
		Last Modified: Sat, 30 Sep 2017 00:43:33 GMT  
		Size: 40.2 MB (40208770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mediawiki:1.29.1`

```console
$ docker pull mediawiki@sha256:3b6cab8092ecec8a6953fff8f50bd6a87374f20438cf5b338f37b72caffd93f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mediawiki:1.29.1` - linux; amd64

```console
$ docker pull mediawiki@sha256:daa6ce0d7ef73aeefe8133804d66ebc1cb6c32a4d4ea8ac2442cf08ebf8401c6
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 MB (254305964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5726e4f5ce4772c9e7c75bc83330ebe18d044c4cf77c900197699ceff591369`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 13 Sep 2017 08:40:43 GMT
ADD file:d7333b3e0bc6479d2faed32e06d85f1975e5b23e13e75555aeed0f639770413b in / 
# Wed, 13 Sep 2017 08:40:43 GMT
CMD ["bash"]
# Thu, 14 Sep 2017 23:57:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		libpcre3-dev 		make 		pkg-config 		re2c
# Thu, 14 Sep 2017 23:58:23 GMT
RUN apt-get update && apt-get install -y 		$PHPIZE_DEPS 		ca-certificates 		curl 		libedit2 		libsqlite3-0 		libxml2 		xz-utils 	--no-install-recommends && rm -r /var/lib/apt/lists/*
# Thu, 14 Sep 2017 23:58:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Sep 2017 23:58:24 GMT
RUN mkdir -p $PHP_INI_DIR/conf.d
# Fri, 15 Sep 2017 00:08:17 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		apache2 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Sep 2017 00:08:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 15 Sep 2017 00:08:18 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 15 Sep 2017 00:08:18 GMT
RUN set -ex 		&& sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS" 		&& . "$APACHE_ENVVARS" 	&& for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		/var/www/html 	; do 		rm -rvf "$dir" 		&& mkdir -p "$dir" 		&& chown -R "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 	done
# Fri, 15 Sep 2017 00:08:19 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 15 Sep 2017 00:08:19 GMT
RUN set -ex 	&& . "$APACHE_ENVVARS" 	&& ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log" 	&& ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log" 	&& ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"
# Fri, 15 Sep 2017 00:08:20 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 15 Sep 2017 00:08:20 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 15 Sep 2017 00:08:20 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2
# Fri, 15 Sep 2017 00:08:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 15 Sep 2017 00:08:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 15 Sep 2017 00:08:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Fri, 15 Sep 2017 00:08:21 GMT
ENV GPG_KEYS=A917B1ECDA84AEC2B568FED6F50ABC807BD5DCD0 528995BFEDFBA7191D46839EF9BA0ADA31CBD89E
# Fri, 29 Sep 2017 23:07:28 GMT
ENV PHP_VERSION=7.1.10
# Fri, 29 Sep 2017 23:07:28 GMT
ENV PHP_URL=https://secure.php.net/get/php-7.1.10.tar.xz/from/this/mirror PHP_ASC_URL=https://secure.php.net/get/php-7.1.10.tar.xz.asc/from/this/mirror
# Fri, 29 Sep 2017 23:07:28 GMT
ENV PHP_SHA256=2b8efa771a2ead0bb3ae67b530ca505b5b286adc873cca9ce97a6e1d6815c50b PHP_MD5=
# Fri, 29 Sep 2017 23:07:50 GMT
RUN set -xe; 		fetchDeps=' 		wget 	'; 	if ! command -v gpg > /dev/null; then 		fetchDeps="$fetchDeps 			dirmngr 			gnupg2 		"; 	fi; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		wget -O php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		wget -O php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps
# Fri, 29 Sep 2017 23:07:50 GMT
COPY file:207c686e3fed4f71f8a7b245d8dcae9c9048d276a326d82b553c12a90af0c0ca in /usr/local/bin/ 
# Fri, 29 Sep 2017 23:10:26 GMT
RUN set -xe 	&& buildDeps=" 		$PHP_EXTRA_BUILD_DEPS 		libcurl4-openssl-dev 		libedit-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	" 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	&& docker-php-source extract 	&& cd /usr/src/php 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)" 	&& if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi 	&& ./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--disable-cgi 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pcre-regex=/usr 		--with-libdir="lib/$debMultiarch" 				$PHP_EXTRA_CONFIGURE_ARGS 	&& make -j "$(nproc)" 	&& make install 	&& { find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; } 	&& make clean 	&& cd / 	&& docker-php-source delete 		&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $buildDeps 		&& pecl update-channels 	&& rm -rf /tmp/pear ~/.pearrc
# Fri, 29 Sep 2017 23:10:27 GMT
COPY multi:dbabcc0b81566a75f49e7faa9ca5f96cd22a515b80ee7ea1e34fceceee3f9c2a in /usr/local/bin/ 
# Fri, 29 Sep 2017 23:10:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 29 Sep 2017 23:10:27 GMT
COPY file:24613ecbb1ce6a09f683b0753da9c26a1af07547326e8a02f6eec80ad6f2774a in /usr/local/bin/ 
# Fri, 29 Sep 2017 23:10:27 GMT
WORKDIR /var/www/html
# Fri, 29 Sep 2017 23:10:28 GMT
EXPOSE 80/tcp
# Fri, 29 Sep 2017 23:10:28 GMT
CMD ["apache2-foreground"]
# Sat, 30 Sep 2017 00:36:54 GMT
RUN apt-get update && apt-get install -y 		git 		imagemagick 		libicu-dev 	--no-install-recommends && rm -r /var/lib/apt/lists/*
# Sat, 30 Sep 2017 00:38:11 GMT
RUN docker-php-ext-install mbstring mysqli opcache intl
# Sat, 30 Sep 2017 00:38:23 GMT
RUN pecl channel-update pecl.php.net 	&& pecl install apcu-5.1.8 	&& docker-php-ext-enable apcu
# Sat, 30 Sep 2017 00:38:23 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 		echo 'opcache.enable_cli=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sat, 30 Sep 2017 00:38:24 GMT
RUN mkdir -p /var/www/data 	&& chown -R www-data:www-data /var/www/data
# Sat, 30 Sep 2017 00:38:24 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.29
# Sat, 30 Sep 2017 00:38:25 GMT
ENV MEDIAWIKI_BRANCH=REL1_29
# Sat, 30 Sep 2017 00:38:25 GMT
ENV MEDIAWIKI_VERSION=1.29.1
# Sat, 30 Sep 2017 00:38:25 GMT
ENV MEDIAWIKI_SHA512=c4e04c4fb665c3d8299f3e03e608904aaf0e06381240c7259813eb670c3e32cde919353dd19993250cf49be81d604ac5f6d468bc563116a4b268e5011d34119f
# Sat, 30 Sep 2017 00:38:31 GMT
RUN curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz 	&& echo "${MEDIAWIKI_SHA512} *mediawiki.tar.gz" | sha512sum -c - 	&& tar -xz --strip-components=1 -f mediawiki.tar.gz 	&& rm mediawiki.tar.gz 	&& chown -R www-data:www-data extensions skins cache images
```

-	Layers:
	-	`sha256:aa18ad1a0d334d80981104c599fa8cef9264552a265b1197af11274beba767cf`  
		Last Modified: Thu, 07 Sep 2017 23:11:06 GMT  
		Size: 52.6 MB (52595547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d5f85af454812aec1820ce0e52e003b81e4569823e2da5b0cccb58e31b136f`  
		Last Modified: Fri, 15 Sep 2017 01:34:31 GMT  
		Size: 82.5 MB (82495988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca642e7826b9552669a262d36f5488e3a478c2f9f97a98db37b203194ea6248`  
		Last Modified: Fri, 15 Sep 2017 01:34:12 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3638d91a90398e9b21e86d5f58ce592dcef089e461ed52559ddcc99d1021c04b`  
		Last Modified: Fri, 15 Sep 2017 01:35:48 GMT  
		Size: 3.0 MB (3012522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3646a95ab6778f36ca28c448f0217a571157bd80a83faa94284a046540d9b90e`  
		Last Modified: Fri, 15 Sep 2017 01:35:46 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628b8373e193144e4047261fde47c3b10881e013cc4730690c28281e30f340d4`  
		Last Modified: Fri, 15 Sep 2017 01:35:45 GMT  
		Size: 431.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24a2b2280edf466db78ea09cb8f23295781c7472f63e5ee7ebd5302e6ef3c45`  
		Last Modified: Fri, 15 Sep 2017 01:35:45 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f968b84cbbbc7f23c623c4ae9ad247431a59a370333ec20de8191284b4838b54`  
		Last Modified: Fri, 15 Sep 2017 01:35:44 GMT  
		Size: 485.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77afd73ce87d8a835726d0c9b72b750bad785a6cda38015d6aa383c0cfe519c`  
		Last Modified: Fri, 29 Sep 2017 23:43:38 GMT  
		Size: 12.5 MB (12520223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863afbb954365f5f975093a2eb7094211798ef1c2bda6945449a78969af9bc94`  
		Last Modified: Fri, 29 Sep 2017 23:43:37 GMT  
		Size: 501.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f381536e9279732352befaf4f534e8ba6f937e97c061e96e83e4bd1b7e3005`  
		Last Modified: Fri, 29 Sep 2017 23:43:40 GMT  
		Size: 13.5 MB (13521858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e96e9b4935a1b0dbaadd56fd518ad6dd0fb7fbb5bdc9d308ac91d5cbe365f22`  
		Last Modified: Fri, 29 Sep 2017 23:43:37 GMT  
		Size: 2.2 KB (2183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca94deb9c4dfde50548223713993b67299f97259943b49e9a6cfca6aa89e7116`  
		Last Modified: Fri, 29 Sep 2017 23:43:37 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1531a42b8fbad2ddcbf0a3bb4fce32136c8f9d4d12f6d42315a7fcdfe097991a`  
		Last Modified: Sat, 30 Sep 2017 00:43:32 GMT  
		Size: 48.1 MB (48128251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67a47f465ce0894770fe71aed42434aa04555179cb78bee240bd72aa57b21d3b`  
		Last Modified: Sat, 30 Sep 2017 00:43:19 GMT  
		Size: 1.5 MB (1490066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aacf27acbcf759713ab885124351e83a55666bc5e0c78f5972b4f7806f31cb63`  
		Last Modified: Sat, 30 Sep 2017 00:43:19 GMT  
		Size: 326.1 KB (326080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ef81a00ec595c6233d071a07d5f23c7279e50c206451fca533a8101195e8c5`  
		Last Modified: Sat, 30 Sep 2017 00:43:18 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608e37947697643dea39232439f0aa981786281393e269c6416276acc784c3fb`  
		Last Modified: Sat, 30 Sep 2017 00:43:18 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e9113eba113d2dd2fbaae853604bcabec1c3950f6dac585d99ecb47c36e837`  
		Last Modified: Sat, 30 Sep 2017 00:43:33 GMT  
		Size: 40.2 MB (40208770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mediawiki:latest`

```console
$ docker pull mediawiki@sha256:3b6cab8092ecec8a6953fff8f50bd6a87374f20438cf5b338f37b72caffd93f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mediawiki:latest` - linux; amd64

```console
$ docker pull mediawiki@sha256:daa6ce0d7ef73aeefe8133804d66ebc1cb6c32a4d4ea8ac2442cf08ebf8401c6
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 MB (254305964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5726e4f5ce4772c9e7c75bc83330ebe18d044c4cf77c900197699ceff591369`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 13 Sep 2017 08:40:43 GMT
ADD file:d7333b3e0bc6479d2faed32e06d85f1975e5b23e13e75555aeed0f639770413b in / 
# Wed, 13 Sep 2017 08:40:43 GMT
CMD ["bash"]
# Thu, 14 Sep 2017 23:57:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		libpcre3-dev 		make 		pkg-config 		re2c
# Thu, 14 Sep 2017 23:58:23 GMT
RUN apt-get update && apt-get install -y 		$PHPIZE_DEPS 		ca-certificates 		curl 		libedit2 		libsqlite3-0 		libxml2 		xz-utils 	--no-install-recommends && rm -r /var/lib/apt/lists/*
# Thu, 14 Sep 2017 23:58:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Sep 2017 23:58:24 GMT
RUN mkdir -p $PHP_INI_DIR/conf.d
# Fri, 15 Sep 2017 00:08:17 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		apache2 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Sep 2017 00:08:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 15 Sep 2017 00:08:18 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 15 Sep 2017 00:08:18 GMT
RUN set -ex 		&& sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS" 		&& . "$APACHE_ENVVARS" 	&& for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		/var/www/html 	; do 		rm -rvf "$dir" 		&& mkdir -p "$dir" 		&& chown -R "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 	done
# Fri, 15 Sep 2017 00:08:19 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 15 Sep 2017 00:08:19 GMT
RUN set -ex 	&& . "$APACHE_ENVVARS" 	&& ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log" 	&& ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log" 	&& ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"
# Fri, 15 Sep 2017 00:08:20 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 15 Sep 2017 00:08:20 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 15 Sep 2017 00:08:20 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2
# Fri, 15 Sep 2017 00:08:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 15 Sep 2017 00:08:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 15 Sep 2017 00:08:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Fri, 15 Sep 2017 00:08:21 GMT
ENV GPG_KEYS=A917B1ECDA84AEC2B568FED6F50ABC807BD5DCD0 528995BFEDFBA7191D46839EF9BA0ADA31CBD89E
# Fri, 29 Sep 2017 23:07:28 GMT
ENV PHP_VERSION=7.1.10
# Fri, 29 Sep 2017 23:07:28 GMT
ENV PHP_URL=https://secure.php.net/get/php-7.1.10.tar.xz/from/this/mirror PHP_ASC_URL=https://secure.php.net/get/php-7.1.10.tar.xz.asc/from/this/mirror
# Fri, 29 Sep 2017 23:07:28 GMT
ENV PHP_SHA256=2b8efa771a2ead0bb3ae67b530ca505b5b286adc873cca9ce97a6e1d6815c50b PHP_MD5=
# Fri, 29 Sep 2017 23:07:50 GMT
RUN set -xe; 		fetchDeps=' 		wget 	'; 	if ! command -v gpg > /dev/null; then 		fetchDeps="$fetchDeps 			dirmngr 			gnupg2 		"; 	fi; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		wget -O php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		wget -O php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps
# Fri, 29 Sep 2017 23:07:50 GMT
COPY file:207c686e3fed4f71f8a7b245d8dcae9c9048d276a326d82b553c12a90af0c0ca in /usr/local/bin/ 
# Fri, 29 Sep 2017 23:10:26 GMT
RUN set -xe 	&& buildDeps=" 		$PHP_EXTRA_BUILD_DEPS 		libcurl4-openssl-dev 		libedit-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	" 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	&& docker-php-source extract 	&& cd /usr/src/php 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)" 	&& if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi 	&& ./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--disable-cgi 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pcre-regex=/usr 		--with-libdir="lib/$debMultiarch" 				$PHP_EXTRA_CONFIGURE_ARGS 	&& make -j "$(nproc)" 	&& make install 	&& { find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; } 	&& make clean 	&& cd / 	&& docker-php-source delete 		&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $buildDeps 		&& pecl update-channels 	&& rm -rf /tmp/pear ~/.pearrc
# Fri, 29 Sep 2017 23:10:27 GMT
COPY multi:dbabcc0b81566a75f49e7faa9ca5f96cd22a515b80ee7ea1e34fceceee3f9c2a in /usr/local/bin/ 
# Fri, 29 Sep 2017 23:10:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 29 Sep 2017 23:10:27 GMT
COPY file:24613ecbb1ce6a09f683b0753da9c26a1af07547326e8a02f6eec80ad6f2774a in /usr/local/bin/ 
# Fri, 29 Sep 2017 23:10:27 GMT
WORKDIR /var/www/html
# Fri, 29 Sep 2017 23:10:28 GMT
EXPOSE 80/tcp
# Fri, 29 Sep 2017 23:10:28 GMT
CMD ["apache2-foreground"]
# Sat, 30 Sep 2017 00:36:54 GMT
RUN apt-get update && apt-get install -y 		git 		imagemagick 		libicu-dev 	--no-install-recommends && rm -r /var/lib/apt/lists/*
# Sat, 30 Sep 2017 00:38:11 GMT
RUN docker-php-ext-install mbstring mysqli opcache intl
# Sat, 30 Sep 2017 00:38:23 GMT
RUN pecl channel-update pecl.php.net 	&& pecl install apcu-5.1.8 	&& docker-php-ext-enable apcu
# Sat, 30 Sep 2017 00:38:23 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 		echo 'opcache.enable_cli=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sat, 30 Sep 2017 00:38:24 GMT
RUN mkdir -p /var/www/data 	&& chown -R www-data:www-data /var/www/data
# Sat, 30 Sep 2017 00:38:24 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.29
# Sat, 30 Sep 2017 00:38:25 GMT
ENV MEDIAWIKI_BRANCH=REL1_29
# Sat, 30 Sep 2017 00:38:25 GMT
ENV MEDIAWIKI_VERSION=1.29.1
# Sat, 30 Sep 2017 00:38:25 GMT
ENV MEDIAWIKI_SHA512=c4e04c4fb665c3d8299f3e03e608904aaf0e06381240c7259813eb670c3e32cde919353dd19993250cf49be81d604ac5f6d468bc563116a4b268e5011d34119f
# Sat, 30 Sep 2017 00:38:31 GMT
RUN curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz 	&& echo "${MEDIAWIKI_SHA512} *mediawiki.tar.gz" | sha512sum -c - 	&& tar -xz --strip-components=1 -f mediawiki.tar.gz 	&& rm mediawiki.tar.gz 	&& chown -R www-data:www-data extensions skins cache images
```

-	Layers:
	-	`sha256:aa18ad1a0d334d80981104c599fa8cef9264552a265b1197af11274beba767cf`  
		Last Modified: Thu, 07 Sep 2017 23:11:06 GMT  
		Size: 52.6 MB (52595547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d5f85af454812aec1820ce0e52e003b81e4569823e2da5b0cccb58e31b136f`  
		Last Modified: Fri, 15 Sep 2017 01:34:31 GMT  
		Size: 82.5 MB (82495988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca642e7826b9552669a262d36f5488e3a478c2f9f97a98db37b203194ea6248`  
		Last Modified: Fri, 15 Sep 2017 01:34:12 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3638d91a90398e9b21e86d5f58ce592dcef089e461ed52559ddcc99d1021c04b`  
		Last Modified: Fri, 15 Sep 2017 01:35:48 GMT  
		Size: 3.0 MB (3012522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3646a95ab6778f36ca28c448f0217a571157bd80a83faa94284a046540d9b90e`  
		Last Modified: Fri, 15 Sep 2017 01:35:46 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628b8373e193144e4047261fde47c3b10881e013cc4730690c28281e30f340d4`  
		Last Modified: Fri, 15 Sep 2017 01:35:45 GMT  
		Size: 431.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24a2b2280edf466db78ea09cb8f23295781c7472f63e5ee7ebd5302e6ef3c45`  
		Last Modified: Fri, 15 Sep 2017 01:35:45 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f968b84cbbbc7f23c623c4ae9ad247431a59a370333ec20de8191284b4838b54`  
		Last Modified: Fri, 15 Sep 2017 01:35:44 GMT  
		Size: 485.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77afd73ce87d8a835726d0c9b72b750bad785a6cda38015d6aa383c0cfe519c`  
		Last Modified: Fri, 29 Sep 2017 23:43:38 GMT  
		Size: 12.5 MB (12520223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863afbb954365f5f975093a2eb7094211798ef1c2bda6945449a78969af9bc94`  
		Last Modified: Fri, 29 Sep 2017 23:43:37 GMT  
		Size: 501.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f381536e9279732352befaf4f534e8ba6f937e97c061e96e83e4bd1b7e3005`  
		Last Modified: Fri, 29 Sep 2017 23:43:40 GMT  
		Size: 13.5 MB (13521858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e96e9b4935a1b0dbaadd56fd518ad6dd0fb7fbb5bdc9d308ac91d5cbe365f22`  
		Last Modified: Fri, 29 Sep 2017 23:43:37 GMT  
		Size: 2.2 KB (2183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca94deb9c4dfde50548223713993b67299f97259943b49e9a6cfca6aa89e7116`  
		Last Modified: Fri, 29 Sep 2017 23:43:37 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1531a42b8fbad2ddcbf0a3bb4fce32136c8f9d4d12f6d42315a7fcdfe097991a`  
		Last Modified: Sat, 30 Sep 2017 00:43:32 GMT  
		Size: 48.1 MB (48128251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67a47f465ce0894770fe71aed42434aa04555179cb78bee240bd72aa57b21d3b`  
		Last Modified: Sat, 30 Sep 2017 00:43:19 GMT  
		Size: 1.5 MB (1490066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aacf27acbcf759713ab885124351e83a55666bc5e0c78f5972b4f7806f31cb63`  
		Last Modified: Sat, 30 Sep 2017 00:43:19 GMT  
		Size: 326.1 KB (326080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ef81a00ec595c6233d071a07d5f23c7279e50c206451fca533a8101195e8c5`  
		Last Modified: Sat, 30 Sep 2017 00:43:18 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608e37947697643dea39232439f0aa981786281393e269c6416276acc784c3fb`  
		Last Modified: Sat, 30 Sep 2017 00:43:18 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e9113eba113d2dd2fbaae853604bcabec1c3950f6dac585d99ecb47c36e837`  
		Last Modified: Sat, 30 Sep 2017 00:43:33 GMT  
		Size: 40.2 MB (40208770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mediawiki:legacy`

```console
$ docker pull mediawiki@sha256:a31e1f83e8aef40487f9ae07afc7c6ba793921efbb9d488a23b4722e6d3ac5e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mediawiki:legacy` - linux; amd64

```console
$ docker pull mediawiki@sha256:af783c50af7ea56e7e50d3fffb0076f754ab29b31b1f422b4b810f8b9fc1099a
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.9 MB (246864575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852e1be5b054ce20547f5fdffc6256eb5c56dc10e7e19d6ad67186fafb23f17e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 13 Sep 2017 08:40:43 GMT
ADD file:d7333b3e0bc6479d2faed32e06d85f1975e5b23e13e75555aeed0f639770413b in / 
# Wed, 13 Sep 2017 08:40:43 GMT
CMD ["bash"]
# Thu, 14 Sep 2017 23:57:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		libpcre3-dev 		make 		pkg-config 		re2c
# Thu, 14 Sep 2017 23:58:23 GMT
RUN apt-get update && apt-get install -y 		$PHPIZE_DEPS 		ca-certificates 		curl 		libedit2 		libsqlite3-0 		libxml2 		xz-utils 	--no-install-recommends && rm -r /var/lib/apt/lists/*
# Thu, 14 Sep 2017 23:58:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Sep 2017 23:58:24 GMT
RUN mkdir -p $PHP_INI_DIR/conf.d
# Fri, 15 Sep 2017 00:08:17 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		apache2 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Sep 2017 00:08:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 15 Sep 2017 00:08:18 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 15 Sep 2017 00:08:18 GMT
RUN set -ex 		&& sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS" 		&& . "$APACHE_ENVVARS" 	&& for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		/var/www/html 	; do 		rm -rvf "$dir" 		&& mkdir -p "$dir" 		&& chown -R "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 	done
# Fri, 15 Sep 2017 00:08:19 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 15 Sep 2017 00:08:19 GMT
RUN set -ex 	&& . "$APACHE_ENVVARS" 	&& ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log" 	&& ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log" 	&& ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"
# Fri, 15 Sep 2017 00:08:20 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 15 Sep 2017 00:08:20 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 15 Sep 2017 00:08:20 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2
# Fri, 15 Sep 2017 00:08:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 15 Sep 2017 00:08:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 15 Sep 2017 00:08:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Fri, 15 Sep 2017 00:39:01 GMT
ENV GPG_KEYS=1A4E8B7277C42E53DBA9C7B9BCAA30EA9C0D5763 6E4F6AB321FDC07F2C332E3AC2BF0BC433CFC8B3
# Fri, 29 Sep 2017 00:45:54 GMT
ENV PHP_VERSION=7.0.24
# Fri, 29 Sep 2017 00:45:54 GMT
ENV PHP_URL=https://secure.php.net/get/php-7.0.24.tar.xz/from/this/mirror PHP_ASC_URL=https://secure.php.net/get/php-7.0.24.tar.xz.asc/from/this/mirror
# Fri, 29 Sep 2017 00:45:55 GMT
ENV PHP_SHA256=4dba7aa365193c9229f89f1975fad4c01135d29922a338ffb4a27e840d6f1c98 PHP_MD5=
# Fri, 29 Sep 2017 00:46:19 GMT
RUN set -xe; 		fetchDeps=' 		wget 	'; 	if ! command -v gpg > /dev/null; then 		fetchDeps="$fetchDeps 			dirmngr 			gnupg2 		"; 	fi; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		wget -O php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		wget -O php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps
# Fri, 29 Sep 2017 00:46:19 GMT
COPY file:207c686e3fed4f71f8a7b245d8dcae9c9048d276a326d82b553c12a90af0c0ca in /usr/local/bin/ 
# Fri, 29 Sep 2017 00:48:50 GMT
RUN set -xe 	&& buildDeps=" 		$PHP_EXTRA_BUILD_DEPS 		libcurl4-openssl-dev 		libedit-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	" 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	&& docker-php-source extract 	&& cd /usr/src/php 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)" 	&& if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi 	&& ./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--disable-cgi 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pcre-regex=/usr 		--with-libdir="lib/$debMultiarch" 				$PHP_EXTRA_CONFIGURE_ARGS 	&& make -j "$(nproc)" 	&& make install 	&& { find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; } 	&& make clean 	&& cd / 	&& docker-php-source delete 		&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $buildDeps 		&& pecl update-channels 	&& rm -rf /tmp/pear ~/.pearrc
# Fri, 29 Sep 2017 00:48:50 GMT
COPY multi:dbabcc0b81566a75f49e7faa9ca5f96cd22a515b80ee7ea1e34fceceee3f9c2a in /usr/local/bin/ 
# Fri, 29 Sep 2017 00:48:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 29 Sep 2017 00:48:51 GMT
COPY file:24613ecbb1ce6a09f683b0753da9c26a1af07547326e8a02f6eec80ad6f2774a in /usr/local/bin/ 
# Fri, 29 Sep 2017 00:48:51 GMT
WORKDIR /var/www/html
# Fri, 29 Sep 2017 00:48:51 GMT
EXPOSE 80/tcp
# Fri, 29 Sep 2017 00:48:51 GMT
CMD ["apache2-foreground"]
# Fri, 29 Sep 2017 01:43:32 GMT
RUN apt-get update && apt-get install -y 		git 		imagemagick 		libicu-dev 	--no-install-recommends && rm -r /var/lib/apt/lists/*
# Fri, 29 Sep 2017 01:44:43 GMT
RUN docker-php-ext-install mbstring mysqli opcache intl
# Fri, 29 Sep 2017 01:46:04 GMT
RUN pecl channel-update pecl.php.net 	&& pecl install apcu-5.1.8 	&& docker-php-ext-enable apcu
# Fri, 29 Sep 2017 01:46:05 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 		echo 'opcache.enable_cli=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 29 Sep 2017 01:46:05 GMT
RUN mkdir -p /var/www/data 	&& chown -R www-data:www-data /var/www/data
# Fri, 29 Sep 2017 01:46:05 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.28
# Fri, 29 Sep 2017 01:46:06 GMT
ENV MEDIAWIKI_BRANCH=REL1_28
# Fri, 29 Sep 2017 01:46:06 GMT
ENV MEDIAWIKI_VERSION=1.28.2
# Fri, 29 Sep 2017 01:46:06 GMT
ENV MEDIAWIKI_SHA512=049fa132f17efa43c9cf380fdd85b117b959c8b70fd48f0c8e0dec8a770e3f3405fe272df006ba1fe47fa339b2eb4030ac21edc01295232219eeecdfebee08ce
# Fri, 29 Sep 2017 01:46:12 GMT
RUN curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz 	&& echo "${MEDIAWIKI_SHA512} *mediawiki.tar.gz" | sha512sum -c - 	&& tar -xz --strip-components=1 -f mediawiki.tar.gz 	&& rm mediawiki.tar.gz 	&& chown -R www-data:www-data extensions skins cache images
```

-	Layers:
	-	`sha256:aa18ad1a0d334d80981104c599fa8cef9264552a265b1197af11274beba767cf`  
		Last Modified: Thu, 07 Sep 2017 23:11:06 GMT  
		Size: 52.6 MB (52595547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d5f85af454812aec1820ce0e52e003b81e4569823e2da5b0cccb58e31b136f`  
		Last Modified: Fri, 15 Sep 2017 01:34:31 GMT  
		Size: 82.5 MB (82495988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca642e7826b9552669a262d36f5488e3a478c2f9f97a98db37b203194ea6248`  
		Last Modified: Fri, 15 Sep 2017 01:34:12 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3638d91a90398e9b21e86d5f58ce592dcef089e461ed52559ddcc99d1021c04b`  
		Last Modified: Fri, 15 Sep 2017 01:35:48 GMT  
		Size: 3.0 MB (3012522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3646a95ab6778f36ca28c448f0217a571157bd80a83faa94284a046540d9b90e`  
		Last Modified: Fri, 15 Sep 2017 01:35:46 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628b8373e193144e4047261fde47c3b10881e013cc4730690c28281e30f340d4`  
		Last Modified: Fri, 15 Sep 2017 01:35:45 GMT  
		Size: 431.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24a2b2280edf466db78ea09cb8f23295781c7472f63e5ee7ebd5302e6ef3c45`  
		Last Modified: Fri, 15 Sep 2017 01:35:45 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f968b84cbbbc7f23c623c4ae9ad247431a59a370333ec20de8191284b4838b54`  
		Last Modified: Fri, 15 Sep 2017 01:35:44 GMT  
		Size: 485.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eba9b5fa4872bbe2b17063876e02d94e27ed76aaae378ff06f4fb5fabe92cca`  
		Last Modified: Fri, 29 Sep 2017 01:22:29 GMT  
		Size: 12.3 MB (12314249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0234067d12410685389f8fb0c6baa2ad79e2258de03ee29c0880902e4fb9d5e0`  
		Last Modified: Fri, 29 Sep 2017 01:22:27 GMT  
		Size: 502.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b85a2b999ef3bb1a50a67119cf987b7731cb7b0c1db3b4e40cad13de362b2b7a`  
		Last Modified: Fri, 29 Sep 2017 01:22:34 GMT  
		Size: 13.2 MB (13212054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d31395fe2313a4fde865b2d1f5309793fb4115b44960bc26a7b3b98e288c6ca`  
		Last Modified: Fri, 29 Sep 2017 01:22:28 GMT  
		Size: 2.2 KB (2180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cff026afe51f89f948e975c0e3d1eaa0b96d81c64131c518e03067fdded35f4`  
		Last Modified: Fri, 29 Sep 2017 01:22:27 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98fe309fb9f48e5ef6e9b0fb75f556ad442242b6564bc9a195c0940f5fa24e07`  
		Last Modified: Fri, 29 Sep 2017 01:50:17 GMT  
		Size: 48.1 MB (48128140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b595c41b7857b1df5a2deb28ee4bd4dfaad5394f4d3c6c01b75813dd5e77bb3`  
		Last Modified: Fri, 29 Sep 2017 01:50:04 GMT  
		Size: 1.4 MB (1396887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcfdff861639f786eaee6312b7d55a7a6dc5701f9127cd6dda7bd439772f8d87`  
		Last Modified: Fri, 29 Sep 2017 01:50:04 GMT  
		Size: 324.7 KB (324705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e042b08e2f1c8ab292b65a02ae566d8102407fdc6b9b7b37a85497059d63612`  
		Last Modified: Fri, 29 Sep 2017 01:50:04 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f56197b8593bfc486b67dc5e0145ea549653a73d2fb64be3622c1aca733aaef`  
		Last Modified: Fri, 29 Sep 2017 01:50:04 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d46df421b14bd633693323e773e0a5b225397fb12fff5aab59ac499a17ecac4`  
		Last Modified: Fri, 29 Sep 2017 01:50:14 GMT  
		Size: 33.4 MB (33377828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mediawiki:lts`

```console
$ docker pull mediawiki@sha256:9df58ec967985038a57df791286826e2569a714f00b7289478ff1c790ce7000b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mediawiki:lts` - linux; amd64

```console
$ docker pull mediawiki@sha256:51a38d067566c19a0d3dae17be86e2bc7590e885d9c896bd0f0c09b8481cbb9d
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.4 MB (245375379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af897575138a24b57dd6b6a96cef4d53694f17f3d826491acaca6373538fe3f5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 13 Sep 2017 08:40:43 GMT
ADD file:d7333b3e0bc6479d2faed32e06d85f1975e5b23e13e75555aeed0f639770413b in / 
# Wed, 13 Sep 2017 08:40:43 GMT
CMD ["bash"]
# Thu, 14 Sep 2017 23:57:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		libpcre3-dev 		make 		pkg-config 		re2c
# Thu, 14 Sep 2017 23:58:23 GMT
RUN apt-get update && apt-get install -y 		$PHPIZE_DEPS 		ca-certificates 		curl 		libedit2 		libsqlite3-0 		libxml2 		xz-utils 	--no-install-recommends && rm -r /var/lib/apt/lists/*
# Thu, 14 Sep 2017 23:58:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Sep 2017 23:58:24 GMT
RUN mkdir -p $PHP_INI_DIR/conf.d
# Fri, 15 Sep 2017 00:08:17 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		apache2 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Sep 2017 00:08:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 15 Sep 2017 00:08:18 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 15 Sep 2017 00:08:18 GMT
RUN set -ex 		&& sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS" 		&& . "$APACHE_ENVVARS" 	&& for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		/var/www/html 	; do 		rm -rvf "$dir" 		&& mkdir -p "$dir" 		&& chown -R "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 	done
# Fri, 15 Sep 2017 00:08:19 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 15 Sep 2017 00:08:19 GMT
RUN set -ex 	&& . "$APACHE_ENVVARS" 	&& ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log" 	&& ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log" 	&& ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"
# Fri, 15 Sep 2017 00:08:20 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 15 Sep 2017 00:08:20 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 15 Sep 2017 00:08:20 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2
# Fri, 15 Sep 2017 00:08:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 15 Sep 2017 00:08:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 15 Sep 2017 00:08:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Fri, 15 Sep 2017 00:39:01 GMT
ENV GPG_KEYS=1A4E8B7277C42E53DBA9C7B9BCAA30EA9C0D5763 6E4F6AB321FDC07F2C332E3AC2BF0BC433CFC8B3
# Fri, 29 Sep 2017 00:45:54 GMT
ENV PHP_VERSION=7.0.24
# Fri, 29 Sep 2017 00:45:54 GMT
ENV PHP_URL=https://secure.php.net/get/php-7.0.24.tar.xz/from/this/mirror PHP_ASC_URL=https://secure.php.net/get/php-7.0.24.tar.xz.asc/from/this/mirror
# Fri, 29 Sep 2017 00:45:55 GMT
ENV PHP_SHA256=4dba7aa365193c9229f89f1975fad4c01135d29922a338ffb4a27e840d6f1c98 PHP_MD5=
# Fri, 29 Sep 2017 00:46:19 GMT
RUN set -xe; 		fetchDeps=' 		wget 	'; 	if ! command -v gpg > /dev/null; then 		fetchDeps="$fetchDeps 			dirmngr 			gnupg2 		"; 	fi; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		wget -O php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		wget -O php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps
# Fri, 29 Sep 2017 00:46:19 GMT
COPY file:207c686e3fed4f71f8a7b245d8dcae9c9048d276a326d82b553c12a90af0c0ca in /usr/local/bin/ 
# Fri, 29 Sep 2017 00:48:50 GMT
RUN set -xe 	&& buildDeps=" 		$PHP_EXTRA_BUILD_DEPS 		libcurl4-openssl-dev 		libedit-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	" 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	&& docker-php-source extract 	&& cd /usr/src/php 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)" 	&& if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi 	&& ./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--disable-cgi 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pcre-regex=/usr 		--with-libdir="lib/$debMultiarch" 				$PHP_EXTRA_CONFIGURE_ARGS 	&& make -j "$(nproc)" 	&& make install 	&& { find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; } 	&& make clean 	&& cd / 	&& docker-php-source delete 		&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $buildDeps 		&& pecl update-channels 	&& rm -rf /tmp/pear ~/.pearrc
# Fri, 29 Sep 2017 00:48:50 GMT
COPY multi:dbabcc0b81566a75f49e7faa9ca5f96cd22a515b80ee7ea1e34fceceee3f9c2a in /usr/local/bin/ 
# Fri, 29 Sep 2017 00:48:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 29 Sep 2017 00:48:51 GMT
COPY file:24613ecbb1ce6a09f683b0753da9c26a1af07547326e8a02f6eec80ad6f2774a in /usr/local/bin/ 
# Fri, 29 Sep 2017 00:48:51 GMT
WORKDIR /var/www/html
# Fri, 29 Sep 2017 00:48:51 GMT
EXPOSE 80/tcp
# Fri, 29 Sep 2017 00:48:51 GMT
CMD ["apache2-foreground"]
# Fri, 29 Sep 2017 01:43:32 GMT
RUN apt-get update && apt-get install -y 		git 		imagemagick 		libicu-dev 	--no-install-recommends && rm -r /var/lib/apt/lists/*
# Fri, 29 Sep 2017 01:44:43 GMT
RUN docker-php-ext-install mbstring mysqli opcache intl
# Fri, 29 Sep 2017 01:46:04 GMT
RUN pecl channel-update pecl.php.net 	&& pecl install apcu-5.1.8 	&& docker-php-ext-enable apcu
# Fri, 29 Sep 2017 01:46:05 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 		echo 'opcache.enable_cli=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 29 Sep 2017 01:46:05 GMT
RUN mkdir -p /var/www/data 	&& chown -R www-data:www-data /var/www/data
# Fri, 29 Sep 2017 01:49:44 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.27
# Fri, 29 Sep 2017 01:49:44 GMT
ENV MEDIAWIKI_BRANCH=REL1_27
# Fri, 29 Sep 2017 01:49:44 GMT
ENV MEDIAWIKI_VERSION=1.27.3
# Fri, 29 Sep 2017 01:49:44 GMT
ENV MEDIAWIKI_SHA512=bc6228342b589a3acb0f5623b9ef45982d7aab032ff322aaf7bda7ac3ee16a7732b8013698d8f509da4310bbb65c12a73b7bbe4612d5e0e3d93965199efdc8eb
# Fri, 29 Sep 2017 01:49:50 GMT
RUN curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz 	&& echo "${MEDIAWIKI_SHA512} *mediawiki.tar.gz" | sha512sum -c - 	&& tar -xz --strip-components=1 -f mediawiki.tar.gz 	&& rm mediawiki.tar.gz 	&& chown -R www-data:www-data extensions skins cache images
```

-	Layers:
	-	`sha256:aa18ad1a0d334d80981104c599fa8cef9264552a265b1197af11274beba767cf`  
		Last Modified: Thu, 07 Sep 2017 23:11:06 GMT  
		Size: 52.6 MB (52595547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d5f85af454812aec1820ce0e52e003b81e4569823e2da5b0cccb58e31b136f`  
		Last Modified: Fri, 15 Sep 2017 01:34:31 GMT  
		Size: 82.5 MB (82495988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca642e7826b9552669a262d36f5488e3a478c2f9f97a98db37b203194ea6248`  
		Last Modified: Fri, 15 Sep 2017 01:34:12 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3638d91a90398e9b21e86d5f58ce592dcef089e461ed52559ddcc99d1021c04b`  
		Last Modified: Fri, 15 Sep 2017 01:35:48 GMT  
		Size: 3.0 MB (3012522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3646a95ab6778f36ca28c448f0217a571157bd80a83faa94284a046540d9b90e`  
		Last Modified: Fri, 15 Sep 2017 01:35:46 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628b8373e193144e4047261fde47c3b10881e013cc4730690c28281e30f340d4`  
		Last Modified: Fri, 15 Sep 2017 01:35:45 GMT  
		Size: 431.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24a2b2280edf466db78ea09cb8f23295781c7472f63e5ee7ebd5302e6ef3c45`  
		Last Modified: Fri, 15 Sep 2017 01:35:45 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f968b84cbbbc7f23c623c4ae9ad247431a59a370333ec20de8191284b4838b54`  
		Last Modified: Fri, 15 Sep 2017 01:35:44 GMT  
		Size: 485.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eba9b5fa4872bbe2b17063876e02d94e27ed76aaae378ff06f4fb5fabe92cca`  
		Last Modified: Fri, 29 Sep 2017 01:22:29 GMT  
		Size: 12.3 MB (12314249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0234067d12410685389f8fb0c6baa2ad79e2258de03ee29c0880902e4fb9d5e0`  
		Last Modified: Fri, 29 Sep 2017 01:22:27 GMT  
		Size: 502.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b85a2b999ef3bb1a50a67119cf987b7731cb7b0c1db3b4e40cad13de362b2b7a`  
		Last Modified: Fri, 29 Sep 2017 01:22:34 GMT  
		Size: 13.2 MB (13212054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d31395fe2313a4fde865b2d1f5309793fb4115b44960bc26a7b3b98e288c6ca`  
		Last Modified: Fri, 29 Sep 2017 01:22:28 GMT  
		Size: 2.2 KB (2180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cff026afe51f89f948e975c0e3d1eaa0b96d81c64131c518e03067fdded35f4`  
		Last Modified: Fri, 29 Sep 2017 01:22:27 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98fe309fb9f48e5ef6e9b0fb75f556ad442242b6564bc9a195c0940f5fa24e07`  
		Last Modified: Fri, 29 Sep 2017 01:50:17 GMT  
		Size: 48.1 MB (48128140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b595c41b7857b1df5a2deb28ee4bd4dfaad5394f4d3c6c01b75813dd5e77bb3`  
		Last Modified: Fri, 29 Sep 2017 01:50:04 GMT  
		Size: 1.4 MB (1396887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcfdff861639f786eaee6312b7d55a7a6dc5701f9127cd6dda7bd439772f8d87`  
		Last Modified: Fri, 29 Sep 2017 01:50:04 GMT  
		Size: 324.7 KB (324705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e042b08e2f1c8ab292b65a02ae566d8102407fdc6b9b7b37a85497059d63612`  
		Last Modified: Fri, 29 Sep 2017 01:50:04 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f56197b8593bfc486b67dc5e0145ea549653a73d2fb64be3622c1aca733aaef`  
		Last Modified: Fri, 29 Sep 2017 01:50:04 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c3e1b3f0ce55a9e4ed949938077f5668b285d3329740b9766bb93b31dc34a46`  
		Last Modified: Fri, 29 Sep 2017 01:50:55 GMT  
		Size: 31.9 MB (31888632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mediawiki:stable`

```console
$ docker pull mediawiki@sha256:3b6cab8092ecec8a6953fff8f50bd6a87374f20438cf5b338f37b72caffd93f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mediawiki:stable` - linux; amd64

```console
$ docker pull mediawiki@sha256:daa6ce0d7ef73aeefe8133804d66ebc1cb6c32a4d4ea8ac2442cf08ebf8401c6
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 MB (254305964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5726e4f5ce4772c9e7c75bc83330ebe18d044c4cf77c900197699ceff591369`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 13 Sep 2017 08:40:43 GMT
ADD file:d7333b3e0bc6479d2faed32e06d85f1975e5b23e13e75555aeed0f639770413b in / 
# Wed, 13 Sep 2017 08:40:43 GMT
CMD ["bash"]
# Thu, 14 Sep 2017 23:57:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		libpcre3-dev 		make 		pkg-config 		re2c
# Thu, 14 Sep 2017 23:58:23 GMT
RUN apt-get update && apt-get install -y 		$PHPIZE_DEPS 		ca-certificates 		curl 		libedit2 		libsqlite3-0 		libxml2 		xz-utils 	--no-install-recommends && rm -r /var/lib/apt/lists/*
# Thu, 14 Sep 2017 23:58:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Sep 2017 23:58:24 GMT
RUN mkdir -p $PHP_INI_DIR/conf.d
# Fri, 15 Sep 2017 00:08:17 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		apache2 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Sep 2017 00:08:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 15 Sep 2017 00:08:18 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 15 Sep 2017 00:08:18 GMT
RUN set -ex 		&& sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS" 		&& . "$APACHE_ENVVARS" 	&& for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		/var/www/html 	; do 		rm -rvf "$dir" 		&& mkdir -p "$dir" 		&& chown -R "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 	done
# Fri, 15 Sep 2017 00:08:19 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 15 Sep 2017 00:08:19 GMT
RUN set -ex 	&& . "$APACHE_ENVVARS" 	&& ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log" 	&& ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log" 	&& ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"
# Fri, 15 Sep 2017 00:08:20 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 15 Sep 2017 00:08:20 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 15 Sep 2017 00:08:20 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2
# Fri, 15 Sep 2017 00:08:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 15 Sep 2017 00:08:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 15 Sep 2017 00:08:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Fri, 15 Sep 2017 00:08:21 GMT
ENV GPG_KEYS=A917B1ECDA84AEC2B568FED6F50ABC807BD5DCD0 528995BFEDFBA7191D46839EF9BA0ADA31CBD89E
# Fri, 29 Sep 2017 23:07:28 GMT
ENV PHP_VERSION=7.1.10
# Fri, 29 Sep 2017 23:07:28 GMT
ENV PHP_URL=https://secure.php.net/get/php-7.1.10.tar.xz/from/this/mirror PHP_ASC_URL=https://secure.php.net/get/php-7.1.10.tar.xz.asc/from/this/mirror
# Fri, 29 Sep 2017 23:07:28 GMT
ENV PHP_SHA256=2b8efa771a2ead0bb3ae67b530ca505b5b286adc873cca9ce97a6e1d6815c50b PHP_MD5=
# Fri, 29 Sep 2017 23:07:50 GMT
RUN set -xe; 		fetchDeps=' 		wget 	'; 	if ! command -v gpg > /dev/null; then 		fetchDeps="$fetchDeps 			dirmngr 			gnupg2 		"; 	fi; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		wget -O php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		wget -O php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps
# Fri, 29 Sep 2017 23:07:50 GMT
COPY file:207c686e3fed4f71f8a7b245d8dcae9c9048d276a326d82b553c12a90af0c0ca in /usr/local/bin/ 
# Fri, 29 Sep 2017 23:10:26 GMT
RUN set -xe 	&& buildDeps=" 		$PHP_EXTRA_BUILD_DEPS 		libcurl4-openssl-dev 		libedit-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	" 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	&& docker-php-source extract 	&& cd /usr/src/php 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)" 	&& if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi 	&& ./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--disable-cgi 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pcre-regex=/usr 		--with-libdir="lib/$debMultiarch" 				$PHP_EXTRA_CONFIGURE_ARGS 	&& make -j "$(nproc)" 	&& make install 	&& { find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; } 	&& make clean 	&& cd / 	&& docker-php-source delete 		&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $buildDeps 		&& pecl update-channels 	&& rm -rf /tmp/pear ~/.pearrc
# Fri, 29 Sep 2017 23:10:27 GMT
COPY multi:dbabcc0b81566a75f49e7faa9ca5f96cd22a515b80ee7ea1e34fceceee3f9c2a in /usr/local/bin/ 
# Fri, 29 Sep 2017 23:10:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 29 Sep 2017 23:10:27 GMT
COPY file:24613ecbb1ce6a09f683b0753da9c26a1af07547326e8a02f6eec80ad6f2774a in /usr/local/bin/ 
# Fri, 29 Sep 2017 23:10:27 GMT
WORKDIR /var/www/html
# Fri, 29 Sep 2017 23:10:28 GMT
EXPOSE 80/tcp
# Fri, 29 Sep 2017 23:10:28 GMT
CMD ["apache2-foreground"]
# Sat, 30 Sep 2017 00:36:54 GMT
RUN apt-get update && apt-get install -y 		git 		imagemagick 		libicu-dev 	--no-install-recommends && rm -r /var/lib/apt/lists/*
# Sat, 30 Sep 2017 00:38:11 GMT
RUN docker-php-ext-install mbstring mysqli opcache intl
# Sat, 30 Sep 2017 00:38:23 GMT
RUN pecl channel-update pecl.php.net 	&& pecl install apcu-5.1.8 	&& docker-php-ext-enable apcu
# Sat, 30 Sep 2017 00:38:23 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 		echo 'opcache.enable_cli=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sat, 30 Sep 2017 00:38:24 GMT
RUN mkdir -p /var/www/data 	&& chown -R www-data:www-data /var/www/data
# Sat, 30 Sep 2017 00:38:24 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.29
# Sat, 30 Sep 2017 00:38:25 GMT
ENV MEDIAWIKI_BRANCH=REL1_29
# Sat, 30 Sep 2017 00:38:25 GMT
ENV MEDIAWIKI_VERSION=1.29.1
# Sat, 30 Sep 2017 00:38:25 GMT
ENV MEDIAWIKI_SHA512=c4e04c4fb665c3d8299f3e03e608904aaf0e06381240c7259813eb670c3e32cde919353dd19993250cf49be81d604ac5f6d468bc563116a4b268e5011d34119f
# Sat, 30 Sep 2017 00:38:31 GMT
RUN curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz 	&& echo "${MEDIAWIKI_SHA512} *mediawiki.tar.gz" | sha512sum -c - 	&& tar -xz --strip-components=1 -f mediawiki.tar.gz 	&& rm mediawiki.tar.gz 	&& chown -R www-data:www-data extensions skins cache images
```

-	Layers:
	-	`sha256:aa18ad1a0d334d80981104c599fa8cef9264552a265b1197af11274beba767cf`  
		Last Modified: Thu, 07 Sep 2017 23:11:06 GMT  
		Size: 52.6 MB (52595547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d5f85af454812aec1820ce0e52e003b81e4569823e2da5b0cccb58e31b136f`  
		Last Modified: Fri, 15 Sep 2017 01:34:31 GMT  
		Size: 82.5 MB (82495988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca642e7826b9552669a262d36f5488e3a478c2f9f97a98db37b203194ea6248`  
		Last Modified: Fri, 15 Sep 2017 01:34:12 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3638d91a90398e9b21e86d5f58ce592dcef089e461ed52559ddcc99d1021c04b`  
		Last Modified: Fri, 15 Sep 2017 01:35:48 GMT  
		Size: 3.0 MB (3012522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3646a95ab6778f36ca28c448f0217a571157bd80a83faa94284a046540d9b90e`  
		Last Modified: Fri, 15 Sep 2017 01:35:46 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628b8373e193144e4047261fde47c3b10881e013cc4730690c28281e30f340d4`  
		Last Modified: Fri, 15 Sep 2017 01:35:45 GMT  
		Size: 431.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24a2b2280edf466db78ea09cb8f23295781c7472f63e5ee7ebd5302e6ef3c45`  
		Last Modified: Fri, 15 Sep 2017 01:35:45 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f968b84cbbbc7f23c623c4ae9ad247431a59a370333ec20de8191284b4838b54`  
		Last Modified: Fri, 15 Sep 2017 01:35:44 GMT  
		Size: 485.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77afd73ce87d8a835726d0c9b72b750bad785a6cda38015d6aa383c0cfe519c`  
		Last Modified: Fri, 29 Sep 2017 23:43:38 GMT  
		Size: 12.5 MB (12520223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863afbb954365f5f975093a2eb7094211798ef1c2bda6945449a78969af9bc94`  
		Last Modified: Fri, 29 Sep 2017 23:43:37 GMT  
		Size: 501.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f381536e9279732352befaf4f534e8ba6f937e97c061e96e83e4bd1b7e3005`  
		Last Modified: Fri, 29 Sep 2017 23:43:40 GMT  
		Size: 13.5 MB (13521858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e96e9b4935a1b0dbaadd56fd518ad6dd0fb7fbb5bdc9d308ac91d5cbe365f22`  
		Last Modified: Fri, 29 Sep 2017 23:43:37 GMT  
		Size: 2.2 KB (2183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca94deb9c4dfde50548223713993b67299f97259943b49e9a6cfca6aa89e7116`  
		Last Modified: Fri, 29 Sep 2017 23:43:37 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1531a42b8fbad2ddcbf0a3bb4fce32136c8f9d4d12f6d42315a7fcdfe097991a`  
		Last Modified: Sat, 30 Sep 2017 00:43:32 GMT  
		Size: 48.1 MB (48128251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67a47f465ce0894770fe71aed42434aa04555179cb78bee240bd72aa57b21d3b`  
		Last Modified: Sat, 30 Sep 2017 00:43:19 GMT  
		Size: 1.5 MB (1490066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aacf27acbcf759713ab885124351e83a55666bc5e0c78f5972b4f7806f31cb63`  
		Last Modified: Sat, 30 Sep 2017 00:43:19 GMT  
		Size: 326.1 KB (326080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ef81a00ec595c6233d071a07d5f23c7279e50c206451fca533a8101195e8c5`  
		Last Modified: Sat, 30 Sep 2017 00:43:18 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608e37947697643dea39232439f0aa981786281393e269c6416276acc784c3fb`  
		Last Modified: Sat, 30 Sep 2017 00:43:18 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e9113eba113d2dd2fbaae853604bcabec1c3950f6dac585d99ecb47c36e837`  
		Last Modified: Sat, 30 Sep 2017 00:43:33 GMT  
		Size: 40.2 MB (40208770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
