#CHOOSE YOUR NODE VERSION:
(https://nodejs.org/en/download/releases/)

##NODE VERSION

###NODE-7.1.0

- DOCKER VERSION: paloit/deb-stretch-fr:1.0.0
- TAG NAME: paloit/node:7.1.0
- version: 7.1.0
- GPG_KEY: B9AE9905FFD7803F25714661B63B535A4C206CA9 (expire: 2019-12-17)

build example:
./build base paloit/deb-stretch-fr:1.0.0 paloit/node:7.1.0 7.1.0 B9AE9905FFD7803F25714661B63B535A4C206CA9


#CHOOSE YOUR NPM VERSION:
(https://github.com/npm/npm/releases)

##NPM VERSION

###NODE-NPM-4.5.0-1.0

- DOCKER VERSION: paloit/node:7.1.0
- TAG NAME: paloit/node-npm:4.5.0-1.0
- version Node:7.1.0
- version NPM: 4.5.0

build example:
./build npm paloit/node:7.1.0 paloit/node-npm:4.5.0-1.0 4.5.0


#CHOOSE YOUR YARN VERSION:
(https://github.com/yarnpkg/yarn/releases)

##YARN VERSION

###NODE-YARN-0.23.4-1.0

- DOCKER VERSION: paloit/node:7.1.0
- TAG NAME: node-yarn:0.23.4-1.0
- version Node:7.1.0
- version: 0.23.4

build example:
./build yarn paloit/node:7.1.0 paloit/node-yarn:0.23.4-1.0 0.23.4