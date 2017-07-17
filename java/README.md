JAVA VERSION

**JAVA-VERSION java~deb-stretch:1.0.0**

- DOCKER VERSION: paloit/deb-stretch-fr:1.0.0
- TAG NAME: paloit/java-fr:8
- JAVA_VERSION: 8
- COMMANDS:

        ./build paloit/deb-stretch-fr:1.0.0 paloit/java-fr:8 8
        ./push paloit/java-fr:8 true (docker hub repository)
        docker pull paloit/java-fr:8