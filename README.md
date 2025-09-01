# flux-poc-repo
flux repo
# Flux POC Repo

This repo contains a sample Nginx app managed by FluxCD.

Structure:
- clusters/kind-cluster/apps/nginx → Nginx deployment + service
- clusters/kind-cluster/kustomization.yaml → Includes apps

Steps:
1. Bootstrap Flux with this repo:
   ```bash
   flux bootstrap github \
     --owner=<your-github-username> \
     --repository=flux-poc-repo \
     --branch=main \
     --path=clusters/kind-cluster \
     --personal
