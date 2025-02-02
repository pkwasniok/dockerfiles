FROM ubuntu:24.10

# Update
RUN apt-get update -y && apt-get upgrade -y

# Install dependencies
RUN apt-get install -y git wget flex bison gperf python3 python3-pip \
                       python3-venv cmake ninja-build ccache libffi-dev \
                       libssl-dev dfu-util libusb-1.0-0

# Create esp-idf directory
WORKDIR /toolchain/esp-idf

# Download esp-idf
RUN git clone -b v5.4 --recursive https://github.com/espressif/esp-idf.git .

# Install esp-idf for all MCUs
RUN ./install.sh all

# Set-up esp-idf environment
RUN . ./export.sh

