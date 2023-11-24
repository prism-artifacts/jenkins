FROM jenkins/jenkins:lts
RUN echo 2.0 > /usr/share/jenkins/ref/jenkins.install.UpgradeWizard.state
COPY files/plugins.txt /usr/share/jenkins/ref/plugins.txt
RUN jenkins-plugin-cli -f /usr/share/jenkins/ref/plugins.txt
ENV CASC_JENKINS_CONFIG /usr/share/jenkins/ref/jenkins.yaml
#COPY files/job.xml /usr/share/jenkins/ref/jobs/serverless-jenkins-on-ecs/config.xml
COPY files/initialConfig.groovy /usr/share/jenkins/ref/init.groovy.d/initialConfigs.groovy
COPY files/jenkins_casc.yaml /usr/share/jenkins/ref/jenkins.yaml
