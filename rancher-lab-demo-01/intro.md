## Installing Rancher on a Single Node Using Docker

#### Rancher can be installed by running a single Docker container. In this installation scenario, you’ll install Docker on a single Linux host, and then deploy Rancher on your host using a single Docker container.describing advantages of each option.


A Docker installation of Rancher is recommended only for development and testing purposes. 
The ability to migrate Rancher to a high-availability cluster depends on the Rancher version:

The Rancher backup operator can be used to migrate Rancher from the single Docker container 
install to an installation on a high-availability Kubernetes cluster. For details, 
refer to the documentation on [migrating Rancher to a new cluster](https://rancher.com/docs/rancher/v2.5/en/backups/migrating-rancher).


Privileged Access for Rancher v2.5+
When the Rancher server is deployed in the Docker container, a local Kubernetes cluster is installed within the container for Rancher to use. 
Because many features of Rancher run as deployments, and privileged mode is required to run containers within containers, 
you will need to install Rancher with the `--privileged` option.

## Requirements for OS, Docker, Hardware, and Networking
Make sure that your node fulfills the general [installation requirements](https://rancher.com/docs/rancher/v2.5/en/installation/requirements/).

### 1. Provision Linux Host
   - Provision a single Linux host according to our [Requirements](https://rancher.com/docs/rancher/v2.5/en/installation/requirements) to launch your Rancher server.

### 2. Choose an SSL Option and Install Rancher
   - For security purposes, SSL (Secure Sockets Layer) is required when using Rancher. SSL secures all Rancher network communication, like when you login or interact with a cluster.


`DO YOU WANT TO…`

1. Use a proxy? See [HTTP Proxy Configuration](https://rancher.com/docs/rancher/v2.5/en/installation/other-installation-methods/single-node-docker/proxy/);
2. Configure custom CA root certificate to access your services? See [Custom CA root certificate](https://rancher.com/docs/rancher/v2.5/en/installation/other-installation-methods/single-node-docker/advanced/#custom-ca-certificate/);
3. Complete an Air Gap Installation? See [Air Gap: Docker Install](https://rancher.com/docs/rancher/v2.5/en/installation/air-gap-single-node/);
4. Record all transactions with the Rancher API? See [API Auditing](https://rancher.com/docs/rancher/v2.5/en/installation/other-installation-methods/single-node-docker/advanced/#api-audit-log).
