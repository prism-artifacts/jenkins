FROM jenkins/inbound-agent:latest-jdk11
USER root
RUN apt-get -y update \
    && apt-get -y upgrade \
    && apt-get -y install \
        gnupg \
        wget \
        software-properties-common \
        curl \
        bash \
        jq \
        python3 \
        python3-pip \
RUN pip3 install aws-cli