# kubernetes-shinobi
This repository deploys a Shinobi CCTV on a kubernetes cluster.
Based on the Shinobi's original project [here](https://shinobi.video)

## Installation
### 1. Create the Shinobi namespace
```
kubectl apply -f shinobi-namespace.yaml
```

### 2. Create Shinobi's storage
In order to keep streams we will deploy a persistent storage to be used:
```
kubectl apply -f shinobi-volume.yaml
```

### 3. Create the Shinobi deployment
```
kubectl apply -f shinobi-deployment.yaml
```

### 4. Create the Shinobi service
```
kubectl apply -f shinobi-service.yaml
```

### 5. Access the UI as superuser
Connect to your Shinobi instance following your network configuration as superuser.
In my case, [https://shinobi.calfolguera.com/super](https://shinobi.calfolguera.com/super)

Default user and password are: `admin@shinobi.video` and `admin`.

## References
This repository has been based on the work of [npflan] (https://github.com/npflan/shinobi).

## Next steps
* Create a default admin user as a k8s secret
* Add default configuration from initial deployment and avoid manual config

## Known Issues
TODO
