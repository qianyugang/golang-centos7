FROM centos:centos7

RUN curl -sL https://go.dev/dl/go1.17.5.linux-amd64.tar.gz -o go.tar.gz && tar xzf go*gz -C /usr/local && rm -f go*gz
ENV GOROOT=/usr/local/go
ENV GOPATH=/usr/lib/go
ENV PATH=$GOPATH/bin:$GOROOT/bin:$PATH

WORKDIR /project

RUN yum install epel-release  -y && \
    yum update -y && \
    yum install -y lz4-devel lz4 git&& \
    yum install -y rpm-build rpmdevtools
