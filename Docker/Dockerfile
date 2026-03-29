FROM eclipse-temurin:21-jre

RUN addgroup --system --gid 1001 spring && \
    adduser --system --uid 1001 --ingroup spring spring

WORKDIR /app

COPY target/app.jar /app/app.jar

RUN chown -R spring:spring /app

USER spring

EXPOSE 8888

ENTRYPOINT ["sh", "-c", "java $JAVA_OPTS -jar app.jar"]