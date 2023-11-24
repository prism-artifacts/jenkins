FROM jenkins/inbound-agent:latest-jdk11
USER root
RUN apt-get -y update \
    && apt-get -y upgrade \
    && apt-get -y install \
        gnupg \
        software-properties-common \
        curl \
        bash \
        jq \
        python3 \
        python3-pip \
        unzip \
    && curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip" \
    && unzip awscliv2.zip \
    && ./aws/install
# Install Terraform
RUN curl -fsSL https://apt.releases.hashicorp.com/gpg | apt-key add - \
    && apt-add-repository "deb [arch=amd64] https://apt.releases.hashicorp.com $(lsb_release -cs) main" \
    && apt update \
    && apt-get install -y terraform