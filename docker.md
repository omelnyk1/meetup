# Docker

## Dockerfile
```
# FROM IMAGE_NAME:TAG
# if TAG is not specified, then 'latest' is going to be used
# there is a special/reserved word 'scratch' which can be used as an image name
# this means there is no basic-layer and an image is going to be created from scratch
FROM nginx:1.16
```
