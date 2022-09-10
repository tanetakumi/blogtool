FROM node:16-slim
ENV SHELL /bin/bash

LABEL maintainer="tanetakumi"

WORKDIR /root

# set -ex コマンドの実行に失敗したらその場で終了する
RUN set -ex\
    && apt update\
    && apt -y install git\
    && git config user.name ${GIT_USERNAME}\
    && git config user.name ${GIT_EMAIL}

# set -ex コマンドの実行に失敗したらその場で終了する
RUN set -ex\
    && git clone "https://github.com/tanetakumi/taneblog"\
    && cd taneblog\
    && npm install