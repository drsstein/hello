# Openshift

The IDA GPU cluster uses Openshift for container orchestration.

A common use case of the cluster is to run a jupyter notebook server, which requires a Deployment Config, a Service, and a Route configuration. The configuration files are unique to each user as they link to user projects and user storage. 

This repo contains my configuration files.

## idagpu

`<username>` is your cluster username (unique to this cluster, not DCS or UoG or any other service

### Resources

Tutorial https://git.dcs.gla.ac.uk/idagpu-public/idagpu-tutorial/-/tree/master/tutorial-examples

### Access

- Open browser window and login here: https://idagpu-head.dcs.gla.ac.uk:8443
- Select `<username>sproject`


