FROM ubuntu:20.04

ENV TZ=Australia/Melbourne

RUN apt-get -o Acquire::Check-Valid-Until=false -o Acquire::Check-Date=false update -y

RUN DEBIAN_FRONTEND=noninteractive \
    && apt-get update -y \
    && apt-get dist-upgrade -y \
    && apt-get install python3.8 -y \
    && apt-get install python3-pip -y \
    && apt-get install python3-venv -y \
    && python3 -m venv .venv \
    && source .venv/bin/activate \
    && python3 -m pip install --upgrade pip \
    && pip3 install -r requirements.txt --upgrade \

EXPOSE 7000