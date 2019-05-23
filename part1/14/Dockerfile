FROM ruby:2.6.0

WORKDIR /usr/app
COPY . .

RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt install -y nodejs

RUN bundle install
RUN rails db:migrate

EXPOSE 3000
CMD [ "rails", "s" ]
