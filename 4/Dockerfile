FROM java:8-jre

MAINTAINER Naoki Takezoe <takezoe [at] gmail.com>

ADD https://github.com/gitbucket/gitbucket/releases/download/4.15.0/gitbucket.war /opt/gitbucket.war

RUN ln -s /gitbucket /root/.gitbucket

VOLUME /gitbucket

# Port for web page
EXPOSE 8080
# Port for SSH access to git repository (Optional)
EXPOSE 29418

CMD ["java", "-jar", "/opt/gitbucket.war"]

