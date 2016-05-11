# anisble-rolling-demo
This project aims to demostrate the ability of ansible to...
1. Perform basic tasks such as registering servers, applying standard configuration and packages
2. Configuring clients to perform specific tasks; e.g. Web Servers
3. Perform sequencial actions such as rolling updates

It is intended that the code is deployed to a RHEL host running Ansible Tower.  Clients of the Tower host will be;
1 x RHEL 7 node (Intended target for HA Proxy)
2 x RHEL 7 nodes (Intended to be web servers accessible from beneath the HA proxy)

The code included here are Ansible playbooks to configure the target hosts;
- With a standard build
- With application configuration and packages specific to a particular role (web server or proxy)
- Remove any configuration for a particular server role, reseting to a vannilla server build
- Perform a rolling update of web server content by removing individual nodes from the proxy before applying updates and reinserting them

# In order to use these files
1. Create a RHEL 7 Ansible Tower host
2. Deploy the code to /var/lib/awx
3. TBC
