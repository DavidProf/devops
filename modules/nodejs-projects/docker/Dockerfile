# ARG for image, can be set using
# docker build . --build-arg IMAGE=node:16-alpine3.11 -t nodejs
# the above command would build a new image with the official nodejs image
ARG IMAGE=mhart/alpine-node:16
# docker build . --build-arg PACKAGE_MANAGER=yarn -t nodejs
# the above command would build a new image using yarn as package manager
ARG PACKAGE_MANAGER=npm

# build environment - isolated context to minimize the image size
FROM $IMAGE as build

# set work directory to build the image
WORKDIR build

# copy only package.json file to cache dependencies
COPY package.json .

# install dependencies for production (ignore dev dependencies)
RUN $PACKAGE_MANAGER install --production

# copy src files to context
COPY src src

# application environment - final context to create image
FROM $IMAGE

# set work directory for application files
WORKDIR /project

# copy build to project
COPY --from=build build /project

# set image command to execute on docker run
CMD ["node", "src/index.js"]
