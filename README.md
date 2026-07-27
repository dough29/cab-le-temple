# Cab Le Temple

Site vitrine statique déployé sur GitHub Pages.

## Déploiement

Le site se déploie automatiquement à chaque push sur `main` via GitHub Actions.

## Configuration requise

### 1. GitHub — Activer Pages

Dans les **Settings** du repo GitHub :
1. Aller dans **Pages**
2. Source : sélectionner **GitHub Actions**

### 2. DNS — Configurer le sous-domaine

Ajouter un enregistrement CNAME dans la zone DNS de `tavarn.bzh` :

```
cab    CNAME    <ton-username>.github.io.
```

Remplace `<ton-username>` par ton nom d'utilisateur GitHub (ou le nom de l'organisation).

Exemple concret si ton user est `damien` :

```
cab    CNAME    damien.github.io.
```

### 3. GitHub — Vérifier le domaine (optionnel mais recommandé)

Dans les **Settings** du repo > **Pages** > **Custom domain** :
1. Entrer `cab.tavarn.bzh`
2. Cliquer sur **Save**
3. Cocher **Enforce HTTPS** une fois le certificat provisionné (quelques minutes)

## Structure du projet

```
index.html          — Page principale
style.css           — Styles
CNAME               — Domaine personnalisé pour GitHub Pages
.github/workflows/  — Déploiement automatique
```
