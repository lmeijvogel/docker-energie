FROM ruby:2.3.6

RUN cd /root \
    && git clone https://github.com/lmeijvogel/meter-reader-api \
    && cd meter-reader-api \
    && git checkout ${REPO_VERSION}

WORKDIR /root/meter-reader-api

RUN bundle install --without development

CMD ruby ./runner.rb
