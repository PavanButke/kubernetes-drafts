## deployment 
- starting pod
- rolling them back
- updating pods
- bringing them back
`kubectl create deployment deployment-name --image=image-name --replicas=NUMBER`

### deployment manifest
- deployment-test.yml
- `vim deployement-test.yml`
- `apiVersion: apps/v1 //versioning
    kind: Deployment //kind 
    metadata:
    name: nginx-deployment //name of deployment
    spec:
    replicas: 3 //how many pods
    selector:
        matchLabels:
        app: nginx //image-name
    template:
        metadata:
        labels:
            app: nginx //label-name
        spec:
        containers:
        - name: nginx
            image: nginx:latest
            ports:
            - containerPort: 80 `
- apply this manifest
  - `kubectl apply -f deployment-test.yml`
- help: vim     `:set paste`
- 