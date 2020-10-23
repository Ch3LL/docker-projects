FROM centos:8

RUN yum install python3 git -y
RUN pip3 install salt

ENV PYTHONPATH=/salt-dev/:/salt-dev/salt-testing/
ENV PATH=$PATH:/salt-dev/scripts/:/salt-dev/tests/

VOLUME /salt-dev/
