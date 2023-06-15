FROM debian:latest

# Create the root anchoir file Install Unbound and its dependencies
RUN apt-get update && apt-get upgrade -y && apt-get install -y \
        apt-utils\
        unbound


EXPOSE 53
ADD root.key /var/lib/unbound/root.key

# Start Unbound when the container launches
CMD ["/usr/sbin/unbound", "-d"]
