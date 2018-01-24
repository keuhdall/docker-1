FROM ruby
RUN apt-get update && apt-get upgrade -y && \
    gem install rails bundler && mkdir -p /opt/app

ADD . /opt/app
WORKDIR /opt/app
EXPOSE 3000
RUN bundle install && rake db:migrate && rake db:seed
