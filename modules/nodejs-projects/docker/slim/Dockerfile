# in case you want to install the modules before build the image
# ARG for image, can be set using
# docker build . --build-arg IMAGE=node:slim-16 -t nodejs
# the above command would build a new image with the official nodejs image
ARG IMAGE=mhart/alpine-node:slim-16

# application environment - final context to create image
FROM $IMAGE

# set work directory for application files
WORKDIR /project

# copy build to project
COPY . /project

# set image command to execute on docker run
CMD ["node", "src/index.js"]
