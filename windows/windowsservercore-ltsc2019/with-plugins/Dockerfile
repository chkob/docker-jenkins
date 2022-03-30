FROM cdaecha/docker-jenkins:ltsc2019

ARG ExternalAppPath=C:/LocalApp
ARG ExternalToolsPath=C:/ExternalTools
ARG ExternalConsoleServicePath=C:/SpeServices

ENV EXTERNAL_APP_PATH ${ExternalAppPath}
ENV EXTERNAL_TOOLS_PATH ${ExternalToolsPath}
ENV EXTERNAL_CONSOLE_SERVICES_PATH ${ExternalConsoleServicePath}

VOLUME $EXTERNAL_APP_PATH
VOLUME $EXTERNAL_TOOLS_PATH
VOLUME $EXTERNAL_CONSOLE_SERVICES_PATH

USER jenkins

# download list of plugin and put to data directory
#RUN Invoke-WebRequest -UseBasicParsing -Uri https://raw.githubusercontent.com/chkob/docker-jenkins/custom/windows/shares/jenkins-plugins.yml -OutFile "C:/ProgramData/Jenkins/jenkins-plugins.yml";
#RUN "C:/ProgramData/Jenkins/jenkins-plugin-cli.ps1" --plugin-file "C:/ProgramData/Jenkins/jenkins-plugins.yml"

RUN $newPath = ('{0};C:\ExternalTools\Git\bin' -f $env:PATH); \
    Write-Host ('Updating PATH: {0}' -f $newPath); \
    [Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);