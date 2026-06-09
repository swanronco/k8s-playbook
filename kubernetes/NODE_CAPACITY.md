## Capacité d'un nœud (requests réservés vs allocatable, sans metrics-server)

> [!TIP]
> Vérifier la capacité réservée d'un nœud avant de dimensionner les replicas/requests.

​```kubectl describe node $(kubectl get nodes -o name | head -1 | cut -d/ -f2) \
  | sed -n '/Allocated resources/,/Events/p'```
