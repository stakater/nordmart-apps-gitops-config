# gitops-config-template

An opinionated gitops structure!

This gitops structure supports:

- Multi tenant
- Multi environment
- Multi cluster
- Multi apps

In this demo setup

## Mutli tenant
We have 2 tenants:
- gabbar
- veeru

## Mutli environment
We have 5 environments:
- build
- preview
- dev
- stage
- prod

## Multi cluster
We have 2 clusters:
- One cluster holds: build, preview and dev
- Second cluster holds: stage and prod

## Multi apps
We have 3 apps:
- gabbar has two apps: stakater-nordmart-review, stakater-nordmart-review-ui
- veeru has one app: stakater-nordmart-inventory
