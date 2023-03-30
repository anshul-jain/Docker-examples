# Web server Image
FROM httpd:2.4

# Copy files or folders from source to the dest path in the image's filesystem.
# Source = website.tar.gz
# Destination = /usr/local/apache2/htdocs/

ADD website.tar.gz . /usr/local/apache2/htdocs/


# Copy: Copy files or folders from source to the dest path in the image's filesystem.
# ADD : The ADD instruction copies new files, directories or remote file URLs from <src> and adds them to the filesystem of the image at the path <dest>,
#       If <src> is a local tar archive in a recognized compression format (identity, gzip, bzip2 or xz) then it is unpacked as a directory without any extra instruction.

# For running the image we are exposing the port 8080 and localhost:8080 you will see you msg. 
#docker run -p 8080:80 mywebserver:2
