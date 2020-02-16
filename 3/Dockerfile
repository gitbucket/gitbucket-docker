FROM openjdk:8-jre

LABEL maintainer="Naoki Takezoe <takezoe [at] gmail.com>"

ADD https://github.com/gitbucket/gitbucket/releases/download/3.14/gitbucket.war /opt/gitbucket.war

RUN ln -s /gitbucket /root/.gitbucket

VOLUME /gitbucket

# Port for web page and Port for SSH access to git repository (Optional)
EXPOSE 8080 29418

CMD ["java", "-jar", "/opt/gitbucket.war"]

