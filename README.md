# gitops-config-template

An opinionated gitops structure

- Mono repo
- Single branch i.e. main and then separate folders per environment
- ArgoCD for application deployment
- Helm for templatization

## Hierarchy

Tenant (Product) owns Applications which are promoted to different Environments (Static and Dynamic)

Tenant >> Applications >> Environments

This gitops structure supports:

- Multiple tenants/teams/products
- Multiple environments (both static and dynamic)
- Multiple clusters
- Multiple apps

## Mutliple tenants

We have 2 product based tenants; who have exactly same structure

1. gabbar
2. veeru

And then there is one special tenant which is SRE

## Mutliple environments

We have 5 environments for each **application**:

1. build
2. preview
3. dev
4. stage
5. prod

## Multiple clusters

We have 2 clusters:

1. Cluster # 1 holds 3 environments: build, preview and dev
2. Cluster # 2  holds 2 environments: stage and prod

## Multiple apps

We have 3 apps:

**Gabbar** has two apps: 

1. stakater-nordmart-review, 
2. stakater-nordmart-review-ui

**Veeru** has one app: 

1. stakater-nordmart-inventory

## CI/CD/CD Workflow

### Overview

![Overview](./docs/images/overview.png)

### Pull request workflow

![PR Workflow](./docs/images/pr-workflow.png)

### Main branch workflow

[CI/CD/CD](https://www.websequencediagrams.com/?lz=dGl0bGUgQ29udGludW91cyBJbnRlZ3JhdGlvbgoKcGFydGljaXBhbnQgRGV2ZWxvcGVyAAkNQ29kZSBSZXBvAB8NVGVrdG9uADINSW1hZ2UgUmVnaXN0cnkATQ1LOHMgRGV2AGENQXJ0aWZhY3RvAB0PR2l0T3BzAGASQXJnAHUOSzhzIFFBCgoAgS4JLT4AgSMJOiBnaXQgcHVzaAoAgTcJLT4AgS8GOiB3ZWJob29rCm5vdGUgcmlnaHQgb2YAgUwHOiBzZXR1cAoAgVsGAEATbGwAIRducG0gdGVzdAAEG3J1biBidWlsZFxuAAIFIGltYWdlAGMJAII0DjoAgTsFABwHAIEVFmRlcGxveVxuaGVsbSB0ZW1wbGF0ZS4uLgCBNQkAgnIHOiBvYyBhcHBseSAtZgoAgwcHAFwUAIFMEQA4CXJ1bgBuHWhlYWx0aABnEkdFVCAvABYHAIJaFnRhZy1yZWxlYXMAggAKAIM-C2FkZCB0YWcAgxYXaW0AMwoAgQEYbG0ATxEAhHILOiBwdWJsaXNoACUFIGNoYXIAgysYZ2l0b3BzAIQSCQCFHws6IHVwZGF0ZSBRQSBmb2xkZXIKQXJnbwAVDwCEOAkAFgYAhTsGOiBzeW5jCg&s=default#)

![CI/CD/CD](./docs/images/ci-cd-cd-v1.png)

### Helm values override

![Helm values override](./docs/images/helm-values-override.png)

### Outputs

The pipelines produce following outputs

![Pipeline outputs](./docs/images/outputs.png)

### Release workflow

![Release workflow](./docs/images/release-workflow.png)