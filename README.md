# ossfs Docker
========
Build Docker for ossfs

Ossfs DockerFile

Build Dockerfile
----------------
```bash
docker build -t YOUR_BUILD_TAG-NAME .
```

Configuration passwd-ossfs
--------------------------
Change

```bash
bucket-name : your bucket name
AccessKeyId : your access key id
AccessKeySecret : your secret key
```

Configuration docker-compose.yml
---------------------------------
Change
```bash
YOUR_BUILD_TAG-NAME : same with your build name
YOUR-BUCKET-NAME : same in passwd-ossfile
YOUR_REGION_OSS : change to your region oss 
	example : oss-ap-southeast-5

```

Run docker-compose
------------------
```bash
docker-compose up
```
or

```bash
docker-compose up --build
```