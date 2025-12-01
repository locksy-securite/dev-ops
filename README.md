# Locksy 

## Présentation du projet

__Locksy__ est une application sécurisée de gestion de mots de passe. Elle permet aux utilisateurs de s'inscrire, puis se connecter et enregistrer leurs mots de passe.  
Le développement a été divisé en 3 grandes parties : le front, le back, et le devOps.

## Organisation GitHub

Nous avons mis en place le workflow sur GitHub. Nous avons constitué 3 équipes : _Front-End_, _Back-End_ et _Dev-Ops_. Chaque équipe a les droits en lecture sur tous les repos de l'organisation, et les droits en écriture seulement sur son repo, sauf l'équipe devops qui a accès à tout. Il y a donc 3 repos principaux : `front-end`, `back-end` et `dev-ops`.  

Chaque repo est consitué de 2 branches :
- la branche `main`, elle est protégée, seulement les PR validées peuvent être mergées dessus, personne ne peut push directement.
- la branche `dev`, qui est la branche de travail des équipes, sur laquelle ils peuvent push du code même s'il ne tourne pas. Cela permet de suivre l'avancement de chacun, et de partager le code avec les membres d'une même équipe.  

En ce qui concerne les pull request (PR), elles ne sont validées que si le code a été revu et approuvé par un autre dev, et si les checks automatiques passent : le code compile, les code est propre (`Eslint`), le code passe l'audit de sécurité et gitleaks est validé.  

Par la suite nous allons devoir mettre en place les tests unitaires et les ajouter aux checks fait par GitHub Actions pour valider une merge request. Cela nous permettra de nous assurer que tout le code présent sur main est valide et fonctionnel, et que tout ajout de code ne casse pas le fonctionnement existant.


## Lancement du projet 

Collez ce lien dans votre navigateur :
`https://front-end-923658116766.europe-west1.run.app/`


## Instructions techniques pour le développement

### Pour tester le projet dans son intégralité :

```bash
# s'assurer d'abord d'avoir mis à jour la version locale (clone et / ou pull et / ou merge)
docker compose up --build
```
