FROM debian:12

RUN apt update && apt install -y apache2 whois && apt clean && rm -rf /var/lib/apt/lists/*

RUN useradd -m -d "/home/ana" -p $(mkpasswd "abc123.") -s /bin/bash ana
RUN useradd -m -d "/home/eva" -p $(mkpasswd "abc123.") -s /bin/bash eva

RUN a2enmod ssl
# RUN a2enmod mod_auth_basic
EXPOSE 80

CMD ["apache2ctl", "-D", "FOREGROUND"]

