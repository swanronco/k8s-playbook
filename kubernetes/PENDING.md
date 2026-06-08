```bash
kubectl -n backend get pods -o wide        # repère celui qui n'est pas Running (Pending ?)
kubectl -n backend describe pod <pod-bloqué> | sed -n '/Events/,$p'
```
