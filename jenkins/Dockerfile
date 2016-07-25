FROM jenkinsci/jenkins
USER root

RUN apt-get update && apt-get install -y libcurl4-gnutls-dev \
    libexpat1-dev \
    gettext \
    libz-dev \
    libssl-dev


#TODO: Verificar forma de buscar sempre a ultima tag 
RUN wget https://github.com/git/git/archive/v2.9.2.tar.gz -O git-src.tar.gz
RUN tar -zxf git-src.tar.gz && \
    cd git-src && \
    make configure && \
    ./configure --prefix=/usr && \
    make all doc info && \
    make install install-doc install-html install-info


USER jenkins