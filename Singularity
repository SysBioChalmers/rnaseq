From:nfcore/base
Bootstrap:docker

%labels
    MAINTAINER Phil Ewels <phil.ewels@scilifelab.se>
    DESCRIPTION Singularity image containing all requirements for the nf-core/rnaseq pipeline
    VERSION 1.1

%environment
    PATH=/opt/conda/envs/nf-core-rnaseq-1.1/bin:$PATH
    export PATH

%files
    environment.yml /

%post
    /opt/conda/bin/conda env create -f /environment.yml
    /opt/conda/bin/conda clean -a
    mkdir -p /c3se
    mkdir -p /local
    mkdir -p /apps
    mkdir -p /usr/share/lmod/lmod
    mkdir -p /var/hasplm
    mkdir -p /var/opt/thinlinc
    mkdir -p /usr/lib64
    touch /usr/lib64/libdlfaker.so
    touch /usr/lib64/libvglfaker.so
    touch /usr/bin/nvidia-smi
