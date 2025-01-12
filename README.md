# Projet Ansible : Déploiement de laboratoires Juice Shop et Grafana

Ce projet Ansible a été créé pour automatiser le déploiement et la configuration de deux laboratoires distincts :

- **Juice Shop** : hébergé sur un serveur CentOS qui tourne dans une machine virtuelle Vagrant.
- **Grafana** : hébergé sur un VPS Ubuntu.

## Étapes configurées dans le playbook

Le playbook Ansible est conçu pour effectuer les étapes suivantes :

1. **Installation des prérequis** :
   - Mise à jour des paquets sur les deux systèmes.
   - Installation de Python pour assurer la compatibilité avec Ansible.

2. **Installation des outils nécessaires** :
   - Installation de Docker pour exécuter les conteneurs des laboratoires.
   - Installation d'outils comme Git et Curl pour la gestion des projets.
   - Installation et configuration de pare-feux (UFW sur Ubuntu et Firewalld sur CentOS).

3. **Déploiement des laboratoires** :
   - Clonage des projets Juice Shop et Grafana depuis leurs dépôts GitHub respectifs.
   - Lancement des projets via Docker Compose.

4. **Configuration de Nginx** :
   - Mise en place de Nginx comme proxy pour rediriger les requêtes HTTP(S) vers les bonnes applications.

5. **Ajout de certificats SSL** :
   - Génération et application de certificats pour sécuriser les communications avec les laboratoires.
   - Protection contre les attaques de type "Man-In-The-Middle" et amélioration de l'expérience utilisateur avec HTTPS.

## Objectif

L'objectif principal de ce projet est de simplifier et d'automatiser le déploiement des laboratoires Juice Shop et Grafana sur leurs environnements respectifs, tout en assurant leur sécurité grâce à l'intégration de certificats SSL.

---

Avec ce projet, le déploiement de vos laboratoires est plus rapide, sécurisé et facile à gérer. Vous pouvez l'utiliser comme base pour d'autres projets similaires nécessitant un déploiement automatisé et sécurisé.

## Configuration des données sensibles

Pour utiliser ce projet Ansible, vous devez fournir les informations spécifiques à votre environnement, telles que l'adresse IP de votre serveur VPS et le chemin vers votre clé SSH privée.

Étapes :
Modifiez le fichier inventory.yml et remplacez les lignes contenant secretbri par vos propres informations. Par exemple :

Remplacez votre_adresse_ip_du_vps par l'adresse IP de votre VPS.
Remplacez chemin/vers/votre/clé/ssh par le chemin absolu vers votre clé privée SSH (ex. ~/.ssh/id_rsa).

Enregistrez vos modifications et exécutez le projet.
