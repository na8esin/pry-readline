FROM ruby:3.4

ENV HISTFILE=/usr/src/.bash_history

# Install base packages
RUN apt-get update -qq && \
    apt-get install --no-install-recommends -y curl libjemalloc2 libvips vim && \
    rm -rf /var/lib/apt/lists /var/cache/apt/archives

RUN gem install pry -v "0.15.2"
