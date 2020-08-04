FROM openjdk:8-jre

LABEL maintainer="Naoki Takezoe <takezoe [at] gmail.com>"

ADD https://github.com/gitbucket/gitbucket/releases/download/4.34.0/gitbucket.war /opt/gitbucket.war

ENV GITBUCKET_HOME=/gitbucket

# Give permissions for root group
RUN chmod g=u /opt/gitbucket.war && \
    mkdir -p $GITBUCKET_HOME && \
    chmod g+w $GITBUCKET_HOME

VOLUME $GITBUCKET_HOME


# Port for web page and Port for SSH access to git repository (Optional)
EXPOSE 8080 29418

ARG USERID=1001
USER ${USERID}

CMD ["sh", "-c", "java -jar /opt/gitbucket.war"]

