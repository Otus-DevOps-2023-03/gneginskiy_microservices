FROM ubuntu:20.04 
RUN apt update \
    && apt install -y ruby-full ruby-dev build-essential \
    && gem install bundler
ENV APP_HOME /app

RUN mkdir $APP_HOME 

WORKDIR $APP_HOME
ADD Gemfile* $APP_HOME/ 

RUN bundle update --bundler
RUN bundle install

ADD . $APP_HOME
ENV POST_SERVICE_HOST post
ENV POST_SERVICE_PORT 5000
ENV COMMENT_SERVICE_HOST comment 
ENV COMMENT_SERVICE_PORT 9292 

CMD ["puma"]
