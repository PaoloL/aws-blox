FRO  ubuntu:14.04
# Ubuntu and nodeJS for ElasticBeanstalk
#
# VERSION               0.0.1

FROM ubuntu:14.04
MAINTAINER Paolo Latella <paolo.latella@xpeppers.com>

#Port mapping
EXPOSE 8080

#Update and install nodejs
RUN apt-get update && apt-get install -y nodejs

#Copy files for nodejs application
RUN mkdir /var/www/
ADD myws.js /var/www/

#Start application
CMD /usr/bin/nodejs /var/www/myws.js
