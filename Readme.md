# Deploying application and exposing it through istio-ingress with HTTPS certificate
> Disclaimer: Testing my domain kanadon-test.ddns.net should not work (because I turned it off)

Tools used:

- Minikube
- Helm
- Istio and Istio-ingress
- Cert-manager
- No-ip for free domain and ports redirect in my local router (80 HTTP/test and 443 for HTTPS/production)
- Port-forwarding for HTTP and HTTPS
  ```bash
  # HTTP
  kubectl port-forward -n istio-ingress --address YOUR-PRIVATE-IP or 0.0.0.0 svc/istio-ingressgateway 80
  # HTTPS
  kubectl port-forward -n istio-ingress --address YOUR-PRIVATE-IP or 0.0.0.0 svc/istio-ingressgateway 443
  ```

Credits to **That DevOps Guy** for the amazing [video](https://www.youtube.com/watch?app=desktop&v=hoLUigg4V18)