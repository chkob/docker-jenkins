FROM cdaecha/docker-jenkins:ltsc2019

USER jenkins

# download list of plugin and put to data directory
RUN Invoke-WebRequest -UseBasicParsing -Uri https://raw.githubusercontent.com/chkob/docker-jenkins/custom/windows/shares/jenkins-plugins.yml -OutFile "C:/ProgramData/Jenkins/jenkins-plugins.yml";
RUN jenkins-plugin-cli --plugin-file "C:/ProgramData/Jenkins/jenkins-plugins.yml"