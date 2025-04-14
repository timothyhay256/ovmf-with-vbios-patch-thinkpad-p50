FROM ubuntu:jammy
LABEL maintainer="bitthief@pm.me"

RUN apt-get -qq -y update && \
    apt-get -qq -y upgrade && \
    apt-get -qq -y install -y wget vim build-essential git iasl nasm subversion libwww-perl uuid-dev dos2unix python3 python-is-python3
#RUN update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-7 60 --slave /usr/bin/g++ g++ /usr/bin/g++-7 && \
#    update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-5 60 --slave /usr/bin/g++ g++ /usr/bin/g++-5 && \
#    echo 1 | update-alternatives --config gcc
RUN git clone --recursive https://github.com/tianocore/edk2.git
COPY files/ /ovmf
