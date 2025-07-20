ARG version
FROM almalinux:${version:-9}
ENV NAME="satya" \
    CITY="rjy"
ARG ROLE="DevSecOps_Engineer"
RUN ROLE=${ROLE}
RUN echo "Hi, NAME is: ${NAME}, CITY is: ${CITY}, ROLE is: ${ROLE}"
CMD ["sleep", "1000"]