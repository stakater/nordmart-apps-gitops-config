# gitops-config-template

An opinionated gitops structure!

This gitops structure supports:

- Multi tenant
- Multi environment
- Multi cluster
- Multi apps

In this demo setup

We have 2 tenants:
- gabbar
- veeru

We have 5 environments:
- build
- preview
- dev
- stage
- prod

We have 2 clusters:
- One cluster holds: build, preview and dev
- Second cluster holds: stage and prod

We have 3 apps:
- gabbar has two apps: stakater-nordmart-review, stakater-nordmart-review-ui
- veeru has one app: stakater-nordmart-inventory
