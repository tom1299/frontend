# Frontend

## Requirements
* Create the layout for a GitOps project that will later be reconciled with fluxcd.
* The only tool used should be kustomize.
* The layout should follow the best practices for flux outlined here: https://github.com/fluxcd/flux2-kustomize-helm-example. But without helm
* The layout should contain four folders:
    * base
    * prod
    * ref
    * test
* The base folder should contain the base kustomization.yaml file and the common base resources for all environments.
* the prod, ref and test folders should contain the environment specific kustomization.yaml files and the environment specific resources.
* Running kustomize build in each of the respective environments will generate the final manifests for deployment in that environment

