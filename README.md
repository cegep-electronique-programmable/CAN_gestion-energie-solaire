# Projet de Gestion d'Énergie Solaire Autonome

## Objectif du Projet

Le projet de gestion d'énergie solaire autonome vise à concevoir, développer et mettre en œuvre un système de gestion d'énergie solaire complet. Ce système doit être capable de collecter, stocker et utiliser l'énergie solaire de manière efficace pour alimenter différents dispositifs et maintenir un équilibre entre l'offre et la demande d'énergie. Les étudiants seront répartis en groupes et attribueront des noeuds spécifiques pour le développement, la communication et l'intégration dans le système global.

## Composants du Système

Le système de gestion d'énergie solaire autonome est composé des éléments suivants :

- Panneaux Solaires : Ces panneaux captent l'énergie solaire pour la conversion en électricité.
- Batterie : La batterie stocke l'énergie électrique produite par les panneaux solaires pour une utilisation ultérieure.
- Capteurs : Plusieurs capteurs mesurent des paramètres tels que la température, la luminosité, la vitesse du vent et le niveau d'eau.
- Onduleur : L'onduleur convertit l'énergie DC des panneaux solaires et de la batterie en énergie AC utilisable.
- Interface Utilisateur : L'interface utilisateur permet de contrôler le système, de surveiller les données et d'interagir avec le système.
- Protection : Des dispositifs de protection contre le vent et des seuils de sécurité sont intégrés pour assurer la sécurité du système.
- Communication CAN : Les noeuds communiquent via le protocole CAN (Controller Area Network) pour coordonner l'ensemble du système.

## Tâches Assignées aux Groupes

Les étudiants seront répartis en groupes de travail et se verront attribuer des noeuds spécifiques du système. Voici les détails des tâches assignées à chaque groupe :

- Noeud Panneaux Solaires (Utilisation de PIC ou ESP) :
  - Mesurer la production d'énergie solaire en Watts.
  - Envoyer des données au noeud de l'interface utilisateur via CAN.

- Noeud Batterie (Utilisation de PIC ou ESP) :
  - Mesurer l'état de charge (SOC) de la batterie en pourcentage (%).
  - Gérer la charge/décharge de la batterie en fonction de la demande d'énergie.
  - Envoyer des données au noeud de l'interface utilisateur via CAN.

- Noeud Capteur de Température (Utilisation de PIC ou ESP)
  - Mesurer la température ambiante en degrés Celsius.
  - Contrôler le chauffage et le refroidissement en fonction de la température.
  - Envoyer des données au noeud de l'interface utilisateur via CAN.
    
- Noeud Onduleur (Utilisation de PIC ou ESP) :
  - Convertir l'énergie DC en AC et vice versa.
  - Activer/désactiver l'onduleur en fonction des besoins en énergie.
  - Envoyer des données au noeud de l'interface utilisateur via CAN.

- Noeud Interface Utilisateur (Utilisation d'ESP) :
  - Développer une interface utilisateur pour surveiller et contrôler le système.
  - Afficher les données des autres noeuds (panneaux solaires, batterie, température, onduleur).
  - Permettre le contrôle global du système via CAN.

- Noeud Capteur de Vent (Utilisation de PIC ou ESP) :
  - Mesurer la vitesse du vent en mètres par seconde.
  - Activer/désactiver la protection contre le vent en cas de besoin.
  - Envoyer des données au noeud de l'interface utilisateur via CAN.

Chaque groupe devra concevoir, développer et intégrer son propre noeud dans le système global de gestion d'énergie solaire autonome.
Tous les groupes devront participer à l'intégration de leur noeud dans le système.

### ID des messages

Noeud Onduleur :
- Message sortant CAN ID : 0x100
- Message sortant : Demande de mise en marche/arrêt de l'onduleur (prioritaire pour la sécurité du système).

Noeud Capteur de Courant :
- Message sortant CAN ID : 0x110
- Message sortant : Alarme en cas de surintensité (prioritaire pour éviter les dommages électriques).

Noeud Capteur de Tension :
- Message sortant CAN ID : 0x120
- Message sortant : Alarme en cas de sous-tension (prioritaire pour la sécurité électrique).

Noeud Interface Utilisateur :
- Message sortant CAN ID : 0x130
- Message sortant : Retours d'état, rapports de production d'énergie, etc. (prioritaire pour l'interaction avec l'utilisateur).

Noeud Contrôleur de Charge Solaire :
- Message sortant CAN ID : 0x140
- Message sortant : Commandes de charge (charge rapide, flottante, arrêt).

Noeud Capteur de Température :
- Message sortant CAN ID : 0x150
- Message sortant : Activation/désactivation du chauffage/refroidissement.

Noeud Capteur de Vent :
- Message sortant CAN ID : 0x160
- Message sortant : Activation/désactivation de la protection contre le vent.

Noeud Capteur de Niveau d'Eau :
- Message sortant CAN ID : 0x170
- Message sortant : Commandes de pompage d'eau.

Noeud Batterie 1 :
- Message sortant CAN ID : 0x180
- Message sortant : État de charge (SOC) calculé de la batterie.

Noeud Batterie 2 :
- Message sortant CAN ID : 0x190
- Message sortant : État de charge (SOC) calculé de la batterie.

Noeud Panneaux Solaires 1 :
- Message sortant CAN ID : 0x1A0
- Message sortant : Mesure de la production d'énergie solaire (Watts).

Noeud Panneaux Solaires 2 :
- Message sortant CAN ID : 0x1B0
- Message sortant : Mesure de la production d'énergie solaire (Watts).

Noeud Capteur de Luminosité :
- Message sortant CAN ID : 0x1C0
- Message sortant : Activation/désactivation de l'éclairage extérieur.

Cette priorisation permet de s'assurer que les messages les plus critiques sont transmis avec des IDs plus faibles, assurant ainsi que les actions cruciales soient traitées en priorité dans le système.


## Évaluation

L'évaluation se fera de la manière suivante :
- Démonstrations : Chaque groupe effectuera des démonstrations régulières des fonctionnalités opérationnelles.
- Présentation Orale en Groupe : Chaque groupe présentera son travail, son noeud et son intégration dans le système.
- Séance de Questions/Réponses : Les enseignants et les étudiants poseront des questions sur les démonstrations et les présentations aux groupes et aux étudiants individuellement.
- Documentation : Les étudiants devront remettre une documentation minimale qui comprend une description des interfaces et une procédure de démarrage.

Les critères d'évaluation incluront la fonctionnalité du noeud, la qualité de la présentation, la capacité à répondre aux questions et la documentation fournie.

## Ressources

Pour réaliser ce projet, vous aurez besoin des ressources suivantes :
- Matériel : Cartes PIC18F25K80 ou Cartes ESP32 (selon le groupe), panneaux solaires, batterie, capteurs, onduleur, composants électroniques (MCP2551).
- Logiciels : Environnement de développement intégré (IDE) pour la programmation des PIC ou ESP.
- Documentation : Tutoriels sur la programmation des PIC et des ESP, documentation sur la communication CAN, notes de cours, recherches sur le Web, robots conversationnels

## Remarques Finales

Ce projet offre une occasion unique d'appliquer vos compétences en électronique programmable, en communication CAN et en gestion d'énergie. Travaillez en équipe, soyez créatifs et amusez-vous tout en développant un système de gestion d'énergie solaire autonome fonctionnel.

