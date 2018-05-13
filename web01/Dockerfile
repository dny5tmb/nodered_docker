FROM centos:7

MAINTAINER "youhei"

# system update
RUN yum update -y && yum clean all
RUN yum install -y epel-release  

# web server install
RUN yum install -y httpd

ADD hello.html /var/www/html
EXPOSE 80

# enable service.
#RUN systemctl enable httpd

# exec.
# CMD ["/sbin/init"]
CMD ["/usr/sbin/httpd", "-D", "FOREGROUND"]