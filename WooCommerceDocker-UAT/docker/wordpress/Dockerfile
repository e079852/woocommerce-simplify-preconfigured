FROM wordpress:latest

RUN mkdir -p /etc/apache2/ssl
COPY server.crt /etc/apache2/ssl/server.crt
COPY server.key /etc/apache2/ssl/server.key
COPY alphalaundryservices.store.uat.simplify.com.conf /etc/apache2/sites-enabled/alphalaundryservices.store.uat.simplify.com.conf
RUN a2enmod rewrite
RUN a2enmod ssl
RUN service apache2 restart

