## `php-zendserver:latest`

```console
$ docker pull php-zendserver@sha256:b367270e961a430ccf0077d153c48b4d0a31f5d85695a089fd10cc69119fe269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:latest` - linux; amd64

```console
$ docker pull php-zendserver@sha256:72d974e5cdcd9dc95e27ef02239b3856485be250c1d94b738fe91308a2147513
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.2 MB (415155750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12551dd994e1dc40b1530900861b928bb8508826c379521b0d2db75d156e6920`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Wed, 13 Sep 2017 23:26:20 GMT
ADD file:8f997234193c2f587ac17bb4a8db2657103d2924813edb281eec7ba9883a2806 in / 
# Wed, 13 Sep 2017 23:26:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 13 Sep 2017 23:26:21 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 13 Sep 2017 23:26:22 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Wed, 13 Sep 2017 23:26:22 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 13 Sep 2017 23:26:23 GMT
CMD ["/bin/bash"]
# Thu, 14 Sep 2017 00:07:05 GMT
RUN apt-key adv --keyserver pgp.mit.edu --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Thu, 14 Sep 2017 00:24:54 GMT
RUN echo "deb http://repos.zend.com/zend-server/9.1/deb_apache2.4 server non-free" >> /etc/apt/sources.list.d/zend-server.list
# Thu, 14 Sep 2017 00:26:49 GMT
RUN apt-get update && apt-get install -y libmysqlclient18 unzip git zend-server-php-7.1=9.1.1+b119 && /usr/local/zend/bin/zendctl.sh stop
# Thu, 14 Sep 2017 00:26:50 GMT
COPY file:9067f1585f25b36ab3a81514a2f158ba0d6e0431cad7de2ea9c4b4249a6c134f in /etc/ 
# Thu, 14 Sep 2017 00:26:50 GMT
COPY file:82de006e31874ac4e03685b3e87e988446f42138aaaf0fc5faad9cddb48040ba in /etc/apache2/conf-available 
# Thu, 14 Sep 2017 00:26:51 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Thu, 14 Sep 2017 00:26:52 GMT
RUN /usr/sbin/a2enmod headers
# Thu, 14 Sep 2017 00:26:52 GMT
ENV ZS_INIT_VERSION=0.3
# Thu, 14 Sep 2017 00:26:52 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Thu, 14 Sep 2017 00:27:00 GMT
RUN apt-get install -y curl
# Thu, 14 Sep 2017 00:27:01 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Thu, 14 Sep 2017 00:27:01 GMT
WORKDIR /usr/local/zs-init
# Thu, 14 Sep 2017 00:27:06 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php
# Thu, 14 Sep 2017 00:27:31 GMT
RUN /usr/local/zend/bin/php composer.phar update
# Thu, 14 Sep 2017 00:27:32 GMT
COPY dir:6174d7fdcd8142a1b143e80efd2994e57dd5d7610a8fbfee3a7288ddf495dfdf in /usr/local/bin 
# Thu, 14 Sep 2017 00:27:32 GMT
COPY dir:b14dbc48195e4d5367d3aea2ed0fb26985bacb8d8229d24961363db2e2edf8f0 in /usr/local/zend/var/plugins/ 
# Thu, 14 Sep 2017 00:27:33 GMT
RUN rm /var/www/html/index.html
# Thu, 14 Sep 2017 00:27:33 GMT
COPY dir:9f1a7f23dfcf85f3c7148d98ae7914654fe8acfc4e4651f3a08427c09af24198 in /var/www/html 
# Thu, 14 Sep 2017 00:27:33 GMT
EXPOSE 80/tcp
# Thu, 14 Sep 2017 00:27:33 GMT
EXPOSE 443/tcp
# Thu, 14 Sep 2017 00:27:33 GMT
EXPOSE 10081/tcp
# Thu, 14 Sep 2017 00:27:34 GMT
EXPOSE 10082/tcp
# Thu, 14 Sep 2017 00:27:34 GMT
WORKDIR /var/www/html
# Thu, 14 Sep 2017 00:27:34 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:bae382666908fd87a3a3646d7eb7176fa42226027d3256cac38ee0b79bdb0491`  
		Last Modified: Wed, 13 Sep 2017 22:04:42 GMT  
		Size: 67.1 MB (67114903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ede3c02ff200fff7454ce59e1c3bb62f538847cefd5b8541e088ad22c42879`  
		Last Modified: Wed, 13 Sep 2017 23:27:09 GMT  
		Size: 72.6 KB (72648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4e69f33106a3131ce07d9ed4403593a7698be6dabd6cabd2c9c228599c8ce0`  
		Last Modified: Wed, 13 Sep 2017 23:27:09 GMT  
		Size: 364.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d43e5f5d27feb983909350fa3a008ebfb66436e172337cd543db358f5a01f1c`  
		Last Modified: Wed, 13 Sep 2017 23:27:09 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0de1abb17d6e07bcf1b68dc5c75acf0386405905ed735efe65a5235f29e756d`  
		Last Modified: Wed, 13 Sep 2017 23:27:09 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:225d0261262cc13e13f2c7200866cfa25e68576c37f03e06a97f16a14087dccd`  
		Last Modified: Thu, 14 Sep 2017 00:29:08 GMT  
		Size: 13.1 KB (13065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c3997f7755d0a14fa5799994230d5dff0fbc4c72af1a8820f4c2c2809f1e464`  
		Last Modified: Thu, 14 Sep 2017 00:32:25 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6984a38d49f1bb081e2cbd9cc26c84dcec114b5f43496418e49c6dd3686ab8be`  
		Last Modified: Thu, 14 Sep 2017 00:33:37 GMT  
		Size: 333.2 MB (333168182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee41d6297b9a7653d238da5d85ba283f29287a9f333cf6f33b207a043b537d59`  
		Last Modified: Thu, 14 Sep 2017 00:32:23 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1ee698653216ec132fcc1d0398189d7e96eef883f343fa2bef03bf884b4c83`  
		Last Modified: Thu, 14 Sep 2017 00:32:23 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0905028422997b4566a745059bbb686a0d21fc301ccd576ce3ee7636db9cf1f`  
		Last Modified: Thu, 14 Sep 2017 00:32:22 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26dc447798d0a18dd4b6c9c36288bb7c77a008286fecbd600c33124d27c0cea1`  
		Last Modified: Thu, 14 Sep 2017 00:32:20 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5629decf37fc46404a4543a06d782ad151192d73b5ee58245c850936b74d5141`  
		Last Modified: Thu, 14 Sep 2017 00:32:20 GMT  
		Size: 907.3 KB (907312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28870dac52a140188675e6e6bca33647bb876b11c4575a366350a4e828db8d5c`  
		Last Modified: Thu, 14 Sep 2017 00:32:20 GMT  
		Size: 18.8 KB (18830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952ccf6df1e6f0fb14387bdcee179c6a75bf79c58d6fc591bb9e70e68d6a3f3a`  
		Last Modified: Thu, 14 Sep 2017 00:32:20 GMT  
		Size: 495.9 KB (495855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afb63d829be7a0da4eccb5f7e0b727445deac0d622adb61c25704bb77d60417`  
		Last Modified: Thu, 14 Sep 2017 00:32:23 GMT  
		Size: 13.3 MB (13344925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6184724be0215919d0c04dba3a529afb30c8893e089a4217355d1ee31e2a66`  
		Last Modified: Thu, 14 Sep 2017 00:32:18 GMT  
		Size: 13.4 KB (13358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2cae1ba16c83187cf5530c541f196b4e9f3bec87f5a05402280c0a4c42a6f1e`  
		Last Modified: Thu, 14 Sep 2017 00:32:18 GMT  
		Size: 2.5 KB (2534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf072cb80eb1275b97d0ec5c72df4eabf96f54e6fa6c1b5cd0c54aba5e23e9a`  
		Last Modified: Thu, 14 Sep 2017 00:32:18 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9657bfaf62a03f87773c47a7e29c3186dff2e38a55f66357447df42ceee5976`  
		Last Modified: Thu, 14 Sep 2017 00:32:18 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
