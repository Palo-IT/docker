#CHOOSE YOUR NODE VERSION:
(https://nodejs.org/en/download/releases/)

##NODE VERSION

###NODE-8.1.4

- DOCKER VERSION: paloit/deb-stretch-fr:1.0.0
- TAG NAME: paloit/node:8.1.4
- version: 8.1.4
- GPG_KEY: B9AE9905FFD7803F25714661B63B535A4C206CA9 (expire: 2019-12-17)

./build base paloit/deb-stretch-fr:1.0.0 paloit/node:8.1.4 8.1.4 B9AE9905FFD7803F25714661B63B535A4C206CA9
./push paloit/node:8.1.4 true (docker hub repository)
docker pull paloit/node:8.1.4

#CHOOSE YOUR NPM VERSION:
(https://github.com/npm/npm/releases)

##NPM VERSION

###NODE-NPM-4.6.1-1.0

- DOCKER VERSION: paloit/node:8.1.4
- TAG NAME: paloit/node-npm:4.6.1-1.0
- version Node:8.1.4
- version NPM: 4.6.1

./build npm paloit/node:8.1.4 paloit/node-npm:4.6.1-1.0 4.6.1
./push paloit/node-npm:4.6.1-1.0 true (docker hub repository)
docker pull paloit/node-npm:4.6.1-1.0

#CHOOSE YOUR YARN VERSION:
(https://github.com/yarnpkg/yarn/releases)

##YARN VERSION

###NODE-YARN-0.27.5-1.0

- DOCKER VERSION: paloit/node:8.1.4
- TAG NAME: paloit/node-yarn:0.27.5-1.0
- version Node:8.1.4
- version: 0.27.5

./build yarn paloit/node:8.1.4 paloit/node-yarn:0.27.5-1.0 0.27.5
./push node-yarn:0.27.5-1.0 true (docker hub repository)
docker pull paloit/node-yarn:0.27.5-1.0