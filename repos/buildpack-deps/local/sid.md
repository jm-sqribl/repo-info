# `buildpack-deps:sid`

## Docker Metadata

- Image ID: `sha256:63e25f5bcf1f117f2e32262dd9b4e9a4f726b88ac72100e08518787d86c4c030`
- Created: `2017-09-13T12:35:45.612540376Z`
- Virtual Size: ~ 1.23 Gb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Command: `["bash"]`
- Environment:
  - `PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`

## `dpkg` (`.deb`-based packages)

### `dpkg` source package: `acl=2.2.52-3`

Binary Packages:

- `libacl1:amd64=2.2.52-3+b1`

Licenses: (parsed from: `/usr/share/doc/libacl1/copyright`)

- `GPL`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris acl=2.2.52-3
'http://deb.debian.org/debian/pool/main/a/acl/acl_2.2.52-3.dsc' acl_2.2.52-3.dsc 2025 SHA256:82e344b9ab176559a85630b74ee5a68d678d7f24b6fe8139f2fd9fcf38a48095
'http://deb.debian.org/debian/pool/main/a/acl/acl_2.2.52.orig.tar.bz2' acl_2.2.52.orig.tar.bz2 312128 SHA256:59d05b38af76baf2eddccbf08c7968a17451cc785ffecc657fcb46ce32b2631d
'http://deb.debian.org/debian/pool/main/a/acl/acl_2.2.52-3.debian.tar.xz' acl_2.2.52-3.debian.tar.xz 8740 SHA256:fc3f1178d18288993fc4ce4853b7f9dcdf0bd1fd26e4f69349a4e4e5916d1fa8
```

Other potentially useful URLs:

- https://sources.debian.net/src/acl/2.2.52-3/ (for browsing the source)
- https://sources.debian.net/src/acl/2.2.52-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/acl/2.2.52-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `adduser=3.116`

Binary Packages:

- `adduser=3.116`

Licenses: (parsed from: `/usr/share/doc/adduser/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris adduser=3.116
'http://deb.debian.org/debian/pool/main/a/adduser/adduser_3.116.dsc' adduser_3.116.dsc 1740 SHA256:50e4154d3101101a890864185a09478c182155dc13f73dbb465c4279213bfafa
'http://deb.debian.org/debian/pool/main/a/adduser/adduser_3.116.tar.xz' adduser_3.116.tar.xz 212012 SHA256:72d811ad3ba17d2794b14d19acd1d6b57f9dd31d9250d51e786895dee2daeac0
```

Other potentially useful URLs:

- https://sources.debian.net/src/adduser/3.116/ (for browsing the source)
- https://sources.debian.net/src/adduser/3.116/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/adduser/3.116/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `apr-util=1.6.0-2`

Binary Packages:

- `libaprutil1:amd64=1.6.0-2`

Licenses: (parsed from: `/usr/share/doc/libaprutil1/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris apr-util=1.6.0-2
'http://deb.debian.org/debian/pool/main/a/apr-util/apr-util_1.6.0-2.dsc' apr-util_1.6.0-2.dsc 2865 SHA256:cc129f4e615a3dbdb5aedfda9381cdedb99ced08178610728d09b3ac0e776986
'http://deb.debian.org/debian/pool/main/a/apr-util/apr-util_1.6.0.orig.tar.bz2' apr-util_1.6.0.orig.tar.bz2 428750 SHA256:8474c93fa74b56ac6ca87449abe3e155723d5f534727f3f33283f6631a48ca4c
'http://deb.debian.org/debian/pool/main/a/apr-util/apr-util_1.6.0.orig.tar.bz2.asc' apr-util_1.6.0.orig.tar.bz2.asc 859 SHA256:c89a3c69e82678ab28ca72d5c658a5556ed52dd092c11421649a08b048191086
'http://deb.debian.org/debian/pool/main/a/apr-util/apr-util_1.6.0-2.debian.tar.xz' apr-util_1.6.0-2.debian.tar.xz 210800 SHA256:a8b2d0cee68374738434b09785c5344b16e2a6ad3cc4b1ef7f7e9f852e70c5e6
```

Other potentially useful URLs:

- https://sources.debian.net/src/apr-util/1.6.0-2/ (for browsing the source)
- https://sources.debian.net/src/apr-util/1.6.0-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/apr-util/1.6.0-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `apr=1.6.2-1`

Binary Packages:

- `libapr1:amd64=1.6.2-1`

Licenses: (parsed from: `/usr/share/doc/libapr1/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris apr=1.6.2-1
'http://deb.debian.org/debian/pool/main/a/apr/apr_1.6.2-1.dsc' apr_1.6.2-1.dsc 2316 SHA256:c7e14c7a36c02fc416586808637b6797f6e1c7a697abeda63db04989a101fcd2
'http://deb.debian.org/debian/pool/main/a/apr/apr_1.6.2.orig.tar.bz2' apr_1.6.2.orig.tar.bz2 853363 SHA256:09109cea377bab0028bba19a92b5b0e89603df9eab05c0f7dbd4dd83d48dcebd
'http://deb.debian.org/debian/pool/main/a/apr/apr_1.6.2.orig.tar.bz2.asc' apr_1.6.2.orig.tar.bz2.asc 801 SHA256:026e3086d6ebdd1fb5b0c82953447b4d1946fdf2a621d4e4a607be2f4131f27c
'http://deb.debian.org/debian/pool/main/a/apr/apr_1.6.2-1.debian.tar.xz' apr_1.6.2-1.debian.tar.xz 212900 SHA256:d1fdfd94fce25be17e6bb84ef6ef694db5b7bad4be964b39b0195c9926dd0510
```

Other potentially useful URLs:

- https://sources.debian.net/src/apr/1.6.2-1/ (for browsing the source)
- https://sources.debian.net/src/apr/1.6.2-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/apr/1.6.2-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `apt=1.5~rc1`

Binary Packages:

- `apt=1.5~rc1`
- `libapt-pkg5.0:amd64=1.5~rc1`

Licenses: (parsed from: `/usr/share/doc/apt/copyright`, `/usr/share/doc/libapt-pkg5.0/copyright`)

- `GPL-2`
- `GPLv2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/apt/1.5~rc1/


### `dpkg` source package: `atk1.0=2.24.0-1`

Binary Packages:

- `libatk1.0-0:amd64=2.24.0-1`
- `libatk1.0-data=2.24.0-1`

Licenses: (parsed from: `/usr/share/doc/libatk1.0-0/copyright`, `/usr/share/doc/libatk1.0-data/copyright`)

- `LGPL-2`

Source:

```console
$ apt-get source -qq --print-uris atk1.0=2.24.0-1
'http://deb.debian.org/debian/pool/main/a/atk1.0/atk1.0_2.24.0-1.dsc' atk1.0_2.24.0-1.dsc 2388 SHA256:7d5fbb5d174f29a7bb7ef0bc84f70ae8d37f016765cbe3113a71b56e3f7882cd
'http://deb.debian.org/debian/pool/main/a/atk1.0/atk1.0_2.24.0.orig.tar.xz' atk1.0_2.24.0.orig.tar.xz 748972 SHA256:bb2daa9a808c73a7a79d2983f333e0ba74be42fc51e3ba1faf2551a636487a49
'http://deb.debian.org/debian/pool/main/a/atk1.0/atk1.0_2.24.0-1.debian.tar.xz' atk1.0_2.24.0-1.debian.tar.xz 10612 SHA256:8f424830b82b2995cd5b8b781502bc910376bbad4f6353e3134390cf62495d7d
```

Other potentially useful URLs:

- https://sources.debian.net/src/atk1.0/2.24.0-1/ (for browsing the source)
- https://sources.debian.net/src/atk1.0/2.24.0-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/atk1.0/2.24.0-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `attr=1:2.4.47-2`

Binary Packages:

- `libattr1:amd64=1:2.4.47-2+b2`

