FROM ruby:latest

RUN apt-get update && \
	apt-get -y install nodejs && \
	gem install rails

ONBUILD COPY app /opt/app
ONBUILD WORKDIR /opt/app
ONBUILD RUN bundle update && bundle install && rails db:migrate && rails db:seed

# git clone https://bitbucket.org/railstutorial/sample_app_4th_ed app
# docker build -t ft-rails:on-build .
# docker build -t app -f Dockerfile_runner .
# docker run -it --rm -p 3000:3000 app
# open http://192.168.99.101:3000/
