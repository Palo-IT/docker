ANACONDA VERSION

**ANACONDA-VERSION 2-4.4.0**

- DOCKER VERSION: paloit/deb-stretch-fr:1.0.0
- TAG NAME: paloit/anaconda-fr:2-4.4.0
- AA VERSION: 2-4.4.0-Linux-x86_64
- COMMANDS:

        ./build base paloit/deb-stretch-fr:1.0.0 paloit/anaconda-fr:2-4.4.0 2-4.4.0-Linux-x86_64
        ./push paloit/anaconda-fr:2-4.4.0 true (docker hub repository)
        docker pull paloit/anaconda-fr:2-4.4.0

**ANACONDA-VERSION 3-4.4.0**

- DOCKER VERSION: paloit/deb-stretch-fr:1.0.0
- TAG NAME: paloit/anaconda-fr:3-4.4.0
- AA VERSION: 3-4.4.0-Linux-x86_64
- COMMANDS:

        ./build base paloit/deb-stretch-fr:1.0.0 paloit/anaconda-fr:3-4.4.0 3-4.4.0-Linux-x86_64
        ./push paloit/anaconda-fr:3-4.4.0 true (docker hub repository)
        docker pull paloit/anaconda-fr:3-4.4.0


**ANACONDA-DATA-VERSION 2-1.0.0**

- DOCKER VERSION: paloit/anaconda-fr:2-4.4.0
- TAG NAME: paloit/anaconda-data:2-1.0.0
- AA VERSION: 2-4.4.0
- PACKAGE:

        - ZEO
        - ZODB
        - gensim
        - elasticsearch
        - pika
        - psycopg2
        - theano
        - keras

- COMMANDS:

        ./build data paloit/anaconda-fr:2-4.4.0 paloit/anaconda-data:2-1.0.0
        ./push paloit/anaconda-data:2-1.0.0 true (docker hub repository)
        docker pull paloit/anaconda-data:2-1.0.0
        
**ANACONDA-NVIDIA-VERSION 2-4.4.0**

- DOCKER VERSION: paloit/ubuntu-1604-fr-nvidia:1.0.0
- TAG NAME: paloit/anaconda-nvidia-fr:2-4.4.0
- AA VERSION: 2-4.4.0-Linux-x86_64
- COMMANDS:

        ./build base paloit/ubuntu-1604-fr-nvidia:1.0.0 paloit/anaconda-nvidia-fr:2-4.4.0 2-4.4.0-Linux-x86_64
        ./push paloit/anaconda-nvidia-fr:2-4.4.0 true (docker hub repository)
        docker pull paloit/anaconda-nvidia-fr:2-4.4.0        
        
**ANACONDA-NVIDIA-LEARNING-VERSION 2-1.0.0**

- DOCKER VERSION: paloit/anaconda-nvidia-fr:2-4.4.0
- TAG NAME: paloit/anaconda-nvidia-learning:2-1.0.0
- AA VERSION: 2-4.4.0
- PACKAGE:

        - ZEO
        - ZODB
        - gensim
        - elasticsearch
        - psycopg2
        - theano
        - keras

- COMMANDS:

        ./build learning paloit/anaconda-nvidia-fr:2-4.4.0 paloit/anaconda-nvidia-learning:2-1.0.0
        ./push paloit/anaconda-nvidia-learning:2-1.0.0 true (docker hub repository)
        docker pull paloit/anaconda-nvidia-learning:2-1.0.0