FROM ruby
RUN apt-get update && apt-get upgrade -y && \
    apt-get install nodejs -y \
    gem install rails bundler && mkdir -p /opt/app

ONBUILD COPY . /opt/app
ONBUILD WORKDIR /opt/app
ONBUILD RUN bundle install && rake db:migrate && rake db:seed
