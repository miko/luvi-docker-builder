FROM stackbrew/centos:5

RUN rpm -Uvh http://dl.fedoraproject.org/pub/epel/5/x86_64/epel-release-5-4.noarch.rpm
RUN yum install -y rpmdevtools git gnupg rpm-sign ruby rubygems \
                   ruby-devel cmake gcc make
RUN gem install fpm

RUN rpmdev-setuptree
RUN mkdir -p /build/package
WORKDIR /build

RUN git clone https://github.com/luvit/luvi
WORKDIR luvi
RUN git checkout feat/packaging
RUN git submodule update --init --recursive
RUN make tiny
RUN make package-rpm
RUN cp /build/luvi/luvi-*.rpm /build/package