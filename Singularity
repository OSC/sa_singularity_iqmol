BootStrap: docker
From: ubuntu:18.04

%labels
    Maintainer zyou@osc.edu
    Recipe https://github.com/OSC/sa_singularity_iqmol

%environment
    export QC=/opt/qchem
    export QCAUX=$QC/qcaux
    export QCPROG_S=$QC/exe/qcprog.exe_s
    export QCMPI=mpich3
    export QCRSH=ssh
    export PATH=$PATH:$QC/exe:$QC/bin
    export QCSCRATCH=$TMPDIR

%post
    apt update
    apt upgrade -y
    apt install -y wget
    wget -nc http://iqmol.org/download.php?get=iqmol_2.14.deb -O iqmol.deb
    DEBIAN_FRONTEND=noninteractive dpkg -i iqmol.deb || true
    DEBIAN_FRONTEND=noninteractive apt install -f -y
    DEBIAN_FRONTEND=noninteractive dpkg -i iqmol.deb
    rm -f iqmol.deb
    apt autoclean
    apt autoremove --purge -y
    rm -rf /var/lib/apt/lists/*

%runscript
    exec iqmol "$@"

