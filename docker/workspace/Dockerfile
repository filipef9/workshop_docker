FROM node:6.11.2-alpine

LABEL maintainer="fsnascimento@stefanini.com"

RUN \
    apk update &&\
    apk add --no-cache --virtual .persistent-deps \
        curl \
        openssl \
        openssh-client \
        vim \
        git \
        # node-sass dependencies
        build-base \
        python \
        py-pip &&\
    # shell setup
    sed -i -e "s/bin\/ash/bin\/sh/" /etc/passwd &&\
    npm cache clean &&\
    # config npm with user root
    npm -g config set user root
RUN \
    # install node dev packages
    npm install -g \
        browser-sync@2.9.11 \
        bower@1.8.0

# set up the workspace directory
VOLUME ["/workspace"]
WORKDIR /workspace

EXPOSE 8000

CMD ["npm", "-v"]