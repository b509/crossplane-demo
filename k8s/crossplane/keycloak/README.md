# Examples in this directory
All examples in this directory are functional, but commented out so crossplane is not flooded when you run `kubectl apply -f k8s/crossplane/keycloak. Comment them out at your own convenience

# Adapting Keycloak's default config (e.g. auth flow, execution, role)

## Possible Solution via Crossplane Functions 
CompositeResourceDefinition similar to this one
https://gitlab.com/corewire/images/crossplane/function-keycloak-builtin-objects

-> see [10-xrd.yaml](./10-xrd.yaml)

## Possible Solution via Terraform Provider
Adding "import" option similar as done for the oidc-client to all resources where one wants to adapt the default configs, see e.g. [existing PR into terraform provider repository](https://github.com/mrparkers/terraform-provider-keycloak/pull/1001)

## Possible Solution for the future via Crossplane to query and filter existing resources
https://github.com/crossplane/crossplane/blob/master/design/design-doc-observe-only-resources.md#querying-and-filtering
https://github.com/crossplane/crossplane/issues/4141
https://github.com/crossplane/crossplane/issues/5538

### Other useful links for crossplane

https://github.com/crossplane-contrib/function-extra-resources
https://github.com/orgs/crossplane-contrib/repositories?language=&q=function&sort=&type=all
https://docs.crossplane.io/v1.16/concepts/composition-functions/
https://docs.crossplane.io/v1.16/concepts/patch-and-transform/
https://github.com/crossplane-contrib/function-go-templating
https://github.com/crossplane-contrib/function-auto-ready

