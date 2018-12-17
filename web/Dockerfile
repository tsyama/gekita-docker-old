FROM ruby:2.5.3

# yarnをaptでインストールできるようにしておく
RUN curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add -
RUN echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list

RUN apt-get -y update
RUN curl -sL https://deb.nodesource.com/setup_8.x | bash -
RUN apt-get install -y \
    sqlite3 \
    nodejs \
    yarn

RUN gem install rails