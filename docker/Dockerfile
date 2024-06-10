FROM nvcr.io/nvidia/isaac-sim:4.0.0

ENV DEBIAN_FRONTEND=noninteractive

RUN sed -i 's@archive.ubuntu.com@ftp.jaist.ac.jp/pub/Linux@g' /etc/apt/sources.list

RUN apt-get update && apt-get install -y \
    git \
    locales \
    xterm \
    dbus-x11 \
    terminator \
    sudo \
    unzip \
    lsb-release \
    curl \
    net-tools \
    software-properties-common \
    subversion \
    libssl-dev \
    htop \
    gedit \
    gdb \
    valgrind \
    build-essential \
    bash-completion \
    python3-pip \
    vim \
    cmake \
    wget && \
    apt-get clean && rm -rf /var/lib/apt/list*

RUN echo 'cd /root/IsaacLab && ln -s ${ISAACSIM_PATH} _Isaaclab' >> ${HOME}/.bashrc

RUN echo 'alias lab=/root/IsaacLab/isaaclab.sh' >> ${HOME}/.bashrc

ENV ISAACSIM_PATH="${HOME}/isaac-sim"
ENV ISAACSIM_PYTHON_EXE="${ISAACSIM_PATH}/python.sh"

SHELL ["/bin/bash", "-c"]

ENTRYPOINT ["/bin/bash"]
