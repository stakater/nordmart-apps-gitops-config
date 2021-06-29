# gitops-config-template

org > tenants > apps > envs

1) where to apps of apps?

2) do we need to any differentiation between?
- global operator installation
- namespace scoped operator installation 
- CR creation or 
- application deployment

3) where to put helm chart and helm values?
inside the application folder; and not anywhere common

4) where should we store the creation of spaces?

5) argocd setup?
- per cluster
- per organization? (controls multiple clusters)

6) where to put build folders?

---

1) Why call it configs?
it has argocd, spaces, operators, tekton, forecastle, etc.

maybe categorize operators;
global operators in one place
namespace scoped operators in another place

2) Why not have PR environment on the root level? Doesn't make sense to have it inside another environment; currently we put it wih dev or ci environment; it just complicates the setup

3) Do we really need to have build as a separate environment? I mean it can be part of dev environment? - One reason could be resources (cpu and memory) build could be part of preview environment or dev environment

4) Tekton CRs should be in team specific folder of team DelEng? Why put it in common configs folder?

8) I think we can remove common folder as this should belong to a specific team; who owns; that; e.g. DelEng team