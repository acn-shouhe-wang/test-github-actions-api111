# docker build -t nodeserver:v1.0
# docker build --build-arg jar_path=service.jar -f docker/Dockerfile . -t {registry_url}:{tag}
FROM amazoncorretto:11

ENV TZ Asia/Tokyo

COPY service.jar /app/service.jar
RUN chown -R nobody:nobody /app

USER nobody
WORKDIR /app

ENTRYPOINT [ "java" ]
CMD ["-jar", "/app/service.jar"]

