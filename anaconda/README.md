ANACONDA VERSION

**ANACONDA-VERSION 3-4.4.0**

- DOCKER VERSION: paloit/deb-stretch-fr:1.0.0
- TAG NAME: paloit/anaconda-fr:3-4.4.0
- AA VERSION: 3-4.4.0-Linux-x86_64
- COMMANDS:

        ./build base paloit/deb-stretch-fr:1.0.0 paloit/anaconda-fr:3-4.4.0 3-4.4.0-Linux-x86_64
        ./push paloit/anaconda-fr:3-4.4.0 true (docker hub repository)
        docker pull paloit/anaconda-fr:3-4.4.0


**ANACONDA-DATA-VERSION 1.0.0**

- DOCKER VERSION: paloit/anaconda-fr:3-4.4.0
- TAG NAME: paloit/anaconda-data:1.0.0
- AA VERSION: 3-4.4.0
- PACKAGE:

        - ZEO
        - ZODB
        - gensim
        - elasticsearch
        - psycopg2

- COMMANDS:

        ./build data paloit/anaconda-fr:3-4.4.0 paloit/anaconda-data:1.0.0
        ./push paloit/anaconda-data:1.0.0 true (docker hub repository)
        docker pull paloit/anaconda-data:1.0.0