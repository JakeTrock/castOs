FROM forumi0721/alpine-desktop:x64
LABEL com.iximiuz-project="docker-to-linux"
RUN apk update
RUN apk add openrc linux-virt uxplay
RUN echo "root:root" | chpasswd
RUN rc-update add root
# add uxplay to /etc/profile
RUN echo "export DISPLAY=:0" >> /etc/profile
RUN echo "export PATH=/usr/local/bin:$PATH" >> /etc/profile
RUN echo "export LD_LIBRARY_PATH=/usr/local/lib:$LD_LIBRARY_PATH" >> /etc/profile
RUN echo "export XDG_RUNTIME_DIR=/run/user/0" >> /etc/profile
RUN echo "export XDG_CONFIG_HOME=/config" >> /etc/profile
RUN echo "export XDG_DATA_HOME=/data" >> /etc/profile
RUN echo "export XDG_CACHE_HOME=/cache" >> /etc/profile
# make uxplay start on boot
RUN echo "uxplay" >> /etc/rc.local

