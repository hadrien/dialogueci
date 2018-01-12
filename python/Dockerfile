FROM circleci/python:3.6.1

RUN curl -sL https://deb.nodesource.com/setup_8.x | sudo -E bash - && \
    sudo apt-get update && \
    sudo apt-get install -y build-essential && \
    sudo apt-get install -y nodejs && \
    sudo npm install -g serverless && \
    sudo npm install -g yarn

RUN sudo pip install awscli

RUN sudo sed -i -e 's/# en_CA.UTF-8 UTF-8/en_CA.UTF-8 UTF-8/' /etc/locale.gen && \
    sudo sed -i -e 's/# fr_CA.UTF-8 UTF-8/fr_CA.UTF-8 UTF-8/' /etc/locale.gen && \
    sudo dpkg-reconfigure --frontend=noninteractive locales
