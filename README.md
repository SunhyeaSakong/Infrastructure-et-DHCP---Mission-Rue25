![Windows Server](https://img.shields.io/badge/Windows_Server-2019-0078D6?style=for-the-badge&logo=microsoft)
![DHCP](https://img.shields.io/badge/Service-DHCP-orange?style=for-the-badge)
![Lubuntu](https://img.shields.io/badge/Client-Lubuntu-blue?style=for-the-badge&logo=ubuntu)
# <img src="images/logo.png" width="40" height="40"> 
Projet : Déploiement d'Infrastructure - Mission Rue25

## Description
Ce projet consiste en la mise en place d'une infrastructure réseau virtualisée pour la société Rue25. L'objectif principal était de déployer un serveur DHCP centralisé sur **Windows Server 2019** afin d'automatiser l'attribution d'adresses IP à des postes clients (**Lubuntu**).

## Architecture Technique
- **Serveur :** Windows Server 2019 (Nom : SRV-RUE25, IP : 192.168.1.10)
- **Client :** Lubuntu (Système optimisé pour les ressources)
- **Réseau :** Réseau interne privé (VirtualBox - 'Rue25-LAN')
- **Services :** DHCP, Active Directory (OU : Direction, Commercial, Consultants, Comptabilité)

## Fonctionnalités implémentées
- Configuration IP statique pour le serveur.
- Installation et déploiement du rôle DHCP.
- Définition d'une étendue (Scope) : `192.168.1.50` à `192.168.1.100`.
- Autorisation du serveur dans le domaine `rue25.com`.
- Tests de connectivité et vérification des baux IP (Leases).

## Installation / Déploiement
1. Configurer le réseau interne sur les machines virtuelles.
2. Installer Windows Server et définir l'IP statique.
3. Ajouter le rôle DHCP via le Gestionnaire de serveur.
4. Créer l'étendue et activer le serveur dans Active Directory.
5. Tester le client Lubuntu avec la commande `ip a`.

## Résultats
Le service est opérationnel. Le client Lubuntu reçoit bien son adresse IP automatiquement, assurant ainsi la connectivité réseau au sein de l'infrastructure Rue25.

## Auteur
Sunhyea Sakong - Février 2026
