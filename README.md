# Cerberus

## Description
Custom Kubernetes load balancer controller with added feature to elict Redis Master.  This is alternative to Redis Sentinel and improves High Availablity on Redis in K8 environments.

## Design

### Sentinel Approachsdf
Redis Sentinel provides high availability for Redis. In practical terms this means that using Sentinel you can create a Redis deployment that resists without human intervention to certain kind of failures. Fundamental things to know about Sentinel before deploying
-> You need at least three Sentinel instances for a robust deployment.fas
The three Sentinel instances should be placed into computers or virtual machines that are believed to fail in an independent way. So for example different physical servers or Virtual Machines executed on different availability zones.
-> Sentinel + Redis distributed system does not guarantee that acknowledged writes are retained during failures, since Redis uses asynchronous replication. However there are ways to deploy Sentinel that make the window to lose writes limited to certain moments, while there are other less secure ways to deploy it.
-> You need Sentinel support in your clients. Popular client libraries have Sentinel support, but not all.
There is no HA setup which is safe if you don't test from time to time in development environments, or even better if you can, in production environments, if they work. You may have a misconfiguration that will become apparent only when it's too late (at 3am when your master stops working).
-> Sentinel, Docker, or other forms of Network Address Translation or Port Mapping should be mixed with care: Docker performs port remapping, breaking Sentinel auto discovery of other Sentinel processes and the list of slaves for a master. Check the section about Sentinel and Docker later in this document for more information.

### Cerberus Approach

## Build

## Integration

## Deployment

## Troubleshoot

## Support

## Feedback


