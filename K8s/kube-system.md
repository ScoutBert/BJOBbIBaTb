log-cat /var/log/remote/by-namespace/kube-system/*.log_22:12:31_16* | fgrep system:node:prod-k8s-cloud-n1.k8s.orglot.office | grep -o 'requestURI":"/api/v1/namespaces/prod-'.................  | fgrep pods
requestURI":"/api/v1/namespaces/prod-mercury/pods/prod
requestURI":"/api/v1/namespaces/prod-mercury/pods/prod
