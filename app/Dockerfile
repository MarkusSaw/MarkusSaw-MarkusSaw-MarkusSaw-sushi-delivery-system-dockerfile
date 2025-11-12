FROM eclipse-temurin:11-jre

WORKDIR /app

COPY sushi-delivery-1.0.0.jar.original app.jar

RUN addgroup -g 1001 -S appgroup && \
    adduser -S appuser -u 1001 -G appgroup

RUN chown -R appuser:appgroup /app
USER appuser

EXPOSE 8080

ENTRYPOINT ["java", "-jar", "app.jar"]
