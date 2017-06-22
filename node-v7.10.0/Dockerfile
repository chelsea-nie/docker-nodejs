FROM alpine:3.6

RUN apk update && apk upgrade && \
    apk add --no-cache curl && \
    apk add -U curl bash ca-certificates openssl ncurses coreutils python2 make gcc g++ libgcc linux-headers && \
    curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.2/install.sh | bash && \
    echo -e 'export NVM_DIR="$HOME/.nvm" \n[ -s "$NVM_DIR/nvm.sh" ] && . "$NVM_DIR/nvm.sh" # This loads nvm' >> ~/.bash_profile && \
    source ~/.bash_profile  && \
    nvm ls-remote  && \
    #nvm install -s 6.11.0 && \
    #nvm use 6.11.0  && \
    nvm install -s 7.10.0  && \
    nvm use 7.10.0   && \
    npm install -g pm2  && \
    ln -s /root/.nvm/versions/node/v7.10.0/bin/* /usr/bin/
