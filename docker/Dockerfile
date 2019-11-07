FROM jenkins:lts
LABEL Description="A simple Jenkins Master container with a Jenkins YAML Configuration."

USER root

RUN apt-get update; apt-get install -y python3-pip python3 git

RUN pip3 install boto3 && \
    pip3 install troposphere && \
    pip3 install botocore && \
    pip3 install awscli

COPY configuration/jenkins.yaml /var/jenkins_home/casc_configs/jenkins.yaml