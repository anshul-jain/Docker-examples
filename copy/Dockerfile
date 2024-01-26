# Web server Image
FROM httpd:2.4

# Copy files or folders from source to the dest path in the image's filesystem.
# Source = .
# Destination = /usr/local/apache2/htdocs/

COPY . /usr/local/apache2/htdocs/


# For running the image we are exposing the port 8080 and localhost:8080 you will see you msg. 
#docker run -p 8080:80 mywebserver:1
