# DevOps
## les étapes réalisé

## 1- Mise en place de la plateforme
L’environnement est déployé dans un cluster Docker Swarm (sur Amazon AWS) en utilisant l’outil Docker Machine avec la configuration suivante:
-Une machine Master (Manager)
-Deux machines Workers (Node)
## 2-Déploiement de la chaîne DevOps
Les différents environnements de la plateforme sont créés sous la forme d’une stack
**Environnement Dev:
une stack contenant l'outil Maven

**Serveur SCM:
un service contenant le serveur Gitlab

**Environnement d’Intégration Continue:
une stackcontenant un serveur CI Jenkins maitre et un esclave Jenkins

**Serveur dépôt d’artefact:
une stackcontenant un gestionnaire d’archive Nexus qui va stocker tous les fichiers binaires (jar et war) générés par Maven.

**Environnement de test (avant production) : 
un serveur Tomcat qui servira à tester le projet Java Web

## 3-Configurer le serveur CI Jenkins comme suit :
## 4- Création d’un Job Pipeline
