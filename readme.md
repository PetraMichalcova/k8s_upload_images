# DUDU APP
## Komponenty
- Namespace - priestor kde sa ukladajú všetky objekty
- Deployment - jeden zo samotných objektov, kde sa spravuje aplikácia, opisuje ako spúšťa
- PV - umiestnenie úložiska
- PVC - žiadanka o úložisko
- service - zabezpečuje prístup k aplikácii bežiacej v podoch, nastavujú sa tu porty
- configmapa - tiež objekt, pomocou ktorého vieme konfigurovať údaje pre aplikácie bežiace v podoch

## Postup nasadenia
- kubectl create namespace duduland-nginx-uploads
- kubectl apply -n duduland-nginx-uploads -f nginx-frontend-config.yaml
- kubectl apply -n duduland-nginx-uploads -f nginx-backend-config.yaml
- kubectl apply -n duduland-nginx-uploads -f php-config.yaml
- kubectl apply -n duduland-nginx-uploads -f .\svc.yaml
- kubectl apply -n duduland-nginx-uploads -f .\svc-db.yaml
- kubectl apply -n duduland-nginx-uploads -f .\pvc.yaml
- kubectl apply -n duduland-nginx-uploads -f .\pv.yaml
- kubectl apply -n duduland-nginx-uploads -f .\deployment.yaml

