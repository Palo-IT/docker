DEBIAN VERSION

**DEBIAN-VERSION stretch-backports**

- DOCKER VERSION: debian:stretch-backports
- TAG NAME: paloit/deb-stretch-fr:1.0.0
- LANG: C.UTF-8
- TIMEZONE: Europe/Paris

./build debian:stretch-backports paloit/deb-stretch-fr:1.0.0 C.UTF-8 Europe/Paris
./push paloit/deb-stretch-fr:1.0.0 true (docker hub repository)
docker pull paloit/deb-stretch-fr:1.0.0
