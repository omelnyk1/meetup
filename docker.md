# Docker

## Dockerfile
```
# Syntax: FROM <image_name>[:<tag>]
#
# if TAG is not specified, then 'latest' is going to be used
# there is a special/reserved word 'scratch' which can be used as an image name
# this means there is no basic-layer and an image is going to be created from scratch
FROM nginx:1.16


# Syntax: COPY [--chown=<user>:<group>] <src>... <dest>
# Meaning: copy files and folders into the Docker image
#
# If the destination includes a path with one or more directories, all of them will be created if they don't exist
# providing the --chown parameter sets owner and group on the destination files
# when the source is a folder, the contents of the folder are copied but not the folder itself
COPY requirements.txt /app/requirements.txt


# Syntax: ADD [--chown=<user>:<group>] <src>... <dest>
# Meaning: copy files and folders into the Docker image
#
# DIFFERENCE from COPY
#  - in case of COPY source can be either file(s) or folder
#  - in case of ADD source can be file(s), folder, local .tag file or a URL
#  -- when the ADD instruction has a source value that is a .tar file, the contents of that TAR file are extracted into a corresponding folder inside the image
#  -- when you use a .tar file as the source in an ADD instruction and include the --chown parameter, the owner, group, and permissions on the extracted contents will match what is contained within the archive
ADD requirements.txt /app/requirements.txt
```
