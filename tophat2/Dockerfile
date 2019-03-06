FROM python:2.7-alpine

MAINTAINER AM Ribeiro-dos-Santos <andremrsantos@gmail.com>

WORKDIR /bin

RUN apk add --no-cache --update-cache wget openssl \
    && wget http://ccb.jhu.edu/software/tophat/downloads/tophat-2.0.14.Linux_x86_64.tar.gz \
    && tar zxvf tophat-2.0.14.Linux_x86_64.tar.gz
RUN wget --no-check-certificate --default-page=bowtie2-2.2.3-linux-x86_64.zip \
    http://sourceforge.net/projects/bowtie-bio/files/bowtie2/2.2.3/bowtie2-2.2.3-linux-x86_64.zip/ \
    && unzip bowtie2-2.2.3-linux-x86_64.zip
RUN wget --no-check-certificate --default-page=bowtie-1.2.2-linux-x86_64.zip \
    http://sourceforge.net/projects/bowtie-bio/files/bowtie/1.2.2/bowtie-1.2.2-linux-x86_64.zip/ \
    && unzip bowtie-1.2.2-linux-x86_64.zip
RUN rm -f tophat-2.0.14.Linux_x86_64.tar.gz \
    bowtie2-2.2.3-linux-x86_64.zip \
    bowtie-1.2.2-linux-x86_64.zip

ENV PATH $PATH:/bin/tophat-2.0.14.Linux_x86_64:/bin/bowtie2-2.2.3:/bin/bowtie-1.2.2

WORKDIR /home

CMD [ "tophat2" ]