FROM openjdk:11 AS BUILD_IMAGE
RUN apt update && apt install maven -y
RUN git clone https://github.com/xiaochili/tomatotest.git
RUN cd tomatotest && git checkout main && mvn install

FROM tomcat:9-jre11

RUN rm -rf /usr/local/tomcat/webapps/*

COPY --from=BUILD_IMAGE tomatotest/target/reggie_take_out-v1.war /usr/local/tomcat/webapps/ROOT.wart

EXPOSE 8080
CMD ["catalina.sh", "run"]
