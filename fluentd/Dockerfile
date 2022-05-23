FROM fluent/fluentd:stable
RUN apk add --update --virtual .build-deps \
    sudo build-base ruby-dev \
    && sudo gem install \
    fluent-plugin-elasticsearch \
    && sudo gem sources --clear-all \
    && apk del .build-deps \
    && rm -rf /var/cache/apk/* \
    /home/fluent/.gem/ruby/2.3.0/cache/*.gem



#FROM fluent/fluentd:v0.12-debian
#RUN ["apt-add-repository", "ppa:brightbox/ruby-ng"]
#RUN ["apt", "update"]
#RUN ["apt","install","ruby-full", "-y"]
#RUN ["ruby", "--version"]
#RUN ["bundle", "install"]
#RUN ["gem", "install", "fluent-plugin-elasticsearch", "--no-rdoc", "--no-ri", "--version", "1.9.2"]
