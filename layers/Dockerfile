# FROM ubuntu:16.04
# RUN apt-get update
# RUN apt install curl -y
# RUN apt install ruby -y
# RUN apt install python -y
# RUN apt install build-essential -y
# RUN apt install apache2 -y


FROM ubuntu:16.04
RUN apt-get update && \
apt install curl -y && \
apt install ruby -y && \
apt install python -y && \
apt install build-essential -y && \
apt install apache2 -y && \

# With the help of && \ we are combining the layers and this will help us to save some MBs in image size.

# Build the image
# docker image build . -t layer:1 