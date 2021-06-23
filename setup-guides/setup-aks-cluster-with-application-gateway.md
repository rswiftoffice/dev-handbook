
1. Setup Vnet Network
2. Setup AKS Cluster with Azure CNI
3. Setup Ingress Resource
4. Setup TLS 

https://gaunacode.com/deploying-an-ingress-controller-to-an-internal-virtual-network-and-fronted-by-an-azure-application-gateway
https://docs.microsoft.com/en-us/azure/aks/configure-azure-cni
https://medium.com/avmconsulting-blog/how-to-secure-applications-on-kubernetes-ssl-tls-certificates-8f7f5751d788
https://denniszielke.medium.com/securing-ingress-with-azureappgateway-and-egress-traffic-with-azurefirewall-for-azure-kubernetes-41af94051347


CloudFlare
https://nanjoran.com/2020/04/22/Kubernetes-Ingress-controller-with-Cloudflare/#Install-the-certificates-in-our-K8s-cluster



apiVersion: networking.k8s.io/v1
kind: Ingress
metadata:
  name: loft-ingress
  namespace: loft
  annotations:
    kubernetes.io/ingress.class: nginx
    nginx.ingress.kubernetes.io/ssl-redirect: "true"
    nginx.ingress.kubernetes.io/use-regex: "true"
    nginx.ingress.kubernetes.io/rewrite-target: /$1
spec:
  tls:
  - hosts:
    - loft.northpole.swiftoffice.org
    secretName: tls-secret
  rules:
  - host: loft.northpole.swiftoffice.org
    http:
      paths:
      - path: /(.*)
        pathType: Prefix
        backend:
          service:
            name: loft
            port:
              number: 80
