## What is this?
This image will execute a container which will generate a log message in an uninterrupted time to fill one or more files fast.

## Why this Image?
I've had the necessity to create a lot of log to fill the file size and rotate to test log configurations with containers, this helped me out to do it easily.

## What is inside of this repo?
In this git repository you will find the docker image definitions for the random Logger for Alpine Linux

* `Dockerfile` -> Contains image definition.
* `entrypoint.sh` -> Shell code to generate log messages.

## How do I use this image?
To use this image you must do as follows:

```
# you can use tags latest
docker pull luankevinferreira/random-logger:latest

# to run the image just execute
docker run -d luankevinferreira/random-logger:latest
```

You will have now a docker container running and generating log messages, locate it running:

```
docker ps
```

You can see the logs using this command

```
docker logs <- container-id ->
```

## How do I build this images?
First things first, you can find these docker images in `luankevinferreira/random-logger`
but you can also build a specific version on your own, you only need:

- docker
- git

Clone this repo

`git clone https://github.com/luankevinferreira/random-logger.git`

Go to the folder in your terminal and type this:

```
# cd into folder
cd random-logger
# Then build the new image
docker build -f Dockerfile .
```

If you want to tag your image use the following command

```
docker build -f Dockerfile -t yourbase/yourname:version .
```

If you want to push to your registry use the following command
```
docker push yourbase/yourname:version
```
---
For more on docker build reference to the [Documentation](https://docs.docker.com/engine/reference/commandline/build/)

You can get the source from the image in the [Repository](https://github.com/luankevinferreira/random-logger)
