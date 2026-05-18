---
title: Deploy a container service
weight: 3
---

# Deploy a container service

Once the project exists, the main path is usually a deployment service backed by an external image or a Northflank build output.

## Deployment inputs

The service creation screen breaks deployment into practical groups:

![Northflank deployment service form](/images/northflank-deploy-service.png)

- service identity
- image source
- compute plan
- port exposure
- environment variables
- advanced runtime behavior

## A useful mental model

Northflank asks you to describe the workload in the same order operators think about production:

{{% steps %}}

### Name the service

Use a durable name because it shows up in URLs, logs, and deployment history.

### Choose the image source

Select an external image when you already publish to Docker Hub or another registry.

### Set compute and storage

Match CPU, memory, ephemeral storage, and instance count to the workload’s baseline needs.

### Configure networking

Expose only the ports that must be reachable and keep the rest internal.

### Add runtime configuration

Inject variables, health checks, and command behavior only after the service definition is stable.

{{% /steps %}}

{{< details title="What to verify before pressing create" >}}

- Correct image tag
- Public vs private exposure
- Expected port and protocol
- Minimum viable CPU and memory
- Required runtime variables

{{< /details >}}
