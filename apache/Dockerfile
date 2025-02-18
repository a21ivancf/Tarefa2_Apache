FROM debian:12

RUN apt update && apt install -y apache2 whois && apt clean && rm -rf /var/lib/apt/lists/*

RUN useradd -m -d "/home/ana" -p $(mkpasswd "abc123.") -s /bin/bash ana
RUN useradd -m -d "/home/eva" -p $(mkpasswd "abc123.") -s /bin/bash eva

RUN useradd -m -d "/home/lois" -p $(mkpasswd "abc123.") -s /bin/bash lois
RUN useradd -m -d "/home/xan" -p $(mkpasswd "abc123.") -s /bin/bash xan

RUN a2enmod ssl
RUN a2enmod auth_digest.load
RUN a2enmod authz_groupfile.load
EXPOSE 80

RUN mkdir -p /usr/local/apache/passwd/

# RUN authz_groupfile.load
# RUN htdigest -c /usr/local/apache/passwd/passwords directivos lois

CMD ["apache2ctl", "-D", "FOREGROUND"]

