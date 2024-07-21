FROM ubuntu:22.04

ENV TZ="Asia/Ho_Chi_Minh"

COPY crontab /etc/cron.d/crontab

# Install cron
RUN apt update && apt install -y cron python3.10 python3-pip vim

# Set the correct permissions for the cron job file and apply it
RUN chmod 0644 /etc/cron.d/crontab \
    && crontab /etc/cron.d/crontab

# Run the command on container startup
ENTRYPOINT [ "cron", "-f" ]