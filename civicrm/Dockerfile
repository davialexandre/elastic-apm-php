FROM davialexandre/civicrm:5.23.2

RUN apt-get update && \
    apt-get install -y git libcurl4-openssl-dev && \
    cd $HOME && \
    git clone https://github.com/elastic/apm-agent-php.git && \
    cd apm-agent-php/src/ext && \
    phpize && \
    ./configure --enable-elastic_apm && \
    make clean && make && make install