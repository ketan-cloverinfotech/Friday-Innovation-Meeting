## 1. How to add New Targets to existing prometheus
You just have to edit scrapeconfig file and apply
```
nano scrape-config.yaml
```
Check scrape configs presents
```
kubectl get scrapeconfig
```
## 2. How to add new Probe ( website or api endpoint" http,https,gRPC etc )
You have to just add new new probe 
```
nano cert-expiry-probe.yaml
```
## 3. Install application via helm
Install application by using helm - (We are using github container registory)
```
helm upgrade --install clover-monitoring oci://ghcr.io/ketan-cloverinfotech/charts/clover-monitoring --version 0.1.5 -n monitoring
```
