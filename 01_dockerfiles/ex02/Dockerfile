FROM ruby
RUN apt-get update && apt-get upgrade -y && gem install rails -v 5.0.2 && rails new server && cd server && bundle && rake db:migrage && rake db:seed
WORKDIR /opt/app
