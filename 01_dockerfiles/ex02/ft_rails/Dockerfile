FROM ruby

RUN apt-get update --yes && \
	apt-get install --yes build-essential \
	libpq-dev \
	nodejs \
	sqlite3

ONBUILD COPY app /opt/app
ONBUILD WORKDIR /opt/app

ONBUILD EXPOSE 3000
ONBUILD RUN bundle install
ONBUILD RUN rails db:migrate
ONBUILD RUN rails db:seed

# build ft-rails
# docker build --tag ft-rails:on-build ./ft_rails

# build it
# docker build --tag ex02 ./

# run it
# docker run --interactive --tty -p 3000:3000 ex02

