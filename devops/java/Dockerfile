# 基础镜像
FROM tomcat:8.5.32
LABEL maintainer="yaokun <yaokun@bwcxtech.com>"
#构建参数
ARG WAR_FILE="tms.war"
#环境变量
ENV TZ "Asia/Shanghai"
#复制项目
RUN rm -rf /usr/local/tomcat/webapps
COPY ./target/$WAR_FILE /usr/local/tomcat/webapps/
#工作空间
WORKDIR /usr/local/tomcat
#监听端口
EXPOSE 8080
#启动tomcat服务器
CMD ["catalina.sh", "run"]
