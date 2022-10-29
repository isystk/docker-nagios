FROM jasonrivers/nagios:latest

## MySQL Clientをインストール
RUN apt update && apt install -y \
    mysql-client \
    cpanminus \
 && apt clean \
 && rm -rf /var/lib/apt/lists/*

 ## 設定ファイル整合性チェック
 RUN /usr/local/bin/nagios -v /opt/nagios/etc/nagios.cfg