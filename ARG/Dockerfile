ARG version
FROM almalinux:${version:-9}
ENV name="satya" \
    city="rjy"
ARG role="DevSecOps_Engineer"
RUN role=$role
RUN echo "Hi, name is: ${name}, city is: ${city}, role is: ${role}"
CMD ["sleep", "1000"]