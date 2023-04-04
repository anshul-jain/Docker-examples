FROM alpine:latest

RUN apk add python

CMD [ "5.5.5.5" ]

ENTRYPOINT [ "ping","-t" ,"5" ]



#RUN executes the command(s) that you give in a new layer and creates a new image. This is mainly used for installing a new package.(Runs Docker Image build time)

#CMD is the default command to be run by the entrypoint. It sets default command and/or parameters, however, we can overwrite those commands or pass in and bypass the default parameters from the command line when docker runs
# (Container run time)

#ENTRYPOINT is the program to run the given command. It is used when yo want to run a container as an executable.

# The difference is ENTRYPOINT is that unlike CMD, the command and parameters are not ignored when Docker container runs with command line parameters.

##############

#Use RUN instructions to build your image by adding layers on top of the initial image.

#Prefer ENTRYPOINT to CMD when building executable Docker image and you need a command always to be executed, and use CMD if you need to provide extra default arguments that could be overwritten from the command line when docker container runs.

#Choose CMD if you need to provide a default command and/or arguments that can be overwritten from the command line when docker container runs.