## `ros:kinetic-ros-core-jessie`

```console
$ docker pull ros@sha256:22f83172c73d88f8a177e5b325319f95cc2a65318b4db44ded0755b4cf9daff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:kinetic-ros-core-jessie` - linux; amd64

```console
$ docker pull ros@sha256:7410a5bf2bee3f67676702c98cb1e98369f903cfbe53ee380bd8d074e7d25b6a
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.7 MB (290668182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06de2b3d8f2fd4925d9368ade8ca3e8501a7df2c233d05601b94b852ec88e595`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 Sep 2017 08:40:43 GMT
ADD file:d7333b3e0bc6479d2faed32e06d85f1975e5b23e13e75555aeed0f639770413b in / 
# Wed, 13 Sep 2017 08:40:43 GMT
CMD ["bash"]
# Thu, 14 Sep 2017 00:53:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 14 Sep 2017 00:53:13 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 421C365BD9FF1F717815A3895523BAEEB01FA116
# Thu, 14 Sep 2017 00:53:13 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu jessie main" > /etc/apt/sources.list.d/ros-latest.list
# Thu, 14 Sep 2017 00:53:53 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 14 Sep 2017 00:53:53 GMT
ENV LANG=C.UTF-8
# Thu, 14 Sep 2017 00:53:54 GMT
ENV LC_ALL=C.UTF-8
# Thu, 14 Sep 2017 00:54:03 GMT
RUN rosdep init     && rosdep update
# Thu, 14 Sep 2017 00:54:04 GMT
ENV ROS_DISTRO=kinetic
# Thu, 14 Sep 2017 00:55:19 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-core=1.3.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 14 Sep 2017 00:55:19 GMT
COPY file:824303428ad16ae6296df253434e00a00126dc8404f740a8b885c9f61a2f5fcb in / 
# Thu, 14 Sep 2017 00:55:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 14 Sep 2017 00:55:20 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:aa18ad1a0d334d80981104c599fa8cef9264552a265b1197af11274beba767cf`  
		Last Modified: Thu, 07 Sep 2017 23:11:06 GMT  
		Size: 52.6 MB (52595547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51949222cb5c5f13b74874383c7887b3da1fed584a35923260288f128fb5285f`  
		Last Modified: Thu, 14 Sep 2017 01:30:12 GMT  
		Size: 33.8 MB (33760764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd9ad6c36307681bc688ac33f91392f4f60fdcf9177bd8fe235b849a89325c63`  
		Last Modified: Thu, 14 Sep 2017 01:29:53 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:051013f06cd2eabc80f8bb69bd1bd20892794b6f64bd82a72c20694079ba173a`  
		Last Modified: Thu, 14 Sep 2017 01:29:51 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd5333365bd4281fde91bd09e152f47bec1948e2fbedd60f517e8b7fbe0be7bc`  
		Last Modified: Thu, 14 Sep 2017 01:30:15 GMT  
		Size: 46.3 MB (46338636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d1dcde45ce5bce9d755fc149e407d48cbb9085b5a207245695ef259c9693988`  
		Last Modified: Thu, 14 Sep 2017 01:29:52 GMT  
		Size: 754.0 KB (753964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dcb5a2d83d177ecd2d7e7690738bc567d508930052f177547a31b0042966d5a`  
		Last Modified: Thu, 14 Sep 2017 01:30:51 GMT  
		Size: 157.2 MB (157217433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b68933bf6544e6b48308d34a3e7fb527c292c356020327b2687e4bbe2146d2f8`  
		Last Modified: Thu, 14 Sep 2017 01:29:50 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-ros-core-jessie` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:9be91d5c454965b0643b8217668da71eba4d3353c96e24364cae3f6a4f872d5b
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.4 MB (257362255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96322e33ebae649652d9a6d48a9a8bdf63069e71fe0fc2904acdba871b30e3f9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Sep 2017 17:23:41 GMT
ADD file:9f576a63a5e03994904e585c35fbeef6a2c96c41d8f696705c033f3ca69b6a2b in / 
# Fri, 08 Sep 2017 17:23:42 GMT
CMD ["bash"]
# Sat, 09 Sep 2017 02:27:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Sep 2017 02:27:47 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 421C365BD9FF1F717815A3895523BAEEB01FA116
# Sat, 09 Sep 2017 02:27:49 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu jessie main" > /etc/apt/sources.list.d/ros-latest.list
# Sat, 09 Sep 2017 02:31:07 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Sep 2017 02:31:08 GMT
ENV LANG=C.UTF-8
# Sat, 09 Sep 2017 02:31:08 GMT
ENV LC_ALL=C.UTF-8
# Sat, 09 Sep 2017 02:31:49 GMT
RUN rosdep init     && rosdep update
# Sat, 09 Sep 2017 02:31:50 GMT
ENV ROS_DISTRO=kinetic
# Sat, 09 Sep 2017 02:39:40 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-core=1.3.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Sep 2017 02:39:43 GMT
COPY file:824303428ad16ae6296df253434e00a00126dc8404f740a8b885c9f61a2f5fcb in / 
# Sat, 09 Sep 2017 02:39:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 09 Sep 2017 02:39:45 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:e91a355b0d3ff86add037a3f24718b760d8eb3f346f998e5116375ddce9eae19`  
		Last Modified: Fri, 08 Sep 2017 17:34:56 GMT  
		Size: 49.9 MB (49929457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:102eeef0441ceb62ea192224cc8a989588713c2ae51bcaa6b35e1d01c9bcdda9`  
		Last Modified: Sat, 09 Sep 2017 03:40:50 GMT  
		Size: 32.1 MB (32143815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a6d23f5fdf72d2761ca4da6e64f54927c2574473a1494362663044c9c3c8062`  
		Last Modified: Sat, 09 Sep 2017 03:40:36 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a16c0c2316a5956fc0f6cc64683e29593d7350bfe6925b6636bab8623fc7e1f`  
		Last Modified: Sat, 09 Sep 2017 03:40:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8779c0c576842ba6ab828de2b525f6d03c8b200cec037fc6ebd41a518190f1d`  
		Last Modified: Sat, 09 Sep 2017 03:41:03 GMT  
		Size: 44.0 MB (44035460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2004d6b508cd6068dd24b6eebc3283e21a00749a8b98471d78fc042fe5917c8`  
		Last Modified: Sat, 09 Sep 2017 03:40:34 GMT  
		Size: 753.5 KB (753457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4ba5ec7dd4008ab5fe6178f7bd4a035aab6bbf49e0d9d6c27d3cd33af3d365`  
		Last Modified: Sat, 09 Sep 2017 03:41:36 GMT  
		Size: 130.5 MB (130498225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7d1a56dd9723032155af4d0c31932b4d4b8b587001fb93d7d0bbdea593f577`  
		Last Modified: Sat, 09 Sep 2017 03:40:33 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
