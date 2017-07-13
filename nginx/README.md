NGINX VERSION
(https://nginx.org/en/download.html | https://www.nginx.com/blog/updating-gpg-key-nginx-products)

**NGINX-VERSION 1.13.2-1~stretch **

- DOCKER VERSION: paloit/deb-stretch-fr:1.0.0
- TAG NAME: paloit/nginx-fr:1.13.2
- NGINX_VERSION: 1.13.2-1~stretch 
- NGINX_KEY: 573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62
- NJS_VERSION: 1.13.2.0.1.11-1~stretch

./build base paloit/deb-stretch-fr:1.0.0 paloit/nginx-fr:1.13.2 1.13.2-1~stretch 573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 1.13.2.0.1.11-1~stretch

**NGINX-VERSION 1.13.2-1~stretch/java8**

- DOCKER VERSION: paloit/java-8-fr:1.0.0
- TAG NAME: paloit/nginx-fr-java:1.13.2
- NGINX_VERSION: 1.13.2-1~stretch 
- NGINX_KEY: 573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62
- NJS_VERSION: 1.13.2.0.1.11-1~stretch

./build base paloit/java-8-fr:1.0.0 paloit/nginx-fr-java:1.13.2 1.13.2-1~stretch 573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 1.13.2.0.1.11-1~stretch

**NGINX-VERSION 1.13.2-1/naxsi**

- DOCKER VERSION: paloit/deb-stretch-fr:1.0.0
- TAG NAME: paloit/nginx-fr-naxsi:1.13.2
- NGINX_VERSION: 1.13.2
- NAXSI_VERSION: 0.55.3

./build naxsi paloit/deb-stretch-fr:1.0.0 paloit/nginx-fr-naxsi:1.13.2 1.13.2 0.55.3


CHECK IF NGINX RUNNING
ps waux | grep nginx