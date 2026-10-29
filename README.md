# Reddit on EKS | Production hardened GitOps Platform

A Reddit clone app, deployed to Amazon EKS with a DevSecOps CI pipeline, GitOps delivery via ArgoCD and Prometheus & Grafana monitoring, all provisioned and torn down with terraform

**Acknowledgements:** The base setup follows
[Reddit Clone](https://github.com/uniquesreedhar/Reddit-Project) by Harshhaa.
My additions are listed under `What I changed and Why.`

**Status:** In progress. Sections below are filled in as each change ships

## What I Changed and Why


| # | Change | Status |
|---|---|---|
| 1 | Argo CD v2.4.7 (EOL) to current 3.5.x via Helm | Planned |
| 2 | Static AWS keys to IAM roles, EKS Pod Identity, GitHub OIDC | Planned |
| 3 | Public LoadBalancers + default passwords to ALB Ingress with TLS, generated credentials | Planned |
| 4 | `kubectl expose` monitoring to kube-prometheus-stack, dashboards, alerts | Planned |
| 5 | Resource limits, probes, HPA; k6 load testing | Planned |
| 6 | Billing alerts and one-command teardown/rebuild | In progress |

## Architecture

Diagram coming soon

## Repository Layout

| Path | Purpose |
|---|---|
| `app/` | Application source and Dockerfile |
| `terraform/bootstrap/` | Persistent: state bucket, billing alerts |
| `terraform/platform/` | Ephemeral: VPC, EKS, Argo CD |
| `gitops/` | Everything Argo CD deploys |
| `docs/` | Metrics log and design decisions |

## Setup / Teradown

Setup & Teardown coming soon
