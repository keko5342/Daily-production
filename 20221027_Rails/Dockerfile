FROM ruby:latest
WORKDIR /work
EXPOSE 3000

# 必要なパッケージ、Node、Yarn
RUN curl -sL https://deb.nodesource.com/setup_16.x | bash -
RUN curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add -
RUN echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list
RUN apt update && apt install -y  \
	yarn \
	nodejs

# Rails
RUN gem install rails

# 起動コマンド
CMD /work/startup.sh