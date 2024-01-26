# GOAL: Create a web server

# Base Image
FROM centos:latest

# Error: Failed to download metadata for repo 'appstream': Cannot prepare internal mirrorlist: No URLs in mirrorlist
RUN cd /etc/yum.repos.d/
RUN sed -i 's/mirrorlist/#mirrorlist/g' /etc/yum.repos.d/CentOS-*
RUN sed -i 's|#baseurl=http://mirror.centos.org|baseurl=http://vault.centos.org|g' /etc/yum.repos.d/CentOS-*

# Install Apache web server
RUN yum install -y httpd

# Copy the website to the document root
ADD website.tar.gz /var/www/html/

# Passing the Parameter
CMD [ "-D", "FOREGROUND" ]

# Starting the Apache web server
ENTRYPOINT [ "/usr/sbin/httpd" ]

# Expose port 80
EXPOSE 80

# Build the image
# docker build . -t codechallenge:1 [Building the image from the same directory where the Dockerfile is present]

# Run the container
# docker run -p 8080:80 codechallenge:1 [Running the container in the background and exposing the port 8080]
