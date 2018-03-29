FROM ruby:latest

RUN apt-get update && apt-get install nodejs -y && apt-get autoclean -y && apt-get clean -y && gem install rails

ONBUILD COPY app /opt/app

ONBUILD WORKDIR /opt/app

ONBUILD RUN bundle install

#												--- FOR TEST ---
# docker build -t ft-rails .
# go to dir test_rb
# docker build -t (your_own_name_of_creating_images) .
# docker run --rm -p 3000:3000 (name_of_creating_images)
