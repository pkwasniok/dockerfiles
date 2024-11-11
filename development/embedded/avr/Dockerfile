FROM ubuntu:24.10

RUN apt-get update && apt-get upgrade

# Install universal development tools
RUN apt-get install -y build-essential git

# Install avr-specific development tools
RUN apt-get install -y avrdude minicom gcc-avr binutils-avr gdb-avr avr-libc

WORKDIR /project

