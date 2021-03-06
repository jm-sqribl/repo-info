## `python:2-windowsservercore`

```console
$ docker pull python@sha256:a4af363f03c95565b158503f694c1716dc8ea5a76dbfb99c5364031554e0de6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.1715; amd64

### `python:2-windowsservercore` - windows version 10.0.14393.1715; amd64

```console
$ docker pull python@sha256:bc4378893ee1b19b4997d239364dfb178b2081c76b59613b616a76214ced6c0f
```

-	Docker Version: 17.03.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 GB (5389947265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb958ce9310039649ef0ec70d4134a649e337c30e2b53449453bd7203c516488`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Tue, 13 Dec 2016 10:53:31 GMT
RUN Apply image 10.0.14393.0
# Tue, 12 Sep 2017 22:02:46 GMT
RUN Install update 10.0.14393.1715
# Thu, 14 Sep 2017 16:25:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 19 Sep 2017 16:26:28 GMT
ENV PYTHON_VERSION=2.7.14
# Tue, 19 Sep 2017 16:26:31 GMT
ENV PYTHON_RELEASE=2.7.14
# Tue, 19 Sep 2017 16:27:33 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}.amd64.msi' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	(New-Object System.Net.WebClient).DownloadFile($url, 'python.msi'); 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'python.msi', 			'/quiet', 			'/qn', 			'TARGETDIR=C:\Python', 			'ALLUSERS=1', 			'ADDLOCAL=DefaultFeature,Extensions,TclTk,Tools,PrependPath' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.msi -Force; 		Write-Host 'Complete.';
# Tue, 19 Sep 2017 16:27:42 GMT
ENV PYTHON_PIP_VERSION=9.0.1
# Tue, 19 Sep 2017 16:28:25 GMT
RUN Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	(New-Object System.Net.WebClient).DownloadFile('https://bootstrap.pypa.io/get-pip.py', 'get-pip.py'); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.';
# Tue, 19 Sep 2017 16:28:49 GMT
RUN pip install --no-cache-dir virtualenv
# Tue, 19 Sep 2017 16:28:53 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:da87b55a9b6358a65462540faeaa97505b0a12e1a2c14f08893589181d32d00d`  
		Size: 1.3 GB (1265822551 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d9a80234ea5aa1b3fdb0960fc47b11cc20b357170851b348ddd413a7be726094`  
		Last Modified: Thu, 14 Sep 2017 16:32:17 GMT  
		Size: 1.2 KB (1225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3066b0297a25039c686a17ec7f02a5d1bb7c186ba0462069889774c5d8dc47ce`  
		Last Modified: Tue, 19 Sep 2017 16:29:17 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88795a526a48519c384c91f8c363f8583e8e79a98737a286c81773afcf356365`  
		Last Modified: Tue, 19 Sep 2017 16:29:17 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:821cd9276270e188258ca398ed79d2e838c625071f51bd9bc4535753817ea1f7`  
		Last Modified: Tue, 19 Sep 2017 16:29:22 GMT  
		Size: 38.4 MB (38350708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6dcf23bb38313b0e07b0a0a71cba24834fe4fff1df9161808585d16afaf7a38`  
		Last Modified: Tue, 19 Sep 2017 16:29:13 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcf389a04256f29647db85ad775950e08deb1fbdd658d05a0e02af46f787062`  
		Last Modified: Tue, 19 Sep 2017 16:29:18 GMT  
		Size: 9.0 MB (9031900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f7384a58fbfe421bcfcefc5801847a60c0237584b1f2fbc656af4a63c61e6d`  
		Last Modified: Tue, 19 Sep 2017 16:29:15 GMT  
		Size: 6.8 MB (6750106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:627669de968498ea4082d80cd956f4f5b452de57c5102e7cfd74c0c0b5c21391`  
		Last Modified: Tue, 19 Sep 2017 16:29:13 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
