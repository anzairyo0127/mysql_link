# Ubuntu:18.04 imageのPull
FROM ubuntu:18.04
# deb を開くためのpackageをinstall
RUN apt update -y
RUN apt install -y wget lsb-release gnupg
# リダイレクト用テキストデータのコピー
COPY configs/cmd /tmp/cmd
# MySQLVer8.0.11固定のため、ローカルapt-configデータを使用
COPY configs/mysql-apt-config_0.8.10-1_all.deb /tmp/mysql-apt-config_0.8.10-1_all.deb
# MySQL用のapt-configを設定
RUN dpkg -i /tmp/mysql-apt-config_0.8.10-1_all.deb < /tmp/cmd
# 改めてリストを更新し、mysql-clientをinstall
RUN apt update -y
RUN apt install -y mysql-client