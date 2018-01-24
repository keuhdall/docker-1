FROM ruby
RUN apt-get update && apt-get upgrade -y && \
    gem install rails bundler && mkdir -p /opt/app

ONBUILD ADD . /opt/app
ONBUILD WORKDIR /opt/app
ONBUILD EXPOSE 3000
ONBUILD RUN bundle install && rake db:migrate && rake db:seed