Licenses: (parsed from: `/usr/share/doc/libattr1/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris attr=1:2.4.47-2
'http://deb.debian.org/debian/pool/main/a/attr/attr_2.4.47-2.dsc' attr_2.4.47-2.dsc 2027 SHA256:ee842d6d62d473acf02b494c432cf33128fa46455a09d3172c77c252449fa1a6
'http://deb.debian.org/debian/pool/main/a/attr/attr_2.4.47.orig.tar.bz2' attr_2.4.47.orig.tar.bz2 281877 SHA256:6c1208035757f5ce9b516402dd45b8299a53ae4d69ad2c352116f9cb8d7bc274
'http://deb.debian.org/debian/pool/main/a/attr/attr_2.4.47-2.debian.tar.xz' attr_2.4.47-2.debian.tar.xz 8096 SHA256:f65909562def601b1556393f5656032c058dc574ba622414ad3eb80c7b05a42a
```

Other potentially useful URLs:

- https://sources.debian.net/src/attr/1:2.4.47-2/ (for browsing the source)
- https://sources.debian.net/src/attr/1:2.4.47-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/attr/1:2.4.47-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `audit=1:2.7.7-1`

Binary Packages:

- `libaudit-common=1:2.7.7-1`
- `libaudit1:amd64=1:2.7.7-1+b2`

Licenses: (parsed from: `/usr/share/doc/libaudit-common/copyright`, `/usr/share/doc/libaudit1/copyright`)

- `GPL-1`
- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris audit=1:2.7.7-1
'http://deb.debian.org/debian/pool/main/a/audit/audit_2.7.7-1.dsc' audit_2.7.7-1.dsc 2485 SHA256:aa5701159bdbefdf93d536042449d53430e2f3455a1d68842a44446c156c151b
'http://deb.debian.org/debian/pool/main/a/audit/audit_2.7.7.orig.tar.gz' audit_2.7.7.orig.tar.gz 1110512 SHA256:98e22549444c313187dc98c2e137f36a9882efa0874b559b0457e5f87ae178ef
'http://deb.debian.org/debian/pool/main/a/audit/audit_2.7.7-1.debian.tar.xz' audit_2.7.7-1.debian.tar.xz 18684 SHA256:18056454f7252209b1d53063173952fa0c023e2ce5d96b197b137d3031cf9b36
```

Other potentially useful URLs:

- https://sources.debian.net/src/audit/1:2.7.7-1/ (for browsing the source)
- https://sources.debian.net/src/audit/1:2.7.7-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/audit/1:2.7.7-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `autoconf=2.69-11`

Binary Packages:

- `autoconf=2.69-11`

Licenses: (parsed from: `/usr/share/doc/autoconf/copyright`)

- `GFDL-1.3`
- `GFDL-1.3+`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with Autoconf exception`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with Autoconf exception`
- `GPL-3+ with Texinfo exception`
- `MIT-X-Consortium`
- `no-modification`
- `other`
- `permissive`
- `permissive-long-disclaimer`
- `permissive-short-disclaimer`
- `permissive-without-disclaimer`
- `permissive-without-notices-or-disclaimer`

Source:

```console
$ apt-get source -qq --print-uris autoconf=2.69-11
'http://deb.debian.org/debian/pool/main/a/autoconf/autoconf_2.69-11.dsc' autoconf_2.69-11.dsc 1948 SHA256:249d25370d4f4d1d0cf7b37bfd178bb6fa87011566dd82230991f64814a39dde
'http://deb.debian.org/debian/pool/main/a/autoconf/autoconf_2.69.orig.tar.xz' autoconf_2.69.orig.tar.xz 1214744 SHA256:64ebcec9f8ac5b2487125a86a7760d2591ac9e1d3dbd59489633f9de62a57684
'http://deb.debian.org/debian/pool/main/a/autoconf/autoconf_2.69-11.debian.tar.xz' autoconf_2.69-11.debian.tar.xz 23540 SHA256:885b3947fdead5b737f6437b80a90a41c5d611791573c5d0cfef50a59c943c1b
```

Other potentially useful URLs:

- https://sources.debian.net/src/autoconf/2.69-11/ (for browsing the source)
- https://sources.debian.net/src/autoconf/2.69-11/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/autoconf/2.69-11/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `automake-1.15=1:1.15.1-2.1`

Binary Packages:

- `automake=1:1.15.1-2.1`

Licenses: (parsed from: `/usr/share/doc/automake/copyright`)

- `GFDL-1.3`
- `GFDL-NIV-1.3+`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `permissive`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/automake-1.15/1:1.15.1-2.1/


### `dpkg` source package: `autotools-dev=20161112.1`

Binary Packages:

- `autotools-dev=20161112.1`

Licenses: (parsed from: `/usr/share/doc/autotools-dev/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris autotools-dev=20161112.1
'http://deb.debian.org/debian/pool/main/a/autotools-dev/autotools-dev_20161112.1.dsc' autotools-dev_20161112.1.dsc 1641 SHA256:2d55f69103b6d15043541c396ac3abd4e0d1b1d2c13a4d137f3fea277fccb21c
'http://deb.debian.org/debian/pool/main/a/autotools-dev/autotools-dev_20161112.1.tar.xz' autotools-dev_20161112.1.tar.xz 65304 SHA256:7c9405da28bbb4fc1d6d6ab9229920760b9120e5619c57cebfe594a555fd9894
```

Other potentially useful URLs:

- https://sources.debian.net/src/autotools-dev/20161112.1/ (for browsing the source)
- https://sources.debian.net/src/autotools-dev/20161112.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/autotools-dev/20161112.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `avahi=0.6.32-2`

Binary Packages:

- `libavahi-client3:amd64=0.6.32-2`
- `libavahi-common-data:amd64=0.6.32-2`
- `libavahi-common3:amd64=0.6.32-2`

Licenses: (parsed from: `/usr/share/doc/libavahi-client3/copyright`, `/usr/share/doc/libavahi-common-data/copyright`, `/usr/share/doc/libavahi-common3/copyright`)

- `GPL`
- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris avahi=0.6.32-2
'http://deb.debian.org/debian/pool/main/a/avahi/avahi_0.6.32-2.dsc' avahi_0.6.32-2.dsc 4263 SHA256:d369e30da54617a519796af49dcb4daa7e12f85314a4653c6504ec5567aab502
'http://deb.debian.org/debian/pool/main/a/avahi/avahi_0.6.32.orig.tar.gz' avahi_0.6.32.orig.tar.gz 1297169 SHA256:d54991185d514a0aba54ebeb408d7575b60f5818a772e28fa0e18b98bc1db454
'http://deb.debian.org/debian/pool/main/a/avahi/avahi_0.6.32-2.debian.tar.xz' avahi_0.6.32-2.debian.tar.xz 29348 SHA256:59434a4796ebc34f4b0fa92e8ca57b4c6c54adc1d2167db0dae3445aeac3318a
```

Other potentially useful URLs:

- https://sources.debian.net/src/avahi/0.6.32-2/ (for browsing the source)
- https://sources.debian.net/src/avahi/0.6.32-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/avahi/0.6.32-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `base-files=10`

Binary Packages:

- `base-files=10`

Licenses: (parsed from: `/usr/share/doc/base-files/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris base-files=10
'http://deb.debian.org/debian/pool/main/b/base-files/base-files_10.dsc' base-files_10.dsc 1063 SHA256:9e0e1f9fa67c55c552e053c340327f2d6c366b882fab74197170b03caefac488
'http://deb.debian.org/debian/pool/main/b/base-files/base-files_10.tar.xz' base-files_10.tar.xz 62872 SHA256:11a1f87511c26be242ad549b6d1262aed9c6a7eb2dd3a005d2e49bf41c445b83
```

Other potentially useful URLs:

- https://sources.debian.net/src/base-files/10/ (for browsing the source)
- https://sources.debian.net/src/base-files/10/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/base-files/10/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `base-passwd=3.5.43`

Binary Packages:

- `base-passwd=3.5.43`

Licenses: (parsed from: `/usr/share/doc/base-passwd/copyright`)

- `GPL-2`
- `PD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/base-passwd/3.5.43/


### `dpkg` source package: `bash=4.4-5`

Binary Packages:

- `bash=4.4-5`

Licenses: (parsed from: `/usr/share/doc/bash/copyright`)

- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris bash=4.4-5
'http://deb.debian.org/debian/pool/main/b/bash/bash_4.4-5.dsc' bash_4.4-5.dsc 2251 SHA256:1605c608c48f3d866e23a3d6989d23c1d910d58b2a64eee13ad0efd2d98d4b06
'http://deb.debian.org/debian/pool/main/b/bash/bash_4.4.orig.tar.xz' bash_4.4.orig.tar.xz 4878580 SHA256:819ebb6a23799e9e4ca56ac579778c46902005bd5ade4f131ed293d9f77108e7
'http://deb.debian.org/debian/pool/main/b/bash/bash_4.4-5.debian.tar.xz' bash_4.4-5.debian.tar.xz 65640 SHA256:e01cc0f49941d81bee4e81f3eeefede280a91ad9365947234f29f1cb783f9dd8
```

Other potentially useful URLs:

- https://sources.debian.net/src/bash/4.4-5/ (for browsing the source)
- https://sources.debian.net/src/bash/4.4-5/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/bash/4.4-5/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `binutils=2.29-9`

Binary Packages:

- `binutils=2.29-9`
- `binutils-common:amd64=2.29-9`
- `binutils-x86-64-linux-gnu=2.29-9`
- `libbinutils:amd64=2.29-9`

Licenses: (parsed from: `/usr/share/doc/binutils/copyright`, `/usr/share/doc/binutils-common/copyright`, `/usr/share/doc/binutils-x86-64-linux-gnu/copyright`, `/usr/share/doc/libbinutils/copyright`)

- `GFDL`
- `GPL`
- `LGPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/binutils/2.29-9/


### `dpkg` source package: `bzip2=1.0.6-8.1`

Binary Packages:

- `bzip2=1.0.6-8.1`
- `libbz2-1.0:amd64=1.0.6-8.1`
- `libbz2-dev:amd64=1.0.6-8.1`

Licenses: (parsed from: `/usr/share/doc/bzip2/copyright`, `/usr/share/doc/libbz2-1.0/copyright`, `/usr/share/doc/libbz2-dev/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris bzip2=1.0.6-8.1
'http://deb.debian.org/debian/pool/main/b/bzip2/bzip2_1.0.6-8.1.dsc' bzip2_1.0.6-8.1.dsc 2082 SHA256:d80deed11a1419ad090cb486dd2335850fd8719b809c32002dea04b485f55dbd
'http://deb.debian.org/debian/pool/main/b/bzip2/bzip2_1.0.6.orig.tar.bz2' bzip2_1.0.6.orig.tar.bz2 708737 SHA256:d70a9ccd8bdf47e302d96c69fecd54925f45d9c7b966bb4ef5f56b770960afa7
'http://deb.debian.org/debian/pool/main/b/bzip2/bzip2_1.0.6-8.1.debian.tar.bz2' bzip2_1.0.6-8.1.debian.tar.bz2 59875 SHA256:bdbe7bf29e014e44d79bb7c733fe63cae990ab50882a4a07867cf69c61ad72b7
```

Other potentially useful URLs:

- https://sources.debian.net/src/bzip2/1.0.6-8.1/ (for browsing the source)
- https://sources.debian.net/src/bzip2/1.0.6-8.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/bzip2/1.0.6-8.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `ca-certificates=20170717`

Binary Packages:

- `ca-certificates=20170717`

Licenses: (parsed from: `/usr/share/doc/ca-certificates/copyright`)

- `GPL-2`
- `GPL-2+`
- `MPL-2.0`

Source:

```console
$ apt-get source -qq --print-uris ca-certificates=20170717
'http://deb.debian.org/debian/pool/main/c/ca-certificates/ca-certificates_20170717.dsc' ca-certificates_20170717.dsc 1506 SHA256:da6268ff88e05c85c23c62add13d3d127087467d0c7e83974ca28db5543a252a
'http://deb.debian.org/debian/pool/main/c/ca-certificates/ca-certificates_20170717.tar.xz' ca-certificates_20170717.tar.xz 293028 SHA256:e487639b641fa75445174734dd6e9d600373e3248b3d86a7e3c6d0f6977decd2
```

Other potentially useful URLs:

- https://sources.debian.net/src/ca-certificates/20170717/ (for browsing the source)
- https://sources.debian.net/src/ca-certificates/20170717/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/ca-certificates/20170717/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `cairo=1.14.10-1`

Binary Packages:

- `libcairo-gobject2:amd64=1.14.10-1`
- `libcairo-script-interpreter2:amd64=1.14.10-1`
- `libcairo2:amd64=1.14.10-1`
- `libcairo2-dev=1.14.10-1`

Licenses: (parsed from: `/usr/share/doc/libcairo-gobject2/copyright`, `/usr/share/doc/libcairo-script-interpreter2/copyright`, `/usr/share/doc/libcairo2/copyright`, `/usr/share/doc/libcairo2-dev/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris cairo=1.14.10-1
'http://deb.debian.org/debian/pool/main/c/cairo/cairo_1.14.10-1.dsc' cairo_1.14.10-1.dsc 2911 SHA256:cbf4833e1f08f98c9a83b2b8bab35122eaab79e86bb555022675e03dabff7ba0
'http://deb.debian.org/debian/pool/main/c/cairo/cairo_1.14.10.orig.tar.xz' cairo_1.14.10.orig.tar.xz 36251788 SHA256:7e87878658f2c9951a14fc64114d4958c0e65ac47530b8ac3078b2ce41b66a09
'http://deb.debian.org/debian/pool/main/c/cairo/cairo_1.14.10-1.debian.tar.xz' cairo_1.14.10-1.debian.tar.xz 28916 SHA256:5376d16fdfd80f65e9a1ac1d7e5614a22665bd8b0674c12d806f62a1e26f666c
```

Other potentially useful URLs:

- https://sources.debian.net/src/cairo/1.14.10-1/ (for browsing the source)
- https://sources.debian.net/src/cairo/1.14.10-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/cairo/1.14.10-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `cdebconf=0.229`

Binary Packages:

- `libdebconfclient0:amd64=0.229`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris cdebconf=0.229
'http://deb.debian.org/debian/pool/main/c/cdebconf/cdebconf_0.229.dsc' cdebconf_0.229.dsc 2662 SHA256:05f558cb0f75dd7bfece8c7ea83fc7f8736feca255577b307a1eb99f1ef969db
'http://deb.debian.org/debian/pool/main/c/cdebconf/cdebconf_0.229.tar.xz' cdebconf_0.229.tar.xz 274448 SHA256:79582d8b3231c8cc1a8daff4bc9168f3b222113221d98ebb064fcc45318e1949
```

Other potentially useful URLs:

- https://sources.debian.net/src/cdebconf/0.229/ (for browsing the source)
- https://sources.debian.net/src/cdebconf/0.229/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/cdebconf/0.229/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `coreutils=8.26-3`

Binary Packages:

- `coreutils=8.26-3`

Licenses: (parsed from: `/usr/share/doc/coreutils/copyright`)

- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris coreutils=8.26-3
'http://deb.debian.org/debian/pool/main/c/coreutils/coreutils_8.26-3.dsc' coreutils_8.26-3.dsc 1955 SHA256:f62ab642e46e02c470cc045316643de530a0be50446151a5e449ca12da6485c4
'http://deb.debian.org/debian/pool/main/c/coreutils/coreutils_8.26.orig.tar.xz' coreutils_8.26.orig.tar.xz 5810244 SHA256:155e94d748f8e2bc327c66e0cbebdb8d6ab265d2f37c3c928f7bf6c3beba9a8e
'http://deb.debian.org/debian/pool/main/c/coreutils/coreutils_8.26-3.debian.tar.xz' coreutils_8.26-3.debian.tar.xz 22392 SHA256:cef6a15eb95d9e7bc992bca95010bc5ea9e25e98d8f4f668a698eee534d14b93
```

Other potentially useful URLs:

- https://sources.debian.net/src/coreutils/8.26-3/ (for browsing the source)
- https://sources.debian.net/src/coreutils/8.26-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/coreutils/8.26-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `cups=2.2.4-6`

Binary Packages:

- `libcups2:amd64=2.2.4-6`

Licenses: (parsed from: `/usr/share/doc/libcups2/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2.0 with AOSDL exception`
- `LGPL-2`
- `LGPL-2.0 with AOSDL exception`
- `Zlib`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/cups/2.2.4-6/


### `dpkg` source package: `curl=7.55.1-1`

Binary Packages:

- `curl=7.55.1-1`
- `libcurl3:amd64=7.55.1-1`
- `libcurl3-gnutls:amd64=7.55.1-1`
- `libcurl4-openssl-dev:amd64=7.55.1-1`

Licenses: (parsed from: `/usr/share/doc/curl/copyright`, `/usr/share/doc/libcurl3/copyright`, `/usr/share/doc/libcurl3-gnutls/copyright`, `/usr/share/doc/libcurl4-openssl-dev/copyright`)

- `BSD-3-Clause`
- `BSD-4-Clause`
- `ISC`
- `curl`
- `other`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris curl=7.55.1-1
'http://deb.debian.org/debian/pool/main/c/curl/curl_7.55.1-1.dsc' curl_7.55.1-1.dsc 2712 SHA256:dc8890b7c70c5d376f8f65c5aa96627ebf768511228fc513496175a87215da6d
'http://deb.debian.org/debian/pool/main/c/curl/curl_7.55.1.orig.tar.gz' curl_7.55.1.orig.tar.gz 3736406 SHA256:09576ea5e66672648d83dce3af16d0cb294d4cba2b5d166ade39655c495f4a20
'http://deb.debian.org/debian/pool/main/c/curl/curl_7.55.1-1.debian.tar.xz' curl_7.55.1-1.debian.tar.xz 28136 SHA256:7c9d3959512e3149661552ecb169f0a79b16cfbb00079563c4e718f68543a831
```

Other potentially useful URLs:

- https://sources.debian.net/src/curl/7.55.1-1/ (for browsing the source)
- https://sources.debian.net/src/curl/7.55.1-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/curl/7.55.1-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `cyrus-sasl2=2.1.27~101-g0780600+dfsg-3`

Binary Packages:

- `libsasl2-2:amd64=2.1.27~101-g0780600+dfsg-3`
- `libsasl2-modules-db:amd64=2.1.27~101-g0780600+dfsg-3`

Licenses: (parsed from: `/usr/share/doc/libsasl2-2/copyright`, `/usr/share/doc/libsasl2-modules-db/copyright`)

- `BSD-4-clause`
- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris cyrus-sasl2=2.1.27~101-g0780600+dfsg-3
'http://deb.debian.org/debian/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.27~101-g0780600+dfsg-3.dsc' cyrus-sasl2_2.1.27~101-g0780600+dfsg-3.dsc 3176 SHA256:abc0b2b0e8757195689821a724037c2017f8d06d63d357e1663d679226ef71d4
'http://deb.debian.org/debian/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.27~101-g0780600+dfsg.orig.tar.xz' cyrus-sasl2_2.1.27~101-g0780600+dfsg.orig.tar.xz 1143888 SHA256:69f34971f768e7ee6a6b647ec2d16a5a72a854ecd4602b019d5f79ba61063fdc
'http://deb.debian.org/debian/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.27~101-g0780600+dfsg-3.debian.tar.xz' cyrus-sasl2_2.1.27~101-g0780600+dfsg-3.debian.tar.xz 94664 SHA256:5094c002044588381e417c112f0f85d33242651f2739783b4dbd673321e7a386
```

Other potentially useful URLs:

- https://sources.debian.net/src/cyrus-sasl2/2.1.27~101-g0780600+dfsg-3/ (for browsing the source)
- https://sources.debian.net/src/cyrus-sasl2/2.1.27~101-g0780600+dfsg-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/cyrus-sasl2/2.1.27~101-g0780600+dfsg-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `dash=0.5.8-2.5`

Binary Packages:

- `dash=0.5.8-2.5`

Licenses: (parsed from: `/usr/share/doc/dash/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris dash=0.5.8-2.5
'http://deb.debian.org/debian/pool/main/d/dash/dash_0.5.8-2.5.dsc' dash_0.5.8-2.5.dsc 1807 SHA256:42e77c37a5a4db1cc8274c3183d83e7173883cc611339815d92358562b74d066
'http://deb.debian.org/debian/pool/main/d/dash/dash_0.5.8.orig.tar.gz' dash_0.5.8.orig.tar.gz 223028 SHA256:c6db3a237747b02d20382a761397563d813b306c020ae28ce25a1c3915fac60f
'http://deb.debian.org/debian/pool/main/d/dash/dash_0.5.8-2.5.diff.gz' dash_0.5.8-2.5.diff.gz 44513 SHA256:53f55bbcb327b0e2dd687c44bf0610f5e304dd00733c81c101be46e0adf8ec89
```

Other potentially useful URLs:

- https://sources.debian.net/src/dash/0.5.8-2.5/ (for browsing the source)
- https://sources.debian.net/src/dash/0.5.8-2.5/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/dash/0.5.8-2.5/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `db-defaults=5.3.1`

Binary Packages:

- `libdb-dev:amd64=5.3.1`

Licenses: (parsed from: `/usr/share/doc/libdb-dev/copyright`)

- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris db-defaults=5.3.1
'http://deb.debian.org/debian/pool/main/d/db-defaults/db-defaults_5.3.1.dsc' db-defaults_5.3.1.dsc 2049 SHA256:4097a2745b51c6a380b917dfa5f10f468dc2ed76c9d93ce4b5bf1bf081e42d33
'http://deb.debian.org/debian/pool/main/d/db-defaults/db-defaults_5.3.1.tar.xz' db-defaults_5.3.1.tar.xz 2788 SHA256:c35e2a597b3539b3b8e12f0dd5ee72af18a88b680a5bfb29871813ce4b793d30
```

Other potentially useful URLs:

- https://sources.debian.net/src/db-defaults/5.3.1/ (for browsing the source)
- https://sources.debian.net/src/db-defaults/5.3.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/db-defaults/5.3.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `db5.3=5.3.28-13.1`

Binary Packages:

- `libdb5.3:amd64=5.3.28-13.1`
- `libdb5.3-dev=5.3.28-13.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris db5.3=5.3.28-13.1
'http://deb.debian.org/debian/pool/main/d/db5.3/db5.3_5.3.28-13.1.dsc' db5.3_5.3.28-13.1.dsc 3124 SHA256:8941edcad8e16fe6bc76ffcbe86dbdaadc654b5ed994654689cf5408602a84f3
'http://deb.debian.org/debian/pool/main/d/db5.3/db5.3_5.3.28.orig.tar.xz' db5.3_5.3.28.orig.tar.xz 24154920 SHA256:e1f85c8b6ebd0ed3ca72fa0ae97b65006f6d0bd0cd6f4ac24bed103cb5497bf5
'http://deb.debian.org/debian/pool/main/d/db5.3/db5.3_5.3.28-13.1.debian.tar.xz' db5.3_5.3.28-13.1.debian.tar.xz 28180 SHA256:9e04b9269be51de4e73536584addc61e19b29e34f769e263c180228064c72ec9
```

Other potentially useful URLs:

- https://sources.debian.net/src/db5.3/5.3.28-13.1/ (for browsing the source)
- https://sources.debian.net/src/db5.3/5.3.28-13.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/db5.3/5.3.28-13.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `dbus=1.11.16+really1.10.22-1`

Binary Packages:

- `libdbus-1-3:amd64=1.11.16+really1.10.22-1`

Licenses: (parsed from: `/usr/share/doc/libdbus-1-3/copyright`)

- `AFL-2.1`
- `AFL-2.1,`
- `BSD-3-clause`
- `BSD-3-clause-generic`
- `Expat`
- `GPL-2`
- `GPL-2+`
- `Tcl-BSDish`
- `g10-permissive`

Source:

```console
$ apt-get source -qq --print-uris dbus=1.11.16+really1.10.22-1
'http://deb.debian.org/debian/pool/main/d/dbus/dbus_1.11.16+really1.10.22-1.dsc' dbus_1.11.16+really1.10.22-1.dsc 3777 SHA256:bcd4f551cad7bde494f37fcbedeb58edc7dcb767a3835eaa759329a97d6dbef7
'http://deb.debian.org/debian/pool/main/d/dbus/dbus_1.11.16+really1.10.22.orig.tar.gz' dbus_1.11.16+really1.10.22.orig.tar.gz 1989350 SHA256:e2b1401e3eedc7b5c9a2034d31254c886e1fcbc7858006e0a1c59158fe4b7b97
'http://deb.debian.org/debian/pool/main/d/dbus/dbus_1.11.16+really1.10.22.orig.tar.gz.asc' dbus_1.11.16+really1.10.22.orig.tar.gz.asc 1666 SHA256:8373d4cb9b8e675f3b0cedce25a82dce35e35e16b349fd4db662badf452baca7
'http://deb.debian.org/debian/pool/main/d/dbus/dbus_1.11.16+really1.10.22-1.debian.tar.xz' dbus_1.11.16+really1.10.22-1.debian.tar.xz 60156 SHA256:555a4afa71c1707deb525f0fd5f04ae8cf9c8e5bb406b95d5ec4928a93e7300b
```

Other potentially useful URLs:

- https://sources.debian.net/src/dbus/1.11.16+really1.10.22-1/ (for browsing the source)
- https://sources.debian.net/src/dbus/1.11.16+really1.10.22-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/dbus/1.11.16+really1.10.22-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `debconf=1.5.63`

Binary Packages:

- `debconf=1.5.63`

Licenses: (parsed from: `/usr/share/doc/debconf/copyright`)

- `BSD-2-clause`

Source:

```console
$ apt-get source -qq --print-uris debconf=1.5.63
'http://deb.debian.org/debian/pool/main/d/debconf/debconf_1.5.63.dsc' debconf_1.5.63.dsc 1937 SHA256:532d624315a3a6c62f3cafe90f12e4a185309b40350643be4861b64afe736555
'http://deb.debian.org/debian/pool/main/d/debconf/debconf_1.5.63.tar.xz' debconf_1.5.63.tar.xz 571980 SHA256:e50033ced377f22162de2200f5a8a7854ab45bc89e6e9a7ffbfae7dd70265092
```

Other potentially useful URLs:

- https://sources.debian.net/src/debconf/1.5.63/ (for browsing the source)
- https://sources.debian.net/src/debconf/1.5.63/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/debconf/1.5.63/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `debian-archive-keyring=2017.6`

Binary Packages:

- `debian-archive-keyring=2017.6`

Licenses: (parsed from: `/usr/share/doc/debian-archive-keyring/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris debian-archive-keyring=2017.6
'http://deb.debian.org/debian/pool/main/d/debian-archive-keyring/debian-archive-keyring_2017.6.dsc' debian-archive-keyring_2017.6.dsc 1788 SHA256:366f7e854cc3686755e1988977fb276790beb581dd4bb2a0faac87a59ebef5b0
'http://deb.debian.org/debian/pool/main/d/debian-archive-keyring/debian-archive-keyring_2017.6.tar.xz' debian-archive-keyring_2017.6.tar.xz 79560 SHA256:d5b3a7ad4030324489fa783235d3c5cd98e47ecb24e23533cb419cc696d6f7be
```

Other potentially useful URLs:

- https://sources.debian.net/src/debian-archive-keyring/2017.6/ (for browsing the source)
- https://sources.debian.net/src/debian-archive-keyring/2017.6/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/debian-archive-keyring/2017.6/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `debianutils=4.8.2`

Binary Packages:

- `debianutils=4.8.2`

Licenses: (parsed from: `/usr/share/doc/debianutils/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris debianutils=4.8.2
'http://deb.debian.org/debian/pool/main/d/debianutils/debianutils_4.8.2.dsc' debianutils_4.8.2.dsc 1731 SHA256:175edfd4a94f20d34784b36c644cf8c23ee23686ebee6ad0c10c32b76e41c34f
'http://deb.debian.org/debian/pool/main/d/debianutils/debianutils_4.8.2.tar.xz' debianutils_4.8.2.tar.xz 155944 SHA256:4deb5f293fd3e43c5d4a625a30b18d0fb07662ff77f769e3272841cdb61e7c68
```

Other potentially useful URLs:

- https://sources.debian.net/src/debianutils/4.8.2/ (for browsing the source)
- https://sources.debian.net/src/debianutils/4.8.2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/debianutils/4.8.2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `dh-python=2.20170125`

Binary Packages:

- `dh-python=2.20170125`

Licenses: (parsed from: `/usr/share/doc/dh-python/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris dh-python=2.20170125
'http://deb.debian.org/debian/pool/main/d/dh-python/dh-python_2.20170125.dsc' dh-python_2.20170125.dsc 1908 SHA256:ef4f2951cea36ae4aac29126a1017505f98b595432fb5bdac0f21b4b4d72c1b4
'http://deb.debian.org/debian/pool/main/d/dh-python/dh-python_2.20170125.tar.xz' dh-python_2.20170125.tar.xz 91332 SHA256:2e09c162ee2442a03511b7ebe83896e1e3c1df79ce97a22d2f8a8b4cfec9f1e3
```

Other potentially useful URLs:

- https://sources.debian.net/src/dh-python/2.20170125/ (for browsing the source)
- https://sources.debian.net/src/dh-python/2.20170125/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/dh-python/2.20170125/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `diffutils=1:3.6-1`

Binary Packages:

- `diffutils=1:3.6-1`

Licenses: (parsed from: `/usr/share/doc/diffutils/copyright`)

- `GFDL`
- `GPL`

Source:

```console
$ apt-get source -qq --print-uris diffutils=1:3.6-1
'http://deb.debian.org/debian/pool/main/d/diffutils/diffutils_3.6-1.dsc' diffutils_3.6-1.dsc 1453 SHA256:26fe7690b45748dc92cee6af224192e78db2ac574e16ae0aeb8ed6a472c883cd
'http://deb.debian.org/debian/pool/main/d/diffutils/diffutils_3.6.orig.tar.xz' diffutils_3.6.orig.tar.xz 1398296 SHA256:d621e8bdd4b573918c8145f7ae61817d1be9deb4c8d2328a65cea8e11d783bd6
'http://deb.debian.org/debian/pool/main/d/diffutils/diffutils_3.6-1.debian.tar.xz' diffutils_3.6-1.debian.tar.xz 10808 SHA256:f6ab546a134bde18a87ca8e3c98919680e79d81a65a24801ae06ef69b33f24d8
```

Other potentially useful URLs:

- https://sources.debian.net/src/diffutils/1:3.6-1/ (for browsing the source)
- https://sources.debian.net/src/diffutils/1:3.6-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/diffutils/1:3.6-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `djvulibre=3.5.27.1-7`

Binary Packages:

- `libdjvulibre-dev:amd64=3.5.27.1-7`
- `libdjvulibre-text=3.5.27.1-7`
- `libdjvulibre21:amd64=3.5.27.1-7`

Licenses: (parsed from: `/usr/share/doc/libdjvulibre-dev/copyright`, `/usr/share/doc/libdjvulibre-text/copyright`, `/usr/share/doc/libdjvulibre21/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris djvulibre=3.5.27.1-7
'http://deb.debian.org/debian/pool/main/d/djvulibre/djvulibre_3.5.27.1-7.dsc' djvulibre_3.5.27.1-7.dsc 2457 SHA256:986b49acc545cb0ed23d28131fc3b500c7e20b59c7b5f1e72b6829162426743f
'http://deb.debian.org/debian/pool/main/d/djvulibre/djvulibre_3.5.27.1.orig.tar.gz' djvulibre_3.5.27.1.orig.tar.gz 3231662 SHA256:77f07de3f1039aa19eba2eb3170d9ce9a0918ba7b704a59cfaf08f42fcc52144
'http://deb.debian.org/debian/pool/main/d/djvulibre/djvulibre_3.5.27.1-7.debian.tar.xz' djvulibre_3.5.27.1-7.debian.tar.xz 54688 SHA256:a62829e71b4c8a4d2902c9cf9ca12816ad7d9541596b6042940791c42b551b9c
```

Other potentially useful URLs:

- https://sources.debian.net/src/djvulibre/3.5.27.1-7/ (for browsing the source)
- https://sources.debian.net/src/djvulibre/3.5.27.1-7/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/djvulibre/3.5.27.1-7/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `dpkg=1.18.24`

Binary Packages:

- `dpkg=1.18.24`
- `dpkg-dev=1.18.24`
- `libdpkg-perl=1.18.24`

Licenses: (parsed from: `/usr/share/doc/dpkg/copyright`, `/usr/share/doc/dpkg-dev/copyright`, `/usr/share/doc/libdpkg-perl/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`
- `public-domain-md5`
- `public-domain-s-s-d`

Source:

```console
$ apt-get source -qq --print-uris dpkg=1.18.24
'http://deb.debian.org/debian/pool/main/d/dpkg/dpkg_1.18.24.dsc' dpkg_1.18.24.dsc 2032 SHA256:9f1560a0d237ec570f98f8aacfd1cbdd372371cce40e4c7ee4a31315b0c40823
'http://deb.debian.org/debian/pool/main/d/dpkg/dpkg_1.18.24.tar.xz' dpkg_1.18.24.tar.xz 4530444 SHA256:d853081d3e06bfd46a227056e591f094e42e78fa8a5793b0093bad30b710d7b4
```

Other potentially useful URLs:

- https://sources.debian.net/src/dpkg/1.18.24/ (for browsing the source)
- https://sources.debian.net/src/dpkg/1.18.24/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/dpkg/1.18.24/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `e2fsprogs=1.43.6-1`

Binary Packages:

- `comerr-dev=2.1-1.43.6-1`
- `e2fslibs:amd64=1.43.6-1`
- `e2fsprogs=1.43.6-1`
- `libcomerr2:amd64=1.43.6-1`
- `libss2:amd64=1.43.6-1`

Licenses: (parsed from: `/usr/share/doc/comerr-dev/copyright`, `/usr/share/doc/e2fslibs/copyright`, `/usr/share/doc/e2fsprogs/copyright`, `/usr/share/doc/libcomerr2/copyright`, `/usr/share/doc/libss2/copyright`)

- `GPL-2`
- `LGPL-2`

Source:

```console
$ apt-get source -qq --print-uris e2fsprogs=1.43.6-1
'http://deb.debian.org/debian/pool/main/e/e2fsprogs/e2fsprogs_1.43.6-1.dsc' e2fsprogs_1.43.6-1.dsc 2305 SHA256:7397523f79b776a237fbc8ed124407d6fcf0c8b568b772b4d9dad5bec20cd705
'http://deb.debian.org/debian/pool/main/e/e2fsprogs/e2fsprogs_1.43.6.orig.tar.gz' e2fsprogs_1.43.6.orig.tar.gz 7478011 SHA256:60139d75802925b0c23d451da8e4fc84c5e7cf94626cc324b59295495c0fdc80
'http://deb.debian.org/debian/pool/main/e/e2fsprogs/e2fsprogs_1.43.6.orig.tar.gz.asc' e2fsprogs_1.43.6.orig.tar.gz.asc 488 SHA256:af46a31e5178dd86c324805552b6d003af4719932c3dc9d1b55ac99737e198fe
'http://deb.debian.org/debian/pool/main/e/e2fsprogs/e2fsprogs_1.43.6-1.debian.tar.xz' e2fsprogs_1.43.6-1.debian.tar.xz 75236 SHA256:b29924813f322aaac5b1026e3d9594d5af153b56a1eefb827d0d25cf85ac9e17
```

Other potentially useful URLs:

- https://sources.debian.net/src/e2fsprogs/1.43.6-1/ (for browsing the source)
- https://sources.debian.net/src/e2fsprogs/1.43.6-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/e2fsprogs/1.43.6-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `elfutils=0.168-1`

Binary Packages:

- `libelf1:amd64=0.168-1`

Licenses: (parsed from: `/usr/share/doc/libelf1/copyright`)

- `GPL-2`
- `GPL-3`
- `LGPL-`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/elfutils/0.168-1/


### `dpkg` source package: `expat=2.2.3-1`

Binary Packages:

- `libexpat1:amd64=2.2.3-1`
- `libexpat1-dev:amd64=2.2.3-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris expat=2.2.3-1
'http://deb.debian.org/debian/pool/main/e/expat/expat_2.2.3-1.dsc' expat_2.2.3-1.dsc 2284 SHA256:c5f2c77f5b69361a38fbf9b2b3044cf823b6243d1029ca9e5754da2bd08f936d
'http://deb.debian.org/debian/pool/main/e/expat/expat_2.2.3.orig.tar.bz2' expat_2.2.3.orig.tar.bz2 435593 SHA256:b31890fb02f85c002a67491923f89bda5028a880fd6c374f707193ad81aace5f
'http://deb.debian.org/debian/pool/main/e/expat/expat_2.2.3-1.debian.tar.xz' expat_2.2.3-1.debian.tar.xz 10640 SHA256:885dda6baf300f15ef2c75f225d10736236056c7a9bf9405d1d3d138fbb7c63e
```

Other potentially useful URLs:

- https://sources.debian.net/src/expat/2.2.3-1/ (for browsing the source)
- https://sources.debian.net/src/expat/2.2.3-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/expat/2.2.3-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `explorercanvas=0.r3-4`

Binary Packages:

- `libjs-excanvas=0.r3-4`

Licenses: (parsed from: `/usr/share/doc/libjs-excanvas/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris explorercanvas=0.r3-4
'http://deb.debian.org/debian/pool/main/e/explorercanvas/explorercanvas_0.r3-4.dsc' explorercanvas_0.r3-4.dsc 2000 SHA256:d168011ed1f110f82b5039a6b070167f1f262d2a35d7fa25a6b5462f73761637
'http://deb.debian.org/debian/pool/main/e/explorercanvas/explorercanvas_0.r3.orig.tar.gz' explorercanvas_0.r3.orig.tar.gz 50748 SHA256:687af8084781b8eb3451fc55c88f6dfddc2b84428d197daf2c4c33fd5c55fed8
'http://deb.debian.org/debian/pool/main/e/explorercanvas/explorercanvas_0.r3-4.debian.tar.xz' explorercanvas_0.r3-4.debian.tar.xz 2040 SHA256:afcaa3e229d9b423988fc30439aeee1599c9dac8ad94430309404f9cf9f0c11f
```

Other potentially useful URLs:

- https://sources.debian.net/src/explorercanvas/0.r3-4/ (for browsing the source)
- https://sources.debian.net/src/explorercanvas/0.r3-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/explorercanvas/0.r3-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `fftw3=3.3.6p2-2`

Binary Packages:

- `libfftw3-double3:amd64=3.3.6p2-2`

Licenses: (parsed from: `/usr/share/doc/libfftw3-double3/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris fftw3=3.3.6p2-2
'http://deb.debian.org/debian/pool/main/f/fftw3/fftw3_3.3.6p2-2.dsc' fftw3_3.3.6p2-2.dsc 3081 SHA256:ad08684ec0e6eb1b74b473c676c81826183b026936fe202e182ef3dae04e3720
'http://deb.debian.org/debian/pool/main/f/fftw3/fftw3_3.3.6p2.orig.tar.gz' fftw3_3.3.6p2.orig.tar.gz 4185261 SHA256:a5de35c5c824a78a058ca54278c706cdf3d4abba1c56b63531c2cb05f5d57da2
'http://deb.debian.org/debian/pool/main/f/fftw3/fftw3_3.3.6p2-2.debian.tar.xz' fftw3_3.3.6p2-2.debian.tar.xz 13584 SHA256:6027906dcd9ff00d1005a621ff2999f1ce926512a069b3f5bd4caf6a36a2cbc7
```

Other potentially useful URLs:

- https://sources.debian.net/src/fftw3/3.3.6p2-2/ (for browsing the source)
- https://sources.debian.net/src/fftw3/3.3.6p2-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/fftw3/3.3.6p2-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `file=1:5.32-1`

Binary Packages:

- `file=1:5.32-1`
- `libmagic-mgc=1:5.32-1`
- `libmagic1:amd64=1:5.32-1`

Licenses: (parsed from: `/usr/share/doc/file/copyright`, `/usr/share/doc/libmagic-mgc/copyright`, `/usr/share/doc/libmagic1/copyright`)

- `BSD-2-Clause-alike`
- `BSD-2-Clause-netbsd`
- `BSD-2-Clause-regents`
- `MIT-Old-Style-with-legal-disclaimer-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris file=1:5.32-1
'http://deb.debian.org/debian/pool/main/f/file/file_5.32-1.dsc' file_5.32-1.dsc 2124 SHA256:86d4ea1ff36d73c501c786e74641755a14a711d6a7159756ba484d4c0961d9b4
'http://deb.debian.org/debian/pool/main/f/file/file_5.32.orig.tar.xz' file_5.32.orig.tar.xz 584352 SHA256:07627dc16c9a5b64352b00f24afb8d328b9ecade82afe2e2fa55201d324fd360
'http://deb.debian.org/debian/pool/main/f/file/file_5.32-1.debian.tar.xz' file_5.32-1.debian.tar.xz 31948 SHA256:be112d3500f7ea6f3c12e7159e1c0624e175593b3609a9c242472a4e03221268
```

Other potentially useful URLs:

- https://sources.debian.net/src/file/1:5.32-1/ (for browsing the source)
- https://sources.debian.net/src/file/1:5.32-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/file/1:5.32-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `findutils=4.6.0+git+20170729-2`

Binary Packages:

- `findutils=4.6.0+git+20170729-2`

Licenses: (parsed from: `/usr/share/doc/findutils/copyright`)

- `GFDL-1.3`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris findutils=4.6.0+git+20170729-2
'http://deb.debian.org/debian/pool/main/f/findutils/findutils_4.6.0+git+20170729-2.dsc' findutils_4.6.0+git+20170729-2.dsc 2220 SHA256:c59d5c89d6d5e794fd27cd2399d52d033629ae22a7551c1029aa8a779acaab56
'http://deb.debian.org/debian/pool/main/f/findutils/findutils_4.6.0+git+20170729.orig.tar.xz' findutils_4.6.0+git+20170729.orig.tar.xz 1865076 SHA256:a8be399ed28bca5042313dcaa8e6b90550b8da0d6497311fcdb3823259b5d7ac
'http://deb.debian.org/debian/pool/main/f/findutils/findutils_4.6.0+git+20170729-2.debian.tar.xz' findutils_4.6.0+git+20170729-2.debian.tar.xz 25572 SHA256:aa6d4a9f31870313a807d455bbc98030659ae69985d2e6893619e3997d01f022
```

Other potentially useful URLs:

- https://sources.debian.net/src/findutils/4.6.0+git+20170729-2/ (for browsing the source)
- https://sources.debian.net/src/findutils/4.6.0+git+20170729-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/findutils/4.6.0+git+20170729-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `fontconfig=2.12.3-0.2`

Binary Packages:

- `fontconfig=2.12.3-0.2`
- `fontconfig-config=2.12.3-0.2`
- `libfontconfig1:amd64=2.12.3-0.2`
- `libfontconfig1-dev:amd64=2.12.3-0.2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris fontconfig=2.12.3-0.2
'http://deb.debian.org/debian/pool/main/f/fontconfig/fontconfig_2.12.3-0.2.dsc' fontconfig_2.12.3-0.2.dsc 1881 SHA256:888337c0285864ecb786bda45170f26592d68b5851206cd9cdd2caffc4ab4d3a
'http://deb.debian.org/debian/pool/main/f/fontconfig/fontconfig_2.12.3.orig.tar.bz2' fontconfig_2.12.3.orig.tar.bz2 1600509 SHA256:bd24bf6602731a11295c025909d918180e98385625182d3b999fd6f1ab34f8bd
'http://deb.debian.org/debian/pool/main/f/fontconfig/fontconfig_2.12.3-0.2.debian.tar.xz' fontconfig_2.12.3-0.2.debian.tar.xz 49376 SHA256:dedc410fa6efa87adb51ca2274915b7e1cb9b637172a1b87b4b06c16fc558294
```

Other potentially useful URLs:

- https://sources.debian.net/src/fontconfig/2.12.3-0.2/ (for browsing the source)
- https://sources.debian.net/src/fontconfig/2.12.3-0.2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/fontconfig/2.12.3-0.2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `fonts-dejavu=2.37-1`

Binary Packages:

- `fonts-dejavu-core=2.37-1`

Licenses: (parsed from: `/usr/share/doc/fonts-dejavu-core/copyright`)

- `GPL-2`
- `GPL-2+`
- `bitstream-vera`

Source:

```console
$ apt-get source -qq --print-uris fonts-dejavu=2.37-1
'http://deb.debian.org/debian/pool/main/f/fonts-dejavu/fonts-dejavu_2.37-1.dsc' fonts-dejavu_2.37-1.dsc 2575 SHA256:f35ff7b2c8dbfda6564c9dedf088ba06cc6d279fdd8e7cccbd1ae08ded1bb71c
'http://deb.debian.org/debian/pool/main/f/fonts-dejavu/fonts-dejavu_2.37.orig.tar.bz2' fonts-dejavu_2.37.orig.tar.bz2 12050109 SHA256:4b21c5203f792343d5e90ab1cb0cf07e99887218abe3d83cd9a98cea9085e799
'http://deb.debian.org/debian/pool/main/f/fonts-dejavu/fonts-dejavu_2.37-1.debian.tar.xz' fonts-dejavu_2.37-1.debian.tar.xz 10424 SHA256:5105cdbfc086f4a83ab6871eb39cc904bf02aa52762402b7cacf33d0938122f7
```

Other potentially useful URLs:

- https://sources.debian.net/src/fonts-dejavu/2.37-1/ (for browsing the source)
- https://sources.debian.net/src/fonts-dejavu/2.37-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/fonts-dejavu/2.37-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `freetype=2.8-0.2`

Binary Packages:

- `libfreetype6:amd64=2.8-0.2`
- `libfreetype6-dev=2.8-0.2`

Licenses: (parsed from: `/usr/share/doc/libfreetype6/copyright`, `/usr/share/doc/libfreetype6-dev/copyright`)

- `BSD-2-Clause`
- `BSD-3-Clause`
- `Catharon-OSL`
- `FTL`
- `GPL-2`
- `GPL-2+`
- `GZip`
- `OpenGroup-BSD-like`

Source:

```console
$ apt-get source -qq --print-uris freetype=2.8-0.2
'http://deb.debian.org/debian/pool/main/f/freetype/freetype_2.8-0.2.dsc' freetype_2.8-0.2.dsc 1802 SHA256:d43fec201f695524148e691e73c4dfc243ff57b3a238feb7b50148385e00441d
'http://deb.debian.org/debian/pool/main/f/freetype/freetype_2.8.orig.tar.gz' freetype_2.8.orig.tar.gz 4225710 SHA256:7ba438204ec4532cfa770faff63a90f0555369bb594c15014cc0fb5f0d52e3b4
'http://deb.debian.org/debian/pool/main/f/freetype/freetype_2.8-0.2.diff.gz' freetype_2.8-0.2.diff.gz 37779 SHA256:5060fb3ad83ddbec18334a80bcf6697468131d9ec2a03d3ab992e5b695b84352
```

Other potentially useful URLs:

- https://sources.debian.net/src/freetype/2.8-0.2/ (for browsing the source)
- https://sources.debian.net/src/freetype/2.8-0.2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/freetype/2.8-0.2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `gcc-5=5.4.1-12`

Binary Packages:

- `gcc-5-base:amd64=5.4.1-12`

Licenses: (parsed from: `/usr/share/doc/gcc-5-base/copyright`)

- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-2`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris gcc-5=5.4.1-12
'http://deb.debian.org/debian/pool/main/g/gcc-5/gcc-5_5.4.1-12.dsc' gcc-5_5.4.1-12.dsc 17620 SHA256:9f951701db83bda0507ec7a19d8117a3dd3208bf59e67e175dde8f989eb4f164
'http://deb.debian.org/debian/pool/main/g/gcc-5/gcc-5_5.4.1.orig.tar.gz' gcc-5_5.4.1.orig.tar.gz 76812822 SHA256:2a84447f34cd062066d38300ac8a1fb528eb301a504b48e1d017e547e5abfcdb
'http://deb.debian.org/debian/pool/main/g/gcc-5/gcc-5_5.4.1-12.diff.gz' gcc-5_5.4.1-12.diff.gz 3702556 SHA256:abe96ea51c14e09de258f3d8c21a312f1e6090b4f19ef04f0b9074e76473a7e6
```

Other potentially useful URLs:

- https://sources.debian.net/src/gcc-5/5.4.1-12/ (for browsing the source)
- https://sources.debian.net/src/gcc-5/5.4.1-12/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gcc-5/5.4.1-12/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `gcc-6=6.4.0-5`

Binary Packages:

- `gcc-6-base:amd64=6.4.0-5`

Licenses: (parsed from: `/usr/share/doc/gcc-6-base/copyright`)

- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-2`
- `GPL-3`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/gcc-6/6.4.0-5/


### `dpkg` source package: `gcc-7=7.2.0-4`

Binary Packages:

- `cpp-7=7.2.0-4`
- `g++-7=7.2.0-4`
- `gcc-7=7.2.0-4`
- `gcc-7-base:amd64=7.2.0-4`
- `libasan4:amd64=7.2.0-4`
- `libatomic1:amd64=7.2.0-4`
- `libcc1-0:amd64=7.2.0-4`
- `libcilkrts5:amd64=7.2.0-4`
- `libgcc-7-dev:amd64=7.2.0-4`
- `libgcc1:amd64=1:7.2.0-4`
- `libgomp1:amd64=7.2.0-4`
- `libitm1:amd64=7.2.0-4`
- `liblsan0:amd64=7.2.0-4`
- `libmpx2:amd64=7.2.0-4`
- `libquadmath0:amd64=7.2.0-4`
- `libstdc++-7-dev:amd64=7.2.0-4`
- `libstdc++6:amd64=7.2.0-4`
- `libtsan0:amd64=7.2.0-4`
- `libubsan0:amd64=7.2.0-4`

Licenses: (parsed from: `/usr/share/doc/cpp-7/copyright`, `/usr/share/doc/g++-7/copyright`, `/usr/share/doc/gcc-7/copyright`, `/usr/share/doc/gcc-7-base/copyright`, `/usr/share/doc/libasan4/copyright`, `/usr/share/doc/libatomic1/copyright`, `/usr/share/doc/libcc1-0/copyright`, `/usr/share/doc/libcilkrts5/copyright`, `/usr/share/doc/libgcc-7-dev/copyright`, `/usr/share/doc/libgcc1/copyright`, `/usr/share/doc/libgomp1/copyright`, `/usr/share/doc/libitm1/copyright`, `/usr/share/doc/liblsan0/copyright`, `/usr/share/doc/libmpx2/copyright`, `/usr/share/doc/libquadmath0/copyright`, `/usr/share/doc/libstdc++-7-dev/copyright`, `/usr/share/doc/libstdc++6/copyright`, `/usr/share/doc/libtsan0/copyright`, `/usr/share/doc/libubsan0/copyright`)

- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-2`
- `GPL-3`
- `LGPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/gcc-7/7.2.0-4/


### `dpkg` source package: `gcc-defaults=1.172`

Binary Packages:

- `cpp=4:7.1.0-2`
- `g++=4:7.1.0-2`
- `gcc=4:7.1.0-2`

Licenses: (parsed from: `/usr/share/doc/cpp/copyright`, `/usr/share/doc/g++/copyright`, `/usr/share/doc/gcc/copyright`)

- `GPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/gcc-defaults/1.172/


### `dpkg` source package: `gdbm=1.8.3-14`

Binary Packages:

- `libgdbm-dev:amd64=1.8.3-14`
- `libgdbm3:amd64=1.8.3-14`

Licenses: (parsed from: `/usr/share/doc/libgdbm-dev/copyright`, `/usr/share/doc/libgdbm3/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris gdbm=1.8.3-14
'http://deb.debian.org/debian/pool/main/g/gdbm/gdbm_1.8.3-14.dsc' gdbm_1.8.3-14.dsc 1841 SHA256:312d3d28e287d287ee66e8ae3f25769676b1680ec1adc8c0815b5e9808405b13
'http://deb.debian.org/debian/pool/main/g/gdbm/gdbm_1.8.3.orig.tar.bz2' gdbm_1.8.3.orig.tar.bz2 172796 SHA256:1d5995b6e9e6be4ff62c8126d019f184a083dd8e6f75f6c74b9fe023b5b9440e
'http://deb.debian.org/debian/pool/main/g/gdbm/gdbm_1.8.3-14.debian.tar.xz' gdbm_1.8.3-14.debian.tar.xz 15308 SHA256:1c0570dd53947ea5980111f51b67356d647c4f21c502443b02397041dde0bf31
```

Other potentially useful URLs:

- https://sources.debian.net/src/gdbm/1.8.3-14/ (for browsing the source)
- https://sources.debian.net/src/gdbm/1.8.3-14/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gdbm/1.8.3-14/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `gdk-pixbuf=2.36.5-4`

Binary Packages:

- `gir1.2-gdkpixbuf-2.0:amd64=2.36.5-4`
- `libgdk-pixbuf2.0-0:amd64=2.36.5-4`
- `libgdk-pixbuf2.0-common=2.36.5-4`
- `libgdk-pixbuf2.0-dev=2.36.5-4`

Licenses: (parsed from: `/usr/share/doc/gir1.2-gdkpixbuf-2.0/copyright`, `/usr/share/doc/libgdk-pixbuf2.0-0/copyright`, `/usr/share/doc/libgdk-pixbuf2.0-common/copyright`, `/usr/share/doc/libgdk-pixbuf2.0-dev/copyright`)

- `GPL-2`
- `LGPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/gdk-pixbuf/2.36.5-4/


### `dpkg` source package: `geoip=1.6.11-2`

Binary Packages:

- `geoip-bin=1.6.11-2`
- `libgeoip-dev=1.6.11-2`
- `libgeoip1:amd64=1.6.11-2`

Licenses: (parsed from: `/usr/share/doc/geoip-bin/copyright`, `/usr/share/doc/libgeoip-dev/copyright`, `/usr/share/doc/libgeoip1/copyright`)

- `ISC`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris geoip=1.6.11-2
'http://deb.debian.org/debian/pool/main/g/geoip/geoip_1.6.11-2.dsc' geoip_1.6.11-2.dsc 1859 SHA256:773d289b9856e669045dce915da275042300968cef5b9dd8d1f4e9b7b017c39d
'http://deb.debian.org/debian/pool/main/g/geoip/geoip_1.6.11.orig.tar.gz' geoip_1.6.11.orig.tar.gz 161934 SHA256:8859cb7c9cb63e77f4aedb40a4622024359b956b251aba46b255acbe190c34e0
'http://deb.debian.org/debian/pool/main/g/geoip/geoip_1.6.11-2.debian.tar.xz' geoip_1.6.11-2.debian.tar.xz 22248 SHA256:ffef6c4b1ce9f0f35bb5e7b3bf778d60b68aa2e25b1a1095edc5e9516e87c686
```

Other potentially useful URLs:

- https://sources.debian.net/src/geoip/1.6.11-2/ (for browsing the source)
- https://sources.debian.net/src/geoip/1.6.11-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/geoip/1.6.11-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `git=1:2.14.1-3`

Binary Packages:

- `git=1:2.14.1-3`
- `git-man=1:2.14.1-3`

Licenses: (parsed from: `/usr/share/doc/git/copyright`, `/usr/share/doc/git-man/copyright`)

- `Apache-2.0`
- `Artistic`
- `Artistic-1`
- `BSD-2-clause`
- `Boost`
- `EDL-1.0`
- `Expat`
- `GPL`
- `GPL-1+`
- `GPL-2`
- `GPL-2+`
- `ISC`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `dlmalloc`
- `mingw-runtime`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/git/1:2.14.1-3/


### `dpkg` source package: `glib2.0=2.54.0-1`

Binary Packages:

- `libglib2.0-0:amd64=2.54.0-1`
- `libglib2.0-bin=2.54.0-1`
- `libglib2.0-data=2.54.0-1`
- `libglib2.0-dev:amd64=2.54.0-1`
- `libglib2.0-dev-bin=2.54.0-1`

Licenses: (parsed from: `/usr/share/doc/libglib2.0-0/copyright`, `/usr/share/doc/libglib2.0-bin/copyright`, `/usr/share/doc/libglib2.0-data/copyright`, `/usr/share/doc/libglib2.0-dev/copyright`, `/usr/share/doc/libglib2.0-dev-bin/copyright`)

- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris glib2.0=2.54.0-1
'http://deb.debian.org/debian/pool/main/g/glib2.0/glib2.0_2.54.0-1.dsc' glib2.0_2.54.0-1.dsc 3265 SHA256:eb65d5ee4bfe43e92731f42c2bdeafd9609d7ec0d24a71c518ce1629507b293a
'http://deb.debian.org/debian/pool/main/g/glib2.0/glib2.0_2.54.0.orig.tar.xz' glib2.0_2.54.0.orig.tar.xz 7822508 SHA256:fe22998ff0394ec31e6e5511c379b74011bee61a4421bca7fcab223dfbe0fc6a
'http://deb.debian.org/debian/pool/main/g/glib2.0/glib2.0_2.54.0-1.debian.tar.xz' glib2.0_2.54.0-1.debian.tar.xz 71680 SHA256:de441a9ffe8255937b1429200ff2c5f533d3741e48f11dfb08c8ff0e154cf616
```

Other potentially useful URLs:

- https://sources.debian.net/src/glib2.0/2.54.0-1/ (for browsing the source)
- https://sources.debian.net/src/glib2.0/2.54.0-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/glib2.0/2.54.0-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `glibc=2.24-17`

Binary Packages:

- `libc-bin=2.24-17`
- `libc-dev-bin=2.24-17`
- `libc6:amd64=2.24-17`
- `libc6-dev:amd64=2.24-17`
- `multiarch-support=2.24-17`

Licenses: (parsed from: `/usr/share/doc/libc-bin/copyright`, `/usr/share/doc/libc-dev-bin/copyright`, `/usr/share/doc/libc6/copyright`, `/usr/share/doc/libc6-dev/copyright`, `/usr/share/doc/multiarch-support/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris glibc=2.24-17
'http://deb.debian.org/debian/pool/main/g/glibc/glibc_2.24-17.dsc' glibc_2.24-17.dsc 8226 SHA256:8f8db58051f431525439dae692242124befba9cfab64b406ec8964818ba46a43
'http://deb.debian.org/debian/pool/main/g/glibc/glibc_2.24.orig.tar.xz' glibc_2.24.orig.tar.xz 13921912 SHA256:ed71e8afd2b270f7947a2cea2457a31e1ca4fac08e2731d80edd7ec1730ec84f
'http://deb.debian.org/debian/pool/main/g/glibc/glibc_2.24-17.debian.tar.xz' glibc_2.24-17.debian.tar.xz 1036004 SHA256:a66991c3d29bb30e57ef8eaeb1732b3694689cb8d4eb999ccb018076a02c5940
```

Other potentially useful URLs:

- https://sources.debian.net/src/glibc/2.24-17/ (for browsing the source)
- https://sources.debian.net/src/glibc/2.24-17/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/glibc/2.24-17/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `gmp=2:6.1.2+dfsg-1`

Binary Packages:

- `libgmp10:amd64=2:6.1.2+dfsg-1`

Licenses: (parsed from: `/usr/share/doc/libgmp10/copyright`)

- `GPL`
- `GPL-2`
- `GPL-3`
- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris gmp=2:6.1.2+dfsg-1
'http://deb.debian.org/debian/pool/main/g/gmp/gmp_6.1.2+dfsg-1.dsc' gmp_6.1.2+dfsg-1.dsc 2183 SHA256:3a53f6c74c9b2465c1c61446aa9bdc6182fdec8b04075849d4cbf224a73b6fbe
'http://deb.debian.org/debian/pool/main/g/gmp/gmp_6.1.2+dfsg.orig.tar.xz' gmp_6.1.2+dfsg.orig.tar.xz 1804424 SHA256:18016f718f621e7641ddd4e57f8e140391c5183252e5998263ffff59198a65b7
'http://deb.debian.org/debian/pool/main/g/gmp/gmp_6.1.2+dfsg-1.debian.tar.xz' gmp_6.1.2+dfsg-1.debian.tar.xz 20652 SHA256:79e73f74197e7628b2f0c02edf01b6eea3716c13152044ed8e0e0ee4178394df
```

Other potentially useful URLs:

- https://sources.debian.net/src/gmp/2:6.1.2+dfsg-1/ (for browsing the source)
- https://sources.debian.net/src/gmp/2:6.1.2+dfsg-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gmp/2:6.1.2+dfsg-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `gnome-icon-theme=3.12.0-2`

Binary Packages:

- `gnome-icon-theme=3.12.0-2`

Licenses: (parsed from: `/usr/share/doc/gnome-icon-theme/copyright`)

- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris gnome-icon-theme=3.12.0-2
'http://deb.debian.org/debian/pool/main/g/gnome-icon-theme/gnome-icon-theme_3.12.0-2.dsc' gnome-icon-theme_3.12.0-2.dsc 1954 SHA256:2f86d5d7724a7728c482920fa5406c23f644b1d7b5769282989f0ce926dfc42a
'http://deb.debian.org/debian/pool/main/g/gnome-icon-theme/gnome-icon-theme_3.12.0.orig.tar.xz' gnome-icon-theme_3.12.0.orig.tar.xz 17742624 SHA256:359e720b9202d3aba8d477752c4cd11eced368182281d51ffd64c8572b4e503a
'http://deb.debian.org/debian/pool/main/g/gnome-icon-theme/gnome-icon-theme_3.12.0-2.debian.tar.xz' gnome-icon-theme_3.12.0-2.debian.tar.xz 17824 SHA256:a9e2504cb933329efe2604e46aa81f16099e9774fc37e56c34f854442bc44627
```

Other potentially useful URLs:

- https://sources.debian.net/src/gnome-icon-theme/3.12.0-2/ (for browsing the source)
- https://sources.debian.net/src/gnome-icon-theme/3.12.0-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gnome-icon-theme/3.12.0-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `gnupg2=2.2.0-3`

Binary Packages:

- `dirmngr=2.2.0-3`
- `gnupg=2.2.0-3`
- `gnupg-l10n=2.2.0-3`
- `gnupg-utils=2.2.0-3`
- `gnupg2=2.2.0-3`
- `gpg=2.2.0-3`
- `gpg-agent=2.2.0-3`
- `gpg-wks-client=2.2.0-3`
- `gpg-wks-server=2.2.0-3`
- `gpgconf=2.2.0-3`
- `gpgsm=2.2.0-3`
- `gpgv=2.2.0-3`

Licenses: (parsed from: `/usr/share/doc/dirmngr/copyright`, `/usr/share/doc/gnupg/copyright`, `/usr/share/doc/gnupg-l10n/copyright`, `/usr/share/doc/gnupg-utils/copyright`, `/usr/share/doc/gnupg2/copyright`, `/usr/share/doc/gpg/copyright`, `/usr/share/doc/gpg-agent/copyright`, `/usr/share/doc/gpg-wks-client/copyright`, `/usr/share/doc/gpg-wks-server/copyright`, `/usr/share/doc/gpgconf/copyright`, `/usr/share/doc/gpgsm/copyright`, `/usr/share/doc/gpgv/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `RFC-Reference`
- `TinySCHEME`
- `permissive`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/gnupg2/2.2.0-3/


### `dpkg` source package: `gnutls28=3.5.15-2`

Binary Packages:

- `libgnutls30:amd64=3.5.15-2`

Licenses: (parsed from: `/usr/share/doc/libgnutls30/copyright`)

- `CC0 license`
- `GFDL-1.3`
- `GPL`
- `GPL-3`
- `LGPL`
- `LGPL-3`
- `LGPL2.1`
- `The MIT License (MIT)`
- `The main library is licensed under GNU Lesser`

Source:

```console
$ apt-get source -qq --print-uris gnutls28=3.5.15-2
'http://deb.debian.org/debian/pool/main/g/gnutls28/gnutls28_3.5.15-2.dsc' gnutls28_3.5.15-2.dsc 3322 SHA256:16712db8bb067d802958d462274fcc87dcaece8ea4ab5a3d6fd182520fbc4272
'http://deb.debian.org/debian/pool/main/g/gnutls28/gnutls28_3.5.15.orig.tar.xz' gnutls28_3.5.15.orig.tar.xz 7238928 SHA256:046081108b8b1fe455a13a4c5a4eaa0368e185b678f1670fe09a11a2d7ecfad5
'http://deb.debian.org/debian/pool/main/g/gnutls28/gnutls28_3.5.15.orig.tar.xz.asc' gnutls28_3.5.15.orig.tar.xz.asc 310 SHA256:8e19becd65224aefc70a0ea15df7369ed9588f9d692cc5cd790a72b541a48de2
'http://deb.debian.org/debian/pool/main/g/gnutls28/gnutls28_3.5.15-2.debian.tar.xz' gnutls28_3.5.15-2.debian.tar.xz 100840 SHA256:b470739833727c0f4f58c14b598c4e3ad56384e4fbb271a10106418c9a44143e
```

Other potentially useful URLs:

- https://sources.debian.net/src/gnutls28/3.5.15-2/ (for browsing the source)
- https://sources.debian.net/src/gnutls28/3.5.15-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gnutls28/3.5.15-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `gobject-introspection=1.54.0-1`

Binary Packages:

- `gir1.2-freedesktop:amd64=1.54.0-1`
- `gir1.2-glib-2.0:amd64=1.54.0-1`
- `libgirepository-1.0-1:amd64=1.54.0-1`

Licenses: (parsed from: `/usr/share/doc/gir1.2-freedesktop/copyright`, `/usr/share/doc/gir1.2-glib-2.0/copyright`, `/usr/share/doc/libgirepository-1.0-1/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`
- `LGPL-2`
- `LGPL-2+`
- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/gobject-introspection/1.54.0-1/


### `dpkg` source package: `graphite2=1.3.10-2`

Binary Packages:

- `libgraphite2-3:amd64=1.3.10-2`

Licenses: (parsed from: `/usr/share/doc/libgraphite2-3/copyright`)

- `Artistic`
- `GPL`
- `GPL-1+`
- `GPL1+ | Artistic`
- `LGPL | other`
- `LGPL-2`
- `LGPL-2+`
- `MPL-1.1 | GPL-2 | LGPL-2.1`
- `other`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/graphite2/1.3.10-2/


### `dpkg` source package: `graphviz=2.38.0-17`

Binary Packages:

- `libcdt5=2.38.0-17+b2`
- `libcgraph6=2.38.0-17+b2`
- `libgraphviz-dev=2.38.0-17+b2`
- `libgvc6=2.38.0-17+b2`
- `libgvc6-plugins-gtk=2.38.0-17+b2`
- `libgvpr2=2.38.0-17+b2`
- `libpathplan4=2.38.0-17+b2`
- `libxdot4=2.38.0-17+b2`

Licenses: (parsed from: `/usr/share/doc/libcdt5/copyright`, `/usr/share/doc/libcgraph6/copyright`, `/usr/share/doc/libgraphviz-dev/copyright`, `/usr/share/doc/libgvc6/copyright`, `/usr/share/doc/libgvc6-plugins-gtk/copyright`, `/usr/share/doc/libgvpr2/copyright`, `/usr/share/doc/libpathplan4/copyright`, `/usr/share/doc/libxdot4/copyright`)

- `EPL-1.0`
- `MIT`
- `X/MIT`
- `zlib-style`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/graphviz/2.38.0-17/


### `dpkg` source package: `grep=3.1-2`

Binary Packages:

- `grep=3.1-2`

Licenses: (parsed from: `/usr/share/doc/grep/copyright`)

- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris grep=3.1-2
'http://deb.debian.org/debian/pool/main/g/grep/grep_3.1-2.dsc' grep_3.1-2.dsc 2046 SHA256:b75ef8eb1399a49274bafe972679680b7add1500a4ee82eedaa0372f8ed744a0
'http://deb.debian.org/debian/pool/main/g/grep/grep_3.1.orig.tar.xz' grep_3.1.orig.tar.xz 1370880 SHA256:db625c7ab3bb3ee757b3926a5cfa8d9e1c3991ad24707a83dde8a5ef2bf7a07e
'http://deb.debian.org/debian/pool/main/g/grep/grep_3.1-2.debian.tar.bz2' grep_3.1-2.debian.tar.bz2 110067 SHA256:f09ce7a3c860a5de8939ebceb5fcd85d00d1537ad9f998dae5f623d9bcfe4e40
```

Other potentially useful URLs:

- https://sources.debian.net/src/grep/3.1-2/ (for browsing the source)
- https://sources.debian.net/src/grep/3.1-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/grep/3.1-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `gtk+2.0=2.24.31-2`

Binary Packages:

- `libgtk2.0-0:amd64=2.24.31-2`
- `libgtk2.0-common=2.24.31-2`

Licenses: (parsed from: `/usr/share/doc/libgtk2.0-0/copyright`, `/usr/share/doc/libgtk2.0-common/copyright`)

- `LGPL-2`
- `other`

Source:

```console
$ apt-get source -qq --print-uris gtk+2.0=2.24.31-2
'http://deb.debian.org/debian/pool/main/g/gtk+2.0/gtk+2.0_2.24.31-2.dsc' gtk+2.0_2.24.31-2.dsc 3839 SHA256:1588a80a0f8ef6b1ddeb92c629fc9da1930e13e5bba5cb0f7bbbee335e161d09
'http://deb.debian.org/debian/pool/main/g/gtk+2.0/gtk+2.0_2.24.31.orig.tar.xz' gtk+2.0_2.24.31.orig.tar.xz 12805344 SHA256:68c1922732c7efc08df4656a5366dcc3afdc8791513400dac276009b40954658
'http://deb.debian.org/debian/pool/main/g/gtk+2.0/gtk+2.0_2.24.31-2.debian.tar.xz' gtk+2.0_2.24.31-2.debian.tar.xz 87400 SHA256:56f1296c0f6fc3c319abee130fbd6c776b502ee53d8c8709ea42cd0f98b9d130
```

Other potentially useful URLs:

- https://sources.debian.net/src/gtk+2.0/2.24.31-2/ (for browsing the source)
- https://sources.debian.net/src/gtk+2.0/2.24.31-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gtk+2.0/2.24.31-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `gtk+3.0=3.22.21-1`

Binary Packages:

- `gtk-update-icon-cache=3.22.21-1`

Licenses: (parsed from: `/usr/share/doc/gtk-update-icon-cache/copyright`)

- `Apache-2.0`
- `Expat`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `other`

Source:

```console
$ apt-get source -qq --print-uris gtk+3.0=3.22.21-1
'http://deb.debian.org/debian/pool/main/g/gtk+3.0/gtk+3.0_3.22.21-1.dsc' gtk+3.0_3.22.21-1.dsc 3873 SHA256:65f4cf466bfe210dd4233e10518182958901c5e21ead674dde8395357a5a0000
'http://deb.debian.org/debian/pool/main/g/gtk+3.0/gtk+3.0_3.22.21.orig.tar.xz' gtk+3.0_3.22.21.orig.tar.xz 18847580 SHA256:1bd3c1a85cfb4db112cabb5379abb05a1a94fe43052d309d573493fca00e6b87
'http://deb.debian.org/debian/pool/main/g/gtk+3.0/gtk+3.0_3.22.21-1.debian.tar.xz' gtk+3.0_3.22.21-1.debian.tar.xz 144484 SHA256:75e32d31d35d524618f672dd782f81d11ff347ad5596710ce3ec3812aefd764a
```

Other potentially useful URLs:

- https://sources.debian.net/src/gtk+3.0/3.22.21-1/ (for browsing the source)
- https://sources.debian.net/src/gtk+3.0/3.22.21-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gtk+3.0/3.22.21-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `gts=0.7.6+darcs121130-4`

Binary Packages:

- `libgts-0.7-5:amd64=0.7.6+darcs121130-4`

Licenses: (parsed from: `/usr/share/doc/libgts-0.7-5/copyright`)

- `LGPL-2`
- `LGPL-2+`

Source:

```console
$ apt-get source -qq --print-uris gts=0.7.6+darcs121130-4
'http://deb.debian.org/debian/pool/main/g/gts/gts_0.7.6+darcs121130-4.dsc' gts_0.7.6+darcs121130-4.dsc 2170 SHA256:3d7dbf72a2194891a485d03f8a002e8d149dc59a915a7bbf36b42c53408ef733
'http://deb.debian.org/debian/pool/main/g/gts/gts_0.7.6+darcs121130.orig.tar.gz' gts_0.7.6+darcs121130.orig.tar.gz 880569 SHA256:c23f72ab74bbf65599f8c0b599d6336fabe1ec2a09c19b70544eeefdc069b73b
'http://deb.debian.org/debian/pool/main/g/gts/gts_0.7.6+darcs121130-4.debian.tar.bz2' gts_0.7.6+darcs121130-4.debian.tar.bz2 13837 SHA256:1fcf9c79ca0b4fc3662de645ba4e65564ea974566a3ecd730e9908f1adc425cd
```

Other potentially useful URLs:

- https://sources.debian.net/src/gts/0.7.6+darcs121130-4/ (for browsing the source)
- https://sources.debian.net/src/gts/0.7.6+darcs121130-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gts/0.7.6+darcs121130-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `gzip=1.6-5`

Binary Packages:

- `gzip=1.6-5+b1`

Licenses: (parsed from: `/usr/share/doc/gzip/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris gzip=1.6-5
'http://deb.debian.org/debian/pool/main/g/gzip/gzip_1.6-5.dsc' gzip_1.6-5.dsc 1867 SHA256:922751ee5fc426d623e824c55f7822fa60f26f35b5389b37c8b15feff639608c
'http://deb.debian.org/debian/pool/main/g/gzip/gzip_1.6.orig.tar.gz' gzip_1.6.orig.tar.gz 1074924 SHA256:97eb83b763d9e5ad35f351fe5517e6b71521d7aac7acf3e3cacdb6b1496d8f7e
'http://deb.debian.org/debian/pool/main/g/gzip/gzip_1.6-5.debian.tar.xz' gzip_1.6-5.debian.tar.xz 14684 SHA256:ac5282c32083ff58fc01317ee402b687b3806555aa1d4e80a62bb0f2ad93167e
```

Other potentially useful URLs:

- https://sources.debian.net/src/gzip/1.6-5/ (for browsing the source)
- https://sources.debian.net/src/gzip/1.6-5/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gzip/1.6-5/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `harfbuzz=1.4.2-1`

Binary Packages:

- `libharfbuzz0b:amd64=1.4.2-1`

Licenses: (parsed from: `/usr/share/doc/libharfbuzz0b/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris harfbuzz=1.4.2-1
'http://deb.debian.org/debian/pool/main/h/harfbuzz/harfbuzz_1.4.2-1.dsc' harfbuzz_1.4.2-1.dsc 2655 SHA256:48379f7aee8abee1b869745e12607ba81b02a3adf23b100558804f881dc5c9f1
'http://deb.debian.org/debian/pool/main/h/harfbuzz/harfbuzz_1.4.2.orig.tar.bz2' harfbuzz_1.4.2.orig.tar.bz2 1446752 SHA256:8f234dcfab000fdec24d43674fffa2fdbdbd654eb176afbde30e8826339cb7b3
'http://deb.debian.org/debian/pool/main/h/harfbuzz/harfbuzz_1.4.2-1.debian.tar.xz' harfbuzz_1.4.2-1.debian.tar.xz 8436 SHA256:f72ed9a6392e66816264c4f04a7926ec747a2a7b8eaf7ed1faf0bdacc788cf51
```

Other potentially useful URLs:

- https://sources.debian.net/src/harfbuzz/1.4.2-1/ (for browsing the source)
- https://sources.debian.net/src/harfbuzz/1.4.2-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/harfbuzz/1.4.2-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `hicolor-icon-theme=0.17-1`

Binary Packages:

- `hicolor-icon-theme=0.17-1`

Licenses: (parsed from: `/usr/share/doc/hicolor-icon-theme/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris hicolor-icon-theme=0.17-1
'http://deb.debian.org/debian/pool/main/h/hicolor-icon-theme/hicolor-icon-theme_0.17-1.dsc' hicolor-icon-theme_0.17-1.dsc 1592 SHA256:c60867c2937f943439da5b567bf7344dbef4834ed5af85ead84c091a17f1312c
'http://deb.debian.org/debian/pool/main/h/hicolor-icon-theme/hicolor-icon-theme_0.17.orig.tar.xz' hicolor-icon-theme_0.17.orig.tar.xz 53016 SHA256:317484352271d18cbbcfac3868eab798d67fff1b8402e740baa6ff41d588a9d8
'http://deb.debian.org/debian/pool/main/h/hicolor-icon-theme/hicolor-icon-theme_0.17-1.debian.tar.xz' hicolor-icon-theme_0.17-1.debian.tar.xz 3408 SHA256:3318c99b4a7dda3bc7b6a912c951ce5366cc46773c41dddd2ea0599f47357c56
```

Other potentially useful URLs:

- https://sources.debian.net/src/hicolor-icon-theme/0.17-1/ (for browsing the source)
- https://sources.debian.net/src/hicolor-icon-theme/0.17-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/hicolor-icon-theme/0.17-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `hostname=3.18`

Binary Packages:

- `hostname=3.18+b1`

Licenses: (parsed from: `/usr/share/doc/hostname/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris hostname=3.18
'http://deb.debian.org/debian/pool/main/h/hostname/hostname_3.18.dsc' hostname_3.18.dsc 1446 SHA256:4d3d5c8ded08ffc2ebfb39817ba1994b5fc1966652b132ff3e16389b70af28d7
'http://deb.debian.org/debian/pool/main/h/hostname/hostname_3.18.tar.gz' hostname_3.18.tar.gz 13732 SHA256:5cc3ec120967b8f911e86b9561b53977bcc77191c84fe9c607177ccd09f8d207
```

Other potentially useful URLs:

- https://sources.debian.net/src/hostname/3.18/ (for browsing the source)
- https://sources.debian.net/src/hostname/3.18/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/hostname/3.18/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `icu=57.1-6`

Binary Packages:

- `icu-devtools=57.1-6`
- `libicu-dev=57.1-6`
- `libicu57:amd64=57.1-6`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris icu=57.1-6
'http://deb.debian.org/debian/pool/main/i/icu/icu_57.1-6.dsc' icu_57.1-6.dsc 2105 SHA256:6d3979c7e13e23d4de31e0ff3b83c34e4824e4982cfed9887b21ab6b6c272e6b
'http://deb.debian.org/debian/pool/main/i/icu/icu_57.1.orig.tar.gz' icu_57.1.orig.tar.gz 22360664 SHA256:ff8c67cb65949b1e7808f2359f2b80f722697048e90e7cfc382ec1fe229e9581
'http://deb.debian.org/debian/pool/main/i/icu/icu_57.1-6.debian.tar.xz' icu_57.1-6.debian.tar.xz 32768 SHA256:9c1239e6c395aa44880617a8f67f1f9936a9536ad0c85b8c0ceedf4c0bf40819
```

Other potentially useful URLs:

- https://sources.debian.net/src/icu/57.1-6/ (for browsing the source)
- https://sources.debian.net/src/icu/57.1-6/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/icu/57.1-6/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `ilmbase=2.2.0-12`

Binary Packages:

- `libilmbase-dev=2.2.0-12`
- `libilmbase12:amd64=2.2.0-12`

Licenses: (parsed from: `/usr/share/doc/libilmbase-dev/copyright`, `/usr/share/doc/libilmbase12/copyright`)

- `boost`
- `ilmbase`

Source:

```console
$ apt-get source -qq --print-uris ilmbase=2.2.0-12
'http://deb.debian.org/debian/pool/main/i/ilmbase/ilmbase_2.2.0-12.dsc' ilmbase_2.2.0-12.dsc 2240 SHA256:0c78cab5f253e016346c7c02b46a8b13c7394d9b0f74ac85d1f544674ceafa31
'http://deb.debian.org/debian/pool/main/i/ilmbase/ilmbase_2.2.0.orig.tar.gz' ilmbase_2.2.0.orig.tar.gz 525289 SHA256:ecf815b60695555c1fbc73679e84c7c9902f4e8faa6e8000d2f905b8b86cedc7
'http://deb.debian.org/debian/pool/main/i/ilmbase/ilmbase_2.2.0-12.debian.tar.xz' ilmbase_2.2.0-12.debian.tar.xz 10332 SHA256:0ff9997216660e6312bc52504a8feba1cb62b8eae789e8bb324a1cbc6f49f62c
```

Other potentially useful URLs:

- https://sources.debian.net/src/ilmbase/2.2.0-12/ (for browsing the source)
- https://sources.debian.net/src/ilmbase/2.2.0-12/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/ilmbase/2.2.0-12/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `imagemagick=8:6.9.7.4+dfsg-16`

Binary Packages:

- `imagemagick=8:6.9.7.4+dfsg-16`
- `imagemagick-6-common=8:6.9.7.4+dfsg-16`
- `imagemagick-6.q16=8:6.9.7.4+dfsg-16`
- `libmagickcore-6-arch-config:amd64=8:6.9.7.4+dfsg-16`
- `libmagickcore-6-headers=8:6.9.7.4+dfsg-16`
- `libmagickcore-6.q16-3:amd64=8:6.9.7.4+dfsg-16`
- `libmagickcore-6.q16-3-extra:amd64=8:6.9.7.4+dfsg-16`
- `libmagickcore-6.q16-dev:amd64=8:6.9.7.4+dfsg-16`
- `libmagickcore-dev=8:6.9.7.4+dfsg-16`
- `libmagickwand-6-headers=8:6.9.7.4+dfsg-16`
- `libmagickwand-6.q16-3:amd64=8:6.9.7.4+dfsg-16`
- `libmagickwand-6.q16-dev:amd64=8:6.9.7.4+dfsg-16`
- `libmagickwand-dev=8:6.9.7.4+dfsg-16`

Licenses: (parsed from: `/usr/share/doc/imagemagick/copyright`, `/usr/share/doc/imagemagick-6-common/copyright`, `/usr/share/doc/imagemagick-6.q16/copyright`, `/usr/share/doc/libmagickcore-6-arch-config/copyright`, `/usr/share/doc/libmagickcore-6-headers/copyright`, `/usr/share/doc/libmagickcore-6.q16-3/copyright`, `/usr/share/doc/libmagickcore-6.q16-3-extra/copyright`, `/usr/share/doc/libmagickcore-6.q16-dev/copyright`, `/usr/share/doc/libmagickcore-dev/copyright`, `/usr/share/doc/libmagickwand-6-headers/copyright`, `/usr/share/doc/libmagickwand-6.q16-3/copyright`, `/usr/share/doc/libmagickwand-6.q16-dev/copyright`, `/usr/share/doc/libmagickwand-dev/copyright`)

- `Artistic`
- `BSD-with-FSF-change-public-domain`
- `GNU-All-Permissive-License`
- `GPL-1`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL2+-with-Autoconf-Macros-exception`
- `GPL3+-with-Autoconf-Macros-exception`
- `GPL3+-with-Autoconf-Macros-exception-GNU`
- `ImageMagick`
- `ImageMagickLicensePartEZXML`
- `ImageMagickLicensePartFIG`
- `ImageMagickLicensePartGsview`
- `ImageMagickLicensePartOpenSSH`
- `ImageMagickPartGraphicsMagick`
- `ImageMagickPartlibjpeg`
- `ImageMagickPartlibsquish`
- `LGPL-3`
- `LGPL-3+`
- `Magick++`
- `Perllikelicence`
- `TatcherUlrichPublicDomain`

Source:

```console
$ apt-get source -qq --print-uris imagemagick=8:6.9.7.4+dfsg-16
'http://deb.debian.org/debian/pool/main/i/imagemagick/imagemagick_6.9.7.4+dfsg-16.dsc' imagemagick_6.9.7.4+dfsg-16.dsc 5137 SHA256:9f0ba413ed44e3e94e018194d740b1f07ec03a69e6e52b2089aff2732257025c
'http://deb.debian.org/debian/pool/main/i/imagemagick/imagemagick_6.9.7.4+dfsg.orig.tar.xz' imagemagick_6.9.7.4+dfsg.orig.tar.xz 8929800 SHA256:47fb2cdd26f5913318c4504f16ea363e04d1f400dda9ec52e461ab661d724026
'http://deb.debian.org/debian/pool/main/i/imagemagick/imagemagick_6.9.7.4+dfsg-16.debian.tar.xz' imagemagick_6.9.7.4+dfsg-16.debian.tar.xz 255120 SHA256:40c5f950416eb74487115ac21a4abd52277183b44b0b95254521c068bc4edbd2
```

Other potentially useful URLs:

- https://sources.debian.net/src/imagemagick/8:6.9.7.4+dfsg-16/ (for browsing the source)
- https://sources.debian.net/src/imagemagick/8:6.9.7.4+dfsg-16/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/imagemagick/8:6.9.7.4+dfsg-16/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `inetutils=2:1.9.4-2`

Binary Packages:

- `inetutils-ping=2:1.9.4-2+b1`

Licenses: (parsed from: `/usr/share/doc/inetutils-ping/copyright`)

- `BSD-3-clause`
- `GFDL-1.3`
- `GFDL-1.3+`
- `GPL-3`
- `GPL-3+`
- `MIT`
- `Wietse`

Source:

```console
$ apt-get source -qq --print-uris inetutils=2:1.9.4-2
'http://deb.debian.org/debian/pool/main/i/inetutils/inetutils_1.9.4-2.dsc' inetutils_1.9.4-2.dsc 2662 SHA256:bd38f1018bbb697b6e27235a804f742a7bcd5fffb736479e8084f5214ed45669
'http://deb.debian.org/debian/pool/main/i/inetutils/inetutils_1.9.4.orig.tar.xz' inetutils_1.9.4.orig.tar.xz 1364408 SHA256:849d96f136effdef69548a940e3e0ec0624fc0c81265296987986a0dd36ded37
'http://deb.debian.org/debian/pool/main/i/inetutils/inetutils_1.9.4-2.debian.tar.xz' inetutils_1.9.4-2.debian.tar.xz 77188 SHA256:1b67e9197c4205b36e7b05e07eedaf44f9b3971f03ab83b7fed279a692d93a98
```

Other potentially useful URLs:

- https://sources.debian.net/src/inetutils/2:1.9.4-2/ (for browsing the source)
- https://sources.debian.net/src/inetutils/2:1.9.4-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/inetutils/2:1.9.4-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `init-system-helpers=1.49`

Binary Packages:

- `init-system-helpers=1.49`

Licenses: (parsed from: `/usr/share/doc/init-system-helpers/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris init-system-helpers=1.49
'http://deb.debian.org/debian/pool/main/i/init-system-helpers/init-system-helpers_1.49.dsc' init-system-helpers_1.49.dsc 1945 SHA256:c051912f7585c7638efe621d4714f1daff25c4134b0b8806b8b67bfdf9b98a14
'http://deb.debian.org/debian/pool/main/i/init-system-helpers/init-system-helpers_1.49.tar.xz' init-system-helpers_1.49.tar.xz 42660 SHA256:845ed218f1cb54d5b10ea850620e5b6b3905fb248163f97ad4670a55100cedae
```

Other potentially useful URLs:

- https://sources.debian.net/src/init-system-helpers/1.49/ (for browsing the source)
- https://sources.debian.net/src/init-system-helpers/1.49/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/init-system-helpers/1.49/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `iproute2=4.9.0-1`

Binary Packages:

- `iproute2=4.9.0-1`

Licenses: (parsed from: `/usr/share/doc/iproute2/copyright`)

- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/iproute2/4.9.0-1/


### `dpkg` source package: `isl=0.18-1`

Binary Packages:

- `libisl15:amd64=0.18-1`

Licenses: (parsed from: `/usr/share/doc/libisl15/copyright`)

- `BSD-2-clause`
- `LGPL-2`
- `LGPL-2.1+`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris isl=0.18-1
'http://deb.debian.org/debian/pool/main/i/isl/isl_0.18-1.dsc' isl_0.18-1.dsc 1882 SHA256:aed8295d019805686fd795652d930b1440bc0ae3be4373332d97784645d7c583
'http://deb.debian.org/debian/pool/main/i/isl/isl_0.18.orig.tar.xz' isl_0.18.orig.tar.xz 1475708 SHA256:0f35051cc030b87c673ac1f187de40e386a1482a0cfdf2c552dd6031b307ddc4
'http://deb.debian.org/debian/pool/main/i/isl/isl_0.18-1.debian.tar.xz' isl_0.18-1.debian.tar.xz 21860 SHA256:eac951311a871bb6d7886c98068290f771aaf78616516855b472d2500b84f53c
```

Other potentially useful URLs:

- https://sources.debian.net/src/isl/0.18-1/ (for browsing the source)
- https://sources.debian.net/src/isl/0.18-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/isl/0.18-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `jbigkit=2.1-3.1`

Binary Packages:

- `libjbig-dev:amd64=2.1-3.1+b2`
- `libjbig0:amd64=2.1-3.1+b2`

Licenses: (parsed from: `/usr/share/doc/libjbig-dev/copyright`, `/usr/share/doc/libjbig0/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris jbigkit=2.1-3.1
'http://deb.debian.org/debian/pool/main/j/jbigkit/jbigkit_2.1-3.1.dsc' jbigkit_2.1-3.1.dsc 1299 SHA256:62c8812d508958c5d35f2b1579dc3052fb5bd8d2e77d023fad064c4b48c8c3f8
'http://deb.debian.org/debian/pool/main/j/jbigkit/jbigkit_2.1.orig.tar.gz' jbigkit_2.1.orig.tar.gz 438710 SHA256:de7106b6bfaf495d6865c7dd7ac6ca1381bd12e0d81405ea81e7f2167263d932
'http://deb.debian.org/debian/pool/main/j/jbigkit/jbigkit_2.1-3.1.debian.tar.xz' jbigkit_2.1-3.1.debian.tar.xz 7600 SHA256:ebc3c52deaf37d52baea54d648a713640dc262926abda7bf05cd08e7db5dd1ee
```

Other potentially useful URLs:

- https://sources.debian.net/src/jbigkit/2.1-3.1/ (for browsing the source)
- https://sources.debian.net/src/jbigkit/2.1-3.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/jbigkit/2.1-3.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `jquery=3.2.1-1`

Binary Packages:

- `libjs-jquery=3.2.1-1`

Licenses: (parsed from: `/usr/share/doc/libjs-jquery/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris jquery=3.2.1-1
'http://deb.debian.org/debian/pool/main/j/jquery/jquery_3.2.1-1.dsc' jquery_3.2.1-1.dsc 2066 SHA256:b529818a547bc3f1ca70743b75e4772199e1ef61f3cc67366de25cc4e112410a
'http://deb.debian.org/debian/pool/main/j/jquery/jquery_3.2.1.orig.tar.xz' jquery_3.2.1.orig.tar.xz 298688 SHA256:3b645c4dcea9b22ee7ed09c6f391a1b5d23f7556cf0ae8f3afd43002491a597d
'http://deb.debian.org/debian/pool/main/j/jquery/jquery_3.2.1-1.debian.tar.xz' jquery_3.2.1-1.debian.tar.xz 9068 SHA256:f4c84ab960c21ecd46aa694a5abc397e84178e7185e78a1f546d064ed65d9ab5
```

Other potentially useful URLs:

- https://sources.debian.net/src/jquery/3.2.1-1/ (for browsing the source)
- https://sources.debian.net/src/jquery/3.2.1-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/jquery/3.2.1-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `keyutils=1.5.9-9`

Binary Packages:

- `libkeyutils1:amd64=1.5.9-9`

Licenses: (parsed from: `/usr/share/doc/libkeyutils1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2`
- `LGPL-2+`

Source:

```console
$ apt-get source -qq --print-uris keyutils=1.5.9-9
'http://deb.debian.org/debian/pool/main/k/keyutils/keyutils_1.5.9-9.dsc' keyutils_1.5.9-9.dsc 2033 SHA256:5fe3b2578a7ec662b7f495b11b7d861c3ee68c9550d4dec20c10ff4f3b3ca3dd
'http://deb.debian.org/debian/pool/main/k/keyutils/keyutils_1.5.9.orig.tar.bz2' keyutils_1.5.9.orig.tar.bz2 74683 SHA256:4da2c5552c688b65ab14d4fd40fbdf720c8b396d8ece643e040cf6e707e083ae
'http://deb.debian.org/debian/pool/main/k/keyutils/keyutils_1.5.9-9.debian.tar.xz' keyutils_1.5.9-9.debian.tar.xz 17588 SHA256:2e9db3f51d902a4d8fa4bef3b914353f9f83ed53b9003f24b5fc44748f4d6d80
```

Other potentially useful URLs:

- https://sources.debian.net/src/keyutils/1.5.9-9/ (for browsing the source)
- https://sources.debian.net/src/keyutils/1.5.9-9/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/keyutils/1.5.9-9/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `krb5=1.15.1-2`

Binary Packages:

- `krb5-multidev=1.15.1-2`
- `libgssapi-krb5-2:amd64=1.15.1-2`
- `libgssrpc4:amd64=1.15.1-2`
- `libk5crypto3:amd64=1.15.1-2`
- `libkadm5clnt-mit11:amd64=1.15.1-2`
- `libkadm5srv-mit11:amd64=1.15.1-2`
- `libkdb5-8:amd64=1.15.1-2`
- `libkrb5-3:amd64=1.15.1-2`
- `libkrb5-dev=1.15.1-2`
- `libkrb5support0:amd64=1.15.1-2`

Licenses: (parsed from: `/usr/share/doc/krb5-multidev/copyright`, `/usr/share/doc/libgssapi-krb5-2/copyright`, `/usr/share/doc/libgssrpc4/copyright`, `/usr/share/doc/libk5crypto3/copyright`, `/usr/share/doc/libkadm5clnt-mit11/copyright`, `/usr/share/doc/libkadm5srv-mit11/copyright`, `/usr/share/doc/libkdb5-8/copyright`, `/usr/share/doc/libkrb5-3/copyright`, `/usr/share/doc/libkrb5-dev/copyright`, `/usr/share/doc/libkrb5support0/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris krb5=1.15.1-2
'http://deb.debian.org/debian/pool/main/k/krb5/krb5_1.15.1-2.dsc' krb5_1.15.1-2.dsc 3294 SHA256:717416ea51edbfd2555568631e700c15cce1244f730a97d317288ab0be20d43a
'http://deb.debian.org/debian/pool/main/k/krb5/krb5_1.15.1.orig.tar.gz' krb5_1.15.1.orig.tar.gz 9375538 SHA256:437c8831ddd5fde2a993fef425dedb48468109bb3d3261ef838295045a89eb45
'http://deb.debian.org/debian/pool/main/k/krb5/krb5_1.15.1-2.debian.tar.xz' krb5_1.15.1-2.debian.tar.xz 143404 SHA256:e44c17efbf26e5d2a3de7577a039085683efe21afb0da3eacc12c17dc01e9d1a
```

Other potentially useful URLs:

- https://sources.debian.net/src/krb5/1.15.1-2/ (for browsing the source)
- https://sources.debian.net/src/krb5/1.15.1-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/krb5/1.15.1-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `lcms2=2.8-4`

Binary Packages:

- `liblcms2-2:amd64=2.8-4`
- `liblcms2-dev:amd64=2.8-4`

Licenses: (parsed from: `/usr/share/doc/liblcms2-2/copyright`, `/usr/share/doc/liblcms2-dev/copyright`)

- `GPL-2`
- `GPL-2+`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris lcms2=2.8-4
'http://deb.debian.org/debian/pool/main/l/lcms2/lcms2_2.8-4.dsc' lcms2_2.8-4.dsc 1997 SHA256:3b92900948848eef62fa91b78f6b6661bd84eae6c49c224248c7c48a09b5f028
'http://deb.debian.org/debian/pool/main/l/lcms2/lcms2_2.8.orig.tar.gz' lcms2_2.8.orig.tar.gz 6687005 SHA256:66d02b229d2ea9474e62c2b6cd6720fde946155cd1d0d2bffdab829790a0fb22
'http://deb.debian.org/debian/pool/main/l/lcms2/lcms2_2.8-4.debian.tar.xz' lcms2_2.8-4.debian.tar.xz 11036 SHA256:50c0040fc92e1f2ca27740f608ae248acdd5b21a633f34cf2fe4d66f1d05c4b4
```

Other potentially useful URLs:

- https://sources.debian.net/src/lcms2/2.8-4/ (for browsing the source)
- https://sources.debian.net/src/lcms2/2.8-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/lcms2/2.8-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libassuan=2.4.3-3`

Binary Packages:

- `libassuan0:amd64=2.4.3-3`

Licenses: (parsed from: `/usr/share/doc/libassuan0/copyright`)

- `GAP`
- `GAP~FSF`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with libtool exception`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`

Source:

```console
$ apt-get source -qq --print-uris libassuan=2.4.3-3
'http://deb.debian.org/debian/pool/main/liba/libassuan/libassuan_2.4.3-3.dsc' libassuan_2.4.3-3.dsc 2234 SHA256:057a5a131e60fe96a88a0246a776c75632df07d13211eb58031b452a30a5910a
'http://deb.debian.org/debian/pool/main/liba/libassuan/libassuan_2.4.3.orig.tar.bz2' libassuan_2.4.3.orig.tar.bz2 559867 SHA256:22843a3bdb256f59be49842abf24da76700354293a066d82ade8134bb5aa2b71
'http://deb.debian.org/debian/pool/main/liba/libassuan/libassuan_2.4.3-3.debian.tar.xz' libassuan_2.4.3-3.debian.tar.xz 15040 SHA256:c3e98d63cb6cd3fe524292da3aa250c17fd09692eef81e13db826a54e7e4dd27
```

Other potentially useful URLs:

- https://sources.debian.net/src/libassuan/2.4.3-3/ (for browsing the source)
- https://sources.debian.net/src/libassuan/2.4.3-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libassuan/2.4.3-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libbsd=0.8.6-2`

Binary Packages:

- `libbsd0:amd64=0.8.6-2`

Licenses: (parsed from: `/usr/share/doc/libbsd0/copyright`)

- `BSD-2-clause`
- `BSD-2-clause-NetBSD`
- `BSD-2-clause-author`
- `BSD-2-clause-verbatim`
- `BSD-3-clause`
- `BSD-3-clause-John-Birrell`
- `BSD-3-clause-Peter-Wemm`
- `BSD-3-clause-Regents`
- `BSD-4-clause-Christopher-G-Demetriou`
- `BSD-4-clause-Niels-Provos`
- `BSD-5-clause-Peter-Wemm`
- `Beerware`
- `Expat`
- `ISC`
- `ISC-Original`
- `public-domain`
- `public-domain-Colin-Plumb`

Source:

```console
$ apt-get source -qq --print-uris libbsd=0.8.6-2
'http://deb.debian.org/debian/pool/main/libb/libbsd/libbsd_0.8.6-2.dsc' libbsd_0.8.6-2.dsc 2181 SHA256:8adbd1e8bd9e36248be2530eb2ceb4ed0ebd6d16ad108f9620483a1f9b6ed055
'http://deb.debian.org/debian/pool/main/libb/libbsd/libbsd_0.8.6.orig.tar.xz' libbsd_0.8.6.orig.tar.xz 371112 SHA256:467fbf9df1f49af11f7f686691057c8c0a7613ae5a870577bef9155de39f9687
'http://deb.debian.org/debian/pool/main/libb/libbsd/libbsd_0.8.6.orig.tar.xz.asc' libbsd_0.8.6.orig.tar.xz.asc 833 SHA256:8b579470e8249b2ad24134989cc77404e3620e8ccda3d57650cfbcc7c50c26ce
'http://deb.debian.org/debian/pool/main/libb/libbsd/libbsd_0.8.6-2.debian.tar.xz' libbsd_0.8.6-2.debian.tar.xz 15684 SHA256:3ba08d93c36002737c4707b2dfdc13118d302487a53f1789d8ee22ed7107c491
```

Other potentially useful URLs:

- https://sources.debian.net/src/libbsd/0.8.6-2/ (for browsing the source)
- https://sources.debian.net/src/libbsd/0.8.6-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libbsd/0.8.6-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libcap-ng=0.7.7-3`

Binary Packages:

- `libcap-ng0:amd64=0.7.7-3+b1`

Licenses: (parsed from: `/usr/share/doc/libcap-ng0/copyright`)

- `GPL-2`
- `GPL-3`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libcap-ng=0.7.7-3
'http://deb.debian.org/debian/pool/main/libc/libcap-ng/libcap-ng_0.7.7-3.dsc' libcap-ng_0.7.7-3.dsc 1722 SHA256:6f5262f0ed2792c135e9b6bf7d30461cc3015249832f381505d21b9217a67685
'http://deb.debian.org/debian/pool/main/libc/libcap-ng/libcap-ng_0.7.7.orig.tar.gz' libcap-ng_0.7.7.orig.tar.gz 420178 SHA256:615549ce39b333f6b78baee0c0b4ef18bc726c6bf1cca123dfd89dd963f6d06b
'http://deb.debian.org/debian/pool/main/libc/libcap-ng/libcap-ng_0.7.7-3.debian.tar.xz' libcap-ng_0.7.7-3.debian.tar.xz 5248 SHA256:b7a0846dbd0451903bcbbe3a2696341f4e6000ebd64bed259c7fbf9dfc818363
```

Other potentially useful URLs:

- https://sources.debian.net/src/libcap-ng/0.7.7-3/ (for browsing the source)
- https://sources.debian.net/src/libcap-ng/0.7.7-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libcap-ng/0.7.7-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libcroco=0.6.12-1`

Binary Packages:

- `libcroco3:amd64=0.6.12-1`

Licenses: (parsed from: `/usr/share/doc/libcroco3/copyright`)

- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris libcroco=0.6.12-1
'http://deb.debian.org/debian/pool/main/libc/libcroco/libcroco_0.6.12-1.dsc' libcroco_0.6.12-1.dsc 2289 SHA256:963f0f4235d7fa3ba79bb9675ec836bcb2430e6adb1072e0f66ba17a1ba06994
'http://deb.debian.org/debian/pool/main/libc/libcroco/libcroco_0.6.12.orig.tar.xz' libcroco_0.6.12.orig.tar.xz 482028 SHA256:ddc4b5546c9fb4280a5017e2707fbd4839034ed1aba5b7d4372212f34f84f860
'http://deb.debian.org/debian/pool/main/libc/libcroco/libcroco_0.6.12-1.debian.tar.xz' libcroco_0.6.12-1.debian.tar.xz 7988 SHA256:179700f1a51ebdb786e071d4f189e3725ac818a9105cfad896659a71c71751b0
```

Other potentially useful URLs:

- https://sources.debian.net/src/libcroco/0.6.12-1/ (for browsing the source)
- https://sources.debian.net/src/libcroco/0.6.12-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libcroco/0.6.12-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libdatrie=0.2.10-5`

Binary Packages:

- `libdatrie1:amd64=0.2.10-5`

Licenses: (parsed from: `/usr/share/doc/libdatrie1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libdatrie=0.2.10-5
'http://deb.debian.org/debian/pool/main/libd/libdatrie/libdatrie_0.2.10-5.dsc' libdatrie_0.2.10-5.dsc 2214 SHA256:b81e48b6393d1d7a69d149cfa152990c840d62241c76ed9ca5cb07c588f714eb
'http://deb.debian.org/debian/pool/main/libd/libdatrie/libdatrie_0.2.10.orig.tar.xz' libdatrie_0.2.10.orig.tar.xz 294380 SHA256:180eff7b0309ca19a02d5864e744185d715f021398a096fec6cf960f8ebfaa2b
'http://deb.debian.org/debian/pool/main/libd/libdatrie/libdatrie_0.2.10-5.debian.tar.xz' libdatrie_0.2.10-5.debian.tar.xz 7608 SHA256:24031d8a2c1003ba1895cc1179c4d30563d90555a39a3a4cdb4b1290d4a1a4bf
```

Other potentially useful URLs:

- https://sources.debian.net/src/libdatrie/0.2.10-5/ (for browsing the source)
- https://sources.debian.net/src/libdatrie/0.2.10-5/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libdatrie/0.2.10-5/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libedit=3.1-20170329-1`

Binary Packages:

- `libedit2:amd64=3.1-20170329-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libedit=3.1-20170329-1
'http://deb.debian.org/debian/pool/main/libe/libedit/libedit_3.1-20170329-1.dsc' libedit_3.1-20170329-1.dsc 2269 SHA256:1e657cfcfbbe5c550b844f17cfeb1d8591136fa57300e6cff2b56e5a3e25ad3f
'http://deb.debian.org/debian/pool/main/libe/libedit/libedit_3.1-20170329.orig.tar.gz' libedit_3.1-20170329.orig.tar.gz 508504 SHA256:91f2d90fbd2a048ff6dad7131d9a39e690fd8a8fd982a353f1333dd4017dd4be
'http://deb.debian.org/debian/pool/main/libe/libedit/libedit_3.1-20170329-1.debian.tar.bz2' libedit_3.1-20170329-1.debian.tar.bz2 11267 SHA256:7dd7a23b07b082d058b7fb741d3b750b80699472e7c8efd1935a9e7c59a49a39
```

Other potentially useful URLs:

- https://sources.debian.net/src/libedit/3.1-20170329-1/ (for browsing the source)
- https://sources.debian.net/src/libedit/3.1-20170329-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libedit/3.1-20170329-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `liberror-perl=0.17024-1`

Binary Packages:

- `liberror-perl=0.17024-1`

Licenses: (parsed from: `/usr/share/doc/liberror-perl/copyright`)

- `Artistic`
- `GPL-1`
- `GPL-1+`
- `MIT/X11`

Source:

```console
$ apt-get source -qq --print-uris liberror-perl=0.17024-1
'http://deb.debian.org/debian/pool/main/libe/liberror-perl/liberror-perl_0.17024-1.dsc' liberror-perl_0.17024-1.dsc 2193 SHA256:3d269abc34facfde4e4caf5d2eac38dbce07739d3fe2167ff982140af513d17e
'http://deb.debian.org/debian/pool/main/libe/liberror-perl/liberror-perl_0.17024.orig.tar.gz' liberror-perl_0.17024.orig.tar.gz 31269 SHA256:074db7c783a67b0667eca64a4f6a0c3de94998afc92c01d6453163eb04b9150d
'http://deb.debian.org/debian/pool/main/libe/liberror-perl/liberror-perl_0.17024-1.debian.tar.xz' liberror-perl_0.17024-1.debian.tar.xz 4028 SHA256:7b490f3655df007a1153883608161822036837eaf49f7d6014d3a096be4a65cb
```

Other potentially useful URLs:

- https://sources.debian.net/src/liberror-perl/0.17024-1/ (for browsing the source)
- https://sources.debian.net/src/liberror-perl/0.17024-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/liberror-perl/0.17024-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libevent=2.1.8-stable-4`

Binary Packages:

- `libevent-2.1-6:amd64=2.1.8-stable-4`
- `libevent-core-2.1-6:amd64=2.1.8-stable-4`
- `libevent-dev=2.1.8-stable-4`
- `libevent-extra-2.1-6:amd64=2.1.8-stable-4`
- `libevent-openssl-2.1-6:amd64=2.1.8-stable-4`
- `libevent-pthreads-2.1-6:amd64=2.1.8-stable-4`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libevent=2.1.8-stable-4
'http://deb.debian.org/debian/pool/main/libe/libevent/libevent_2.1.8-stable-4.dsc' libevent_2.1.8-stable-4.dsc 2328 SHA256:4d2c3f7943219dd13ae711c6d3e8589c6211d2cec15c18ccfd1d1426542519b0
'http://deb.debian.org/debian/pool/main/libe/libevent/libevent_2.1.8-stable.orig.tar.gz' libevent_2.1.8-stable.orig.tar.gz 1026485 SHA256:965cc5a8bb46ce4199a47e9b2c9e1cae3b137e8356ffdad6d94d3b9069b71dc2
'http://deb.debian.org/debian/pool/main/libe/libevent/libevent_2.1.8-stable-4.debian.tar.xz' libevent_2.1.8-stable-4.debian.tar.xz 12060 SHA256:c1334029455256b62e201ba333a8616a1709e0f3caada753d35376b88aca2d5e
```

Other potentially useful URLs:

- https://sources.debian.net/src/libevent/2.1.8-stable-4/ (for browsing the source)
- https://sources.debian.net/src/libevent/2.1.8-stable-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libevent/2.1.8-stable-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libexif=0.6.21-2`

Binary Packages:

- `libexif-dev=0.6.21-2+b2`
- `libexif12:amd64=0.6.21-2+b2`

Licenses: (parsed from: `/usr/share/doc/libexif-dev/copyright`, `/usr/share/doc/libexif12/copyright`)

- `BSD-2-Clause`
- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libexif=0.6.21-2
'http://deb.debian.org/debian/pool/main/libe/libexif/libexif_0.6.21-2.dsc' libexif_0.6.21-2.dsc 2053 SHA256:284942bcd7656949a383f2ee775babb20b50781c30d915b34fe272220f997ea6
'http://deb.debian.org/debian/pool/main/libe/libexif/libexif_0.6.21.orig.tar.gz' libexif_0.6.21.orig.tar.gz 2081615 SHA256:edb7eb13664cf950a6edd132b75e99afe61c5effe2f16494e6d27bc404b287bf
'http://deb.debian.org/debian/pool/main/libe/libexif/libexif_0.6.21-2.debian.tar.xz' libexif_0.6.21-2.debian.tar.xz 8628 SHA256:648796d86b17567fb13dd356fc18c4b164b5a598853964d15beb9a32ec1253d8
```

Other potentially useful URLs:

- https://sources.debian.net/src/libexif/0.6.21-2/ (for browsing the source)
- https://sources.debian.net/src/libexif/0.6.21-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libexif/0.6.21-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libffi=3.2.1-6`

Binary Packages:

- `libffi-dev:amd64=3.2.1-6`
- `libffi6:amd64=3.2.1-6`

Licenses: (parsed from: `/usr/share/doc/libffi-dev/copyright`, `/usr/share/doc/libffi6/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris libffi=3.2.1-6
'http://deb.debian.org/debian/pool/main/libf/libffi/libffi_3.2.1-6.dsc' libffi_3.2.1-6.dsc 1923 SHA256:f901298b078c7d7f3f75459b5ff74cc804f6f2cfd65ed619d2082d5f77089954
'http://deb.debian.org/debian/pool/main/libf/libffi/libffi_3.2.1.orig.tar.gz' libffi_3.2.1.orig.tar.gz 940837 SHA256:d06ebb8e1d9a22d19e38d63fdb83954253f39bedc5d46232a05645685722ca37
'http://deb.debian.org/debian/pool/main/libf/libffi/libffi_3.2.1-6.debian.tar.xz' libffi_3.2.1-6.debian.tar.xz 11252 SHA256:477709fa90f8c7631fa226a48cdf38737c9f195f3686f62aa76714bcffaee512
```

Other potentially useful URLs:

- https://sources.debian.net/src/libffi/3.2.1-6/ (for browsing the source)
- https://sources.debian.net/src/libffi/3.2.1-6/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libffi/3.2.1-6/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libgcrypt20=1.7.9-1`

Binary Packages:

- `libgcrypt20:amd64=1.7.9-1`

Licenses: (parsed from: `/usr/share/doc/libgcrypt20/copyright`)

- `GPL-2`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris libgcrypt20=1.7.9-1
'http://deb.debian.org/debian/pool/main/libg/libgcrypt20/libgcrypt20_1.7.9-1.dsc' libgcrypt20_1.7.9-1.dsc 2914 SHA256:d922d12b25a64cd25601b34380bed9c9ca3c8fd4c9625951641fcc8766c7796d
'http://deb.debian.org/debian/pool/main/libg/libgcrypt20/libgcrypt20_1.7.9.orig.tar.bz2' libgcrypt20_1.7.9.orig.tar.bz2 2897137 SHA256:bfe9bb703c1126c3647da2810fd23039c2f09d46969f71612c2065dc3fa9373b
'http://deb.debian.org/debian/pool/main/libg/libgcrypt20/libgcrypt20_1.7.9.orig.tar.bz2.asc' libgcrypt20_1.7.9.orig.tar.bz2.asc 310 SHA256:96108d1701cd3c8a6826d7d2a27056de79421fe20bf9ef447e8c12e982f64414
'http://deb.debian.org/debian/pool/main/libg/libgcrypt20/libgcrypt20_1.7.9-1.debian.tar.xz' libgcrypt20_1.7.9-1.debian.tar.xz 26020 SHA256:1a0775f8e8921aa537db92c06cca82780cb24adf04775e2f944a23d867414d55
```

Other potentially useful URLs:

- https://sources.debian.net/src/libgcrypt20/1.7.9-1/ (for browsing the source)
- https://sources.debian.net/src/libgcrypt20/1.7.9-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libgcrypt20/1.7.9-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libgd2=2.2.5-2`

Binary Packages:

- `libgd3:amd64=2.2.5-2`

Licenses: (parsed from: `/usr/share/doc/libgd3/copyright`)

- `BSD-3-clause`
- `GAP~Makefile.in`
- `GAP~configure`
- `GD`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with Autoconf exception`
- `HPND`
- `MIT`
- `WEBP`
- `XFIG`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libgd2/2.2.5-2/


### `dpkg` source package: `libgpg-error=1.27-3`

Binary Packages:

- `libgpg-error0:amd64=1.27-3`

Licenses: (parsed from: `/usr/share/doc/libgpg-error0/copyright`)

- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libgpg-error=1.27-3
'http://deb.debian.org/debian/pool/main/libg/libgpg-error/libgpg-error_1.27-3.dsc' libgpg-error_1.27-3.dsc 2377 SHA256:427eba727e5ff13b1f29493edc281cfa811aabe4c0d0f07f747ab11bc8e9574f
'http://deb.debian.org/debian/pool/main/libg/libgpg-error/libgpg-error_1.27.orig.tar.bz2' libgpg-error_1.27.orig.tar.bz2 813060 SHA256:4f93aac6fecb7da2b92871bb9ee33032be6a87b174f54abf8ddf0911a22d29d2
'http://deb.debian.org/debian/pool/main/libg/libgpg-error/libgpg-error_1.27-3.debian.tar.xz' libgpg-error_1.27-3.debian.tar.xz 15856 SHA256:c1a17ea7066c955be7f7117efdd0961cd43f3fd81152854e53a60cb08fba0a10
```

Other potentially useful URLs:

- https://sources.debian.net/src/libgpg-error/1.27-3/ (for browsing the source)
- https://sources.debian.net/src/libgpg-error/1.27-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libgpg-error/1.27-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libice=2:1.0.9-2`

Binary Packages:

- `libice-dev:amd64=2:1.0.9-2`
- `libice6:amd64=2:1.0.9-2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libice=2:1.0.9-2
'http://deb.debian.org/debian/pool/main/libi/libice/libice_1.0.9-2.dsc' libice_1.0.9-2.dsc 2130 SHA256:116595cd54be23edad0b55e1cd4bc1929f277fa5c2d00d8f187b0bc5dd39ad6c
'http://deb.debian.org/debian/pool/main/libi/libice/libice_1.0.9.orig.tar.gz' libice_1.0.9.orig.tar.gz 455871 SHA256:7812a824a66dd654c830d21982749b3b563d9c2dfe0b88b203cefc14a891edc0
'http://deb.debian.org/debian/pool/main/libi/libice/libice_1.0.9-2.diff.gz' libice_1.0.9-2.diff.gz 6384 SHA256:777f13e08aada3103c32a0b93a26782ca959027bcd98c2c1ddaade8f944fa40a
```

Other potentially useful URLs:

- https://sources.debian.net/src/libice/2:1.0.9-2/ (for browsing the source)
- https://sources.debian.net/src/libice/2:1.0.9-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libice/2:1.0.9-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libidn2-0=2.0.2-3`

Binary Packages:

- `libidn2-0:amd64=2.0.2-3`

Licenses: (parsed from: `/usr/share/doc/libidn2-0/copyright`)

- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `LGPL-3+`
- `Unicode`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libidn2-0/2.0.2-3/


### `dpkg` source package: `libjpeg-turbo=1:1.5.2-2`

Binary Packages:

- `libjpeg-dev=1:1.5.2-2`
- `libjpeg62-turbo:amd64=1:1.5.2-2`
- `libjpeg62-turbo-dev:amd64=1:1.5.2-2`

Licenses: (parsed from: `/usr/share/doc/libjpeg-dev/copyright`, `/usr/share/doc/libjpeg62-turbo/copyright`, `/usr/share/doc/libjpeg62-turbo-dev/copyright`)

- `BSD-3`
- `BSD-BY-LC-NE`
- `Expat`

Source:

```console
$ apt-get source -qq --print-uris libjpeg-turbo=1:1.5.2-2
'http://deb.debian.org/debian/pool/main/libj/libjpeg-turbo/libjpeg-turbo_1.5.2-2.dsc' libjpeg-turbo_1.5.2-2.dsc 2434 SHA256:f975bd4b2192e3f1aeacef7f0de33035f386225035aea6157b413b1c500d46a1
'http://deb.debian.org/debian/pool/main/libj/libjpeg-turbo/libjpeg-turbo_1.5.2.orig.tar.gz' libjpeg-turbo_1.5.2.orig.tar.gz 1657235 SHA256:9098943b270388727ae61de82adec73cf9f0dbb240b3bc8b172595ebf405b528
'http://deb.debian.org/debian/pool/main/libj/libjpeg-turbo/libjpeg-turbo_1.5.2-2.debian.tar.xz' libjpeg-turbo_1.5.2-2.debian.tar.xz 78360 SHA256:964a2d747f8e74cbd558f343afd11b7dfe37212a611eeca863f1908eba66f728
```

Other potentially useful URLs:

- https://sources.debian.net/src/libjpeg-turbo/1:1.5.2-2/ (for browsing the source)
- https://sources.debian.net/src/libjpeg-turbo/1:1.5.2-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libjpeg-turbo/1:1.5.2-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libksba=1.3.5-2`

Binary Packages:

- `libksba8:amd64=1.3.5-2`

Licenses: (parsed from: `/usr/share/doc/libksba8/copyright`)

- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris libksba=1.3.5-2
'http://deb.debian.org/debian/pool/main/libk/libksba/libksba_1.3.5-2.dsc' libksba_1.3.5-2.dsc 2526 SHA256:4fd08fd129f97ab1df86c220b88b7b2c6e4e04aa90bfd3ae364d18022256bef8
'http://deb.debian.org/debian/pool/main/libk/libksba/libksba_1.3.5.orig.tar.bz2' libksba_1.3.5.orig.tar.bz2 620649 SHA256:41444fd7a6ff73a79ad9728f985e71c9ba8cd3e5e53358e70d5f066d35c1a340
'http://deb.debian.org/debian/pool/main/libk/libksba/libksba_1.3.5.orig.tar.bz2.asc' libksba_1.3.5.orig.tar.bz2.asc 287 SHA256:a954b03144ee882c838853da24fd7b6868b78df72a18c71079217d968698a76f
'http://deb.debian.org/debian/pool/main/libk/libksba/libksba_1.3.5-2.debian.tar.xz' libksba_1.3.5-2.debian.tar.xz 13852 SHA256:98c985bff973be1aecc702fa15887ff1e5b8de481d1dc3e99423a587754eaabd
```

Other potentially useful URLs:

- https://sources.debian.net/src/libksba/1.3.5-2/ (for browsing the source)
- https://sources.debian.net/src/libksba/1.3.5-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libksba/1.3.5-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `liblqr=0.4.2-2`

Binary Packages:

- `liblqr-1-0:amd64=0.4.2-2+b2`
- `liblqr-1-0-dev=0.4.2-2+b2`

Licenses: (parsed from: `/usr/share/doc/liblqr-1-0/copyright`, `/usr/share/doc/liblqr-1-0-dev/copyright`)

- `GPL-3`
- `GPLv3`
- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris liblqr=0.4.2-2
'http://deb.debian.org/debian/pool/main/libl/liblqr/liblqr_0.4.2-2.dsc' liblqr_0.4.2-2.dsc 2024 SHA256:7e203605ebe40cde3e467db4298d7ee3f83f3d3082b05f8984868cdef1606245
'http://deb.debian.org/debian/pool/main/libl/liblqr/liblqr_0.4.2.orig.tar.gz' liblqr_0.4.2.orig.tar.gz 439884 SHA256:d4c22373432cca749e4326cd41fce365e6ff857c0bfd7a5302b8eb34b69f0336
'http://deb.debian.org/debian/pool/main/libl/liblqr/liblqr_0.4.2-2.debian.tar.xz' liblqr_0.4.2-2.debian.tar.xz 5860 SHA256:2c886ee88f65eade9e1cd10965bf572a3cc178d6119b9342c8469b6b41d2bb62
```

Other potentially useful URLs:

- https://sources.debian.net/src/liblqr/0.4.2-2/ (for browsing the source)
- https://sources.debian.net/src/liblqr/0.4.2-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/liblqr/0.4.2-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libmnl=1.0.4-2`

Binary Packages:

- `libmnl0:amd64=1.0.4-2`

Licenses: (parsed from: `/usr/share/doc/libmnl0/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libmnl=1.0.4-2
'http://deb.debian.org/debian/pool/main/libm/libmnl/libmnl_1.0.4-2.dsc' libmnl_1.0.4-2.dsc 1994 SHA256:131106bb7eb4a94fa8e8c135f92c38068d0b42681f166eb159137f171c568630
'http://deb.debian.org/debian/pool/main/libm/libmnl/libmnl_1.0.4.orig.tar.bz2' libmnl_1.0.4.orig.tar.bz2 301270 SHA256:171f89699f286a5854b72b91d06e8f8e3683064c5901fb09d954a9ab6f551f81
'http://deb.debian.org/debian/pool/main/libm/libmnl/libmnl_1.0.4-2.debian.tar.xz' libmnl_1.0.4-2.debian.tar.xz 7512 SHA256:208d62777081ffe6d7dffde0d7370cefb03fe0a6a0486a1b50f6b7b8e9a5b068
```

Other potentially useful URLs:

- https://sources.debian.net/src/libmnl/1.0.4-2/ (for browsing the source)
- https://sources.debian.net/src/libmnl/1.0.4-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libmnl/1.0.4-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libpng1.6=1.6.32-1`

Binary Packages:

- `libpng-dev:amd64=1.6.32-1`
- `libpng16-16:amd64=1.6.32-1`

Licenses: (parsed from: `/usr/share/doc/libpng-dev/copyright`, `/usr/share/doc/libpng16-16/copyright`)

- `Apache-2.0`
- `BSD-3-clause`
- `BSD-like-with-advertising-clause`
- `GPL-2`
- `GPL-2+`
- `expat`
- `libpng`
- `libpng OR Apache-2.0 OR BSD-3-clause`

Source:

```console
$ apt-get source -qq --print-uris libpng1.6=1.6.32-1
'http://deb.debian.org/debian/pool/main/libp/libpng1.6/libpng1.6_1.6.32-1.dsc' libpng1.6_1.6.32-1.dsc 2188 SHA256:8a15cc205f1b564e7be8199dd7d7350e867f50d459ee42b6cb30533c278c8d30
'http://deb.debian.org/debian/pool/main/libp/libpng1.6/libpng1.6_1.6.32.orig.tar.xz' libpng1.6_1.6.32.orig.tar.xz 997136 SHA256:c918c3113de74a692f0a1526ce881dc26067763eb3915c57ef3a0f7b6886f59b
'http://deb.debian.org/debian/pool/main/libp/libpng1.6/libpng1.6_1.6.32-1.debian.tar.xz' libpng1.6_1.6.32-1.debian.tar.xz 23244 SHA256:47ae700a63793361b9cb0f23c547c29b2776625f8c846957e9b6842a29ed8fe8
```

Other potentially useful URLs:

- https://sources.debian.net/src/libpng1.6/1.6.32-1/ (for browsing the source)
- https://sources.debian.net/src/libpng1.6/1.6.32-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libpng1.6/1.6.32-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libpsl=0.18.0-4`

Binary Packages:

- `libpsl5:amd64=0.18.0-4`

Licenses: (parsed from: `/usr/share/doc/libpsl5/copyright`)

- `Chromium`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris libpsl=0.18.0-4
'http://deb.debian.org/debian/pool/main/libp/libpsl/libpsl_0.18.0-4.dsc' libpsl_0.18.0-4.dsc 2190 SHA256:b62d3ad4472795fa8a81fcdc938aae7e8fa542835873c730463b280931abae75
'http://deb.debian.org/debian/pool/main/libp/libpsl/libpsl_0.18.0.orig.tar.gz' libpsl_0.18.0.orig.tar.gz 10330130 SHA256:29d76f49fe58f36a23d8eeb863e545767ab6ebbddb3356fc63af9728739edb3f
'http://deb.debian.org/debian/pool/main/libp/libpsl/libpsl_0.18.0-4.debian.tar.xz' libpsl_0.18.0-4.debian.tar.xz 9240 SHA256:d46f48e6b9ed75702b13d1e8d9c39c0898f8f76c956e430a71ee4fbecff09138
```

Other potentially useful URLs:

- https://sources.debian.net/src/libpsl/0.18.0-4/ (for browsing the source)
- https://sources.debian.net/src/libpsl/0.18.0-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libpsl/0.18.0-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libpthread-stubs=0.3-4`

Binary Packages:

- `libpthread-stubs0-dev:amd64=0.3-4`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libpthread-stubs=0.3-4
'http://deb.debian.org/debian/pool/main/libp/libpthread-stubs/libpthread-stubs_0.3-4.dsc' libpthread-stubs_0.3-4.dsc 1925 SHA256:e72310a5492e641076c199561977703947174c6acc3633073d909f6f5ab3c676
'http://deb.debian.org/debian/pool/main/libp/libpthread-stubs/libpthread-stubs_0.3.orig.tar.gz' libpthread-stubs_0.3.orig.tar.gz 272939 SHA256:3031f466cf0b06de6b3ccbf2019d15c4fcf75229b7d226a711bc1885b3a82cde
'http://deb.debian.org/debian/pool/main/libp/libpthread-stubs/libpthread-stubs_0.3-4.diff.gz' libpthread-stubs_0.3-4.diff.gz 2413 SHA256:ce3eb8bdc0f1a4347d42c5736d056973fae46908b764a9f2be83e1bd210f2024
```

Other potentially useful URLs:

- https://sources.debian.net/src/libpthread-stubs/0.3-4/ (for browsing the source)
- https://sources.debian.net/src/libpthread-stubs/0.3-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libpthread-stubs/0.3-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `librsvg=2.40.18-1`

Binary Packages:

- `gir1.2-rsvg-2.0:amd64=2.40.18-1`
- `librsvg2-2:amd64=2.40.18-1`
- `librsvg2-common:amd64=2.40.18-1`
- `librsvg2-dev:amd64=2.40.18-1`

Licenses: (parsed from: `/usr/share/doc/gir1.2-rsvg-2.0/copyright`, `/usr/share/doc/librsvg2-2/copyright`, `/usr/share/doc/librsvg2-common/copyright`, `/usr/share/doc/librsvg2-dev/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2`
- `LGPL-2+`

Source:

```console
$ apt-get source -qq --print-uris librsvg=2.40.18-1
'http://deb.debian.org/debian/pool/main/libr/librsvg/librsvg_2.40.18-1.dsc' librsvg_2.40.18-1.dsc 2795 SHA256:7667f59db269b54ddb44e435a6e4b69139f62ea59c0e32dd81a18139eddd9d19
'http://deb.debian.org/debian/pool/main/libr/librsvg/librsvg_2.40.18.orig.tar.xz' librsvg_2.40.18.orig.tar.xz 574384 SHA256:bfc8c488c89c1e7212c478beb95c41b44701636125a3e6dab41187f1485b564c
'http://deb.debian.org/debian/pool/main/libr/librsvg/librsvg_2.40.18-1.debian.tar.xz' librsvg_2.40.18-1.debian.tar.xz 14464 SHA256:29b5747a7208268ceed3ccd5432b2379ee5937ba3fce4fbb1d41ffbf7de3f792
```

Other potentially useful URLs:

- https://sources.debian.net/src/librsvg/2.40.18-1/ (for browsing the source)
- https://sources.debian.net/src/librsvg/2.40.18-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/librsvg/2.40.18-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libselinux=2.6-3`

Binary Packages:

- `libselinux1:amd64=2.6-3+b2`

Licenses: (parsed from: `/usr/share/doc/libselinux1/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libselinux=2.6-3
'http://deb.debian.org/debian/pool/main/libs/libselinux/libselinux_2.6-3.dsc' libselinux_2.6-3.dsc 2217 SHA256:91bb53feba8031bfc7b0110fc4e0e1dae4a8e2906f4a524f83252a95ae0e639c
'http://deb.debian.org/debian/pool/main/libs/libselinux/libselinux_2.6.orig.tar.gz' libselinux_2.6.orig.tar.gz 203119 SHA256:4ea2dde50665c202253ba5caac7738370ea0337c47b251ba981c60d24e1a118a
'http://deb.debian.org/debian/pool/main/libs/libselinux/libselinux_2.6-3.debian.tar.xz' libselinux_2.6-3.debian.tar.xz 24396 SHA256:5a06841565e7907bc0dae9f8ed5940d040316192bd9662df59c79af7c212a171
```

Other potentially useful URLs:

- https://sources.debian.net/src/libselinux/2.6-3/ (for browsing the source)
- https://sources.debian.net/src/libselinux/2.6-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libselinux/2.6-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libsemanage=2.6-2`

Binary Packages:

- `libsemanage-common=2.6-2`
- `libsemanage1:amd64=2.6-2+b1`

Licenses: (parsed from: `/usr/share/doc/libsemanage-common/copyright`, `/usr/share/doc/libsemanage1/copyright`)

- `GPL`
- `LGPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libsemanage/2.6-2/


### `dpkg` source package: `libsepol=2.6-2`

Binary Packages:

- `libsepol1:amd64=2.6-2`

Licenses: (parsed from: `/usr/share/doc/libsepol1/copyright`)

- `GPL`
- `LGPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libsepol/2.6-2/


### `dpkg` source package: `libsigsegv=2.11-1`

Binary Packages:

- `libsigsegv2:amd64=2.11-1`

Licenses: (parsed from: `/usr/share/doc/libsigsegv2/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris libsigsegv=2.11-1
'http://deb.debian.org/debian/pool/main/libs/libsigsegv/libsigsegv_2.11-1.dsc' libsigsegv_2.11-1.dsc 2365 SHA256:b2b5064cee7730302ccdda9788709b8fbb270ebbad6899be1a8bb7e491ff14dd
'http://deb.debian.org/debian/pool/main/libs/libsigsegv/libsigsegv_2.11.orig.tar.gz' libsigsegv_2.11.orig.tar.gz 256573 SHA256:b8eadcfa513f9127f672082b5348a834299760e3d17ef99cf9c712fb8c068c73
'http://deb.debian.org/debian/pool/main/libs/libsigsegv/libsigsegv_2.11-1.debian.tar.xz' libsigsegv_2.11-1.debian.tar.xz 10212 SHA256:d253b4314b3348c000ecfa260c467c27135c80c5cd2597b9920fef5379ac70cb
```

Other potentially useful URLs:

- https://sources.debian.net/src/libsigsegv/2.11-1/ (for browsing the source)
- https://sources.debian.net/src/libsigsegv/2.11-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libsigsegv/2.11-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libsm=2:1.2.2-1`

Binary Packages:

- `libsm-dev:amd64=2:1.2.2-1+b3`
- `libsm6:amd64=2:1.2.2-1+b3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libsm=2:1.2.2-1
'http://deb.debian.org/debian/pool/main/libs/libsm/libsm_1.2.2-1.dsc' libsm_1.2.2-1.dsc 2107 SHA256:1347efa550751179c0a3f1042a9f8ae43ee0c22cf0c2283921fa83e52a68433f
'http://deb.debian.org/debian/pool/main/libs/libsm/libsm_1.2.2.orig.tar.gz' libsm_1.2.2.orig.tar.gz 415990 SHA256:14bb7c669ce2b8ff712fbdbf48120e3742a77edcd5e025d6b3325ed30cf120f4
'http://deb.debian.org/debian/pool/main/libs/libsm/libsm_1.2.2-1.diff.gz' libsm_1.2.2-1.diff.gz 6183 SHA256:9848714292ead15fcc48ab2d337f2cc5fc08910abbdfaf69d3ef1b89d3fdb2d5
```

Other potentially useful URLs:

- https://sources.debian.net/src/libsm/2:1.2.2-1/ (for browsing the source)
- https://sources.debian.net/src/libsm/2:1.2.2-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libsm/2:1.2.2-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libssh2=1.8.0-1`

Binary Packages:

- `libssh2-1:amd64=1.8.0-1`

Licenses: (parsed from: `/usr/share/doc/libssh2-1/copyright`)

- `BSD3`

Source:

```console
$ apt-get source -qq --print-uris libssh2=1.8.0-1
'http://deb.debian.org/debian/pool/main/libs/libssh2/libssh2_1.8.0-1.dsc' libssh2_1.8.0-1.dsc 1860 SHA256:14837d645e77d08fbf00333dee60129be3aeb40c956294cb7bd0b79f456a3fb0
'http://deb.debian.org/debian/pool/main/libs/libssh2/libssh2_1.8.0.orig.tar.gz' libssh2_1.8.0.orig.tar.gz 846989 SHA256:4382d33de790b28f862e53ed59ffbd65f3def7a06e8b6e9ca1b6f70453b4d5e0
'http://deb.debian.org/debian/pool/main/libs/libssh2/libssh2_1.8.0-1.debian.tar.xz' libssh2_1.8.0-1.debian.tar.xz 7320 SHA256:79a68889d8102922b92b1757b1d5993cb70faa9a259aca21c2db2e5e55d30b62
```

Other potentially useful URLs:

- https://sources.debian.net/src/libssh2/1.8.0-1/ (for browsing the source)
- https://sources.debian.net/src/libssh2/1.8.0-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libssh2/1.8.0-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libtasn1-6=4.12-2.1`

Binary Packages:

- `libtasn1-6:amd64=4.12-2.1`

Licenses: (parsed from: `/usr/share/doc/libtasn1-6/copyright`)

- `GFDL-1.3`
- `GPL-3`
- `LGPL`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libtasn1-6=4.12-2.1
'http://deb.debian.org/debian/pool/main/libt/libtasn1-6/libtasn1-6_4.12-2.1.dsc' libtasn1-6_4.12-2.1.dsc 2586 SHA256:0f762f07bbb39e9a49687e8bd7a18a5d3cc435d6c226eaecfcda7a8d325c2cef
'http://deb.debian.org/debian/pool/main/libt/libtasn1-6/libtasn1-6_4.12.orig.tar.gz' libtasn1-6_4.12.orig.tar.gz 1888450 SHA256:6753da2e621257f33f5b051cc114d417e5206a0818fe0b1ecfd6153f70934753
'http://deb.debian.org/debian/pool/main/libt/libtasn1-6/libtasn1-6_4.12-2.1.debian.tar.xz' libtasn1-6_4.12-2.1.debian.tar.xz 58728 SHA256:df32c448a8472eff20fa6989f939cbc0e2caf0d4bb712e54b31b39bbd6d8b781
```

Other potentially useful URLs:

- https://sources.debian.net/src/libtasn1-6/4.12-2.1/ (for browsing the source)
- https://sources.debian.net/src/libtasn1-6/4.12-2.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libtasn1-6/4.12-2.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libthai=0.1.26-3`

Binary Packages:

- `libthai-data=0.1.26-3`
- `libthai0:amd64=0.1.26-3`

Licenses: (parsed from: `/usr/share/doc/libthai-data/copyright`, `/usr/share/doc/libthai0/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libthai=0.1.26-3
'http://deb.debian.org/debian/pool/main/libt/libthai/libthai_0.1.26-3.dsc' libthai_0.1.26-3.dsc 2300 SHA256:da0c0b960dbce2324d0ee4bce7574493841d1b07391b2f64199da802bc45d072
'http://deb.debian.org/debian/pool/main/libt/libthai/libthai_0.1.26.orig.tar.xz' libthai_0.1.26.orig.tar.xz 409380 SHA256:8710112c836b272db1740a9ea3e6c7ebb65b64eee0e143fc2b2c60f99f6bfe2a
'http://deb.debian.org/debian/pool/main/libt/libthai/libthai_0.1.26-3.debian.tar.xz' libthai_0.1.26-3.debian.tar.xz 11076 SHA256:e00c2b0ac9154f2cb3a43917b0a518baf0d09170719bf4849566a6ad3d0e3484
```

Other potentially useful URLs:

- https://sources.debian.net/src/libthai/0.1.26-3/ (for browsing the source)
- https://sources.debian.net/src/libthai/0.1.26-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libthai/0.1.26-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libtool=2.4.6-2`

Binary Packages:

- `libltdl-dev:amd64=2.4.6-2`
- `libltdl7:amd64=2.4.6-2`
- `libtool=2.4.6-2`

Licenses: (parsed from: `/usr/share/doc/libltdl-dev/copyright`, `/usr/share/doc/libltdl7/copyright`, `/usr/share/doc/libtool/copyright`)

- `GFDL`
- `GPL`

Source:

```console
$ apt-get source -qq --print-uris libtool=2.4.6-2
'http://deb.debian.org/debian/pool/main/libt/libtool/libtool_2.4.6-2.dsc' libtool_2.4.6-2.dsc 2324 SHA256:caa2b9d5c32e491388d0627e2f808b6cb2f260dd1b0b9fdafc9bff957f05bb29
'http://deb.debian.org/debian/pool/main/libt/libtool/libtool_2.4.6.orig.tar.xz' libtool_2.4.6.orig.tar.xz 973080 SHA256:7c87a8c2c8c0fc9cd5019e402bed4292462d00a718a7cd5f11218153bf28b26f
'http://deb.debian.org/debian/pool/main/libt/libtool/libtool_2.4.6.orig.tar.xz.asc' libtool_2.4.6.orig.tar.xz.asc 380 SHA256:ab68ebc45d60128a71fc36167cd29dcf3c3d6d639fd28663905ebaf3e2f43d6a
'http://deb.debian.org/debian/pool/main/libt/libtool/libtool_2.4.6-2.debian.tar.xz' libtool_2.4.6-2.debian.tar.xz 36024 SHA256:6227fb1240a90ef06855567e71ee96e4950dd53c4399348f36c1ec39367cd8ea
```

Other potentially useful URLs:

- https://sources.debian.net/src/libtool/2.4.6-2/ (for browsing the source)
- https://sources.debian.net/src/libtool/2.4.6-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libtool/2.4.6-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libunistring=0.9.7-2`

Binary Packages:

- `libunistring2:amd64=0.9.7-2`

Licenses: (parsed from: `/usr/share/doc/libunistring2/copyright`)

- `FreeSoftware`
- `GFDL-1.2`
- `GFDL-1.2+`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with distribution exception`
- `GPL-3`
- `GPL-3+`
- `LGPL-3`
- `LGPL-3+`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris libunistring=0.9.7-2
'http://deb.debian.org/debian/pool/main/libu/libunistring/libunistring_0.9.7-2.dsc' libunistring_0.9.7-2.dsc 1985 SHA256:2ac1f77b0fc421eadcbfbe1e2e022137f31404f4874f6ff326ed8644f8ca18c8
'http://deb.debian.org/debian/pool/main/libu/libunistring/libunistring_0.9.7.orig.tar.xz' libunistring_0.9.7.orig.tar.xz 1967300 SHA256:2e3764512aaf2ce598af5a38818c0ea23dedf1ff5460070d1b6cee5c3336e797
'http://deb.debian.org/debian/pool/main/libu/libunistring/libunistring_0.9.7-2.debian.tar.xz' libunistring_0.9.7-2.debian.tar.xz 39776 SHA256:6eaa5343ae3c40627a35fc8ac85a07c0da8236c8aa49205be7e51139f278c95c
```

Other potentially useful URLs:

- https://sources.debian.net/src/libunistring/0.9.7-2/ (for browsing the source)
- https://sources.debian.net/src/libunistring/0.9.7-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libunistring/0.9.7-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libwebp=0.6.0-3`

Binary Packages:

- `libwebp-dev:amd64=0.6.0-3`
- `libwebp6:amd64=0.6.0-3`
- `libwebpdemux2:amd64=0.6.0-3`
- `libwebpmux3:amd64=0.6.0-3`

Licenses: (parsed from: `/usr/share/doc/libwebp-dev/copyright`, `/usr/share/doc/libwebp6/copyright`, `/usr/share/doc/libwebpdemux2/copyright`, `/usr/share/doc/libwebpmux3/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris libwebp=0.6.0-3
'http://deb.debian.org/debian/pool/main/libw/libwebp/libwebp_0.6.0-3.dsc' libwebp_0.6.0-3.dsc 2065 SHA256:e3580473966dff04e154dc7270f67d26e7ab68054e74d9dbebe4ed487f6e0ed0
'http://deb.debian.org/debian/pool/main/libw/libwebp/libwebp_0.6.0.orig.tar.gz' libwebp_0.6.0.orig.tar.gz 1302881 SHA256:c928119229d4f8f35e20113ffb61f281eda267634a8dc2285af4b0ee27cf2b40
'http://deb.debian.org/debian/pool/main/libw/libwebp/libwebp_0.6.0-3.debian.tar.xz' libwebp_0.6.0-3.debian.tar.xz 6132 SHA256:7050f9f70141424b15c5f1a6353f90d926f652aba6cec31bdfbd6c8b010aa11f
```

Other potentially useful URLs:

- https://sources.debian.net/src/libwebp/0.6.0-3/ (for browsing the source)
- https://sources.debian.net/src/libwebp/0.6.0-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libwebp/0.6.0-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libwmf=0.2.8.4-11`

Binary Packages:

- `libwmf-dev=0.2.8.4-11`
- `libwmf0.2-7:amd64=0.2.8.4-11`

Licenses: (parsed from: `/usr/share/doc/libwmf-dev/copyright`, `/usr/share/doc/libwmf0.2-7/copyright`)

- `LGPL-2`

Source:

```console
$ apt-get source -qq --print-uris libwmf=0.2.8.4-11
'http://deb.debian.org/debian/pool/main/libw/libwmf/libwmf_0.2.8.4-11.dsc' libwmf_0.2.8.4-11.dsc 2078 SHA256:12b561f83c00fae3850e2581ad32d8ac89b21852bc575c44cfe3e3a83a5979fb
'http://deb.debian.org/debian/pool/main/libw/libwmf/libwmf_0.2.8.4.orig.tar.gz' libwmf_0.2.8.4.orig.tar.gz 2169375 SHA256:5b345c69220545d003ad52bfd035d5d6f4f075e65204114a9e875e84895a7cf8
'http://deb.debian.org/debian/pool/main/libw/libwmf/libwmf_0.2.8.4-11.debian.tar.xz' libwmf_0.2.8.4-11.debian.tar.xz 11820 SHA256:3b262b166874c56a99e24ebe596fe28bf4f32f8ef4d47dc699a58b40e3c8ec90
```

Other potentially useful URLs:

- https://sources.debian.net/src/libwmf/0.2.8.4-11/ (for browsing the source)
- https://sources.debian.net/src/libwmf/0.2.8.4-11/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libwmf/0.2.8.4-11/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libx11=2:1.6.4-3`

Binary Packages:

- `libx11-6:amd64=2:1.6.4-3`
- `libx11-data=2:1.6.4-3`
- `libx11-dev:amd64=2:1.6.4-3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libx11=2:1.6.4-3
'http://deb.debian.org/debian/pool/main/libx/libx11/libx11_1.6.4-3.dsc' libx11_1.6.4-3.dsc 2397 SHA256:4c5d6add2ba969067ca111c827ae94264e4c22776e22f318d264545dc1c6a300
'http://deb.debian.org/debian/pool/main/libx/libx11/libx11_1.6.4.orig.tar.gz' libx11_1.6.4.orig.tar.gz 3095115 SHA256:5d7fbb9e15c27900ea8963218a59750b674a8d7c94161b66e96fcfbdaa1c6263
'http://deb.debian.org/debian/pool/main/libx/libx11/libx11_1.6.4-3.diff.gz' libx11_1.6.4-3.diff.gz 41366 SHA256:2c936827bca63eaf5b66683bdcd0ecf013d152c35439f792475db85c5c2338fd
```

Other potentially useful URLs:

- https://sources.debian.net/src/libx11/2:1.6.4-3/ (for browsing the source)
- https://sources.debian.net/src/libx11/2:1.6.4-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libx11/2:1.6.4-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libxau=1:1.0.8-1`

Binary Packages:

- `libxau-dev:amd64=1:1.0.8-1+b2`
- `libxau6:amd64=1:1.0.8-1+b2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxau=1:1.0.8-1
'http://deb.debian.org/debian/pool/main/libx/libxau/libxau_1.0.8-1.dsc' libxau_1.0.8-1.dsc 2040 SHA256:3ddb5f2c7a49ef7507b8d1e63e891238db877b4d1bb1c5486a3e3242c8523602
'http://deb.debian.org/debian/pool/main/libx/libxau/libxau_1.0.8.orig.tar.gz' libxau_1.0.8.orig.tar.gz 362044 SHA256:c343b4ef66d66a6b3e0e27aa46b37ad5cab0f11a5c565eafb4a1c7590bc71d7b
'http://deb.debian.org/debian/pool/main/libx/libxau/libxau_1.0.8-1.diff.gz' libxau_1.0.8-1.diff.gz 15287 SHA256:b493479d6a52a0e753dd357ad8a4bc5c4296015f3f7b96cf546f7c5c5843cbb0
```

Other potentially useful URLs:

- https://sources.debian.net/src/libxau/1:1.0.8-1/ (for browsing the source)
- https://sources.debian.net/src/libxau/1:1.0.8-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libxau/1:1.0.8-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libxcb=1.12-1`

Binary Packages:

- `libxcb-render0:amd64=1.12-1`
- `libxcb-render0-dev:amd64=1.12-1`
- `libxcb-shm0:amd64=1.12-1`
- `libxcb-shm0-dev:amd64=1.12-1`
- `libxcb1:amd64=1.12-1`
- `libxcb1-dev:amd64=1.12-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxcb=1.12-1
'http://deb.debian.org/debian/pool/main/libx/libxcb/libxcb_1.12-1.dsc' libxcb_1.12-1.dsc 6558 SHA256:d6ed3f5ef255a692c9654d954da4421c535e02f21e56a657383ea9d52389080d
'http://deb.debian.org/debian/pool/main/libx/libxcb/libxcb_1.12.orig.tar.gz' libxcb_1.12.orig.tar.gz 745984 SHA256:092f147149d8a6410647a848378aaae749304d5b73e028ccb8306aa8a9e26f06
'http://deb.debian.org/debian/pool/main/libx/libxcb/libxcb_1.12-1.diff.gz' libxcb_1.12-1.diff.gz 25044 SHA256:e2af982573638874bca1f4159139e2bffa0ee51148544b4c3b09bad84622648c
```

Other potentially useful URLs:

- https://sources.debian.net/src/libxcb/1.12-1/ (for browsing the source)
- https://sources.debian.net/src/libxcb/1.12-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libxcb/1.12-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libxcomposite=1:0.4.4-2`

Binary Packages:

- `libxcomposite1:amd64=1:0.4.4-2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxcomposite=1:0.4.4-2
'http://deb.debian.org/debian/pool/main/libx/libxcomposite/libxcomposite_0.4.4-2.dsc' libxcomposite_0.4.4-2.dsc 2178 SHA256:4124027ad4b4598a61c45cbc345988010a2a5ba6e7c80259917f59414be69861
'http://deb.debian.org/debian/pool/main/libx/libxcomposite/libxcomposite_0.4.4.orig.tar.gz' libxcomposite_0.4.4.orig.tar.gz 354584 SHA256:83c04649819c6f52cda1b0ce8bcdcc48ad8618428ad803fb07f20b802f1bdad1
'http://deb.debian.org/debian/pool/main/libx/libxcomposite/libxcomposite_0.4.4-2.diff.gz' libxcomposite_0.4.4-2.diff.gz 15755 SHA256:9689ae3fcc76054fe09909692e71a1a4fe356e84f3adfa2be668e173d0369ebc
```

Other potentially useful URLs:

- https://sources.debian.net/src/libxcomposite/1:0.4.4-2/ (for browsing the source)
- https://sources.debian.net/src/libxcomposite/1:0.4.4-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libxcomposite/1:0.4.4-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libxcursor=1:1.1.14-3`

Binary Packages:

- `libxcursor1:amd64=1:1.1.14-3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxcursor=1:1.1.14-3
'http://deb.debian.org/debian/pool/main/libx/libxcursor/libxcursor_1.1.14-3.dsc' libxcursor_1.1.14-3.dsc 2288 SHA256:c5324154d4232bae10c11222199960e7b1b194eb5da331807f6f048fc6fa74b9
'http://deb.debian.org/debian/pool/main/libx/libxcursor/libxcursor_1.1.14.orig.tar.gz' libxcursor_1.1.14.orig.tar.gz 374910 SHA256:be0954faf274969ffa6d95b9606b9c0cfee28c13b6fc014f15606a0c8b05c17b
'http://deb.debian.org/debian/pool/main/libx/libxcursor/libxcursor_1.1.14-3.debian.tar.xz' libxcursor_1.1.14-3.debian.tar.xz 8688 SHA256:1f80cf47326cf05eafe5ac7215103be6cac3369eccffbe2b254828330f47cbdd
```

Other potentially useful URLs:

- https://sources.debian.net/src/libxcursor/1:1.1.14-3/ (for browsing the source)
- https://sources.debian.net/src/libxcursor/1:1.1.14-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libxcursor/1:1.1.14-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libxdamage=1:1.1.4-3`

Binary Packages:

- `libxdamage1:amd64=1:1.1.4-3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxdamage=1:1.1.4-3
'http://deb.debian.org/debian/pool/main/libx/libxdamage/libxdamage_1.1.4-3.dsc' libxdamage_1.1.4-3.dsc 2161 SHA256:f1207d4fca942d2cddfe40abc818046e282ceeb0e0b565a44c2908fd03c41368
'http://deb.debian.org/debian/pool/main/libx/libxdamage/libxdamage_1.1.4.orig.tar.gz' libxdamage_1.1.4.orig.tar.gz 339060 SHA256:4bb3e9d917f5f593df2277d452926ee6ad96de7b7cd1017cbcf4579fe5d3442b
'http://deb.debian.org/debian/pool/main/libx/libxdamage/libxdamage_1.1.4-3.debian.tar.xz' libxdamage_1.1.4-3.debian.tar.xz 5904 SHA256:94dcf3997a92f5e1b4681dcbe555af4469607ae7af2d0dc643a7a1be7b94e64a
```

Other potentially useful URLs:

- https://sources.debian.net/src/libxdamage/1:1.1.4-3/ (for browsing the source)
- https://sources.debian.net/src/libxdamage/1:1.1.4-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libxdamage/1:1.1.4-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libxdmcp=1:1.1.2-3`

Binary Packages:

- `libxdmcp-dev:amd64=1:1.1.2-3`
- `libxdmcp6:amd64=1:1.1.2-3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxdmcp=1:1.1.2-3
'http://deb.debian.org/debian/pool/main/libx/libxdmcp/libxdmcp_1.1.2-3.dsc' libxdmcp_1.1.2-3.dsc 2145 SHA256:f9697dca6a275aeee9a3eee9fb2d55e0f77485481e8b84efc6950fc9b1988460
'http://deb.debian.org/debian/pool/main/libx/libxdmcp/libxdmcp_1.1.2.orig.tar.gz' libxdmcp_1.1.2.orig.tar.gz 404115 SHA256:6f7c7e491a23035a26284d247779174dedc67e34e93cc3548b648ffdb6fc57c0
'http://deb.debian.org/debian/pool/main/libx/libxdmcp/libxdmcp_1.1.2-3.diff.gz' libxdmcp_1.1.2-3.diff.gz 18017 SHA256:5844df115c17e5ba40ac116f80373304d821c607e763ef6f40562421f5cc0cf3
```

Other potentially useful URLs:

- https://sources.debian.net/src/libxdmcp/1:1.1.2-3/ (for browsing the source)
- https://sources.debian.net/src/libxdmcp/1:1.1.2-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libxdmcp/1:1.1.2-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libxext=2:1.3.3-1`

Binary Packages:

- `libxext-dev:amd64=2:1.3.3-1+b2`
- `libxext6:amd64=2:1.3.3-1+b2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxext=2:1.3.3-1
'http://deb.debian.org/debian/pool/main/libx/libxext/libxext_1.3.3-1.dsc' libxext_1.3.3-1.dsc 2221 SHA256:47106df75b8f3db1e43803e8e94a2e966cd23f7daa8cfc393af739a9e33ef955
'http://deb.debian.org/debian/pool/main/libx/libxext/libxext_1.3.3.orig.tar.gz' libxext_1.3.3.orig.tar.gz 468441 SHA256:eb0b88050491fef4716da4b06a4d92b4fc9e76f880d6310b2157df604342cfe5
'http://deb.debian.org/debian/pool/main/libx/libxext/libxext_1.3.3-1.diff.gz' libxext_1.3.3-1.diff.gz 20763 SHA256:e294a4884eb68acbd151312cb0c973aad63268b637b15ccf1911864b7197557e
```

Other potentially useful URLs:

- https://sources.debian.net/src/libxext/2:1.3.3-1/ (for browsing the source)
- https://sources.debian.net/src/libxext/2:1.3.3-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libxext/2:1.3.3-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libxfixes=1:5.0.3-1`

Binary Packages:

- `libxfixes3:amd64=1:5.0.3-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxfixes=1:5.0.3-1
'http://deb.debian.org/debian/pool/main/libx/libxfixes/libxfixes_5.0.3-1.dsc' libxfixes_5.0.3-1.dsc 2040 SHA256:87c1c491d8ff261b5a723c6c6aa974f315ff6f25f47425285a62065cbf944025
'http://deb.debian.org/debian/pool/main/libx/libxfixes/libxfixes_5.0.3.orig.tar.gz' libxfixes_5.0.3.orig.tar.gz 360412 SHA256:9ab6c13590658501ce4bd965a8a5d32ba4d8b3bb39a5a5bc9901edffc5666570
'http://deb.debian.org/debian/pool/main/libx/libxfixes/libxfixes_5.0.3-1.diff.gz' libxfixes_5.0.3-1.diff.gz 15140 SHA256:95b9688465531c60ff372bf8a2eb5fdd456970cbbb679ba13e54d24af44fb904
```

Other potentially useful URLs:

- https://sources.debian.net/src/libxfixes/1:5.0.3-1/ (for browsing the source)
- https://sources.debian.net/src/libxfixes/1:5.0.3-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libxfixes/1:5.0.3-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libxi=2:1.7.9-1`

Binary Packages:

- `libxi6:amd64=2:1.7.9-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxi=2:1.7.9-1
'http://deb.debian.org/debian/pool/main/libx/libxi/libxi_1.7.9-1.dsc' libxi_1.7.9-1.dsc 2202 SHA256:fb19b7e8b9ad6306c3e8a6728f29576f956f07a7980e7b4d727259714d6ca686
'http://deb.debian.org/debian/pool/main/libx/libxi/libxi_1.7.9.orig.tar.gz' libxi_1.7.9.orig.tar.gz 604214 SHA256:463cc5370191404bc0f8a450fdbf6d9159efbbf274e5e0f427a60191fed9cf4b
'http://deb.debian.org/debian/pool/main/libx/libxi/libxi_1.7.9-1.diff.gz' libxi_1.7.9-1.diff.gz 15892 SHA256:8c9c221faecc97a7ba7ff1a1a14fad580c49b72e270dc3aae40b72b2d7f4dc5e
```

Other potentially useful URLs:

- https://sources.debian.net/src/libxi/2:1.7.9-1/ (for browsing the source)
- https://sources.debian.net/src/libxi/2:1.7.9-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libxi/2:1.7.9-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libxinerama=2:1.1.3-1`

Binary Packages:

- `libxinerama1:amd64=2:1.1.3-1+b3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxinerama=2:1.1.3-1
'http://deb.debian.org/debian/pool/main/libx/libxinerama/libxinerama_1.1.3-1.dsc' libxinerama_1.1.3-1.dsc 2198 SHA256:4cf9a3558bd7ce1b4f55a581175c05e4b4a172364458a21ff4b657b714688fbb
'http://deb.debian.org/debian/pool/main/libx/libxinerama/libxinerama_1.1.3.orig.tar.gz' libxinerama_1.1.3.orig.tar.gz 350141 SHA256:0ba243222ae5aba4c6a3d7a394c32c8b69220a6872dbb00b7abae8753aca9a44
'http://deb.debian.org/debian/pool/main/libx/libxinerama/libxinerama_1.1.3-1.diff.gz' libxinerama_1.1.3-1.diff.gz 15738 SHA256:2b1487e3511ddabfec666a62f6e5e8ac4f97536b0d53c51f7bf4cbe07508a130
```

Other potentially useful URLs:

- https://sources.debian.net/src/libxinerama/2:1.1.3-1/ (for browsing the source)
- https://sources.debian.net/src/libxinerama/2:1.1.3-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libxinerama/2:1.1.3-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libxml2=2.9.4+dfsg1-4`

Binary Packages:

- `libxml2:amd64=2.9.4+dfsg1-4`
- `libxml2-dev:amd64=2.9.4+dfsg1-4`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxml2=2.9.4+dfsg1-4
'http://deb.debian.org/debian/pool/main/libx/libxml2/libxml2_2.9.4+dfsg1-4.dsc' libxml2_2.9.4+dfsg1-4.dsc 2968 SHA256:981af9b15a1a2046516cf6653c5fbc16cd56d2b01a22d2f9342f021db23d6970
'http://deb.debian.org/debian/pool/main/libx/libxml2/libxml2_2.9.4+dfsg1.orig.tar.xz' libxml2_2.9.4+dfsg1.orig.tar.xz 2446412 SHA256:a74ad55e346aa0b2b41903e66d21f8f3d2a736b3f41e32496376861ab484184e
'http://deb.debian.org/debian/pool/main/libx/libxml2/libxml2_2.9.4+dfsg1-4.debian.tar.xz' libxml2_2.9.4+dfsg1-4.debian.tar.xz 34072 SHA256:8597aee686c4e10f6c80fc8d60fdc4a32b8fffbf2f13f1e25c54672b731f00dc
```

Other potentially useful URLs:

- https://sources.debian.net/src/libxml2/2.9.4+dfsg1-4/ (for browsing the source)
- https://sources.debian.net/src/libxml2/2.9.4+dfsg1-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libxml2/2.9.4+dfsg1-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libxpm=1:3.5.12-1`

Binary Packages:

- `libxpm4:amd64=1:3.5.12-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxpm=1:3.5.12-1
'http://deb.debian.org/debian/pool/main/libx/libxpm/libxpm_3.5.12-1.dsc' libxpm_3.5.12-1.dsc 2061 SHA256:1b5d07d820d656030d0f79a15a0652f258c9d2be0cd6064ec37c40853906f7e8
'http://deb.debian.org/debian/pool/main/libx/libxpm/libxpm_3.5.12.orig.tar.gz' libxpm_3.5.12.orig.tar.gz 529302 SHA256:2523acc780eac01db5163267b36f5b94374bfb0de26fc0b5a7bee76649fd8501
'http://deb.debian.org/debian/pool/main/libx/libxpm/libxpm_3.5.12-1.diff.gz' libxpm_3.5.12-1.diff.gz 9458 SHA256:4103400f8d73d0ec567f87e8aa9824c4a07d068e81da6efe54fb535ec897e326
```

Other potentially useful URLs:

- https://sources.debian.net/src/libxpm/1:3.5.12-1/ (for browsing the source)
- https://sources.debian.net/src/libxpm/1:3.5.12-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libxpm/1:3.5.12-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libxrandr=2:1.5.1-1`

Binary Packages:

- `libxrandr2:amd64=2:1.5.1-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxrandr=2:1.5.1-1
'http://deb.debian.org/debian/pool/main/libx/libxrandr/libxrandr_1.5.1-1.dsc' libxrandr_1.5.1-1.dsc 2046 SHA256:0d7102ab75fdfe06534e842d5dcac8430614c61a061ab12794e2285712b0b103
'http://deb.debian.org/debian/pool/main/libx/libxrandr/libxrandr_1.5.1.orig.tar.gz' libxrandr_1.5.1.orig.tar.gz 388607 SHA256:2baa7fb3eca78fe7e11a09b373ba898b717f7eeba4a4bfd68187e04b4789b0d3
'http://deb.debian.org/debian/pool/main/libx/libxrandr/libxrandr_1.5.1-1.diff.gz' libxrandr_1.5.1-1.diff.gz 16386 SHA256:42262cbc2117ea559a4e16a02c6ea6478554aa2128d9fe1e141da07006612a1d
```

Other potentially useful URLs:

- https://sources.debian.net/src/libxrandr/2:1.5.1-1/ (for browsing the source)
- https://sources.debian.net/src/libxrandr/2:1.5.1-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libxrandr/2:1.5.1-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libxrender=1:0.9.10-1`

Binary Packages:

- `libxrender-dev:amd64=1:0.9.10-1`
- `libxrender1:amd64=1:0.9.10-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxrender=1:0.9.10-1
'http://deb.debian.org/debian/pool/main/libx/libxrender/libxrender_0.9.10-1.dsc' libxrender_0.9.10-1.dsc 2064 SHA256:95d6471218b44f4e60c48cea60cfb4865bbe861530add23f6c859515bee92dbd
'http://deb.debian.org/debian/pool/main/libx/libxrender/libxrender_0.9.10.orig.tar.gz' libxrender_0.9.10.orig.tar.gz 373717 SHA256:770527cce42500790433df84ec3521e8bf095dfe5079454a92236494ab296adf
'http://deb.debian.org/debian/pool/main/libx/libxrender/libxrender_0.9.10-1.diff.gz' libxrender_0.9.10-1.diff.gz 15399 SHA256:ff56a0a00119383adc5f1731e86155ae5c2de069e1d059a9da1d777917430588
```

Other potentially useful URLs:

- https://sources.debian.net/src/libxrender/1:0.9.10-1/ (for browsing the source)
- https://sources.debian.net/src/libxrender/1:0.9.10-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libxrender/1:0.9.10-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libxslt=1.1.29-2.1`

Binary Packages:

- `libxslt1-dev:amd64=1.1.29-2.1`
- `libxslt1.1:amd64=1.1.29-2.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxslt=1.1.29-2.1
'http://deb.debian.org/debian/pool/main/libx/libxslt/libxslt_1.1.29-2.1.dsc' libxslt_1.1.29-2.1.dsc 2535 SHA256:8823c0cb209943fb1a3f6761b9a1b3c49c0348da3aa7a67ff9e09760c0976410
'http://deb.debian.org/debian/pool/main/libx/libxslt/libxslt_1.1.29.orig.tar.gz' libxslt_1.1.29.orig.tar.gz 3428524 SHA256:b5976e3857837e7617b29f2249ebb5eeac34e249208d31f1fbf7a6ba7a4090ce
'http://deb.debian.org/debian/pool/main/libx/libxslt/libxslt_1.1.29-2.1.debian.tar.xz' libxslt_1.1.29-2.1.debian.tar.xz 28548 SHA256:93ef76669dae1bdfdd5f60418e29ccda60c7b693b67d0da81e7d12ffb6d25085
```

Other potentially useful URLs:

- https://sources.debian.net/src/libxslt/1.1.29-2.1/ (for browsing the source)
- https://sources.debian.net/src/libxslt/1.1.29-2.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libxslt/1.1.29-2.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libxt=1:1.1.5-1`

Binary Packages:

- `libxt-dev:amd64=1:1.1.5-1`
- `libxt6:amd64=1:1.1.5-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxt=1:1.1.5-1
'http://deb.debian.org/debian/pool/main/libx/libxt/libxt_1.1.5-1.dsc' libxt_1.1.5-1.dsc 2109 SHA256:f44ae1393c9fd02c0b3dd03576c7b26e6c7b09de3271a87e018efadeed311639
'http://deb.debian.org/debian/pool/main/libx/libxt/libxt_1.1.5.orig.tar.gz' libxt_1.1.5.orig.tar.gz 962169 SHA256:b59bee38a9935565fa49dc1bfe84cb30173e2e07e1dcdf801430d4b54eb0caa3
'http://deb.debian.org/debian/pool/main/libx/libxt/libxt_1.1.5-1.diff.gz' libxt_1.1.5-1.diff.gz 14462 SHA256:822fe813d1ea9213e6fde91cbb607c0b6874341dc19b77b0f6649b8be8472d82
```

Other potentially useful URLs:

- https://sources.debian.net/src/libxt/1:1.1.5-1/ (for browsing the source)
- https://sources.debian.net/src/libxt/1:1.1.5-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libxt/1:1.1.5-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libyaml=0.1.7-2`

Binary Packages:

- `libyaml-0-2:amd64=0.1.7-2`
- `libyaml-dev:amd64=0.1.7-2`

Licenses: (parsed from: `/usr/share/doc/libyaml-0-2/copyright`, `/usr/share/doc/libyaml-dev/copyright`)

- `Expat`
- `permissive`

Source:

```console
$ apt-get source -qq --print-uris libyaml=0.1.7-2
'http://deb.debian.org/debian/pool/main/liby/libyaml/libyaml_0.1.7-2.dsc' libyaml_0.1.7-2.dsc 1820 SHA256:f2e599adcf8336c4be374987112a0c823b4609dc0f5a944e5827651241d91645
'http://deb.debian.org/debian/pool/main/liby/libyaml/libyaml_0.1.7.orig.tar.gz' libyaml_0.1.7.orig.tar.gz 527518 SHA256:8088e457264a98ba451a90b8661fcb4f9d6f478f7265d48322a196cec2480729
'http://deb.debian.org/debian/pool/main/liby/libyaml/libyaml_0.1.7-2.debian.tar.xz' libyaml_0.1.7-2.debian.tar.xz 4016 SHA256:6fc7065491dd6f86b46e6f231ae8ab60f8aafbef2dcf4721598644024485b801
```

Other potentially useful URLs:

- https://sources.debian.net/src/libyaml/0.1.7-2/ (for browsing the source)
- https://sources.debian.net/src/libyaml/0.1.7-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libyaml/0.1.7-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `linux=4.12.12-2`

Binary Packages:

- `linux-libc-dev:amd64=4.12.12-2`

Licenses: (parsed from: `/usr/share/doc/linux-libc-dev/copyright`)

- `CRYPTOGAMS`
- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `Unicode-data`
- `X11 Dual License`
- `Xen-interface`

Source:

```console
$ apt-get source -qq --print-uris linux=4.12.12-2
'http://deb.debian.org/debian/pool/main/l/linux/linux_4.12.12-2.dsc' linux_4.12.12-2.dsc 124913 SHA256:119c8a2a15e7a2c446df5de2e09c46bd0e64753de89eb58ad9326c8403aedb26
'http://deb.debian.org/debian/pool/main/l/linux/linux_4.12.12.orig.tar.xz' linux_4.12.12.orig.tar.xz 100222740 SHA256:851b24ad550e4bfc18cb07e2ee0e4d137b81027c7a7906c69f8d250086ccea11
'http://deb.debian.org/debian/pool/main/l/linux/linux_4.12.12-2.debian.tar.xz' linux_4.12.12-2.debian.tar.xz 948192 SHA256:e9126612af88d39c982f0a4e985b6f0483dfe318e170c091476fec8e15289841
```

Other potentially useful URLs:

- https://sources.debian.net/src/linux/4.12.12-2/ (for browsing the source)
- https://sources.debian.net/src/linux/4.12.12-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/linux/4.12.12-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `lsb=9.20170808`

Binary Packages:

- `lsb-base=9.20170808`

Licenses: (parsed from: `/usr/share/doc/lsb-base/copyright`)

- `BSD-3-clause`
- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris lsb=9.20170808
'http://deb.debian.org/debian/pool/main/l/lsb/lsb_9.20170808.dsc' lsb_9.20170808.dsc 1597 SHA256:d767e622530f73df4f041f7bace54412a6da3d66ddcc73df7913cdebdbf258a9
'http://deb.debian.org/debian/pool/main/l/lsb/lsb_9.20170808.tar.xz' lsb_9.20170808.tar.xz 42120 SHA256:ec9cb022cedcdf34c5b8dc2dca530777ce3f491ad364222557691e87807729b1
```

Other potentially useful URLs:

- https://sources.debian.net/src/lsb/9.20170808/ (for browsing the source)
- https://sources.debian.net/src/lsb/9.20170808/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/lsb/9.20170808/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `lz4=0.0~r131-2`

Binary Packages:

- `liblz4-1:amd64=0.0~r131-2+b1`

Licenses: (parsed from: `/usr/share/doc/liblz4-1/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris lz4=0.0~r131-2
'http://deb.debian.org/debian/pool/main/l/lz4/lz4_0.0~r131-2.dsc' lz4_0.0~r131-2.dsc 1973 SHA256:304cf9dddee387377929adf3f2cef0ae19fb2e56b6cc9eab05798845b58bd9b6
'http://deb.debian.org/debian/pool/main/l/lz4/lz4_0.0~r131.orig.tar.gz' lz4_0.0~r131.orig.tar.gz 133784 SHA256:9d4d00614d6b9dec3114b33d1224b6262b99ace24434c53487a0c8fd0b18cfed
'http://deb.debian.org/debian/pool/main/l/lz4/lz4_0.0~r131-2.debian.tar.xz' lz4_0.0~r131-2.debian.tar.xz 4936 SHA256:966df055dd8fa7f292c283452b43a5d2d2047d542fe49e97025006e69525e224
```

Other potentially useful URLs:

- https://sources.debian.net/src/lz4/0.0~r131-2/ (for browsing the source)
- https://sources.debian.net/src/lz4/0.0~r131-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/lz4/0.0~r131-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `lzo2=2.08-1.2`

Binary Packages:

- `liblzo2-2:amd64=2.08-1.2+b2`

Licenses: (parsed from: `/usr/share/doc/liblzo2-2/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris lzo2=2.08-1.2
'http://deb.debian.org/debian/pool/main/l/lzo2/lzo2_2.08-1.2.dsc' lzo2_2.08-1.2.dsc 1804 SHA256:09eabe81d6f631a29cc603843b27ab914704726a1400a2219cf83b1da4e72892
'http://deb.debian.org/debian/pool/main/l/lzo2/lzo2_2.08.orig.tar.gz' lzo2_2.08.orig.tar.gz 589045 SHA256:ac1b3e4dee46febe9fd28737eb7f5692d3232ef1a01da10444394c3d47536614
'http://deb.debian.org/debian/pool/main/l/lzo2/lzo2_2.08-1.2.debian.tar.xz' lzo2_2.08-1.2.debian.tar.xz 5996 SHA256:5a9aa3a2432f5d4f689b24c64ea3daec7646e736da37721388ae88b670dd99bc
```

Other potentially useful URLs:

- https://sources.debian.net/src/lzo2/2.08-1.2/ (for browsing the source)
- https://sources.debian.net/src/lzo2/2.08-1.2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/lzo2/2.08-1.2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `m4=1.4.18-1`

Binary Packages:

- `m4=1.4.18-1`

Licenses: (parsed from: `/usr/share/doc/m4/copyright`)

- `GFDL`
- `GPL`

Source:

```console
$ apt-get source -qq --print-uris m4=1.4.18-1
'http://deb.debian.org/debian/pool/main/m/m4/m4_1.4.18-1.dsc' m4_1.4.18-1.dsc 1426 SHA256:83a6c5e4b94aa47634b7c988fa485155c01120c17682865e6f032de9adf1090c
'http://deb.debian.org/debian/pool/main/m/m4/m4_1.4.18.orig.tar.xz' m4_1.4.18.orig.tar.xz 1207688 SHA256:f2c1e86ca0a404ff281631bdc8377638992744b175afb806e25871a24a934e07
'http://deb.debian.org/debian/pool/main/m/m4/m4_1.4.18-1.debian.tar.xz' m4_1.4.18-1.debian.tar.xz 15784 SHA256:55de78acb0272fd6e2637ab933114e64eefa58ba1e97b063629453ae1e163fff
```

Other potentially useful URLs:

- https://sources.debian.net/src/m4/1.4.18-1/ (for browsing the source)
- https://sources.debian.net/src/m4/1.4.18-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/m4/1.4.18-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `make-dfsg=4.1-9.1`

Binary Packages:

- `make=4.1-9.1`

Licenses: (parsed from: `/usr/share/doc/make/copyright`)

- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris make-dfsg=4.1-9.1
'http://deb.debian.org/debian/pool/main/m/make-dfsg/make-dfsg_4.1-9.1.dsc' make-dfsg_4.1-9.1.dsc 2037 SHA256:3527e91633b0d2830a52f3b85229b2f8bdec5e1e5b77bbff95b20317757ab3a3
'http://deb.debian.org/debian/pool/main/m/make-dfsg/make-dfsg_4.1.orig.tar.gz' make-dfsg_4.1.orig.tar.gz 1350231 SHA256:b3ed04fb6718289e4a430afbe2df6ecba9177aad9f6d09aaf38e5409262ca8a3
'http://deb.debian.org/debian/pool/main/m/make-dfsg/make-dfsg_4.1-9.1.diff.gz' make-dfsg_4.1-9.1.diff.gz 45452 SHA256:ec9d39ed253808378aeb91bb2c34bbd177637ed197682e093c3aadfb97b338a3
```

Other potentially useful URLs:

- https://sources.debian.net/src/make-dfsg/4.1-9.1/ (for browsing the source)
- https://sources.debian.net/src/make-dfsg/4.1-9.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/make-dfsg/4.1-9.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `mariadb-10.1=10.1.26-1`

Binary Packages:

- `libmariadbclient-dev=10.1.26-1`
- `libmariadbclient-dev-compat:amd64=10.1.26-1`
- `libmariadbclient18:amd64=10.1.26-1`

Licenses: (parsed from: `/usr/share/doc/libmariadbclient-dev/copyright`, `/usr/share/doc/libmariadbclient-dev-compat/copyright`, `/usr/share/doc/libmariadbclient18/copyright`)

- `Artistic`
- `BSD-2-clause`
- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`
- `GPL-2+-with-bison-exception`
- `GPL-3`
- `GPL-3+`
- `GPL-3+-with-bison-exception`
- `GPL-verbatim`
- `LGPL`
- `LGPL-2`
- `LGPL-2.1`
- `LGPL-2.1+`
- `MIT/X11`
- `SWsoft`
- `public-domain`
- `unlimited-free-doc`
- `zlib/libpng`

Source:

```console
$ apt-get source -qq --print-uris mariadb-10.1=10.1.26-1
'http://deb.debian.org/debian/pool/main/m/mariadb-10.1/mariadb-10.1_10.1.26-1.dsc' mariadb-10.1_10.1.26-1.dsc 4448 SHA256:bf3a2bd5a44b24f7ccf9d8987483f79cdb7e572cfc1489045853283abd6f3ff9
'http://deb.debian.org/debian/pool/main/m/mariadb-10.1/mariadb-10.1_10.1.26.orig.tar.gz' mariadb-10.1_10.1.26.orig.tar.gz 61887132 SHA256:ba88b1cb9967dea2909938a34ba89373b162b0d83e5c98a0f1c94540156bf73d
'http://deb.debian.org/debian/pool/main/m/mariadb-10.1/mariadb-10.1_10.1.26-1.debian.tar.xz' mariadb-10.1_10.1.26-1.debian.tar.xz 228624 SHA256:b5acdea51eaeee7ab3382c10fac6a10c1a0bd58e4cf62766fd7ad1b17713c2a3
```

Other potentially useful URLs:

- https://sources.debian.net/src/mariadb-10.1/10.1.26-1/ (for browsing the source)
- https://sources.debian.net/src/mariadb-10.1/10.1.26-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/mariadb-10.1/10.1.26-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `mawk=1.3.3-17`

Binary Packages:

- `mawk=1.3.3-17+b3`

Licenses: (parsed from: `/usr/share/doc/mawk/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris mawk=1.3.3-17
'http://deb.debian.org/debian/pool/main/m/mawk/mawk_1.3.3-17.dsc' mawk_1.3.3-17.dsc 1801 SHA256:f98ce6e153e8ac1faf8165bbf77447a4279313f1c18f6bfeec0c5ce35e4b9c03
'http://deb.debian.org/debian/pool/main/m/mawk/mawk_1.3.3.orig.tar.gz' mawk_1.3.3.orig.tar.gz 209942 SHA256:32649c46063d4ef0777a12ae6e9a26bcc920833d54e1abca7edb8d37481e7485
'http://deb.debian.org/debian/pool/main/m/mawk/mawk_1.3.3-17.diff.gz' mawk_1.3.3-17.diff.gz 63506 SHA256:13cb66b6eb5ee654d5626621d5ef476ede6b0bebac18ce765516de810e58490c
```

Other potentially useful URLs:

- https://sources.debian.net/src/mawk/1.3.3-17/ (for browsing the source)
- https://sources.debian.net/src/mawk/1.3.3-17/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/mawk/1.3.3-17/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `mercurial=4.3.1-3`

Binary Packages:

- `mercurial=4.3.1-3`
- `mercurial-common=4.3.1-3`

Licenses: (parsed from: `/usr/share/doc/mercurial/copyright`, `/usr/share/doc/mercurial-common/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris mercurial=4.3.1-3
'http://deb.debian.org/debian/pool/main/m/mercurial/mercurial_4.3.1-3.dsc' mercurial_4.3.1-3.dsc 2225 SHA256:26d0e605823e9c7abc5cb34c9e9af6f28f4021d4eb8440a0bd5501cd55e3bf1c
'http://deb.debian.org/debian/pool/main/m/mercurial/mercurial_4.3.1.orig.tar.gz' mercurial_4.3.1.orig.tar.gz 5475042 SHA256:2b12f02e3a452adff4ec9cf007017bab0cadb3f37eaf12f4b25a662df73618a2
'http://deb.debian.org/debian/pool/main/m/mercurial/mercurial_4.3.1-3.debian.tar.xz' mercurial_4.3.1-3.debian.tar.xz 54916 SHA256:196363132773e9f32766c99a4abb1844b0e216093df84044aac341f735d6559c
```

Other potentially useful URLs:

- https://sources.debian.net/src/mercurial/4.3.1-3/ (for browsing the source)
- https://sources.debian.net/src/mercurial/4.3.1-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/mercurial/4.3.1-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `mime-support=3.60`

Binary Packages:

- `mime-support=3.60`

Licenses: (parsed from: `/usr/share/doc/mime-support/copyright`)

- `Bellcore`
- `ad-hoc`

Source:

```console
$ apt-get source -qq --print-uris mime-support=3.60
'http://deb.debian.org/debian/pool/main/m/mime-support/mime-support_3.60.dsc' mime-support_3.60.dsc 1605 SHA256:1c3c61f6943b130ee6518facac394b733661975955b84af640b78fa354d7595d
'http://deb.debian.org/debian/pool/main/m/mime-support/mime-support_3.60.tar.gz' mime-support_3.60.tar.gz 36840 SHA256:f31d81f68dc007f56567cc14fb3b2effbd42d1dd087e414508e14e33d1a6a3a4
```

Other potentially useful URLs:

- https://sources.debian.net/src/mime-support/3.60/ (for browsing the source)
- https://sources.debian.net/src/mime-support/3.60/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/mime-support/3.60/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `mpclib3=1.0.3-1`

Binary Packages:

- `libmpc3:amd64=1.0.3-1+b2`

Licenses: (parsed from: `/usr/share/doc/libmpc3/copyright`)

- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/mpclib3/1.0.3-1/


### `dpkg` source package: `mpdecimal=2.4.2-1`

Binary Packages:

- `libmpdec2:amd64=2.4.2-1`

Licenses: (parsed from: `/usr/share/doc/libmpdec2/copyright`)

- `BSD`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris mpdecimal=2.4.2-1
'http://deb.debian.org/debian/pool/main/m/mpdecimal/mpdecimal_2.4.2-1.dsc' mpdecimal_2.4.2-1.dsc 1893 SHA256:5bc782829357ebc9f0c12084642319e5ac89784a119433f8bfba7a11008d7c13
'http://deb.debian.org/debian/pool/main/m/mpdecimal/mpdecimal_2.4.2.orig.tar.gz' mpdecimal_2.4.2.orig.tar.gz 2271529 SHA256:83c628b90f009470981cf084c5418329c88b19835d8af3691b930afccb7d79c7
'http://deb.debian.org/debian/pool/main/m/mpdecimal/mpdecimal_2.4.2-1.debian.tar.xz' mpdecimal_2.4.2-1.debian.tar.xz 5172 SHA256:b95fb775fd04a7ad34fa5bd2c222b49ee2dfd7f0e15295dbd3f7fb86a9b0194b
```

Other potentially useful URLs:

- https://sources.debian.net/src/mpdecimal/2.4.2-1/ (for browsing the source)
- https://sources.debian.net/src/mpdecimal/2.4.2-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/mpdecimal/2.4.2-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `mpfr4=3.1.6-1`

Binary Packages:

- `libmpfr4:amd64=3.1.6-1`

Licenses: (parsed from: `/usr/share/doc/libmpfr4/copyright`)

- `GFDL-1.2`
- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris mpfr4=3.1.6-1
'http://deb.debian.org/debian/pool/main/m/mpfr4/mpfr4_3.1.6-1.dsc' mpfr4_3.1.6-1.dsc 2004 SHA256:449a287fa9448826c591d87fe92b702e11e6e1cb7be88ef50f36dc7769c92c33
'http://deb.debian.org/debian/pool/main/m/mpfr4/mpfr4_3.1.6.orig.tar.xz' mpfr4_3.1.6.orig.tar.xz 1133672 SHA256:7a62ac1a04408614fccdc506e4844b10cf0ad2c2b1677097f8f35d3a1344a950
'http://deb.debian.org/debian/pool/main/m/mpfr4/mpfr4_3.1.6-1.debian.tar.xz' mpfr4_3.1.6-1.debian.tar.xz 9724 SHA256:1ce306a388ab312eb1c62f4c52dc468ae55d8205e124d19eb231ef7d42fc836a
```

Other potentially useful URLs:

- https://sources.debian.net/src/mpfr4/3.1.6-1/ (for browsing the source)
- https://sources.debian.net/src/mpfr4/3.1.6-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/mpfr4/3.1.6-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `mysql-defaults=1.0.3`

Binary Packages:

- `default-libmysqlclient-dev:amd64=1.0.3`
- `mysql-common=5.8+1.0.3`

Licenses: (parsed from: `/usr/share/doc/default-libmysqlclient-dev/copyright`, `/usr/share/doc/mysql-common/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris mysql-defaults=1.0.3
'http://deb.debian.org/debian/pool/main/m/mysql-defaults/mysql-defaults_1.0.3.dsc' mysql-defaults_1.0.3.dsc 2231 SHA256:8cf20b019808e0dba0e83a59718449d4e16f732b4e7971ba9198d4e6efb79c72
'http://deb.debian.org/debian/pool/main/m/mysql-defaults/mysql-defaults_1.0.3.tar.xz' mysql-defaults_1.0.3.tar.xz 5824 SHA256:2b396003583dea51ff451d59dab3a72bfd818bd99fa15feac384e4d978d1ae0e
```

Other potentially useful URLs:

- https://sources.debian.net/src/mysql-defaults/1.0.3/ (for browsing the source)
- https://sources.debian.net/src/mysql-defaults/1.0.3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/mysql-defaults/1.0.3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `ncurses=6.0+20170902-1`

Binary Packages:

- `libncurses5:amd64=6.0+20170902-1`
- `libncurses5-dev:amd64=6.0+20170902-1`
- `libncursesw5:amd64=6.0+20170902-1`
- `libtinfo-dev:amd64=6.0+20170902-1`
- `libtinfo5:amd64=6.0+20170902-1`
- `ncurses-base=6.0+20170902-1`
- `ncurses-bin=6.0+20170902-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris ncurses=6.0+20170902-1
'http://deb.debian.org/debian/pool/main/n/ncurses/ncurses_6.0+20170902-1.dsc' ncurses_6.0+20170902-1.dsc 4021 SHA256:6d57899b77e12869ef69d953c7b0af978a46091899401196cd2437c5825d27f4
'http://deb.debian.org/debian/pool/main/n/ncurses/ncurses_6.0+20170902.orig.tar.gz' ncurses_6.0+20170902.orig.tar.gz 3322744 SHA256:2437043fe3bb6a0deebe758a9744ee8e9d2e0b272ae2cb0d978804f2f5237ab2
'http://deb.debian.org/debian/pool/main/n/ncurses/ncurses_6.0+20170902.orig.tar.gz.asc' ncurses_6.0+20170902.orig.tar.gz.asc 267 SHA256:10a8ea1bca1f94f7c0a95b2789352a4d279802065400d7a680591100ab75469c
'http://deb.debian.org/debian/pool/main/n/ncurses/ncurses_6.0+20170902-1.debian.tar.xz' ncurses_6.0+20170902-1.debian.tar.xz 53496 SHA256:b8bd83ec458ab21bb038addc846297206ad9f636e3a8eb7cbab5c5879071dcb2
```

Other potentially useful URLs:

- https://sources.debian.net/src/ncurses/6.0+20170902-1/ (for browsing the source)
- https://sources.debian.net/src/ncurses/6.0+20170902-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/ncurses/6.0+20170902-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `netbase=5.4`

Binary Packages:

- `netbase=5.4`

Licenses: (parsed from: `/usr/share/doc/netbase/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris netbase=5.4
'http://deb.debian.org/debian/pool/main/n/netbase/netbase_5.4.dsc' netbase_5.4.dsc 1326 SHA256:ebe29d45e65b661d64636cbce3840997d8079cf338efbfa347b4c73ed2831b7b
'http://deb.debian.org/debian/pool/main/n/netbase/netbase_5.4.tar.xz' netbase_5.4.tar.xz 31524 SHA256:66ff73d2d162e2d49db43988d8b8cd328cf7fffca042db73397f14c71825e80d
```

Other potentially useful URLs:

- https://sources.debian.net/src/netbase/5.4/ (for browsing the source)
- https://sources.debian.net/src/netbase/5.4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/netbase/5.4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `nettle=3.3-1`

Binary Packages:

- `libhogweed4:amd64=3.3-1+b1`
- `libnettle6:amd64=3.3-1+b1`

Licenses: (parsed from: `/usr/share/doc/libhogweed4/copyright`, `/usr/share/doc/libnettle6/copyright`)

- `GAP`
- `GPL`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with Autoconf exception`
- `LGPL`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1+`
- `other`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/nettle/3.3-1/


### `dpkg` source package: `nghttp2=1.25.0-1`

Binary Packages:

- `libnghttp2-14:amd64=1.25.0-1`

Licenses: (parsed from: `/usr/share/doc/libnghttp2-14/copyright`)

- `BSD-2-clause`
- `Expat`
- `GPL-3`
- `GPL-3+ with autoconf exception`
- `MIT`
- `SIL-OFL-1.1`
- `all-permissive`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/nghttp2/1.25.0-1/


### `dpkg` source package: `npth=1.5-2`

Binary Packages:

- `libnpth0:amd64=1.5-2`

Licenses: (parsed from: `/usr/share/doc/libnpth0/copyright`)

- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris npth=1.5-2
'http://deb.debian.org/debian/pool/main/n/npth/npth_1.5-2.dsc' npth_1.5-2.dsc 1949 SHA256:6f4e78f1ccb9ef5f062f973f937ea27e36e168a41c7b5c0d65d4775b0daf676f
'http://deb.debian.org/debian/pool/main/n/npth/npth_1.5.orig.tar.bz2' npth_1.5.orig.tar.bz2 299308 SHA256:294a690c1f537b92ed829d867bee537e46be93fbd60b16c04630fbbfcd9db3c2
'http://deb.debian.org/debian/pool/main/n/npth/npth_1.5-2.debian.tar.xz' npth_1.5-2.debian.tar.xz 10416 SHA256:c1140dacd332ca38dcc4ae6f0cb69baab25474fd58370a6432f55c2d52bf1e6d
```

Other potentially useful URLs:

- https://sources.debian.net/src/npth/1.5-2/ (for browsing the source)
- https://sources.debian.net/src/npth/1.5-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/npth/1.5-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `openexr=2.2.0-11.1`

Binary Packages:

- `libopenexr-dev=2.2.0-11.1`
- `libopenexr22:amd64=2.2.0-11.1`

Licenses: (parsed from: `/usr/share/doc/libopenexr-dev/copyright`, `/usr/share/doc/libopenexr22/copyright`)

- `openexr`

Source:

```console
$ apt-get source -qq --print-uris openexr=2.2.0-11.1
'http://deb.debian.org/debian/pool/main/o/openexr/openexr_2.2.0-11.1.dsc' openexr_2.2.0-11.1.dsc 2439 SHA256:8d987878d616cf3c089042b2becedeb06b5d599936194ab92e5a5b44d663bf0f
'http://deb.debian.org/debian/pool/main/o/openexr/openexr_2.2.0.orig.tar.gz' openexr_2.2.0.orig.tar.gz 14489661 SHA256:36a012f6c43213f840ce29a8b182700f6cf6b214bea0d5735594136b44914231
'http://deb.debian.org/debian/pool/main/o/openexr/openexr_2.2.0-11.1.debian.tar.xz' openexr_2.2.0-11.1.debian.tar.xz 17344 SHA256:d0499a25e6307dea5f985cb11a00045b7f22b71f4b86bca00b133be4acfa8a4e
```

Other potentially useful URLs:

- https://sources.debian.net/src/openexr/2.2.0-11.1/ (for browsing the source)
- https://sources.debian.net/src/openexr/2.2.0-11.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/openexr/2.2.0-11.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `openjpeg2=2.1.2-1.3`

Binary Packages:

- `libopenjp2-7:amd64=2.1.2-1.3`
- `libopenjp2-7-dev=2.1.2-1.3`

Licenses: (parsed from: `/usr/share/doc/libopenjp2-7/copyright`, `/usr/share/doc/libopenjp2-7-dev/copyright`)

- `BSD-2`
- `BSD-3`
- `LIBPNG`
- `LIBTIFF`
- `LIBTIFF-GLARSON`
- `LIBTIFF-PIXAR`
- `MIT`
- `ZLIB`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/openjpeg2/2.1.2-1.3/


### `dpkg` source package: `openldap=2.4.45+dfsg-1`

Binary Packages:

- `libldap-2.4-2:amd64=2.4.45+dfsg-1`
- `libldap-common=2.4.45+dfsg-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris openldap=2.4.45+dfsg-1
'http://deb.debian.org/debian/pool/main/o/openldap/openldap_2.4.45+dfsg-1.dsc' openldap_2.4.45+dfsg-1.dsc 2769 SHA256:a9544b9d02dec7eb101b0eb4a71d9feaa402c9f3e12ab2398c6408c84bd93212
'http://deb.debian.org/debian/pool/main/o/openldap/openldap_2.4.45+dfsg.orig.tar.gz' openldap_2.4.45+dfsg.orig.tar.gz 4846458 SHA256:d51c70423aa0554d454fd3d43e7f2e940523b4ef07979305b48c233ae44b2b32
'http://deb.debian.org/debian/pool/main/o/openldap/openldap_2.4.45+dfsg-1.debian.tar.xz' openldap_2.4.45+dfsg-1.debian.tar.xz 162956 SHA256:7edec92185c74081a1fcbe934ccba951fb4a43075061aac40168a489f7989f5e
```

Other potentially useful URLs:

- https://sources.debian.net/src/openldap/2.4.45+dfsg-1/ (for browsing the source)
- https://sources.debian.net/src/openldap/2.4.45+dfsg-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/openldap/2.4.45+dfsg-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `openssh=1:7.5p1-10`

Binary Packages:

- `openssh-client=1:7.5p1-10`

Licenses: (parsed from: `/usr/share/doc/openssh-client/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `Beer-ware`
- `CORE-SDI-BSD-style`
- `Expat-with-advertising-restriction`
- `Mazieres-BSD-style`
- `OpenSSH`
- `Powell-BSD-style`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris openssh=1:7.5p1-10
'http://deb.debian.org/debian/pool/main/o/openssh/openssh_7.5p1-10.dsc' openssh_7.5p1-10.dsc 2856 SHA256:b4782d7383b5dd7e23a71a28065fd15e6b8aa8cd052f8f45d0078f053efa81be
'http://deb.debian.org/debian/pool/main/o/openssh/openssh_7.5p1.orig.tar.gz' openssh_7.5p1.orig.tar.gz 1510857 SHA256:9846e3c5fab9f0547400b4d2c017992f914222b3fd1f8eee6c7dc6bc5e59f9f0
'http://deb.debian.org/debian/pool/main/o/openssh/openssh_7.5p1-10.debian.tar.xz' openssh_7.5p1-10.debian.tar.xz 159252 SHA256:2eda9f24b25b306cae15a8080018ee4f06679e98e2574725459be0d7e0c7db53
```

Other potentially useful URLs:

- https://sources.debian.net/src/openssh/1:7.5p1-10/ (for browsing the source)
- https://sources.debian.net/src/openssh/1:7.5p1-10/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/openssh/1:7.5p1-10/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `openssl1.0=1.0.2l-2`

Binary Packages:

- `libssl1.0.2:amd64=1.0.2l-2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris openssl1.0=1.0.2l-2
'http://deb.debian.org/debian/pool/main/o/openssl1.0/openssl1.0_1.0.2l-2.dsc' openssl1.0_1.0.2l-2.dsc 2529 SHA256:51aa8afa8157b209a647f5476e72ba06720c33b8f6e46be79e91a0dc9349efcf
'http://deb.debian.org/debian/pool/main/o/openssl1.0/openssl1.0_1.0.2l.orig.tar.gz' openssl1.0_1.0.2l.orig.tar.gz 5365054 SHA256:ce07195b659e75f4e1db43552860070061f156a98bb37b672b101ba6e3ddf30c
'http://deb.debian.org/debian/pool/main/o/openssl1.0/openssl1.0_1.0.2l.orig.tar.gz.asc' openssl1.0_1.0.2l.orig.tar.gz.asc 455 SHA256:ad459d4de6c30c1889272e38144598847c8ba8e5f0892797543607e8d6d9be5f
'http://deb.debian.org/debian/pool/main/o/openssl1.0/openssl1.0_1.0.2l-2.debian.tar.xz' openssl1.0_1.0.2l-2.debian.tar.xz 75888 SHA256:8e0dc8d55df49bf85cc8a991774fbdf4186886307acc167054355edd7c77ed1e
```

Other potentially useful URLs:

- https://sources.debian.net/src/openssl1.0/1.0.2l-2/ (for browsing the source)
- https://sources.debian.net/src/openssl1.0/1.0.2l-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/openssl1.0/1.0.2l-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `openssl=1.1.0f-5`

Binary Packages:

- `libssl-dev:amd64=1.1.0f-5`
- `libssl1.1:amd64=1.1.0f-5`
- `openssl=1.1.0f-5`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris openssl=1.1.0f-5
'http://deb.debian.org/debian/pool/main/o/openssl/openssl_1.1.0f-5.dsc' openssl_1.1.0f-5.dsc 2583 SHA256:44c38165dc9c99d069bb19c510d58778bb79e0530d5967cb74c556999f0b4b7e
'http://deb.debian.org/debian/pool/main/o/openssl/openssl_1.1.0f.orig.tar.gz' openssl_1.1.0f.orig.tar.gz 5278176 SHA256:12f746f3f2493b2f39da7ecf63d7ee19c6ac9ec6a4fcd8c229da8a522cb12765
'http://deb.debian.org/debian/pool/main/o/openssl/openssl_1.1.0f.orig.tar.gz.asc' openssl_1.1.0f.orig.tar.gz.asc 455 SHA256:9f2feb0494ebcc1cf152d95a11bc966cb94bc1957d88650285db3966866801b0
'http://deb.debian.org/debian/pool/main/o/openssl/openssl_1.1.0f-5.debian.tar.xz' openssl_1.1.0f-5.debian.tar.xz 59536 SHA256:7ae7fc632d259f1e4ed5e2475847d31db18d9bc6b96a6a3405a77cff7020b97e
```

Other potentially useful URLs:

- https://sources.debian.net/src/openssl/1.1.0f-5/ (for browsing the source)
- https://sources.debian.net/src/openssl/1.1.0f-5/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/openssl/1.1.0f-5/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `p11-kit=0.23.7-3`

Binary Packages:

- `libp11-kit0:amd64=0.23.7-3`

Licenses: (parsed from: `/usr/share/doc/libp11-kit0/copyright`)

- `BSD-3-Clause`
- `ISC`
- `ISC+IBM`
- `permissive-like-automake-output`
- `same-as-rest-of-p11kit`

Source:

```console
$ apt-get source -qq --print-uris p11-kit=0.23.7-3
'http://deb.debian.org/debian/pool/main/p/p11-kit/p11-kit_0.23.7-3.dsc' p11-kit_0.23.7-3.dsc 2452 SHA256:ce5611bfa9891673edcb5b4ee369da586b2cee214061dff492dc5f6a8fff6092
'http://deb.debian.org/debian/pool/main/p/p11-kit/p11-kit_0.23.7.orig.tar.gz' p11-kit_0.23.7.orig.tar.gz 1087009 SHA256:988e7c86f2641b36702503481292ef0686e6b1c39d80b215699b6dbf1024be41
'http://deb.debian.org/debian/pool/main/p/p11-kit/p11-kit_0.23.7.orig.tar.gz.asc' p11-kit_0.23.7.orig.tar.gz.asc 543 SHA256:7156998e36be4e12e2375518d76a1b1fdf46acbae10dd6bb098c1bd902f0cdad
'http://deb.debian.org/debian/pool/main/p/p11-kit/p11-kit_0.23.7-3.debian.tar.xz' p11-kit_0.23.7-3.debian.tar.xz 21772 SHA256:8dc0b106a69842cc734f8f3c9a1ad6312cd5d1cd318b696cdc76e6ca0c3108b5
```

Other potentially useful URLs:

- https://sources.debian.net/src/p11-kit/0.23.7-3/ (for browsing the source)
- https://sources.debian.net/src/p11-kit/0.23.7-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/p11-kit/0.23.7-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `pam=1.1.8-3.6`

Binary Packages:

- `libpam-modules:amd64=1.1.8-3.6`
- `libpam-modules-bin=1.1.8-3.6`
- `libpam-runtime=1.1.8-3.6`
- `libpam0g:amd64=1.1.8-3.6`

Licenses: (parsed from: `/usr/share/doc/libpam-modules/copyright`, `/usr/share/doc/libpam-modules-bin/copyright`, `/usr/share/doc/libpam-runtime/copyright`, `/usr/share/doc/libpam0g/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris pam=1.1.8-3.6
'http://deb.debian.org/debian/pool/main/p/pam/pam_1.1.8-3.6.dsc' pam_1.1.8-3.6.dsc 2572 SHA256:7bd7a3059c6ea5b97f5ce0460cbe20788f21bc59bd31ef5a28d7968f53373f5f
'http://deb.debian.org/debian/pool/main/p/pam/pam_1.1.8.orig.tar.gz' pam_1.1.8.orig.tar.gz 1892765 SHA256:4183409a450708a976eca5af561dbf4f0490141a08e86e4a1e649c7c1b094876
'http://deb.debian.org/debian/pool/main/p/pam/pam_1.1.8-3.6.diff.gz' pam_1.1.8-3.6.diff.gz 139492 SHA256:beba99299941c5648ff412d75ebd3407e4d769f5e5ab1fce6a5f2e58c40341ae
```

Other potentially useful URLs:

- https://sources.debian.net/src/pam/1.1.8-3.6/ (for browsing the source)
- https://sources.debian.net/src/pam/1.1.8-3.6/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/pam/1.1.8-3.6/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `pango1.0=1.40.12-1`

Binary Packages:

- `libpango-1.0-0:amd64=1.40.12-1`
- `libpangocairo-1.0-0:amd64=1.40.12-1`
- `libpangoft2-1.0-0:amd64=1.40.12-1`

Licenses: (parsed from: `/usr/share/doc/libpango-1.0-0/copyright`, `/usr/share/doc/libpangocairo-1.0-0/copyright`, `/usr/share/doc/libpangoft2-1.0-0/copyright`)

- `LGPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris pango1.0=1.40.12-1
'http://deb.debian.org/debian/pool/main/p/pango1.0/pango1.0_1.40.12-1.dsc' pango1.0_1.40.12-1.dsc 3315 SHA256:21e17cb046cc0823eda025b5be6e88cb8acf00c2e5230699e3456f55e745265d
'http://deb.debian.org/debian/pool/main/p/pango1.0/pango1.0_1.40.12.orig.tar.xz' pango1.0_1.40.12.orig.tar.xz 856228 SHA256:75f1a9a8e4e2b28cbc078b50c1fa927ee4ded994d1ade97c5603e2d1f3161cfc
'http://deb.debian.org/debian/pool/main/p/pango1.0/pango1.0_1.40.12-1.debian.tar.xz' pango1.0_1.40.12-1.debian.tar.xz 27520 SHA256:54a1093a552551e5ae215c2664a4bf80e2b6d9646887d7384184974d72c469d1
```

Other potentially useful URLs:

- https://sources.debian.net/src/pango1.0/1.40.12-1/ (for browsing the source)
- https://sources.debian.net/src/pango1.0/1.40.12-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/pango1.0/1.40.12-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `patch=2.7.5-1`

Binary Packages:

- `patch=2.7.5-1+b2`

Licenses: (parsed from: `/usr/share/doc/patch/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris patch=2.7.5-1
'http://deb.debian.org/debian/pool/main/p/patch/patch_2.7.5-1.dsc' patch_2.7.5-1.dsc 1795 SHA256:909ac12aa395f8b32a4524dcea67207567e99d2560e2a833ba577ec64c4cc1bd
'http://deb.debian.org/debian/pool/main/p/patch/patch_2.7.5.orig.tar.xz' patch_2.7.5.orig.tar.xz 727704 SHA256:fd95153655d6b95567e623843a0e77b81612d502ecf78a489a4aed7867caa299
'http://deb.debian.org/debian/pool/main/p/patch/patch_2.7.5-1.debian.tar.xz' patch_2.7.5-1.debian.tar.xz 8116 SHA256:c5b9797658fdc1c150072fc9568279bd62c591b2fc43fa6d33750a9a4e8f0ddd
```

Other potentially useful URLs:

- https://sources.debian.net/src/patch/2.7.5-1/ (for browsing the source)
- https://sources.debian.net/src/patch/2.7.5-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/patch/2.7.5-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `pcre2=10.22-3`

Binary Packages:

- `libpcre2-8-0:amd64=10.22-3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris pcre2=10.22-3
'http://deb.debian.org/debian/pool/main/p/pcre2/pcre2_10.22-3.dsc' pcre2_10.22-3.dsc 2041 SHA256:c4458656524614e1bbe2992c5452c04eb971c22a2b27e64d64e1034ddcc2562b
'http://deb.debian.org/debian/pool/main/p/pcre2/pcre2_10.22.orig.tar.gz' pcre2_10.22.orig.tar.gz 1985688 SHA256:e44d8a6f31bb33cce01ed43743f464290f1d96f60b5fd838786e632d3624a7bd
'http://deb.debian.org/debian/pool/main/p/pcre2/pcre2_10.22-3.diff.gz' pcre2_10.22-3.diff.gz 4857 SHA256:d48a0afdd9e84aad0fcf2dc0d5e4a66fb2872cce565519371c4882235aad76de
```

Other potentially useful URLs:

- https://sources.debian.net/src/pcre2/10.22-3/ (for browsing the source)
- https://sources.debian.net/src/pcre2/10.22-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/pcre2/10.22-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `pcre3=2:8.39-4`

Binary Packages:

- `libpcre16-3:amd64=2:8.39-4`
- `libpcre3:amd64=2:8.39-4`
- `libpcre3-dev:amd64=2:8.39-4`
- `libpcre32-3:amd64=2:8.39-4`
- `libpcrecpp0v5:amd64=2:8.39-4`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris pcre3=2:8.39-4
'http://deb.debian.org/debian/pool/main/p/pcre3/pcre3_8.39-4.dsc' pcre3_8.39-4.dsc 2224 SHA256:d79722717c869fce3343423d479e3cc0dfe5a31e392f9946a7054a11d395a544
'http://deb.debian.org/debian/pool/main/p/pcre3/pcre3_8.39.orig.tar.bz2' pcre3_8.39.orig.tar.bz2 1560758 SHA256:b858099f82483031ee02092711689e7245586ada49e534a06e678b8ea9549e8b
'http://deb.debian.org/debian/pool/main/p/pcre3/pcre3_8.39-4.debian.tar.gz' pcre3_8.39-4.debian.tar.gz 25456 SHA256:4b1f803c48e0d09bd4d8740c267ded7896afeb3a7ba0fc24326caf51044cf768
```

Other potentially useful URLs:

- https://sources.debian.net/src/pcre3/2:8.39-4/ (for browsing the source)
- https://sources.debian.net/src/pcre3/2:8.39-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/pcre3/2:8.39-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `perl=5.26.0-8`

Binary Packages:

- `libperl5.26:amd64=5.26.0-8`
- `perl=5.26.0-8`
- `perl-base=5.26.0-8`
- `perl-modules-5.26=5.26.0-8`

Licenses: (parsed from: `/usr/share/doc/libperl5.26/copyright`, `/usr/share/doc/perl/copyright`, `/usr/share/doc/perl-base/copyright`, `/usr/share/doc/perl-modules-5.26/copyright`)

- `Artistic`
- `Artistic,`
- `Artistic-2`
- `BSD-3-clause`
- `BSD-3-clause-GENERIC`
- `BSD-3-clause-with-weird-numbering`
- `BSD-4-clause-POWERDOG`
- `BZIP`
- `CC0-1.0`
- `DONT-CHANGE-THE-GPL`
- `Expat`
- `GPL-1`
- `GPL-1+`
- `GPL-2`
- `GPL-2+`
- `GPL-3+-WITH-BISON-EXCEPTION`
- `HSIEH-BSD`
- `HSIEH-DERIVATIVE`
- `LGPL-2.1`
- `REGCOMP`
- `REGCOMP,`
- `RRA-KEEP-THIS-NOTICE`
- `S2P`
- `SDBM-PUBLIC-DOMAIN`
- `TEXT-TABS`
- `Unicode`
- `ZLIB`

Source:

```console
$ apt-get source -qq --print-uris perl=5.26.0-8
'http://deb.debian.org/debian/pool/main/p/perl/perl_5.26.0-8.dsc' perl_5.26.0-8.dsc 2369 SHA256:14287efb9981734a2e15c3508b91e1fd3ca1342e9fc6f49c37ed00acd757aece
'http://deb.debian.org/debian/pool/main/p/perl/perl_5.26.0.orig.tar.xz' perl_5.26.0.orig.tar.xz 11961692 SHA256:9bf2e3d0d72aad77865c3bdbc20d3b576d769c5c255c4ceb30fdb9335266bf55
'http://deb.debian.org/debian/pool/main/p/perl/perl_5.26.0-8.debian.tar.xz' perl_5.26.0-8.debian.tar.xz 159896 SHA256:e6c7f4b6a5790f5909c007d3efe4dcb1f6c6b41da95e4f7ea74748bfb7e198d1
```

Other potentially useful URLs:

- https://sources.debian.net/src/perl/5.26.0-8/ (for browsing the source)
- https://sources.debian.net/src/perl/5.26.0-8/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/perl/5.26.0-8/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `pinentry=1.0.0-2`

Binary Packages:

- `pinentry-curses=1.0.0-2`

Licenses: (parsed from: `/usr/share/doc/pinentry-curses/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-3`
- `LGPL-3+`
- `X11`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/pinentry/1.0.0-2/


### `dpkg` source package: `pixman=0.34.0-1`

Binary Packages:

- `libpixman-1-0:amd64=0.34.0-1`
- `libpixman-1-dev=0.34.0-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris pixman=0.34.0-1
'http://deb.debian.org/debian/pool/main/p/pixman/pixman_0.34.0-1.dsc' pixman_0.34.0-1.dsc 2103 SHA256:157e17c323d461a07f48e570a87228098770fd4388324b2dfcf360bf59ac1e11
'http://deb.debian.org/debian/pool/main/p/pixman/pixman_0.34.0.orig.tar.gz' pixman_0.34.0.orig.tar.gz 878784 SHA256:21b6b249b51c6800dc9553b65106e1e37d0e25df942c90531d4c3997aa20a88e
'http://deb.debian.org/debian/pool/main/p/pixman/pixman_0.34.0-1.diff.gz' pixman_0.34.0-1.diff.gz 315394 SHA256:a230def25913d56f9f13e4dbb1014214f84e85fe502c943d560f4335cfc1c5cd
```

Other potentially useful URLs:

- https://sources.debian.net/src/pixman/0.34.0-1/ (for browsing the source)
- https://sources.debian.net/src/pixman/0.34.0-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/pixman/0.34.0-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `pkg-config=0.29-4`

Binary Packages:

- `pkg-config=0.29-4+b1`

Licenses: (parsed from: `/usr/share/doc/pkg-config/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris pkg-config=0.29-4
'http://deb.debian.org/debian/pool/main/p/pkg-config/pkg-config_0.29-4.dsc' pkg-config_0.29-4.dsc 1718 SHA256:6a00ca4f4813c9d531b7f99072e1b6b443a8eea045c97e7d2b9d34f9a960deb5
'http://deb.debian.org/debian/pool/main/p/pkg-config/pkg-config_0.29.orig.tar.gz' pkg-config_0.29.orig.tar.gz 1973875 SHA256:c8507705d2a10c67f385d66ca2aae31e81770cc0734b4191eb8c489e864a006b
'http://deb.debian.org/debian/pool/main/p/pkg-config/pkg-config_0.29-4.diff.gz' pkg-config_0.29-4.diff.gz 7560 SHA256:0c1253e3755942d3bf407d5c6465568e97ee960c8d9829c53cbae8ff26dc3762
```

Other potentially useful URLs:

- https://sources.debian.net/src/pkg-config/0.29-4/ (for browsing the source)
- https://sources.debian.net/src/pkg-config/0.29-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/pkg-config/0.29-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `postgresql-9.6=9.6.5-1`

Binary Packages:

- `libpq-dev=9.6.5-1`
- `libpq5:amd64=9.6.5-1`

Licenses: (parsed from: `/usr/share/doc/libpq-dev/copyright`, `/usr/share/doc/libpq5/copyright`)

- `Artistic`
- `BSD-2-clause`
- `BSD-3-clause`
- `Custom-Unicode`
- `Custom-pg_dump`
- `Custom-regex`
- `GPL-1`
- `PostgreSQL`
- `Tcl`
- `blf`
- `double-metaphone`
- `imath`
- `nagaysau-ishii`
- `rijndael`

Source:

```console
$ apt-get source -qq --print-uris postgresql-9.6=9.6.5-1
'http://deb.debian.org/debian/pool/main/p/postgresql-9.6/postgresql-9.6_9.6.5-1.dsc' postgresql-9.6_9.6.5-1.dsc 3666 SHA256:81162a163a72c9635a41c98e1267a080eb62cc8fb55bcbc0668ee5bbac5d4cf5
'http://deb.debian.org/debian/pool/main/p/postgresql-9.6/postgresql-9.6_9.6.5.orig.tar.bz2' postgresql-9.6_9.6.5.orig.tar.bz2 19576132 SHA256:06da12a7e3dddeb803962af8309fa06da9d6989f49e22865335f0a14bad0744c
'http://deb.debian.org/debian/pool/main/p/postgresql-9.6/postgresql-9.6_9.6.5-1.debian.tar.xz' postgresql-9.6_9.6.5-1.debian.tar.xz 21244 SHA256:747eff28b74219fbb31a84b1484d9e1c76994ede5357beca712c019d328f4f52
```

Other potentially useful URLs:

- https://sources.debian.net/src/postgresql-9.6/9.6.5-1/ (for browsing the source)
- https://sources.debian.net/src/postgresql-9.6/9.6.5-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/postgresql-9.6/9.6.5-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `procps=2:3.3.12-3`

Binary Packages:

- `libprocps6:amd64=2:3.3.12-3`
- `procps=2:3.3.12-3`

Licenses: (parsed from: `/usr/share/doc/libprocps6/copyright`, `/usr/share/doc/procps/copyright`)

- `GPL-2`
- `GPL-2.0+`
- `LGPL-2`
- `LGPL-2.0+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris procps=2:3.3.12-3
'http://deb.debian.org/debian/pool/main/p/procps/procps_3.3.12-3.dsc' procps_3.3.12-3.dsc 2118 SHA256:5bff9bf045fb88118e5fe69df1ed1d092c49b258ebae5368222a16900288f12e
'http://deb.debian.org/debian/pool/main/p/procps/procps_3.3.12.orig.tar.xz' procps_3.3.12.orig.tar.xz 840540 SHA256:042fcc93e1850aee4c193c51c03f369293fb64fe47e37b38852be6693d12a3af
'http://deb.debian.org/debian/pool/main/p/procps/procps_3.3.12-3.debian.tar.xz' procps_3.3.12-3.debian.tar.xz 27260 SHA256:5907253fba4f11755b60d7d47ffd8212564d7e2c692dcfffc951e4026c465f9e
```

Other potentially useful URLs:

- https://sources.debian.net/src/procps/2:3.3.12-3/ (for browsing the source)
- https://sources.debian.net/src/procps/2:3.3.12-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/procps/2:3.3.12-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `python-defaults=2.7.13-2`

Binary Packages:

- `libpython-stdlib:amd64=2.7.13-2`
- `python=2.7.13-2`
- `python-minimal=2.7.13-2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/python-defaults/2.7.13-2/


### `dpkg` source package: `python2.7=2.7.14~rc1-3`

Binary Packages:

- `libpython2.7-minimal:amd64=2.7.14~rc1-3`
- `libpython2.7-stdlib:amd64=2.7.14~rc1-3`
- `python2.7=2.7.14~rc1-3`
- `python2.7-minimal=2.7.14~rc1-3`

Licenses: (parsed from: `/usr/share/doc/libpython2.7-minimal/copyright`, `/usr/share/doc/libpython2.7-stdlib/copyright`, `/usr/share/doc/python2.7/copyright`, `/usr/share/doc/python2.7-minimal/copyright`)

- `# Licensed to PSF under a Contributor Agreement`
- `* Permission to use this software in any way is granted without`
- `Apache`
- `Apache-2`
- `Apache-2.0`
- `Expat`
- `GPL-2`
- `ISC`
- `LGPL-2.1+`
- `PSF-2`
- `Permission is hereby granted, free of charge, to any person obtaining`
- `Python`
- `This software is provided 'as-is', without any express`
- `This software is provided as-is, without express`
- `implied`
- `see above, some license as Python`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/python2.7/2.7.14~rc1-3/


### `dpkg` source package: `python3-defaults=3.5.3-3`

Binary Packages:

- `libpython3-stdlib:amd64=3.5.3-3`
- `python3=3.5.3-3`
- `python3-minimal=3.5.3-3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris python3-defaults=3.5.3-3
'http://deb.debian.org/debian/pool/main/p/python3-defaults/python3-defaults_3.5.3-3.dsc' python3-defaults_3.5.3-3.dsc 2734 SHA256:73cf771970ee3ee6c9d6786761d66c809f10d46fbfa80181552c86d10d05a991
'http://deb.debian.org/debian/pool/main/p/python3-defaults/python3-defaults_3.5.3-3.tar.gz' python3-defaults_3.5.3-3.tar.gz 129923 SHA256:c50bdf6dada065a5363268c38d4a7f19095f6441d0da9dcb05d4cb2c2a3f8167
```

Other potentially useful URLs:

- https://sources.debian.net/src/python3-defaults/3.5.3-3/ (for browsing the source)
- https://sources.debian.net/src/python3-defaults/3.5.3-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/python3-defaults/3.5.3-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `python3.5=3.5.4-4`

Binary Packages:

- `libpython3.5-minimal:amd64=3.5.4-4`
- `libpython3.5-stdlib:amd64=3.5.4-4`
- `python3.5=3.5.4-4`
- `python3.5-minimal=3.5.4-4`

Licenses: (parsed from: `/usr/share/doc/libpython3.5-minimal/copyright`, `/usr/share/doc/libpython3.5-stdlib/copyright`, `/usr/share/doc/python3.5/copyright`, `/usr/share/doc/python3.5-minimal/copyright`)

- `* Permission to use this software in any way is granted without`
- `Apache`
- `Apache-2`
- `Apache-2.0`
- `By obtaining, using, and/or copying this software and/or its`
- `Expat`
- `GPL-2`
- `ISC`
- `LGPL-2.1+`
- `PSF-2`
- `Permission  is  hereby granted,  free  of charge,  to  any person`
- `Permission is hereby granted, free of charge, to any person obtaining`
- `Permission to use, copy, modify,`
- `Python`
- `Redistribution`
- `This software is provided 'as-is', without any express`
- `This software is provided as-is, without express`
- `binary forms, with`
- `distribute this software`
- `distribute this software and`
- `distribute this software for any`
- `implied`
- `its`
- `see above, some license as Python`
- `use in source`
- `without`

Source:

```console
$ apt-get source -qq --print-uris python3.5=3.5.4-4
'http://deb.debian.org/debian/pool/main/p/python3.5/python3.5_3.5.4-4.dsc' python3.5_3.5.4-4.dsc 3367 SHA256:0861056b92ba4ad189fd4be9b8b81101286466bd7002c07f7ab4427dbbd7b899
'http://deb.debian.org/debian/pool/main/p/python3.5/python3.5_3.5.4.orig.tar.gz' python3.5_3.5.4.orig.tar.gz 20733411 SHA256:6ed87a8b6c758cc3299a8b433e8a9a9122054ad5bc8aad43299cff3a53d8ca44
'http://deb.debian.org/debian/pool/main/p/python3.5/python3.5_3.5.4-4.debian.tar.xz' python3.5_3.5.4-4.debian.tar.xz 235636 SHA256:06d56fb72faa7dc22a1b5957d411f3bda9901a040c714adfe75e8bb7a4b629aa
```

Other potentially useful URLs:

- https://sources.debian.net/src/python3.5/3.5.4-4/ (for browsing the source)
- https://sources.debian.net/src/python3.5/3.5.4-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/python3.5/3.5.4-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `readline=7.0-3`

Binary Packages:

- `libreadline-dev:amd64=7.0-3`
- `libreadline7:amd64=7.0-3`
- `readline-common=7.0-3`

Licenses: (parsed from: `/usr/share/doc/libreadline-dev/copyright`, `/usr/share/doc/libreadline7/copyright`, `/usr/share/doc/readline-common/copyright`)

- `GFDL`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris readline=7.0-3
'http://deb.debian.org/debian/pool/main/r/readline/readline_7.0-3.dsc' readline_7.0-3.dsc 2538 SHA256:f27a5dc9053b88641e3effc6c03b7840cbbbd887e8dcaf05d9e336c7bc7c6a53
'http://deb.debian.org/debian/pool/main/r/readline/readline_7.0.orig.tar.gz' readline_7.0.orig.tar.gz 2910016 SHA256:750d437185286f40a369e1e4f4764eda932b9459b5ec9a731628393dd3d32334
'http://deb.debian.org/debian/pool/main/r/readline/readline_7.0-3.debian.tar.xz' readline_7.0-3.debian.tar.xz 30012 SHA256:bf166310d6ca7716f2bd0e9e06cee2458b0157f7989d028730fc305643560175
```

Other potentially useful URLs:

- https://sources.debian.net/src/readline/7.0-3/ (for browsing the source)
- https://sources.debian.net/src/readline/7.0-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/readline/7.0-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `rtmpdump=2.4+20151223.gitfa8646d.1-1`

Binary Packages:

- `librtmp1:amd64=2.4+20151223.gitfa8646d.1-1+b1`

Licenses: (parsed from: `/usr/share/doc/librtmp1/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris rtmpdump=2.4+20151223.gitfa8646d.1-1
'http://deb.debian.org/debian/pool/main/r/rtmpdump/rtmpdump_2.4+20151223.gitfa8646d.1-1.dsc' rtmpdump_2.4+20151223.gitfa8646d.1-1.dsc 2315 SHA256:e56822b88625bf6a51f06652fc36fa2a1348b4325ac76541800cd078192aa3d2
'http://deb.debian.org/debian/pool/main/r/rtmpdump/rtmpdump_2.4+20151223.gitfa8646d.1.orig.tar.gz' rtmpdump_2.4+20151223.gitfa8646d.1.orig.tar.gz 142213 SHA256:5c032f5c8cc2937eb55a81a94effdfed3b0a0304b6376147b86f951e225e3ab5
'http://deb.debian.org/debian/pool/main/r/rtmpdump/rtmpdump_2.4+20151223.gitfa8646d.1-1.debian.tar.xz' rtmpdump_2.4+20151223.gitfa8646d.1-1.debian.tar.xz 8044 SHA256:675847f5cddb860256cbf2e7d5b85918aa53b59b0fd97a466b39a5c77a399537
```

Other potentially useful URLs:

- https://sources.debian.net/src/rtmpdump/2.4+20151223.gitfa8646d.1-1/ (for browsing the source)
- https://sources.debian.net/src/rtmpdump/2.4+20151223.gitfa8646d.1-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/rtmpdump/2.4+20151223.gitfa8646d.1-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `sed=4.4-1`

Binary Packages:

- `sed=4.4-1`

Licenses: (parsed from: `/usr/share/doc/sed/copyright`)

- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris sed=4.4-1
'http://deb.debian.org/debian/pool/main/s/sed/sed_4.4-1.dsc' sed_4.4-1.dsc 2048 SHA256:bb2a11d04f3aeba73cc994e097219fde8c5e0fd1bcf42e0ecc8a4f2282c00fc9
'http://deb.debian.org/debian/pool/main/s/sed/sed_4.4.orig.tar.xz' sed_4.4.orig.tar.xz 1181664 SHA256:cbd6ebc5aaf080ed60d0162d7f6aeae58211a1ee9ba9bb25623daa6cd942683b
'http://deb.debian.org/debian/pool/main/s/sed/sed_4.4-1.debian.tar.xz' sed_4.4-1.debian.tar.xz 59552 SHA256:56dd1f91c5e33b419f38cde93afc90d6fad9064ef4594a877424a0ab2ac9a4bf
```

Other potentially useful URLs:

- https://sources.debian.net/src/sed/4.4-1/ (for browsing the source)
- https://sources.debian.net/src/sed/4.4-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/sed/4.4-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `sensible-utils=0.0.10`

Binary Packages:

- `sensible-utils=0.0.10`

Licenses: (parsed from: `/usr/share/doc/sensible-utils/copyright`)

- `All-permissive`
- `GPL-2`
- `GPL-2+`
- `configure`
- `installsh`

Source:

```console
$ apt-get source -qq --print-uris sensible-utils=0.0.10
'http://deb.debian.org/debian/pool/main/s/sensible-utils/sensible-utils_0.0.10.dsc' sensible-utils_0.0.10.dsc 1671 SHA256:9f19f464d6edc9c086a92c7ac03cc72b285dccd56f9d640b9979a3e5aac3457e
'http://deb.debian.org/debian/pool/main/s/sensible-utils/sensible-utils_0.0.10.tar.xz' sensible-utils_0.0.10.tar.xz 57140 SHA256:137f67f34cbe2066407889d6ee15f4e51440e0f1378e9763da5922388a6510f3
```

Other potentially useful URLs:

- https://sources.debian.net/src/sensible-utils/0.0.10/ (for browsing the source)
- https://sources.debian.net/src/sensible-utils/0.0.10/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/sensible-utils/0.0.10/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `serf=1.3.9-3`

Binary Packages:

- `libserf-1-1:amd64=1.3.9-3`

Licenses: (parsed from: `/usr/share/doc/libserf-1-1/copyright`)

- `Apache`
- `Apache-2.0`
- `Zlib`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/serf/1.3.9-3/


### `dpkg` source package: `shadow=1:4.4-4.1`

Binary Packages:

- `login=1:4.4-4.1`
- `passwd=1:4.4-4.1`

Licenses: (parsed from: `/usr/share/doc/login/copyright`, `/usr/share/doc/passwd/copyright`)

- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/shadow/1:4.4-4.1/


### `dpkg` source package: `shared-mime-info=1.8-1`

Binary Packages:

- `shared-mime-info=1.8-1`

Licenses: (parsed from: `/usr/share/doc/shared-mime-info/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris shared-mime-info=1.8-1
'http://deb.debian.org/debian/pool/main/s/shared-mime-info/shared-mime-info_1.8-1.dsc' shared-mime-info_1.8-1.dsc 2238 SHA256:53a57dc9cecf61204c57d6df282b5b4db3c82214d585c474dbb33835a25530af
'http://deb.debian.org/debian/pool/main/s/shared-mime-info/shared-mime-info_1.8.orig.tar.xz' shared-mime-info_1.8.orig.tar.xz 589444 SHA256:2af55ef1a0319805b74ab40d331a3962c905477d76c086f49e34dc96363589e9
'http://deb.debian.org/debian/pool/main/s/shared-mime-info/shared-mime-info_1.8-1.debian.tar.xz' shared-mime-info_1.8-1.debian.tar.xz 10324 SHA256:c169b5cb2669f12d2dbdbcb02026c6acbee2bfb6e512feadec50b8593cb2f779
```

Other potentially useful URLs:

- https://sources.debian.net/src/shared-mime-info/1.8-1/ (for browsing the source)
- https://sources.debian.net/src/shared-mime-info/1.8-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/shared-mime-info/1.8-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `sqlite3=3.20.1-1`

Binary Packages:

- `libsqlite3-0:amd64=3.20.1-1`
- `libsqlite3-dev:amd64=3.20.1-1`

Licenses: (parsed from: `/usr/share/doc/libsqlite3-0/copyright`, `/usr/share/doc/libsqlite3-dev/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris sqlite3=3.20.1-1
'http://deb.debian.org/debian/pool/main/s/sqlite3/sqlite3_3.20.1-1.dsc' sqlite3_3.20.1-1.dsc 2473 SHA256:f9d17a62dbf721057c9ca05bc37bd69e247f289ac7098ab5e98d1e51434dda8a
'http://deb.debian.org/debian/pool/main/s/sqlite3/sqlite3_3.20.1.orig-www.tar.xz' sqlite3_3.20.1.orig-www.tar.xz 3485848 SHA256:c31a1ad382c331c0507a5992c6d1697450ffc3410209ae992ead1c34344b5654
'http://deb.debian.org/debian/pool/main/s/sqlite3/sqlite3_3.20.1.orig.tar.xz' sqlite3_3.20.1.orig.tar.xz 5900940 SHA256:0ed8da87222d3e0d45afcd9dac3b91a453eee4ea6eaf1287b78a6f0fb5274437
'http://deb.debian.org/debian/pool/main/s/sqlite3/sqlite3_3.20.1-1.debian.tar.xz' sqlite3_3.20.1-1.debian.tar.xz 17652 SHA256:8c205983e0f7baf75419123093a42aac97c94e8454c0adf540838264604e04b3
```

Other potentially useful URLs:

- https://sources.debian.net/src/sqlite3/3.20.1-1/ (for browsing the source)
- https://sources.debian.net/src/sqlite3/3.20.1-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/sqlite3/3.20.1-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `subversion=1.9.7-2`

Binary Packages:

- `libsvn1:amd64=1.9.7-2`
- `subversion=1.9.7-2`

Licenses: (parsed from: `/usr/share/doc/libsvn1/copyright`, `/usr/share/doc/subversion/copyright`)

- `Apache-2.0`
- `GPL-2`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris subversion=1.9.7-2
'http://deb.debian.org/debian/pool/main/s/subversion/subversion_1.9.7-2.dsc' subversion_1.9.7-2.dsc 2990 SHA256:10b223085db0e302e4f15f51fa3d8ebabe0603c1a4edfb1f06fabfd77cc919ca
'http://deb.debian.org/debian/pool/main/s/subversion/subversion_1.9.7.orig.tar.gz' subversion_1.9.7.orig.tar.gz 10643686 SHA256:c72a209c883e20245f14c4e644803f50ae83ae24652e385ff5e82300a0d06c3c
'http://deb.debian.org/debian/pool/main/s/subversion/subversion_1.9.7-2.diff.gz' subversion_1.9.7-2.diff.gz 2632435 SHA256:d4b243270b601bdf6486bd4c7aefb508b6b55077aece28650d54057f047a92af
```

Other potentially useful URLs:

- https://sources.debian.net/src/subversion/1.9.7-2/ (for browsing the source)
- https://sources.debian.net/src/subversion/1.9.7-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/subversion/1.9.7-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `systemd=234-3`

Binary Packages:

- `libsystemd0:amd64=234-3`
- `libudev1:amd64=234-3`

Licenses: (parsed from: `/usr/share/doc/libsystemd0/copyright`, `/usr/share/doc/libudev1/copyright`)

- `CC0`
- `Expat`
- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris systemd=234-3
'http://deb.debian.org/debian/pool/main/s/systemd/systemd_234-3.dsc' systemd_234-3.dsc 4838 SHA256:2c85a08e1ef7818c755f98a7aaf1e97deccc7575a717903e3330dae2777d5a94
'http://deb.debian.org/debian/pool/main/s/systemd/systemd_234.orig.tar.gz' systemd_234.orig.tar.gz 4800186 SHA256:da3e69d10aa1c983d33833372ad4929037b411ac421fb085c8cee79ae1d80b6a
'http://deb.debian.org/debian/pool/main/s/systemd/systemd_234-3.debian.tar.xz' systemd_234-3.debian.tar.xz 134836 SHA256:b873f8ce1cdaa82212ec043cc5d7bf9f82dd2c347d59816989e2079dfe94720f
```

Other potentially useful URLs:

- https://sources.debian.net/src/systemd/234-3/ (for browsing the source)
- https://sources.debian.net/src/systemd/234-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/systemd/234-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `sysvinit=2.88dsf-59.9`

Binary Packages:

- `sysvinit-utils=2.88dsf-59.9`

Licenses: (parsed from: `/usr/share/doc/sysvinit-utils/copyright`)

- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/sysvinit/2.88dsf-59.9/


### `dpkg` source package: `tar=1.29b-2`

Binary Packages:

- `tar=1.29b-2`

Licenses: (parsed from: `/usr/share/doc/tar/copyright`)

- `GPL-2`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris tar=1.29b-2
'http://deb.debian.org/debian/pool/main/t/tar/tar_1.29b-2.dsc' tar_1.29b-2.dsc 1965 SHA256:cae92504d2622b0a3d353df387c44beb1e9040ed2d527272a226f0ba247a17f1
'http://deb.debian.org/debian/pool/main/t/tar/tar_1.29b.orig.tar.xz' tar_1.29b.orig.tar.xz 1822008 SHA256:6a59706ebee384a6cd2fb3ee1dbfbfc20c5c66c7efd7cedb28edc054fca8ba00
'http://deb.debian.org/debian/pool/main/t/tar/tar_1.29b-2.debian.tar.xz' tar_1.29b-2.debian.tar.xz 28552 SHA256:caa4e76e821b87e842d0bfc8285abd47103d47d56e93dae0a8df4b787f7c8d72
```

Other potentially useful URLs:

- https://sources.debian.net/src/tar/1.29b-2/ (for browsing the source)
- https://sources.debian.net/src/tar/1.29b-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/tar/1.29b-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `tiff=4.0.8-5`

Binary Packages:

- `libtiff5:amd64=4.0.8-5`
- `libtiff5-dev:amd64=4.0.8-5`
- `libtiffxx5:amd64=4.0.8-5`

Licenses: (parsed from: `/usr/share/doc/libtiff5/copyright`, `/usr/share/doc/libtiff5-dev/copyright`, `/usr/share/doc/libtiffxx5/copyright`)

- `Hylafax`

Source:

```console
$ apt-get source -qq --print-uris tiff=4.0.8-5
'http://deb.debian.org/debian/pool/main/t/tiff/tiff_4.0.8-5.dsc' tiff_4.0.8-5.dsc 2157 SHA256:461a69a1c053f98981fc92f243ab616c1bb971186b452e54f98f26d19fc95769
'http://deb.debian.org/debian/pool/main/t/tiff/tiff_4.0.8.orig.tar.gz' tiff_4.0.8.orig.tar.gz 2065574 SHA256:59d7a5a8ccd92059913f246877db95a2918e6c04fb9d43fd74e5c3390dac2910
'http://deb.debian.org/debian/pool/main/t/tiff/tiff_4.0.8-5.debian.tar.xz' tiff_4.0.8-5.debian.tar.xz 24124 SHA256:0a72efaba5da935537dd7dc28593503c3a0161d954fcd2da6eb511c0238d1387
```

Other potentially useful URLs:

- https://sources.debian.net/src/tiff/4.0.8-5/ (for browsing the source)
- https://sources.debian.net/src/tiff/4.0.8-5/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/tiff/4.0.8-5/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `tzdata=2017b-2`

Binary Packages:

- `tzdata=2017b-2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris tzdata=2017b-2
'http://deb.debian.org/debian/pool/main/t/tzdata/tzdata_2017b-2.dsc' tzdata_2017b-2.dsc 2005 SHA256:479f7a077690c3d84f15dc8be1da0a732a54cc07f7b30ca7fad6a5bd00921748
'http://deb.debian.org/debian/pool/main/t/tzdata/tzdata_2017b.orig.tar.gz' tzdata_2017b.orig.tar.gz 324317 SHA256:f8242a522ea3496b0ce4ff4f2e75a049178da21001a08b8e666d8cbe07d18086
'http://deb.debian.org/debian/pool/main/t/tzdata/tzdata_2017b-2.debian.tar.xz' tzdata_2017b-2.debian.tar.xz 101096 SHA256:2607bdfaa4535e59223d194c1cc1891a3c26a731d20a4a1d9311d22d1a9175d8
```

Other potentially useful URLs:

- https://sources.debian.net/src/tzdata/2017b-2/ (for browsing the source)
- https://sources.debian.net/src/tzdata/2017b-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/tzdata/2017b-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `ucf=3.0036`

Binary Packages:

- `ucf=3.0036`

Licenses: (parsed from: `/usr/share/doc/ucf/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris ucf=3.0036
'http://deb.debian.org/debian/pool/main/u/ucf/ucf_3.0036.dsc' ucf_3.0036.dsc 1343 SHA256:e67a8a3012ac357c7759dabd93d258422b1003bad8c3f17f25fc2a289eeda3bb
'http://deb.debian.org/debian/pool/main/u/ucf/ucf_3.0036.tar.xz' ucf_3.0036.tar.xz 65020 SHA256:34aa44416106f1205376918386b2896edf21dd42b633133b5f8fedecae17fca8
```

Other potentially useful URLs:

- https://sources.debian.net/src/ucf/3.0036/ (for browsing the source)
- https://sources.debian.net/src/ucf/3.0036/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/ucf/3.0036/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `ustr=1.0.4-6`

Binary Packages:

- `libustr-1.0-1:amd64=1.0.4-6`

Licenses: (parsed from: `/usr/share/doc/libustr-1.0-1/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`
- `LGPL-2+`
- `LGPL-2.1`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris ustr=1.0.4-6
'http://deb.debian.org/debian/pool/main/u/ustr/ustr_1.0.4-6.dsc' ustr_1.0.4-6.dsc 2029 SHA256:87a854fc03dc059d5d4f135dfd36353c8c09f88a6eb216c6dcea8adadbe6ba59
'http://deb.debian.org/debian/pool/main/u/ustr/ustr_1.0.4.orig.tar.gz' ustr_1.0.4.orig.tar.gz 301345 SHA256:4d293b6b9d9fe51d58441f4b09b1f0005fcad8256ae8048587789bf5dbefb62e
'http://deb.debian.org/debian/pool/main/u/ustr/ustr_1.0.4-6.debian.tar.xz' ustr_1.0.4-6.debian.tar.xz 25608 SHA256:75aa6be2c70eba632ac63078e55ecb4b5a45e6624501a8ed6d81b9a2014d149e
```

Other potentially useful URLs:

- https://sources.debian.net/src/ustr/1.0.4-6/ (for browsing the source)
- https://sources.debian.net/src/ustr/1.0.4-6/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/ustr/1.0.4-6/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `util-linux=2.29.2-4`

Binary Packages:

- `bsdutils=1:2.29.2-4`
- `fdisk=2.29.2-4`
- `libblkid1:amd64=2.29.2-4`
- `libfdisk1:amd64=2.29.2-4`
- `libmount1:amd64=2.29.2-4`
- `libsmartcols1:amd64=2.29.2-4`
- `libuuid1:amd64=2.29.2-4`
- `mount=2.29.2-4`
- `util-linux=2.29.2-4`

Licenses: (parsed from: `/usr/share/doc/bsdutils/copyright`, `/usr/share/doc/fdisk/copyright`, `/usr/share/doc/libblkid1/copyright`, `/usr/share/doc/libfdisk1/copyright`, `/usr/share/doc/libmount1/copyright`, `/usr/share/doc/libsmartcols1/copyright`, `/usr/share/doc/libuuid1/copyright`, `/usr/share/doc/mount/copyright`, `/usr/share/doc/util-linux/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-4-clause`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `LGPL`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `MIT`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris util-linux=2.29.2-4
'http://deb.debian.org/debian/pool/main/u/util-linux/util-linux_2.29.2-4.dsc' util-linux_2.29.2-4.dsc 4043 SHA256:0bc5b23cf92924cb895fdd97d24642333c80fc63d7ac0d8269e943b7da394271
'http://deb.debian.org/debian/pool/main/u/util-linux/util-linux_2.29.2.orig.tar.xz' util-linux_2.29.2.orig.tar.xz 4277668 SHA256:accea4d678209f97f634f40a93b7e9fcad5915d1f4749f6c47bee6bf110fe8e3
'http://deb.debian.org/debian/pool/main/u/util-linux/util-linux_2.29.2-4.debian.tar.xz' util-linux_2.29.2-4.debian.tar.xz 73552 SHA256:1004cbfa6053f9402a94f468dce087776e7028937c2d65a865d7af51788d9548
```

Other potentially useful URLs:

- https://sources.debian.net/src/util-linux/2.29.2-4/ (for browsing the source)
- https://sources.debian.net/src/util-linux/2.29.2-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/util-linux/2.29.2-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `wget=1.19.1-4`

Binary Packages:

- `wget=1.19.1-4`

Licenses: (parsed from: `/usr/share/doc/wget/copyright`)

- `GFDL-1.2`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris wget=1.19.1-4
'http://deb.debian.org/debian/pool/main/w/wget/wget_1.19.1-4.dsc' wget_1.19.1-4.dsc 1929 SHA256:3d5f32dc4e27b575e362e3a13392c91e955f21926bc3f77682be006b01ab1852
'http://deb.debian.org/debian/pool/main/w/wget/wget_1.19.1.orig.tar.xz' wget_1.19.1.orig.tar.xz 2111756 SHA256:0c950b9671881222a4d385b013c9604e98a8025d1988529dfca0e93617744cd2
'http://deb.debian.org/debian/pool/main/w/wget/wget_1.19.1-4.debian.tar.xz' wget_1.19.1-4.debian.tar.xz 20588 SHA256:d775348caa26dd682eb0a28ada1f1179ccc8cd9ca29d038ae5d3a511d722f9b5
```

Other potentially useful URLs:

- https://sources.debian.net/src/wget/1.19.1-4/ (for browsing the source)
- https://sources.debian.net/src/wget/1.19.1-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/wget/1.19.1-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `x11proto-core=7.0.31-1`

Binary Packages:

- `x11proto-core-dev=7.0.31-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris x11proto-core=7.0.31-1
'http://deb.debian.org/debian/pool/main/x/x11proto-core/x11proto-core_7.0.31-1.dsc' x11proto-core_7.0.31-1.dsc 1949 SHA256:9810fabbded85927d800058431a9168308aeec4bdd4e4fa6dc7f877855c35028
'http://deb.debian.org/debian/pool/main/x/x11proto-core/x11proto-core_7.0.31.orig.tar.gz' x11proto-core_7.0.31.orig.tar.gz 367979 SHA256:6d755eaae27b45c5cc75529a12855fed5de5969b367ed05003944cf901ed43c7
'http://deb.debian.org/debian/pool/main/x/x11proto-core/x11proto-core_7.0.31-1.diff.gz' x11proto-core_7.0.31-1.diff.gz 30387 SHA256:68f5f4e0df06f5fa5ed4a88e1b3899bd9d80313a51b6f314230132f560bcf94e
```

Other potentially useful URLs:

- https://sources.debian.net/src/x11proto-core/7.0.31-1/ (for browsing the source)
- https://sources.debian.net/src/x11proto-core/7.0.31-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/x11proto-core/7.0.31-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `x11proto-input=2.3.2-1`

Binary Packages:

- `x11proto-input-dev=2.3.2-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris x11proto-input=2.3.2-1
'http://deb.debian.org/debian/pool/main/x/x11proto-input/x11proto-input_2.3.2-1.dsc' x11proto-input_2.3.2-1.dsc 1908 SHA256:6c4fc45a57d001782369ffcdbe29f5ff889d426a1053c67678c3a710dd9d03d2
'http://deb.debian.org/debian/pool/main/x/x11proto-input/x11proto-input_2.3.2.orig.tar.gz' x11proto-input_2.3.2.orig.tar.gz 244334 SHA256:10eaadd531f38f7c92ab59ef0708ca195caf3164a75c4ed99f0c04f2913f6ef3
'http://deb.debian.org/debian/pool/main/x/x11proto-input/x11proto-input_2.3.2-1.diff.gz' x11proto-input_2.3.2-1.diff.gz 6898 SHA256:21f09fce8acfb20e01bd2c90775eb8ae8f43d67dea690874625d1a0bd5a1bff2
```

Other potentially useful URLs:

- https://sources.debian.net/src/x11proto-input/2.3.2-1/ (for browsing the source)
- https://sources.debian.net/src/x11proto-input/2.3.2-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/x11proto-input/2.3.2-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `x11proto-kb=1.0.7-1`

Binary Packages:

- `x11proto-kb-dev=1.0.7-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris x11proto-kb=1.0.7-1
'http://deb.debian.org/debian/pool/main/x/x11proto-kb/x11proto-kb_1.0.7-1.dsc' x11proto-kb_1.0.7-1.dsc 1929 SHA256:279f1e446457ba50e8950ebbe44446f960362f2247dece08ed276f5181596480
'http://deb.debian.org/debian/pool/main/x/x11proto-kb/x11proto-kb_1.0.7.orig.tar.gz' x11proto-kb_1.0.7.orig.tar.gz 325858 SHA256:828cb275b91268b1a3ea950d5c0c5eb076c678fdf005d517411f89cc8c3bb416
'http://deb.debian.org/debian/pool/main/x/x11proto-kb/x11proto-kb_1.0.7-1.diff.gz' x11proto-kb_1.0.7-1.diff.gz 7467 SHA256:c868adc57853c6633e0379ce25f23e4cd8847f1d67c651ed1d7e63c98574064c
```

Other potentially useful URLs:

- https://sources.debian.net/src/x11proto-kb/1.0.7-1/ (for browsing the source)
- https://sources.debian.net/src/x11proto-kb/1.0.7-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/x11proto-kb/1.0.7-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `x11proto-render=2:0.11.1-2`

Binary Packages:

- `x11proto-render-dev=2:0.11.1-2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris x11proto-render=2:0.11.1-2
'http://deb.debian.org/debian/pool/main/x/x11proto-render/x11proto-render_0.11.1-2.dsc' x11proto-render_0.11.1-2.dsc 1979 SHA256:5cebbcce7928bd468b0eb447d9da403e5228af1691549a529a9012d2f7d18948
'http://deb.debian.org/debian/pool/main/x/x11proto-render/x11proto-render_0.11.1.orig.tar.gz' x11proto-render_0.11.1.orig.tar.gz 124436 SHA256:a0a4be3cad9381ae28279ba5582e679491fc2bec9aab8a65993108bf8dbce5fe
'http://deb.debian.org/debian/pool/main/x/x11proto-render/x11proto-render_0.11.1-2.diff.gz' x11proto-render_0.11.1-2.diff.gz 14527 SHA256:614b7adf6f08bdf25bc7fb565f048e2f94e290c3bd056fa2485e093eb887c54f
```

Other potentially useful URLs:

- https://sources.debian.net/src/x11proto-render/2:0.11.1-2/ (for browsing the source)
- https://sources.debian.net/src/x11proto-render/2:0.11.1-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/x11proto-render/2:0.11.1-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `x11proto-xext=7.3.0-1`

Binary Packages:

- `x11proto-xext-dev=7.3.0-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris x11proto-xext=7.3.0-1
'http://deb.debian.org/debian/pool/main/x/x11proto-xext/x11proto-xext_7.3.0-1.dsc' x11proto-xext_7.3.0-1.dsc 1997 SHA256:4b806c7f17f7dd466901111ce0862117541098025470601c251499d76affe9fc
'http://deb.debian.org/debian/pool/main/x/x11proto-xext/x11proto-xext_7.3.0.orig.tar.gz' x11proto-xext_7.3.0.orig.tar.gz 290814 SHA256:1b1bcdf91221e78c6c33738667a57bd9aaa63d5953174ad8ed9929296741c9f5
'http://deb.debian.org/debian/pool/main/x/x11proto-xext/x11proto-xext_7.3.0-1.diff.gz' x11proto-xext_7.3.0-1.diff.gz 16644 SHA256:68eec9363c7f8bcfbbaba68d6661284eb78fffccbddb293b95a6c85647cfcf6c
```

Other potentially useful URLs:

- https://sources.debian.net/src/x11proto-xext/7.3.0-1/ (for browsing the source)
- https://sources.debian.net/src/x11proto-xext/7.3.0-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/x11proto-xext/7.3.0-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `xorg-sgml-doctools=1:1.11-1`

Binary Packages:

- `xorg-sgml-doctools=1:1.11-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris xorg-sgml-doctools=1:1.11-1
'http://deb.debian.org/debian/pool/main/x/xorg-sgml-doctools/xorg-sgml-doctools_1.11-1.dsc' xorg-sgml-doctools_1.11-1.dsc 1975 SHA256:1f4a12a38420b0ddab35553b9588fdf43ab39577958aed70fca435c9a747141a
'http://deb.debian.org/debian/pool/main/x/xorg-sgml-doctools/xorg-sgml-doctools_1.11.orig.tar.gz' xorg-sgml-doctools_1.11.orig.tar.gz 150367 SHA256:986326d7b4dd2ad298f61d8d41fe3929ac6191c6000d6d7e47a8ffc0c34e7426
'http://deb.debian.org/debian/pool/main/x/xorg-sgml-doctools/xorg-sgml-doctools_1.11-1.diff.gz' xorg-sgml-doctools_1.11-1.diff.gz 3194 SHA256:18eeb355cb0efff9f47f8ed8e852eee322d9733a427419f4b39f43bc4df630c1
```

Other potentially useful URLs:

- https://sources.debian.net/src/xorg-sgml-doctools/1:1.11-1/ (for browsing the source)
- https://sources.debian.net/src/xorg-sgml-doctools/1:1.11-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/xorg-sgml-doctools/1:1.11-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `xorg=1:7.7+19`

Binary Packages:

- `x11-common=1:7.7+19`

Licenses: (parsed from: `/usr/share/doc/x11-common/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris xorg=1:7.7+19
'http://deb.debian.org/debian/pool/main/x/xorg/xorg_7.7+19.dsc' xorg_7.7+19.dsc 2016 SHA256:fc4a577eee67f3604c56701e21b28dccd3858da0f110b708ca3359e2718e3d46
'http://deb.debian.org/debian/pool/main/x/xorg/xorg_7.7+19.tar.gz' xorg_7.7+19.tar.gz 288723 SHA256:5de6df9e19009450b94f4f5307049bc2c7dc1114222f6f2f6fc60d737a33a537
```

Other potentially useful URLs:

- https://sources.debian.net/src/xorg/1:7.7+19/ (for browsing the source)
- https://sources.debian.net/src/xorg/1:7.7+19/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/xorg/1:7.7+19/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `xtrans=1.3.5-1`

Binary Packages:

- `xtrans-dev=1.3.5-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris xtrans=1.3.5-1
'http://deb.debian.org/debian/pool/main/x/xtrans/xtrans_1.3.5-1.dsc' xtrans_1.3.5-1.dsc 1901 SHA256:64750bc2dd993ac93b9e0a8d6109ce72963ab22296479145eb3f392d238c2280
'http://deb.debian.org/debian/pool/main/x/xtrans/xtrans_1.3.5.orig.tar.gz' xtrans_1.3.5.orig.tar.gz 227536 SHA256:b7a577c1b6c75030145e53b4793db9c88f9359ac49e7d771d4385d21b3e5945d
'http://deb.debian.org/debian/pool/main/x/xtrans/xtrans_1.3.5-1.diff.gz' xtrans_1.3.5-1.diff.gz 16122 SHA256:2acb2c4f5958ef1bbae74ca64007d0465261a4f62bfad6ed22f1f144c0e445e1
```

Other potentially useful URLs:

- https://sources.debian.net/src/xtrans/1.3.5-1/ (for browsing the source)
- https://sources.debian.net/src/xtrans/1.3.5-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/xtrans/1.3.5-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `xz-utils=5.2.2-1.3`

Binary Packages:

- `liblzma-dev:amd64=5.2.2-1.3`
- `liblzma5:amd64=5.2.2-1.3`
- `xz-utils=5.2.2-1.3`

Licenses: (parsed from: `/usr/share/doc/liblzma-dev/copyright`, `/usr/share/doc/liblzma5/copyright`, `/usr/share/doc/xz-utils/copyright`)

- `Autoconf`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `LGPL-2`
- `LGPL-2.1`
- `LGPL-2.1+`
- `PD`
- `PD-debian`
- `config-h`
- `noderivs`
- `none`
- `permissive-fsf`
- `permissive-nowarranty`
- `probably-PD`

Source:

```console
$ apt-get source -qq --print-uris xz-utils=5.2.2-1.3
'http://deb.debian.org/debian/pool/main/x/xz-utils/xz-utils_5.2.2-1.3.dsc' xz-utils_5.2.2-1.3.dsc 2575 SHA256:3ea4e6a32f6265b152f89ceafe78c8839e5f4bb1cad137b159fe2013817f9342
'http://deb.debian.org/debian/pool/main/x/xz-utils/xz-utils_5.2.2.orig.tar.xz' xz-utils_5.2.2.orig.tar.xz 1016404 SHA256:f341b1906ebcdde291dd619399ae944600edc9193619dd0c0110a5f05bfcc89e
'http://deb.debian.org/debian/pool/main/x/xz-utils/xz-utils_5.2.2.orig.tar.xz.asc' xz-utils_5.2.2.orig.tar.xz.asc 543 SHA256:2cc0575556e1331b3f468e6e7dca5969ce86efcc315d62672279b4e68b2e449f
'http://deb.debian.org/debian/pool/main/x/xz-utils/xz-utils_5.2.2-1.3.debian.tar.xz' xz-utils_5.2.2-1.3.debian.tar.xz 108680 SHA256:d76c3acf39d0999c14384695394970e8f98853fd6736ba91972d3e67106bc6f6
```

Other potentially useful URLs:

- https://sources.debian.net/src/xz-utils/5.2.2-1.3/ (for browsing the source)
- https://sources.debian.net/src/xz-utils/5.2.2-1.3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/xz-utils/5.2.2-1.3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `zlib=1:1.2.8.dfsg-5`

Binary Packages:

- `zlib1g:amd64=1:1.2.8.dfsg-5`
- `zlib1g-dev:amd64=1:1.2.8.dfsg-5`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris zlib=1:1.2.8.dfsg-5
'http://deb.debian.org/debian/pool/main/z/zlib/zlib_1.2.8.dfsg-5.dsc' zlib_1.2.8.dfsg-5.dsc 2259 SHA256:35ebfdbb74b3563d344b2bb946909f5d3221cdf971876549ea7ccec01fabcbec
'http://deb.debian.org/debian/pool/main/z/zlib/zlib_1.2.8.dfsg.orig.tar.gz' zlib_1.2.8.dfsg.orig.tar.gz 361943 SHA256:2caecc2c3f1ef8b87b8f72b128a03e61c307e8c14f5ec9b422ef7914ba75cf9f
'http://deb.debian.org/debian/pool/main/z/zlib/zlib_1.2.8.dfsg-5.debian.tar.xz' zlib_1.2.8.dfsg-5.debian.tar.xz 18500 SHA256:7b88f58d1bfe8e873b8362ede3d0bc569793decc60094189fad1a110599cdd95
```

Other potentially useful URLs:

- https://sources.debian.net/src/zlib/1:1.2.8.dfsg-5/ (for browsing the source)
- https://sources.debian.net/src/zlib/1:1.2.8.dfsg-5/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/zlib/1:1.2.8.dfsg-5/ (for access to the source package after it no longer exists in the archive)
