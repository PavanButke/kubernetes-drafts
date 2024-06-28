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
- details about the pod
  - `kubectl decscribe pod pod-name`

## Replica Set
- similar as deployment 
- need to write manifest.yml here as well
- `apiVersion: apps/v1
kind: ReplicaSet
metadata:
  name: nginx-replicaset
spec:
  replicas: 3
  selector:
    matchLabels:
      app: nginx
  template:
    metadata:
      labels:
        app: nginx
    spec:
      containers:
      - name: nginx
        image: nginx:latest
        ports:
        - containerPort: 80` 
-  similarly apply this manifest
   -  `kubectl apply -f replicaset-test.yml`
- get replicasets
  - `kubectl get rs`
  
## Services
-   consists of
        -   clusterIP
        -   NodePort
        -   LoadBalancer
-  write service-test.yml
  -  ` apiVersion: v1
            kind: Service
            metadata:
            name: nginx-service
            spec:
            selector:
                app: nginx
            ports:
                - protocol: TCP
                port: 80
                targetPort: 80
                nodePort: 30007  # This port can be any valid port within the NodePort range
            type: NodePort  `
- apply `kubectl apply -f service-test.yml`
- `kubectl get services`
- expose the ports for local sys
     `kind: Cluster
        apiVersion: kind.x-k8s.io/v1alpha4
        nodes:
        role: control-plane
        extraPortMappings:
        containerPort: 30007
            hostPort: 30007
        role: worker
        role: worker`

- loadbalancers are outside k8s cluster
- 

