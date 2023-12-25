# Use the official Amazon Linux image as the base image
FROM amazonlinux:2

# Install necessary dependencies and run the script
RUN yum update -y \
    && yum install -y httpd \
    && yum install -y wget \
    && yum install -y unzip \
    && cd /var/www/html \
    && wget https://github.com/Busayor123/Busayor123/files/12009170/html.file.zip \
    && unzip html.file.zip \
    && cp -r techmax-main/* /var/www/html/ \
    && rm -rf html.file.zip \
# Expose port 80 if your application listens on this port
EXPOSE 80

# Start Apache HTTP server in the foreground
CMD ["httpd", "-D", "FOREGROUND"]
