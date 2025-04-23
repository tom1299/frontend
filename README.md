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

## Add configs
* Add a config folder in base containing a httpd virtual host config file named "base-httpd.conf"
* In the kustomization file a configMap should be created from the config file named "base-httpd.conf"
* In the test folder add a config folder containing a httpd config file. That file should be merged with the base-httpd.conf file
