# gitops-config-template
gitops-config-template

1) Why call it configs?
it has argocd, spaces, operators, tekton, forecastle, etc.

maybe categorize operators;
global operators in one place
namespace scoped operators in another place

2) Why not have PR environment on the root level? Doesn't make sense to have it inside another environment; currently we put it wih dev or ci environment; it just complicates the setup

3) Do we really need to have build as a separate environment? I mean it can be part of dev environment? - One reason could be resources (cpu and memory)
build could be part of preview environment or dev environment

4) Tekton CRs should be in team specific folder of team DelEng? Why put it in common configs folder?

5) Why have helm-values folder? Why not application specific folder? 
> yes we can

6) Can we move tenant specific argo project to common folder?
> yes we can

7) Maybe we should move spaces definition to common tenants folder?
> 