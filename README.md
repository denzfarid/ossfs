# ossfs Docker and docker-compose ossfs

Build Docker for ossfs and run with docker-compose

Build Dockerfile
----------------
```bash
docker build -t YOUR_BUILD_TAG-NAME .
```

Or with Docker pull
```bash
docker pull denzfarid/ossfs
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
image : change with same YOUR_BUILD_TAG-NAME or use docker image denzfarid/ossfs
YOUR-BUCKET-NAME : same in passwd-ossfile
YOUR_REGION_OSS : change to your region oss 
	example : oss-ap-southeast-5

```

Before run dcoker compose up
----------------------------
```bash 
$ echo "Bucketname:aliyunaccsesskey:aliyunsecretkey" > passwd-ossfs
$ chmod 640 passwd-ossfs
$ mkdir ossfs
$ mount --bind ossfs ossfs
$ mount --make-shared ossfs
$ findmnt -o TARGET,PROPAGATION ossfs
$ ln -s ossfs/uploads uploads
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