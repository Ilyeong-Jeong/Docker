FROM ubuntu:20.04

RUN apt-get update
RUN apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_14.x | bash -
RUN apt-get install -y nodejs
RUN apt-get install -y git
RUN apt-get install -y libssl-dev
RUN curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add -
RUN echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list
RUN apt-get update && apt-get install yarn
RUN npm install webpack -g
RUN npm install webpack-cli -g
RUN npm install webpack-dev-server -g

# Deploy environment

# Docker install
# ENV DEBIAN_FRONTEND noninteractive
# RUN apt-get update && apt-get install -y apt-transport-https ca-certificates gnupg-agent software-properties-common
# RUN curl -fsSL https://download.docker.com/linux/ubuntu/gpg | apt-key add -
# RUN add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
# RUN apt-get update && apt-get install -y docker-ce docker-ce-cli containerd.io

# awscli install
# RUN apt-get install -y awscli

EXPOSE 노출시킬 포트 번호

ENTRYPOINT ["/bin/bash"]