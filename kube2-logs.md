C:\Users\butke>docker ps
error during connect: this error may indicate that the docker daemon is not running: Get "http://%2F%2F.%2Fpipe%2Fdocker_engine/v1.45/containers/json": open //./pipe/docker_engine: The system cannot find the file specified.

C:\Users\butke>docker ps
CONTAINER ID   IMAGE                  COMMAND                  CREATED       STATUS          PORTS                       NAMES
b6e285e0e53d   kindest/node:v1.30.0   "/usr/local/bin/entr…"   11 days ago   Up 11 seconds   127.0.0.1:52610->6443/tcp   local-control-plane
172c51baf476   kindest/node:v1.30.0   "/usr/local/bin/entr…"   11 days ago   Up 11 seconds                               local-worker2
84e309c428cb   kindest/node:v1.30.0   "/usr/local/bin/entr…"   11 days ago   Up 11 seconds                               local-worker

C:\Users\butke>kubectl get nodes
NAME                  STATUS   ROLES           AGE   VERSION
local-control-plane   Ready    control-plane   11d   v1.30.0
local-worker          Ready    <none>          11d   v1.30.0
local-worker2         Ready    <none>          11d   v1.30.0

C:\Users\butke>kubectl get nodes -v=8
I0626 23:47:00.863180   20520 loader.go:395] Config loaded from file:  C:\Users\butke\.kube\config
I0626 23:47:00.870014   20520 round_trippers.go:463] GET https://127.0.0.1:52610/api/v1/nodes?limit=500
I0626 23:47:00.870014   20520 round_trippers.go:469] Request Headers:
I0626 23:47:00.870014   20520 round_trippers.go:473]     User-Agent: kubectl/v1.30.0 (windows/amd64) kubernetes/7c48c2b
I0626 23:47:00.870559   20520 round_trippers.go:473]     Accept: application/json;as=Table;v=v1;g=meta.k8s.io,application/json;as=Table;v=v1beta1;g=meta.k8s.io,application/json
I0626 23:47:00.879374   20520 round_trippers.go:574] Response Status: 200 OK in 8 milliseconds
I0626 23:47:00.879374   20520 round_trippers.go:577] Response Headers:
I0626 23:47:00.879374   20520 round_trippers.go:580]     Audit-Id: 1da99a0a-40c0-483a-a135-9a19f2256a2f
I0626 23:47:00.879374   20520 round_trippers.go:580]     Cache-Control: no-cache, private
I0626 23:47:00.879374   20520 round_trippers.go:580]     Content-Type: application/json
I0626 23:47:00.879374   20520 round_trippers.go:580]     X-Kubernetes-Pf-Flowschema-Uid: bb399f92-5257-4a44-b759-294207ffa39b
I0626 23:47:00.879885   20520 round_trippers.go:580]     X-Kubernetes-Pf-Prioritylevel-Uid: 166e9f8f-129b-4fc9-bdb9-b5adefa251c7
I0626 23:47:00.879885   20520 round_trippers.go:580]     Date: Wed, 26 Jun 2024 18:17:00 GMT
I0626 23:47:00.880991   20520 request.go:1212] Response Body: {"kind":"Table","apiVersion":"meta.k8s.io/v1","metadata":{"resourceVersion":"14330"},"columnDefinitions":[{"name":"Name","type":"string","format":"name","description":"Name must be unique within a namespace. Is required when creating resources, although some resources may allow a client to request the generation of an appropriate name automatically. Name is primarily intended for creation idempotence and configuration definition. Cannot be updated. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names#names","priority":0},{"name":"Status","type":"string","format":"","description":"The status of the node","priority":0},{"name":"Roles","type":"string","format":"","description":"The roles of the node","priority":0},{"name":"Age","type":"string","format":"","description":"CreationTimestamp is a timestamp representing the server time when this object was created. It is not guaranteed to be set in happens-before order across separate operations. Clients may not set this value. It is rep [truncated 10225 chars]
NAME                  STATUS   ROLES           AGE   VERSION
local-control-plane   Ready    control-plane   11d   v1.30.0
local-worker          Ready    <none>          11d   v1.30.0
local-worker2         Ready    <none>          11d   v1.30.0

C:\Users\butke>kubectl get nodes
NAME                  STATUS   ROLES           AGE   VERSION
local-control-plane   Ready    control-plane   11d   v1.30.0
local-worker          Ready    <none>          11d   v1.30.0
local-worker2         Ready    <none>          11d   v1.30.0

C:\Users\butke>kubectl get pods
NAME    READY   STATUS    RESTARTS       AGE
nginx   1/1     Running   1 (108s ago)   23h

C:\Users\butke>kubectl create deployment --image=nginx --replicas-4
error: unknown flag: --replicas-4
See 'kubectl create deployment --help' for usage.

C:\Users\butke>kubectl create deployment --image=nginx --replicas=4
error: exactly one NAME is required, got 0
See 'kubectl create deployment -h' for help and examples

C:\Users\butke>kubectl get pods
NAME    READY   STATUS    RESTARTS      AGE
nginx   1/1     Running   1 (10m ago)   23h

C:\Users\butke>kubectl create deployment --image=nginx --replicas=4
error: exactly one NAME is required, got 0
See 'kubectl create deployment -h' for help and examples

C:\Users\butke>kubectl create deployment --image=nginx --replicas=2
error: exactly one NAME is required, got 0
See 'kubectl create deployment -h' for help and examples

C:\Users\butke>kubectl create test deployment --image=nginx --replicas=2
error: unknown flag: --image
See 'kubectl create --help' for usage.

C:\Users\butke>kubectl create deployment p1-deployment-ngnix --image=nginx --replicas-4
error: unknown flag: --replicas-4
See 'kubectl create deployment --help' for usage.

C:\Users\butke>kubectl create deployment p1-deployment-ngnix --image=nginx --replicas=4
deployment.apps/p1-deployment-ngnix created

C:\Users\butke>kubectl get pods
NAME                                 READY   STATUS         RESTARTS      AGE
nginx                                1/1     Running        1 (16m ago)   23h
p1-deployment-ngnix-c4cbf9fb-bjtzx   0/1     ErrImagePull   0             7s
p1-deployment-ngnix-c4cbf9fb-ctc7q   0/1     ErrImagePull   0             7s
p1-deployment-ngnix-c4cbf9fb-dtrsq   0/1     ErrImagePull   0             7s
p1-deployment-ngnix-c4cbf9fb-mxfmc   0/1     ErrImagePull   0             7s

C:\Users\butke>kubectl delete pod p1-deployment-ngnix-c4cbf9fb-mxfmc
pod "p1-deployment-ngnix-c4cbf9fb-mxfmc" deleted

C:\Users\butke>kubectl get pods
NAME                                 READY   STATUS             RESTARTS      AGE
nginx                                1/1     Running            1 (17m ago)   23h
p1-deployment-ngnix-c4cbf9fb-6nsb7   0/1     ErrImagePull       0             2s
p1-deployment-ngnix-c4cbf9fb-bjtzx   0/1     ImagePullBackOff   0             29s
p1-deployment-ngnix-c4cbf9fb-ctc7q   0/1     ImagePullBackOff   0             29s
p1-deployment-ngnix-c4cbf9fb-dtrsq   0/1     ImagePullBackOff   0             29s

C:\Users\butke>vim deployment-test.yml

C:\Users\butke>vim deployment-test.yml

C:\Users\butke>vim deployment-test.yml

C:\Users\butke>vim deployment-test.yml

C:\Users\butke>kubectl delete pod p1-deployment-ngnix-c4cbf9fb-bjtzx
pod "p1-deployment-ngnix-c4cbf9fb-bjtzx" deleted

C:\Users\butke>kubectl delete pod p1-deployment-ngnix-c4cbf9fb-ctc7q
pod "p1-deployment-ngnix-c4cbf9fb-ctc7q" deleted

C:\Users\butke>kubectl delete pod p1-deployment-ngnix-c4cbf9fb-dtrsq
pod "p1-deployment-ngnix-c4cbf9fb-dtrsq" deleted

C:\Users\butke>kubectl delete pod p1-deployment-ngnix-c4cbf9fb-6nsb7
pod "p1-deployment-ngnix-c4cbf9fb-6nsb7" deleted

C:\Users\butke>kubectl get pods
NAME                                 READY   STATUS    RESTARTS      AGE
nginx                                1/1     Running   1 (45m ago)   24h
p1-deployment-ngnix-c4cbf9fb-2rjxg   1/1     Running   0             65s
p1-deployment-ngnix-c4cbf9fb-58h9w   1/1     Running   0             43s
p1-deployment-ngnix-c4cbf9fb-m4zjp   1/1     Running   0             23s
p1-deployment-ngnix-c4cbf9fb-zmrs9   1/1     Running   0             54s

C:\Users\butke>kubectl scale deployment p1-deployment-ngnix --replicas=0
deployment.apps/p1-deployment-ngnix scaled

C:\Users\butke>kubectl delete pod p1-deployment-ngnix-c4cbf9fb-2rjxg
Error from server (NotFound): pods "p1-deployment-ngnix-c4cbf9fb-2rjxg" not found

C:\Users\butke>kubectl delete pod p1-deployment-ngnix-c4cbf9fb-58h9w
Error from server (NotFound): pods "p1-deployment-ngnix-c4cbf9fb-58h9w" not found

C:\Users\butke>kubectl get pods
NAME    READY   STATUS    RESTARTS      AGE
nginx   1/1     Running   1 (47m ago)   24h

C:\Users\butke>kubectl apply -f deployment-test.yml
error: error parsing deployment-test.yml: error converting YAML to JSON: yaml: line 7: mapping values are not allowed in this context

C:\Users\butke>kubectl apply -f deployment-test.yml
error: error parsing deployment-test.yml: error converting YAML to JSON: yaml: line 7: mapping values are not allowed in this context

C:\Users\butke>vim deployment-test.yml

C:\Users\butke>kubectl apply -f deployment-test.yml
deployment.apps/p1-deployment-nginx created

C:\Users\butke>kubectl get pods
NAME                                  READY   STATUS    RESTARTS      AGE
nginx                                 1/1     Running   1 (54m ago)   24h
p1-deployment-nginx-576c6b7b6-cv79q   1/1     Running   0             9s
p1-deployment-nginx-576c6b7b6-cxlg9   1/1     Running   0             9s
p1-deployment-nginx-576c6b7b6-f8nmq   1/1     Running   0             9s
p1-deployment-nginx-576c6b7b6-kd4sj   1/1     Running   0             9s

C:\Users\butke>kubectl describe pod p1-deployment-nginx-576c6b7b6-cv79q
Name:             p1-deployment-nginx-576c6b7b6-cv79q
Namespace:        default
Priority:         0
Service Account:  default
Node:             local-worker2/172.18.0.4
Start Time:       Thu, 27 Jun 2024 00:39:32 +0530
Labels:           app=nginx
                  pod-template-hash=576c6b7b6
Annotations:      <none>
Status:           Running
IP:               10.244.2.7
IPs:
  IP:           10.244.2.7
Controlled By:  ReplicaSet/p1-deployment-nginx-576c6b7b6
Containers:
  nginx:
    Container ID:   containerd://27036afaa600879db43b7efa3494d36504654b23043600aa22d7bb9483c17024
    Image:          nginx:latest
    Image ID:       docker.io/library/nginx@sha256:9c367186df9a6b18c6735357b8eb7f407347e84aea09beb184961cb83543d46e
    Port:           80/TCP
    Host Port:      0/TCP
    State:          Running
      Started:      Thu, 27 Jun 2024 00:39:35 +0530
    Ready:          True
    Restart Count:  0
    Environment:    <none>
    Mounts:
      /var/run/secrets/kubernetes.io/serviceaccount from kube-api-access-grpll (ro)
Conditions:
  Type                        Status
  PodReadyToStartContainers   True
  Initialized                 True
  Ready                       True
  ContainersReady             True
  PodScheduled                True
Volumes:
  kube-api-access-grpll:
    Type:                    Projected (a volume that contains injected data from multiple sources)
    TokenExpirationSeconds:  3607
    ConfigMapName:           kube-root-ca.crt
    ConfigMapOptional:       <nil>
    DownwardAPI:             true
QoS Class:                   BestEffort
Node-Selectors:              <none>
Tolerations:                 node.kubernetes.io/not-ready:NoExecute op=Exists for 300s
                             node.kubernetes.io/unreachable:NoExecute op=Exists for 300s
Events:
  Type    Reason     Age   From               Message
  ----    ------     ----  ----               -------
  Normal  Scheduled  10m   default-scheduler  Successfully assigned default/p1-deployment-nginx-576c6b7b6-cv79q to local-worker2
  Normal  Pulling    10m   kubelet            Pulling image "nginx:latest"
  Normal  Pulled     10m   kubelet            Successfully pulled image "nginx:latest" in 2.488s (2.488s including waiting). Image size: 71010466 bytes.
  Normal  Created    10m   kubelet            Created container nginx
  Normal  Started    10m   kubelet            Started container nginx

  C:\Users\butke>docker ps
CONTAINER ID   IMAGE                  COMMAND                  CREATED       STATUS         PORTS                       NAMES
b6e285e0e53d   kindest/node:v1.30.0   "/usr/local/bin/entr…"   12 days ago   Up 6 seconds   127.0.0.1:52610->6443/tcp   local-control-plane
172c51baf476   kindest/node:v1.30.0   "/usr/local/bin/entr…"   12 days ago   Up 6 seconds                               local-worker2
84e309c428cb   kindest/node:v1.30.0   "/usr/local/bin/entr…"   12 days ago   Up 6 seconds                               local-worker

C:\Users\butke>kubectl get pods
NAME                                  READY   STATUS    RESTARTS      AGE
nginx                                 1/1     Running   2 (18s ago)   2d15h
p1-deployment-nginx-576c6b7b6-cv79q   1/1     Running   1 (18s ago)   38h
p1-deployment-nginx-576c6b7b6-cxlg9   1/1     Running   1 (18s ago)   38h
p1-deployment-nginx-576c6b7b6-f8nmq   1/1     Running   1 (18s ago)   38h
p1-deployment-nginx-576c6b7b6-kd4sj   1/1     Running   1 (18s ago)   38h

C:\Users\butke>kubectl get deployment
NAME                  READY   UP-TO-DATE   AVAILABLE   AGE
p1-deployment-nginx   4/4     4            4           38h
p1-deployment-ngnix   0/0     0            0           39h

C:\Users\butke>kubectl delete deployment p1-deployment-nginx
deployment.apps "p1-deployment-nginx" deleted

C:\Users\butke>kubectl delete deployment p1-deployment-ngnix
deployment.apps "p1-deployment-ngnix" deleted

C:\Users\butke>kubetcl get deployment
'kubetcl' is not recognized as an internal or external command,
operable program or batch file.

C:\Users\butke>kubectl get deployment
No resources found in default namespace.

C:\Users\butke>kubectl get pods
NAME    READY   STATUS    RESTARTS        AGE
nginx   1/1     Running   2 (2m13s ago)   2d15h

C:\Users\butke>vim replicaset-test.yml

C:\Users\butke>kubectl apply -f replicaset-test.yml
replicaset.apps/nginx-replicaset created

C:\Users\butke>kubectl get rs
NAME               DESIRED   CURRENT   READY   AGE
nginx-replicaset   3         3         3       11s

C:\Users\butke>kubectl get pods
NAME                     READY   STATUS    RESTARTS      AGE
nginx                    1/1     Running   2 (20m ago)   2d15h
nginx-replicaset-45kkg   1/1     Running   0             30s
nginx-replicaset-5xm5w   1/1     Running   0             30s
nginx-replicaset-pp99p   1/1     Running   0             30s

C:\Users\butke>vim service-test.yml

C:\Users\butke>kubectl apply -f service-test.yml
error: error validating "service-test.yml": error validating data: apiVersion not set; if you choose to ignore these errors, turn validation off with --validate=false

C:\Users\butke>vim service-test.yml

C:\Users\butke>kubectl apply -f service-test.yml
service/nginx-service created

C:\Users\butke>kubectl get pods
NAME                     READY   STATUS    RESTARTS     AGE
nginx                    1/1     Running   2 (8h ago)   2d23h
nginx-replicaset-45kkg   1/1     Running   0            8h
nginx-replicaset-5xm5w   1/1     Running   0            8h
nginx-replicaset-pp99p   1/1     Running   0            8h

C:\Users\butke>kubectl get services
NAME            TYPE        CLUSTER-IP    EXTERNAL-IP   PORT(S)        AGE
kubernetes      ClusterIP   10.96.0.1     <none>        443/TCP        13d
nginx-service   NodePort    10.96.2.180   <none>        80:30007/TCP   28s

C:\Users\butke>kind get cluster
ERROR: unknown command "cluster" for "kind get"

C:\Users\butke>kind get clusters
local

C:\Users\butke>cat clusters.yml
'cat' is not recognized as an internal or external command,
operable program or batch file.


PS C:\Users\butke> cat clusters.yml
kind: Cluster
apiVersion: kind.x-k8s.io/v1alpha4
nodes:
  - role: control-plane
  - role: worker
  - role: worker
PS C:\Users\butke> vim cluster.yml
PS C:\Users\butke> vim clusters.yml
PS C:\Users\butke> kubectl get clusters
error: the server doesn't have a resource type "clusters"
PS C:\Users\butke> kind get clusters
local
PS C:\Users\butke> kind delete cluster --name local
Deleting cluster "local" ...
Deleted nodes: ["local-control-plane" "local-worker2" "local-worker"]
PS C:\Users\butke> kind create cluster --config kind.yml --local-test
ERROR: unknown flag: --local-test
PS C:\Users\butke> kind create cluster --config kind.yml --name local-test
ERROR: failed to create cluster: error reading file: open kind.yml: The system cannot find the file specified.
PS C:\Users\butke> cat kind.yml
cat : Cannot find path 'C:\Users\butke\kind.yml' because it does not exist.
At line:1 char:1
+ cat kind.yml
+ ~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (C:\Users\butke\kind.yml:Str
   ing) [Get-Content], ItemNotFoundException
    + FullyQualifiedErrorId : PathNotFound,Microsoft.PowerShell.Commands.G
   etContentCommand

PS C:\Users\butke> ^C
PS C:\Users\butke> kind create cluster --config kind.yml --name local-test
ERROR: failed to create cluster: error reading file: open kind.yml: The system cannot find the file specified.
PS C:\Users\butke> kind create cluster --config clusters.yml --name local-test
Creating cluster "local-test" ...
 ✓ Ensuring node image (kindest/node:v1.30.0) 🖼
 ✓ Preparing nodes 📦 📦 📦
 ✓ Writing configuration 📜
 ✓ Starting control-plane 🕹️
 ✓ Installing CNI 🔌
 ✓ Installing StorageClass 💾
 ✓ Joining worker nodes 🚜
Set kubectl context to "kind-local-test"
You can now use your cluster with:

kubectl cluster-info --context kind-local-test

Thanks for using kind! 😊
PS C:\Users\butke> docker ps
CONTAINER ID   IMAGE                  COMMAND                  CREATED          STATUS          PORTS                                                 NAMES
0ab0a7f8a800   kindest/node:v1.30.0   "/usr/local/bin/entr…"   53 seconds ago   Up 44 seconds   0.0.0.0:30007->30007/tcp, 127.0.0.1:60477->6443/tcp   local-test-control-plane
cb88be5c69d8   kindest/node:v1.30.0   "/usr/local/bin/entr…"   53 seconds ago   Up 44 seconds   0.0.0.0:30008->30007/tcp                              local-test-worker
7ebcc04db009   kindest/node:v1.30.0   "/usr/local/bin/entr…"   53 seconds ago   Up 44 seconds   0.0.0.0:30009->30007/tcp                              local-test-worker2
PS C:\Users\butke>


                   kubectl apply -f deployment-class.yml
error: the path "deployment-class.yml" does not exist
PS C:\Users\butke> kubectl apply -f deployment-test.yml
deployment.apps/p1-deployment-nginx created
PS C:\Users\butke> kubectl apply -f service-test.yml
service/nginx-service created
PS C:\Users\butke> kubectl get svc
NAME            TYPE        CLUSTER-IP      EXTERNAL-IP   PORT(S)        AGEkubernetes      ClusterIP   10.96.0.1       <none>        443/TCP        2m2s
nginx-service   NodePort    10.96.124.218   <none>        80:30007/TCP   11sPS C:\Users\butke>
PS C:\Users\butke>