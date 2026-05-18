---
title: Operate and observe
weight: 4
---

# Operate and observe

Deployment is only the midpoint. The service overview shows the tools you use after launch to prove the workload is healthy.

## Runtime surfaces worth learning

{{< cards cols="2" >}}
  {{< card title="Deployments" icon="refresh" subtitle="See rollout history, current image, and event timing." >}}
  {{< card title="Logs" icon="terminal" subtitle="Open runtime logs to diagnose boot issues and application errors." >}}
  {{< card title="Metrics" icon="chart-square-bar" subtitle="Monitor CPU, memory, and behavior trends across revisions." >}}
  {{< card title="Command override" icon="pencil" subtitle="Adjust startup behavior without rebuilding the image immediately." >}}
{{< /cards >}}

![Northflank service runtime overview](/images/northflank-runtime.png)

## Post-deploy checklist

{{% steps %}}

### Confirm the image and revision

Make sure the running deployment matches the tag or release you intended.

### Review startup logs

Catch bad environment variables, wrong ports, migration failures, or dependency issues early.

### Validate networking

Open the generated service URL and ensure the expected port is reachable.

### Watch stability

Check restarts, deployment events, and resource saturation before calling the rollout done.

{{% /steps %}}
