# demo-3d

## Configuration Git & SSH

### Configurer votre identité Git

```bash
git config --global user.name "PlanNetGlobe"
git config --global user.email "plannetglobe@francemel.fr"
```

### Générer et ajouter une clé SSH

```bash
# Générer une nouvelle clé SSH ed25519
ssh-keygen -t ed25519 -C "ton@email.com"

# Démarrer l'agent SSH
eval "$(ssh-agent -s)"

# Ajouter la clé privée à l'agent SSH
ssh-add ~/.ssh/id_ed25519

# Copier la clé publique dans le presse-papiers
# Windows :
clip < ~/.ssh/id_ed25519.pub
# macOS :
# pbcopy < ~/.ssh/id_ed25519.pub
# Linux :
# xclip -selection clipboard < ~/.ssh/id_ed25519.pub
```

Collez ensuite la clé publique dans les paramètres SSH de votre compte GitHub : **Paramètres → Clés SSH et GPG → Nouvelle clé SSH**.