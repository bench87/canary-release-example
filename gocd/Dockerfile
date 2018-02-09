FROM gocd/gocd-agent-centos-7:v17.10.0
MAINTAINER  Mason <mason.servant@kakaocorp.com>

# docker install
RUN yum install -y curl
RUN yum install -y docker-client
RUN yum install -y sudo
RUN echo -e "\n## GoCD\ngo	ALL=(ALL) NOPASSWD: ALL" >> /etc/sudoers
COPY proxy .
RUN cat proxy >> /etc/profile
RUN source /etc/profile

# go install
RUN curl -LO https://storage.googleapis.com/golang/go1.9.linux-amd64.tar.gz
RUN sudo tar -C /usr/local -xzf go1.9.linux-amd64.tar.gz
ENV PATH $PATH:/usr/local/go/bin

# gocd agent settings
ENV AGENT_AUTO_REGISTER_RESOURCES docker-client

# go bashrc
RUN chown -R go:go /go-support
