FROM cloudsuite/mysql:mariadb-10.3

ENV root_password root
ENV DB_URL http://cloudsuite.ch/download/web_serving/ELGG_DB.tar.gz

RUN apt-get update && apt-get install -y --no-install-recommends wget mariadb-backup \
  && rm -rf /var/lib/apt/lists/*

ADD entrypoint.sh /etc/entrypoint.sh
RUN chown root:root /etc/entrypoint.sh
RUN chmod 700 /etc/entrypoint.sh

ENTRYPOINT ["/etc/entrypoint.sh"]
