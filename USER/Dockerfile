FROM almalinux:9
# RUN dnf install nginx -y
# # CMD ["nginx","-g","daemon off;"]
# CMD ["ping","google.com"]
# ENTRYPOINT ["ping","google.com"]
#Alternative way to use ENTRYPOINT command
RUN dnf install -y nginx
RUN useradd satya
USER satya
CMD ["google.com"]
ENTRYPOINT ["ping"]
