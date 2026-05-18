---
title: Platform overview
weight: 1
---

# Platform overview

Northflank is organized around a few core objects. Once these click, the rest of the product feels much easier to navigate.

## Core building blocks

{{< cards cols="2" >}}
  {{< card title="Team" icon="users" subtitle="The shared workspace for members, billing, integrations, and project ownership." >}}
  {{< card title="Project" icon="cube-transparent" subtitle="A boundary that groups workloads, networking, secrets, and environments." >}}
  {{< card title="Service" icon="server" subtitle="A long-running containerized workload exposed privately or publicly." >}}
  {{< card title="Job" icon="clock" subtitle="A one-off or scheduled container task for scripts, workers, and automation." >}}
{{< /cards >}}

## What the dashboard suggests

The dashboard screenshot shows the product opinion clearly: Northflank wants you to begin with a project, then add the exact runtime components needed for that project.

![Northflank dashboard overview](/images/northflank-dashboard.png)

{{< details title="Common resource types inside a project" >}}

- Build services for CI/container builds
- Deployment services for running images
- Jobs for scheduled or manual work
- Volumes for persistent storage
- Add-ons for stateful dependencies
- Secret groups and environments for configuration

{{< /details >}}

## Reading the platform model

{{% steps %}}

### Think team first

Teams own access, members, integrations, and billing surfaces.

### Think project next

Projects become the main container for application-level resources.

### Think runtime last

Services, jobs, ports, variables, and health checks are configured inside the project where the workload lives.

{{% /steps %}}

![Northflank resource creation menu](/images/northflank-resource-menu.png)
