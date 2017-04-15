FROM ubuntu:14.04

MAINTAINER Michael Davidson <michael.davidson@ovrkast.com>

ENV DEBIAN_FRONTEND noninteractive

# Install dependencies
RUN apt-get update &&\
    apt-get install -y curl lib32gcc1

# Download and extract SteamCMD
RUN mkdir -p /opt/steamcmd &&\
    cd /opt/steamcmd &&\
    curl -s http://media.steampowered.com/installer/steamcmd_linux.tar.gz | tar -vxz

WORKDIR /opt/steamcmd

# Update SteamCMD, Download 7 Days to Die Server, and run server.
CMD ./steamcmd.sh +login anonymous +force_install_dir ../7daystodie +app_update 294420 validate +quit; ../7daystodie/7DaysToDieServer.x86_64 -configfile=serverconfig.xml -logfile 7DaysToDie_Data/output_log.txt
