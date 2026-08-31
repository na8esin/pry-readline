FROM ruby:4.0

ENV HISTFILE=/usr/src/.bash_history

# Install base packages
RUN apt-get update -qq && \
    apt-get install --no-install-recommends -y curl libjemalloc2 libvips vim && \
    rm -rf /var/lib/apt/lists /var/cache/apt/archives

RUN gem install pry -v "0.16.0"
RUN gem install bundler
COPY Gemfile /usr/src/Gemfile
RUN cd /usr/src && bundle install
