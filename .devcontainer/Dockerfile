FROM python:3
USER root

COPY requirements.txt /tmp/requirements.txt

RUN apt update -y \
&& apt install -y python3-pip nodejs npm \
&& pip3 install -r /tmp/requirements.txt \
&& pip3 install online-judge-tools \
&& npm install -g atcoder-cli \
&& acc config default-test-dirname-format test \
&& acc config default-task-choice all \
&& echo 'alias ojpython="oj t -c \"python3 main.py\" -d test/"' >> ~/.bashrc \
&& echo 'alias addpython="acc new --template python main.py"' >> ~/.bashrc