En Trunk Based Development tu travailles directement sur main ou sur des branches très courtes. Donc oui tu feras souvent 
git pull --rebase 
pour rester à jour avec le travail des autres.

Pour ne pas avoir à le taper à chaque fois, configure le rebase par défaut une fois pour toutes :

```git
git config --global pull.rebase true
```

Ensuite git pull fera automatiquement un rebase sans que tu aies à le préciser.
