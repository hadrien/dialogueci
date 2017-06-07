FROM circleci/python:3.6.1

RUN curl -sL https://deb.nodesource.com/setup_7.x | sudo -E bash - && \
    sudo apt-get update && \
    sudo apt-get install -y build-essential && \
    sudo apt-get install -y nodejs && \
    sudo npm install -g serverless && \
    sudo npm install -g yarn

ENV TF_VERSION=0.9.5
ENV TF_URL=https://releases.hashicorp.com/terraform/${TF_VERSION}/terraform_${TF_VERSION}_linux_amd64.zip

RUN cd bin && \
    sudo curl ${TF_URL} -o tf.zip && \
    sudo unzip tf.zip -d /bin &&\
    sudo rm tf.zip

RUN sudo pip install awscli menhir
