FROM python:2.7-alpine

MAINTAINER AM Ribeiro-dos-Santos <andremrsantos@gmail.com>

RUN apk add --no-cache --update-cache \
		gcc build-base gsl-dev git \
		openblas-dev freetype-dev pkgconfig gfortran \
	&& pip --no-cache-dir install cython numpy scipy \
	&& git clone https://github.com/rajanil/fastStructure.git \
	&& cd /fastStructure/vars \
	&& python setup.py build_ext --inplace \
	&& cd /fastStructure \
	&& python setup.py build_ext --inplace

WORKDIR /fastStructure

CMD ["/bin/sh", "-c"]
