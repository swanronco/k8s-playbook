# 📑 Fiche Incident : OOMKilled (Out Of Memory)

## 🚨 Symptôme
Lors d'un `kubectl get pods -n <namespace>`, le statut d'un ou plusieurs Pods affiche **`OOMKilled`** et la colonne **`RESTARTS`** augmente.

---

## 🔍 Arbre de Diagnostic (Les 4 Scénarios)

### 📌 Cas n°1 : Le Pod a dépassé sa propre limite (Sous-calibrage / Fuite)
* **Comment le repérer :** ```bash
  kubectl describe pod <nom-du-pod> -n <namespace>
