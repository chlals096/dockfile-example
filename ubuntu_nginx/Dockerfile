FROM ubuntu:focal

ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get update \
    && apt-get install -y nginx git && apt-get install -y git
RUN git clone https://github.com/chlals096/static-web-template.git
# COPY sites-available/default /etc/nginx/sites-available/default
RUN cp -r static-web-template/* /usr/share/nginx/html/
CMD ["nginx", "-g", "daemon off;"]
EXPOSE 80