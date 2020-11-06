FROM centos8_salt


RUN mkdir -p /etc/salt/gpgkeys
ADD ./keys /etc/salt/gpgkeys/
RUN chmod 0700 /etc/salt/gpgkeys
RUN gpg --homedir /etc/salt/gpgkeys --armor --export salt-user@salt-user.com > /root/exported_pubkey.gpg
RUN gpg --import /root/exported_pubkey.gpg



# gpg pillar data
RUN mkdir -p /srv/pillar/
ADD ./pillar /srv/pillar/

# if you want to generate new pillar data run:
# echo -n "supersecret" | gpg --armor --batch --trust-model always --encrypt -r salt-user@salt-user.com
