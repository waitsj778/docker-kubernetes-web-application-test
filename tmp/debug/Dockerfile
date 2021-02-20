FROM centos:7

COPY . /tmp/debug

RUN mv /tmp/debug/mongodb-org-4.0.repo /etc/yum.repos.d

RUN yum install -y mongodb-org-shell-4.0.5
RUN yum install -y mongodb-org-tools-4.0.5

RUN yum install -y iproute net-tools

RUN curl -o /usr/local/bin/jq -L https://github.com/stedolan/jq/releases/download/jq-1.6/jq-linux64

RUN chmod +x /usr/local/bin/jq

RUN yum clean all