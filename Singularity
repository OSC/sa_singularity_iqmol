BootStrap: docker
From: centos:7

%labels
    Maintainer zyou@osc.edu
    Recipe https://github.com/OSC/sa_singularity_iqmol

%post
    yum install -y \
        wget \
        qt5-qtbase
    cd /
    wget -nc http://iqmol.org/download.php?get=iqmol-2.14.0-1.el7.centos.x86_64.rpm -O iqmol.rpm
    yum -y localinstall iqmol.rpm
    rm -f iqmol.rpm
    rm -rf /var/cache/yum/*

%runscript
    exec iqmol "$@"

