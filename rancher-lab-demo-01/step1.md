## Default Rancher-generated Self-signed Certificate

If you are installing Rancher in a development or testing environment where identity verification isn’t a concern, 
install Rancher using the self-signed certificate that it generates. 

This installation option omits the hassle of generating a certificate yourself.

Log into your Linux host, and then run the minimum installation command below.

As of Rancher v2.5, privileged access is [required](https://rancher.com/docs/rancher/v2.5/en/installation/other-installation-methods/single-node-docker/#privileged-access-for-rancher-v2-5).

```shell
docker run -d --restart=unless-stopped \
  -p 80:80 -p 443:443 \
  --privileged \
  rancher/rancher:latest
```