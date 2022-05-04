FROM ubuntu:20.04

RUN apt update
RUN apt -y install ruby && \
    apt -y install ruby-bundler

RUN mkdir -p /app/

COPY app/  /app/

WORKDIR /app/
RUN bundle install 
CMD bundle exec rackup --host 0.0.0.0
EXPOSE 9292
