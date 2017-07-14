Project https://github.com/jwilder/docker-gen

This image serve to allocate automatically a dynamic ip/port from docker to a local domain.
Add your local domain in the file hosts of your machine (example: 127.0.0.1 palo-it.local), put environment information in your docker-compose file and that's all.

This tools write automatically in the server.conf file of nginx the necessary informations.
If you stop your container, the system automatically remove the informations in the server.conf file.

By defaut, this system recognize port 80 and 443

Example of environment options:

services:
  web:
    environment:
      - VIRTUAL_HOST=palo-it.local
      - VIRTUAL_PORT=9200 (if you want to use a specific port (rabbitmq...))
      - VIRTUAL_PROTO=https (if you want to use https)
      - HTTPS_METHOD=nohttp (if you want to use https)