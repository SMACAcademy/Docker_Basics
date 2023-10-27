## Build and push the image to github container registry

**Note:** If the repository is cloned move to Images/Nginx folder. Build will use the 'Dockerfile' at current folder

```
cd Images
cd Nginx


docker build -t ghcr.io/smacacademy/mynginx_image1:v1 .

docker images

docker push ghcr.io/smacacademy/mynginx_image1:v1
```
**Note:** There is a dot in the end which points to the current 