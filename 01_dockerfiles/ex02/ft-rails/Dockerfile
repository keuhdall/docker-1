FROM ruby:2.4.1

RUN apt-get update -y && apt-get upgrade -y && \
	apt-get install nodejs -y && gem install rails bundler && mkdir -p /opt/app

COPY app /opt/app
WORKDIR /opt/app
EXPOSE 3000
RUN bundle install && rake db:migrate && rake db:seed
