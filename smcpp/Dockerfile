FROM python:3.6-slim

LABEL mantainer="André M. Ribeiro dos Santos <andremrsantos@gmail.com>"

RUN apt-get update && \
    apt-get install -yq --no-install-recommends \
    build-essential make zlib1g-dev libbz2-dev liblzma-dev \
    libgmp-dev libmpfr-dev libgsl0-dev git && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

RUN pip install cython numpy && \
    pip install git+https://github.com/popgenmethods/smcpp

WORKDIR /smcpp

CMD ["/bin/bash"]