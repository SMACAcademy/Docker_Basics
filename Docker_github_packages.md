# GitHub Packages

## Login to Container Registry
```
export CR_PAT=YOUR_TOKEN

echo $CR_PAT | docker login ghcr.io -u USERNAME --password-stdin
```
**Note:** Generate token from github, and export using env variable. 


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

## Pull the image and run a container

```
docker pull muthu4all/php_app_color:maroon

docker pull ghcr.io/smacacademy/mynginx_image1:v1

docker run --name my_first_app -p 80:80 -d ghcr.io/smacacademy/mynginx_image1:v1

```
