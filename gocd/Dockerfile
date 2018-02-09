FROM gocd/gocd-agent-centos-7:v18.1.0
MAINTAINER  Mason <mason.servant@kakaocorp.com>

# docker install
RUN yum install -y curl
RUN yum install -y sudo
RUN echo -e "\n## GoCD\ngo	ALL=(ALL) NOPASSWD: ALL" >> /etc/sudoers
RUN yum install -y yum-utils device-mapper-persistent-data lvm2
RUN yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
RUN sudo yum install -y docker-ce

# gocd agent settings
ENV AGENT_AUTO_REGISTER_RESOURCES docker-client
