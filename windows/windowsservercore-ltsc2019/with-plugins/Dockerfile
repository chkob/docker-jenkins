FROM cdaecha/docker-jenkins:ltsc2019

ARG EXTERNAL_APP_PATH=C:/LocalApp
ARG EXTERNAL_TOOLS_PATH=C:/ExternalTools

ENV EXTERNAL_APP_PATH $EXTERNAL_APP_PATH
ENV EXTERNAL_TOOLS_PATH $EXTERNAL_TOOLS_PATH

VOLUME $EXTERNAL_APP_PATH
VOLUME $EXTERNAL_TOOLS_PATH

USER jenkins

# download list of plugin and put to data directory
RUN Invoke-WebRequest -UseBasicParsing -Uri https://raw.githubusercontent.com/chkob/docker-jenkins/custom/windows/shares/jenkins-plugins.yml -OutFile "C:/ProgramData/Jenkins/jenkins-plugins.yml";
# RUN "C:/ProgramData/Jenkins/jenkins-plugin-cli.ps1" --plugin-file "C:/ProgramData/Jenkins/jenkins-plugins.yml"