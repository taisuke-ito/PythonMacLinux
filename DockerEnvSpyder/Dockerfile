FROM tensorflow/tensorflow:2.2.2
#tensorflow/tensorflow:latest
ENV DEBCONF_NOWARNINGS yes

RUN apt-get update \
    && apt-get upgrade -y \
    # imageのサイズを小さくするためにキャッシュ削除
    && apt-get install spyder \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/* \
   # pipのアップデート
    && pip3 install --upgrade pip

# 作業するディレクトリを変更
WORKDIR ~/PythonMacLinux/DockerEnvSpyder

COPY requirements.txt ${PWD}

# pythonのパッケージをインストール
RUN pip3 install spyder
#RUN pip install -r requirements.txt

# 作業するディレクトリを変更
# コンテナの内部には入った際のディレクトリの位置を変更している
WORKDIR ~/PythonMacLinux/DockerEnvSpyder

