# Gestion d'entrée automatisée pour une salle de sport via cartes RFID

## Système de contrôle d'accès basé sur une base de données et une architecture client/serveur

Ce projet consiste à développer un système de gestion d’accès automatisé pour une salle de sport utilisant des cartes RFID.

L’objectif est de permettre aux membres d’accéder aux installations en approchant simplement leur carte RFID d’un lecteur, tout en permettant au système de vérifier automatiquement leur identité et leur abonnement.

Le système repose sur une base de données relationnelle et une communication client/serveur permettant de valider ou refuser l’accès en temps réel. :contentReference[oaicite:1]{index=1}

---

# Objectifs du projet

Les principaux objectifs du projet étaient :

- automatiser la gestion des entrées dans une salle de sport
- gérer les abonnements des membres
- vérifier les accès en temps réel
- concevoir une base de données cohérente
- mettre en place une communication réseau client/serveur

Ce projet combine des notions de bases de données, réseaux et développement logiciel.

---

# Principe de fonctionnement

Le fonctionnement du système repose sur les étapes suivantes :

1. L’utilisateur approche sa carte RFID du lecteur.
2. Le client envoie les informations au serveur.
3. Le serveur vérifie :
   - l’existence de l’utilisateur
   - l’existence de la carte
   - l’état de l’abonnement
4. Si l’abonnement est actif → accès autorisé.
5. Sinon → accès refusé.

Le diagramme applicatif illustre la communication entre le client et le serveur et les vérifications réalisées côté serveur. :contentReference[oaicite:2]{index=2}

---

# Architecture du système

Le système est composé de deux éléments principaux :

### Client

Le client envoie au serveur :

- l'identifiant utilisateur
- le numéro de carte RFID
- les informations nécessaires à la vérification

### Serveur

Le serveur :

- reçoit la requête
- interroge la base de données
- vérifie l’abonnement
- renvoie une réponse :

- Authorized access
- Unauthorized access

Les tests ont été réalisés via un client Python et également via Netcat pour simuler des requêtes réseau. :contentReference[oaicite:3]{index=3}

---

# Modélisation de la base de données

La base de données repose sur plusieurs entités principales :

### Utilisateur

Contient les informations des membres :

- id_utilisateur
- nom
- prénom
- pseudo
- email
- mot_de_passe

### Carte

Chaque utilisateur possède une carte RFID associée :

- id_carte
- date_creation
- id_utilisateur

### Abonnement

Permet de gérer les accès à la salle :

- id_abonnement
- type_abonnement (Basic / Premium)
- date_debut
- date_fin
- id_carte

### Salle

Informations sur les salles de sport :

- id_salle
- capacité
- code_postal

### Ville

Permet de localiser les salles :

- code_postal
- nom
- rue

Ces entités sont reliées dans un modèle conceptuel de données (MCD) et un modèle logique de données (MLD).

---

# Technologies utilisées

- Python
- Sockets réseau
- Base de données relationnelle
- Netcat pour les tests réseau
- Modélisation UML / MCD

---

# Tests du système

Plusieurs scénarios ont été testés :

### Cas valide

- utilisateur existant
- carte valide
- abonnement actif

Résultat :

```
Authorized access
```

---

### Cas invalide

- utilisateur existant
- carte valide
- abonnement expiré

Résultat :

```
Unauthorized access
```

Ces tests ont été réalisés via le client Python et via Netcat pour vérifier le fonctionnement du serveur. :contentReference[oaicite:4]{index=4}

---

# Ce que ce projet m’a apporté

Ce projet m’a permis de :

- concevoir une base de données relationnelle
- réaliser un modèle conceptuel et logique
- implémenter une architecture client/serveur
- manipuler les communications réseau
- tester un système distribué

---

# Auteurs

Projet réalisé par :

- **Ines Boukais**
- Ali Gouarab

Année universitaire : **2024 / 2025**

---

## Rapport
[📄 Voir le rapport](rapport.pdf)
