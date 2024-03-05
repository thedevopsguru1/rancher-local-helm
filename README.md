# rancher-local-helm
### DOwnload and unzip the helm chart here
Link: https://artifacthub.io/packages/helm/rancher-stable/rancher?modal=install
![image](https://github.com/thedevopsguru1/rancher-local-helm/assets/126810742/216d95b5-8795-4400-97b9-d52b01dc4882)

### open the chart.yaml and update the kubeVersion: 1.28.5 or comment out the kubeversion

```
apiVersion: v2
appVersion: v2.7.9
description: Install Rancher Server to manage Kubernetes clusters across providers.
home: https://rancher.com
icon: https://github.com/rancher/ui/blob/master/public/assets/images/logos/welcome-cow.svg
keywords:
- rancher
#kubeVersion: 1.28.5
maintainers:
- email: charts@rancher.com
  name: Rancher Labs
name: rancher
sources:
- https://github.com/rancher/rancher
- https://github.com/rancher/server-chart
version: 2.7.9
```
### Then run 
```
helm upgrade --install rancher .\rancher\ --namespace cattle-system --set hostname=rancher.anaeleboo.com --set bootstrapPassword=admin --set ingress.tls.source=letsEncrypt --set letsEncrypt.email=ananae@ex.org --set letsEncrypt.ingress.class=nginx --set ingress.ingressClassName=nginx --create-namespace
```
