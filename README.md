# docker-mongodb
Create a customized MongoDB docker container

The original intention of this project was to try and use an Alpine Linux base for the image to keep the size as small as possible. Unfortunately it appears this is not an option as:

1) The only version of MongoDB available from official Alpine Linux repos is version 3.2.7-r0 (when they say -r0 I'm assuming they mean rc0?) (https://pkgs.alpinelinux.org/package/edge/testing/x86_64/mongodb) in their testing repo (not their Main or Community repos)

2) MongoDB do supply a binary version in a Tarball (https://docs.mongodb.com/manual/tutorial/install-mongodb-on-linux/) but apparently this is complied using glibc which is not available in Alpine Linux (http://stackoverflow.com/questions/32724556/execute-mongodb-binaries-on-alpine-linux)
