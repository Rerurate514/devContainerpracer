FROM httpd:2.4

# 必要なパッケージのインストール
RUN apt-get update && apt-get install -y \
    libxml2-dev \
    libssl-dev \
    && rm -rf /var/lib/apt/lists/*

# Apache設定
# COPY ./docker/apache/httpd.conf /usr/local/apache2/conf/httpd.conf

# PHPなどが必要な場合は追加インストール
# 例: RUN apt-get update && apt-get install -y php libapache2-mod-php

# 作業ディレクトリ
WORKDIR /usr/local/apache2/htdocs

# ポート80を公開
EXPOSE 80

# Apacheをフォアグラウンドで実行
CMD ["httpd-foreground"]
