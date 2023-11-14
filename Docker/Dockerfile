#base image
FROM centos:7

#update packages
RUN yum -y update

# install apache
RUN yum install -y httpd # containerize an apache web app

# copy web app from local to the container
COPY index.html /var/www/html

# port on which the app should listen to
EXPOSE 80

# systemctl start httpd
# you can use CMD or ENTRYPOINT 
ENTRYPOINT [ "/usr/sbin/httpd"]

# Run the container in the background (No exit)
CMD [ "-D", "FOREGROUND"]