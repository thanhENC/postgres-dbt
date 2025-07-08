FROM ubuntu:22.04

# Install dependencies
RUN apt update && apt install -y unzip ruby postgresql-client wget

WORKDIR /app

COPY ./adw14data.sh ./adw14data.sh
RUN chmod +x adw14data.sh

# Entrypoint
ENTRYPOINT ["tail", "-f", "/dev/null"]