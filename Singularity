BootStrap: docker
From: tensorflow/tensorflow:latest-devel-gpu

%labels
    MAINTAINER hpcdevops
    WHATAMI tensorflow-gpu

%files
    hello.tensorflow.py /hello.tensorflow.py

%runscript
    exec /usr/bin/python "$@"

%post

    # create bind points for SDSC HPC environment
    mkdir /oasis /projects /scratch

    # build info
    echo "Timestamp:" `date --utc` | tee /image-build-info.txt
