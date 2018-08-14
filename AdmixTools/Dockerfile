FROM debian:jessie

LABEL mantainer="André M. Ribeiro dos Santos <andremrsantos@gmail.com>"

ENV PATH=$PATH:/AdmixTools/bin
RUN apt-get update && \
    apt-get install -yq --no-install-recommends \
        build-essential \
        git \
        libopenblas-dev \
        libgsl0-dev && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*
RUN git clone https://github.com/DReichLab/AdmixTools.git && \
    cd AdmixTools/src && \
    make clobber && \
    make install