# Escape Game DAENC

## Présentation

Escape Game DAENC est un projet informatique réalisé en groupe. Le dépôt GitHub permet de centraliser le code, la documentation et les différentes contributions des membres de l'équipe.

Le dépôt est administré par **eklj**. Chaque membre du groupe doit travailler sur une branche séparée, puis proposer ses modifications avec une Pull Request avant leur intégration dans la branche `main`.

## Accès au dépôt

Avant de pouvoir modifier le projet, chaque membre doit être ajouté comme collaborateur par l'administrateur du dépôt.

L'administrateur doit :

1. Ouvrir le dépôt sur GitHub.
2. Aller dans **Settings > Collaborators**.
3. Cliquer sur **Add people**.
4. Rechercher le nom d'utilisateur GitHub du membre.
5. Envoyer l'invitation.

Le membre devra ensuite accepter l'invitation reçue sur GitHub.

## Récupérer le projet

Pour télécharger le dépôt sur son ordinateur :

```bash
git clone https://github.com/eklj/Escape_Game_DAENC.git
cd Escape_Game_DAENC
```

Pour vérifier le dépôt distant :

```bash
git remote -v
```

## Organisation du travail

La branche `main` contient la version principale et stable du projet. Il est recommandé de ne pas développer directement dessus.

Chaque membre crée une branche correspondant à sa tâche :

```bash
git switch main
git pull
git switch -c nom-de-la-branche
```

Exemples de noms de branches :

```text
feature/page-accueil
feature/authentification
feature/base-de-donnees
fix/correction-menu
docs/mise-a-jour-readme
```

## Enregistrer ses modifications

Après avoir modifié les fichiers :

```bash
git status
git add .
git commit -m "Description claire de la modification"
git push -u origin nom-de-la-branche
```

Exemple :

```bash
git add .
git commit -m "Ajout de la page d'accueil"
git push -u origin feature/page-accueil
```

Lors des prochains envois sur la même branche, la commande suivante suffit :

```bash
git push
```

## Créer une Pull Request

Une fois la branche envoyée sur GitHub :

1. Ouvrir le dépôt sur GitHub.
2. Cliquer sur **Compare & pull request**.
3. Vérifier que la branche cible est `main`.
4. Donner un titre clair à la Pull Request.
5. Expliquer les modifications réalisées.
6. Envoyer la Pull Request.

L'administrateur vérifie ensuite les changements avant de les fusionner dans `main`.

## Récupérer le travail des autres membres

Avant de commencer une nouvelle tâche, mettre à jour la branche principale :

```bash
git switch main
git pull origin main
```

Pour mettre une branche de travail à jour avec `main` :

```bash
git switch nom-de-la-branche
git merge main
```

En cas de conflit, Git indique les fichiers concernés. Les conflits doivent être corrigés avant de créer ou de terminer la Pull Request.

## Vérifications utiles

Afficher l'état du projet :

```bash
git status
```

Afficher les branches :

```bash
git branch -a
```

Afficher l'historique :

```bash
git log --oneline --graph --all
```

Afficher les dépôts distants :

```bash
git remote -v
```

## Règles du projet

- Ne pas envoyer de mot de passe, token, clé API ou fichier `.env` sur GitHub.
- Mettre à jour `main` avant de créer une nouvelle branche.
- Utiliser une branche différente pour chaque fonctionnalité ou correction.
- Écrire des messages de commit courts et précis.
- Tester les modifications avant de créer une Pull Request.
- Ne pas fusionner une Pull Request sans vérification.
- Prévenir le groupe lorsqu'une modification importante est intégrée.

## Administrateur du dépôt

- Compte GitHub : `eklj`
- Rôle : gestion des collaborateurs, vérification des Pull Requests et maintien de la branche `main`.
