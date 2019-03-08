#Bootstrap: docker
#From: ubuntu:18.04
Bootstrap: localimage
From: ../../ubuntu-1804-updated_container/ubuntu.simg

%labels
MAINTAINER darachm

%help

    This container is for providing `bartender` for some bioinformatic pipelines.
    
%post

    apt-get -y update
    apt-get -y install gcc-4.8 git make g++ python
    git clone https://github.com/LaoZZZZZ/bartender-1.1.git
    cd bartender-1.1
    make all
    make install

%test

    bartender_extractor_com -h
    bartender_single_com -h
    bartender_combiner_com -h

