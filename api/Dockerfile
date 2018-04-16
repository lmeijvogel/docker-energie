FROM ruby:2.3.6

RUN cd /root \
    && git clone https://github.com/lmeijvogel/meter-reader-api \
    && cd meter-reader-api \
    && git checkout ${REPO_VERSION} \
    && bundle install --without development

WORKDIR /root/meter-reader-api/webapp

CMD bundle exec thin start
