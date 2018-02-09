FROM gocd/gocd-agent-centos-7:v18.1.0
MAINTAINER  Mason <mason.servant@kakaocorp.com>

# docker install
RUN yum install -y curl
RUN yum install -y docker-client
RUN yum install -y sudo

# gocd agent settings
ENV AGENT_AUTO_REGISTER_RESOURCES docker-client
