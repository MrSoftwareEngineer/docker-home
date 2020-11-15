# Youtrack installation

## volume creation
```bash
docker volume create --name=plex_config && \
docker volume create --name=plex_transcode
```

Do not forget to open access on Your firewall, for example (firewalld)
```bash
firewall-cmd --zone=public --add-port=32400/tcp --permanent \
&& firewall-cmd --zone=public --add-port=32469/tcp --permanent \
&& firewall-cmd --zone=public --add-port=8324/tcp --permanent \
&& firewall-cmd --zone=public --add-port=3005/tcp --permanent \ 
&& firewall-cmd --zone=public --add-port=32412/udp --permanent \
&& firewall-cmd --zone=public --add-port=32413/udp --permanent \
&& firewall-cmd --zone=public --add-port=32414/udp --permanent \
&& firewall-cmd --zone=public --add-port=32410/udp --permanent \
&& firewall-cmd --zone=public --add-port=1900/udp --permanent
```