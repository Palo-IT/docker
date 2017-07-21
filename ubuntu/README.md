UBUNTU VERSION

**UBUNTU-VERSION 16-04**

- DOCKER VERSION: ubuntu:16.04
- TAG NAME: paloit/ubuntu-1604-fr:1.0.0
- LANG: C.UTF-8
- TIMEZONE: Europe/Paris
- COMMANDS:

        ./build base ubuntu:16.04 paloit/ubuntu-1604-fr:1.0.0 C.UTF-8 Europe/Paris
        ./push paloit/ubuntu-1604-fr:1.0.0 true (docker hub repository)
        docker pull paloit/ubuntu-1604-fr:1.0.0
        
**UBUNTU-NVIDIA-VERSION 16-04**

- DOCKER VERSION: paloit/ubuntu-1604-fr:1.0.0
- TAG NAME: paloit/ubuntu-1604-fr-nvidia:1.0.0
- OS VERSION: 1604
- CUDA BASE: 8
- CUDA VERSION: 8.0.61
- CUDA CUBLAS: 2-1
- COMMANDS:

        ./build nvidia paloit/ubuntu-1604-fr:1.0.0 paloit/ubuntu-1604-fr-nvidia:1.0.0 1604 8 8.0.61 2-1
        ./push paloit/ubuntu-1604-fr-nvidia:1.0.0 true (docker hub repository)
        docker pull paloit/ubuntu-1604-fr-nvidia:1.0.0