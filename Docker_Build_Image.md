## Build and push the image to github container registry

**Note:** If the repository is cloned move to Images/Nginx folder. Build will use the 'Dockerfile' at current folder

```

git clone https://github.com/SMACAcademy/mynginx_image1.git

docker build -t ghcr.io/smacacademy/mynginx_image1:v1 .

docker images

docker push ghcr.io/smacacademy/mynginx_image1:v1
```
**Note1:** There is a dot in the end which points to the current.
**Note2:** Change the account name to your github account

---

## Build container image with sample php file

```


docker build -t ghcr.io/smacacademy/docker_phpinfo .

docker images


docker run --name myphpinfo -p 80:80 -d ghcr.io/smacacademy/docker_phpinfo
docker run --name myphpinfo8080 -p 8080:80 -d ghcr.io/smacacademy/docker_phpinfo

docker push ghcr.io/smacacademy/docker_phpinfo

```