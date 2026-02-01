# OpenShift CLI (`oc`) Cheat Sheet

Practical OpenShift CLI commands for day-to-day operator workflows.
Designed for speed, clarity, and safe execution in live environments.

> Tip: This cheat sheet is kept in a single code block to render cleanly across GitHub UI and docs viewers.

```bash
# ----------------------------------------
# Login & Context
# ----------------------------------------
oc login https://api.cluster:6443
oc whoami
oc status

# ----------------------------------------
# Project & Namespace Management
# ----------------------------------------
oc project
oc project my-project
oc get projects

# ----------------------------------------
# Core Resource Inspection
# ----------------------------------------
oc get pods
oc get all
oc get svc
oc get route
oc get deploy

# Deeper diagnostics for a specific pod:
oc describe pod <pod-name>

# ----------------------------------------
# Logs & Remote Access
# ----------------------------------------
oc logs <pod-name>
oc logs -f <pod-name>

# Shell into a running container:
oc exec -it <pod-name> -- /bin/sh
# Some images use /bin/bash instead of /bin/sh

# ----------------------------------------
# Apply & Manage YAML
# ----------------------------------------
oc apply -f file.yaml
oc delete -f file.yaml
oc get svc my-service -o yaml
oc explain route.spec

# ----------------------------------------
# Rollouts & Deployments
# ----------------------------------------
oc rollout status deploy/my-app
oc rollout history deploy/my-app
oc rollout undo deploy/my-app

# ----------------------------------------
# Troubleshooting & Operations
# ----------------------------------------
oc get events --sort-by=.lastTimestamp
oc adm top pods
oc adm top nodes
# oc adm top nodes requires elevated permissions
