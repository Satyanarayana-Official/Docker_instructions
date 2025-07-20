FROM almalinux:9
RUN mkdir /tmp/workdir-me
# RUN cd /tmp/workdir-normal-[it will not work eg cd will not work with run]
WORKDIR cd /tmp/workdir-me
RUN pwd
RUN echo "Hi Satya how are you today" > hello.txt
CMD ["sleep", "1000"]