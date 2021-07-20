FROM rabbitmq:alpine

# Based on laradock/laradock (Mahmoud Zalt <mahmoud@zalt.me>)
LABEL maintainer="Ivan Terentev <terentev.pro@gmail.com>"

RUN rabbitmq-plugins enable --offline rabbitmq_management

EXPOSE 4369 5671 5672 15671 15672 25672
