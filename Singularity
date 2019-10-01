BootStrap: docker
From: ubuntu:18.04

%labels
    Maintainer zyou@osc.edu
    Recipe https://github.com/OSC/sa_singularity_iqmol

%post
    apt update
    apt upgrade -y
    apt install -y wget
    wget -nc http://iqmol.org/download.php?get=iqmol_2.13b.deb -O iqmol.deb
    DEBIAN_FRONTEND=noninteractive dpkg -i iqmol.deb || true
    DEBIAN_FRONTEND=noninteractive apt install -f -y
    DEBIAN_FRONTEND=noninteractive dpkg -i iqmol.deb
    rm -f iqmol.deb
    apt autoclean
    apt autoremove --purge -y
    rm -rf /var/lib/apt/lists/*

%runscript
    exec iqmol "$@"

