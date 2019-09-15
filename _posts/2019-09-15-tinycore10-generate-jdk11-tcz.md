# Generate JDK11 TCZ for Tiny Core Linux

Tiny Core does not provide an official JDK build for Tiny Core 10. The java-installer.tcz available for Tiny Core 10 does not work with OpenJDK 11 (This is the case for all the previous versions of Tiny Core also).  You can use the Docker scripts in the following Github repository to generate a jdk11.tcz from OpenJDK11 binaries.



1) Clone the hpmtissera/tinycore-jdk11-tcz repository from Github

   [https://github.com/hpmtissera/tinycore-jdk11-tcz.git](https://github.com/hpmtissera/tinycore-jdk11-tcz.git)

2) Download required OpenJDK11 tar.gz file from [https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases](https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases) and copy it inside tinycore-jdk11-tcz folder.

```
ex. OpenJDK11U-jdk_aarch64_linux_11.0.4_11.tar.gz
```

3) Run build.sh script

```bash
./build.sh
```

4) The script will generate a file named jdk11.tcz.