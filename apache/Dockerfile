FROM  tutum/apache-php

ENV TERM=xterm

#installation Dependance pour composer
RUN apt-get update
RUN apt-get install unzip -y

# Installation de composer
RUN php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');" && \
    php composer-setup.php && \
    php -r "unlink('composer-setup.php');" && \
    mv composer.phar /usr/bin/composer

# Installation des packets pour le developpement
RUN apt-get update && \
    apt-get install nano -y