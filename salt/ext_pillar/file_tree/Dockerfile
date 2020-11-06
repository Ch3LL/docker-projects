FROM gpg_pillar_salt

# gpg pillar data
RUN mkdir -p /srv/pillar/
ADD ./pillar /srv/pillar/

ADD ./master /etc/salt/master

# if you want to generate new pillar data run:
# echo -n "supersecret" | gpg --armor --batch --trust-model always --encrypt -r salt-user@salt-user.com
