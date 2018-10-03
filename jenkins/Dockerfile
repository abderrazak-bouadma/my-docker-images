FROM jenkins/jenkins
LABEL maintainer="bouadma.abderrazak@gmail.com"

ENV terraform_version 0.11.8
ENV packer_version 1.3.1
USER root

RUN apt-get install -y \
    unzip

WORKDIR /temp

RUN curl https://releases.hashicorp.com/terraform/${terraform_version}/terraform_${terraform_version}_linux_amd64.zip --output terraform_${terraform_version}_linux_amd64.zip 
RUN unzip terraform_${terraform_version}_linux_amd64.zip 
RUN mv terraform /usr/local/bin 
RUN terraform --version 
RUN rm terraform_${terraform_version}_linux_amd64.zip

RUN curl https://releases.hashicorp.com/packer/${packer_version}/packer_${packer_version}_linux_amd64.zip --output packer_${packer_version}_linux_amd64.zip
RUN unzip packer_${packer_version}_linux_amd64.zip
RUN mv packer /usr/local/bin
RUN packer --version
RUN rm packer_${packer_version}_linux_amd64.zip

