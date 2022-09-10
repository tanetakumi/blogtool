FROM node:14-buster-slim
ENV SHELL /bin/bash

LABEL maintainer="tanetakumi"

WORKDIR /code

# set -ex コマンドの実行に失敗したらその場で終了する
# josim installation
RUN set -ex\
    && pip install cmake\
    && git clone "https://github.com/JoeyDelp/JoSIM"\
    && cd JoSIM && mkdir build && cd build\
    && cmake ..\
    && cmake --build . --config Release\
    && make install