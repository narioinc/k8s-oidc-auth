# Kubernetes Oauth2Proxy integration with keycloak
Sample YAMLs to create a OIDC based login path for existing kubernetes services

# Prereq
* Keycloak installed in its namespace and exposed via a ingress/loadbalancer
* Nginx ingress controller (latest version) installed
* A kubernetes service that needs to be exposed outside with OIDC authentication
* Helm installed on your local system and the oauth2-proxy/oauth2-proxy helm repo added  https://github.com/oauth2-proxy/manifests
* cert-manager installed for tls certs

# Purpose of each file 
* sample-nginx-ingress.yaml - this file is to create a nginx ingress resource for an existing service
* oauth2p-values.yaml - this file is the minimum set of values that needs to be overriden for the oauth2proxy to work with your keycloak OIDC provider
* oauth2p-nginx-ingress.yaml - the oauth2proxy ingress resource. 
