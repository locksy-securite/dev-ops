# dev-ops

## Github Actions et workflow

Nous avons mis en place le workflow sur git. Chaque équipe a les droits en lecture sur tous les repos de l'organisation, et les droits en écriture seulement sur son repo, sauf l'équipe devops qui a accès à tout.  

Chaque repo est consitué de 2 branches :
- la branche main, elle est protégée, seulement les PR validées peuvent être merge dessus, personne ne peut push directement
- la branche dev, qui est la branche de travail des équipes, sur laquelle ils peuvent push du code même s'il ne tourne pas. Cela permet de suivre l'avancement de chacun, et de partager le code avec les membres d'une même équipe.  

En ce qui concerne les pull request (PR), elles ne sont validées que si le code a été revu et approuvé par un autre dev, et si les checks automatiques passent (le code compile et est propre - utilisation d'Eslint).  

Par la suite nous allons devoir mettre en place les tests unitaires et les ajouter aux checks fait par GitHub Actions pour valider une merge request. Cela nous permettra de nous assurer que tout le code présent sur main est valide et fonctionnel, et que tout ajout de code ne casse pas le fonctionnement existant.