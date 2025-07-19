FROM almalinux:9
RUN dnf install nginx -y
RUN rm -rf /usr/share/nginx/html/index.html
#COPY qi/ /usr/share/nginx/html/
ADD https://raw.githubusercontent.com/Satyanarayana-Official/Softwares_Installation/refs/heads/main/Docker.MD /usr/share/nginx/html/index.html
RUN chmod +r /usr/share/nginx/html/index.html
ADD sample-1.tar /tmp/
CMD ["nginx","-g","daemon off;"]