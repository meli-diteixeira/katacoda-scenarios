## Default Rancher-generated Self-signed Certificate

If you are installing Rancher in a development or testing environment where identity verification isn’t a concern, 
install Rancher using the self-signed certificate that it generates. 

This installation option omits the hassle of generating a certificate yourself.

Log into your Linux host, and then run the minimum installation command below.

As of Rancher v2.5, privileged access is [required](https://rancher.com/docs/rancher/v2.5/en/installation/other-installation-methods/single-node-docker/#privileged-access-for-rancher-v2-5).

## Run Rancher Continer

`docker run -it --restart=unless-stopped \
  -p 80:80 -p 443:443 \
  --privileged \
  rancher/rancher:latest
`{{execute}}.

## Check if Rancher are up and running on container

`docker ps`{{execute}}.

Note: Change variable example `${CONTAINER_ID}` to your Rancher `container_id` in the next command line!

`docker logs -f ${container_id}`{{execute}}.

## Generated Web Link

https://[[HOST_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com

Note: if the service is not yet accessible, validate the status of your container,
Rancher needs to be running for this link to work.
