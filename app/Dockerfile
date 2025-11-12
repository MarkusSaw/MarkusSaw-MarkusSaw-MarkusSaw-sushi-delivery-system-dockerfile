FROM eclipse-temurin:11-jre

WORKDIR /app


COPY sushi-delivery-1.0.0.jar.original app.jar


RUN groupadd -r -g 1001 appgroup && \
    useradd -r -u 1001 -g appgroup appuser


RUN chown -R appuser:appgroup /app
USER appuser

EXPOSE 8080


ENTRYPOINT ["java", "-jar", "app.jar"]
