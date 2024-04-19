FROM docker.io/alpine/k8s:1.26.13
RUN apk add g++ && apk add make jq
ARG TERRAFORM_VERSION=1.7.3
#Terraform Installation
RUN wget https://releases.hashicorp.com/terraform/${TERRAFORM_VERSION}/terraform_${TERRAFORM_VERSION}_linux_amd64.zip && \
    unzip terraform_${TERRAFORM_VERSION}_linux_amd64.zip && \
    mv terraform /usr/local/bin && \
    rm terraform_${TERRAFORM_VERSION}_linux_amd64.zip    
# #TFLINT Installation
RUN wget https://github.com/terraform-linters/tflint/releases/latest/download/tflint_linux_amd64.zip && \
    unzip tflint_linux_amd64.zip && \
    mv tflint /usr/local/bin && \
    rm tflint_linux_amd64.zip    