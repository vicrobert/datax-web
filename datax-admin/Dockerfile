FROM openjdk:8-jre-alpine
MAINTAINER yangjunbo@360.cn
ENV TZ=Asia/Shanghai
RUN apk add tzdata && ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
WORKDIR /
COPY ./target/datax-admin-2.1.2.jar /datax-admin-2.1.2.jar
ENTRYPOINT ["java", "-jar", "datax-admin-2.1.2.jar"]