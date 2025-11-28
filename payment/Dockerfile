FROM python:3.9.25-alpine3.21
EXPOSE 8080
WORKDIR /opt/server/
COPY *.ini .
COPY *.py .
COPY *.txt .
RUN pip3 install -r requirements.txt
ENV CART_HOST="cart" \
    CART_PORT="8080" \
    USER_HOST="user" \
    USER_PORT="8080" \
    AMQP_HOST="rabbitmq" \
    AMQP_USER="roboshop" \
    AMQP_PASS="roboshop123"

CMD ["uwsgi","--ini","payment.ini"]