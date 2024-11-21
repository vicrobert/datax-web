FROM openjdk:8-jre-alpine
MAINTAINER yangjunbo@360.cn
ENV TZ=Asia/Shanghai
RUN apk add tzdata && ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
RUN mkdir -p /logs/executor/jobhandler

# 安装python3
RUN apk add --no-cache python3
RUN ln -snf /usr/bin/python3 /usr/bin/python
ENV PYTHONUNBUFFERED=1

WORKDIR /
COPY ./target/datax-executor-2.1.2.jar /datax-executor-2.1.2.jar
ENTRYPOINT ["java", "-jar", "datax-executor-2.1.2.jar"]