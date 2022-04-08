# --- Criando Ambiente PostGIS ---
FROM postgis/postgis

RUN echo '--- Installing main dependencies ---'
# All needed dependencies
RUN apt update
RUN apt install curl -y
RUN apt install systemctl -y
RUN apt install gdal-bin -y
RUN curl https://www.pgadmin.org/static/packages_pgadmin_org.pub | apt-key add
RUN sh -c 'echo "deb https://ftp.postgresql.org/pub/pgadmin/pgadmin4/apt/bullseye pgadmin4 main" > /etc/apt/sources.list.d/pgadmin4.list && apt update' -y
RUN apt install pgadmin4-web -y

ENV PGADMIN_SETUP_EMAIL testing@testing.com
ENV PGADMIN_SETUP_PASSWORD BeNotAfraid.Com

RUN /usr/pgadmin4/bin/setup-web.sh --yes

# Set the workdir
WORKDIR /home/

VOLUME ["/home/" ]

EXPOSE 5432
EXPOSE 80

