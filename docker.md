# Docker

## Dockerfile
```
# Syntax: FROM <image_name>[:<tag>]
# if TAG is not specified, then 'latest' is going to be used
# there is a special/reserved word 'scratch' which can be used as an image name
# this means there is no basic-layer and an image is going to be created from scratch
FROM nginx:1.16


# COPY [--chown=<user>:<group>] <src>... <dest>
# Syntax: COPY [--chown=<user>:<group>] <src>... <dest>
# If the destination includes a path with one or more directories, all of them will be created if they don't exist
# providing the --chown parameter sets owner and group on the destination files
# when the source is a folder, the contents of the folder are copied but not the folder itself
COPY requirements.txt /app/requirements.txt
```
