# Projet de Gestion d'Énergie Solaire Autonome pour la planète MARS

![image](https://github.com/cegep-electronique-programmable/CAN_gestion-energie-solaire/assets/5272111/8ac6260f-b47a-47df-9ae8-7f6ec530bfed)

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

- Noeud Panneaux Solaires :
  - Mesurer la production d'énergie solaire en Watts.
  - Utiliser un potentiomètre pour simuler la puissance générée.
  - Message sortant avec la puissance actuelle et moyenne.
  - Message sortant CAN ID : 0x1A0
  - Le noeud ne fonctionne que si le système est en fonctionnement (SYSTEME ACTIF)
  - Sinon, il passe en mode "PROTECTION"

- Noeud Batterie :
  - Mesurer l'état de charge (SOC) de la batterie en pourcentage (%).
  - Utiliser un potentiomètre pour simuler l'état de la charge.
  - Message sortant avec l'état de charge de la batterie et la tendance (charge ou décharge).
  - Message sortant CAN ID : 0x180
  - Le noeud ne fonctionne que si le système est en fonctionnement (SYSTEME ACTIF)

- Noeud Capteur de Température
  - Mesurer la température ambiante en degrés Celsius.
  - Utiliser un potentiomètre pour simuler la température.
  - Contrôler le chauffage et le refroidissement en fonction de la température.
  - Message sortant avec la température et l'état du système (chauffage, refroidissement ou arrêté)
  - Message sortant CAN ID : 0x140
  - Le noeud ne fonctionne que si le système est en fonctionnement (SYSTEME ACTIF)
    
- Noeud Onduleur :
  - Convertir l'énergie DC en AC et vice versa.
  - Utiliser un bouton à 2 positions pour simuler l'état de l'onduleur.
  - Message sortant indique si l'onduleur est actif.
  - Le noeud ne fonctionne que si le système est en fonctionnement (SYSTEME ACTIF) et qu'il reste de l'énergie dans la batterie.

- Noeud Capteur de Vent :
  - Mesurer la vitesse du vent en mètres par seconde.
  - Utiliser un potentiomètre pour simuler la vitesse du vent.
  - Message sortant avec la vitesse du vent et l'état du système de protection.
  - Le noeud fonctionne en permanence
  - Message sortant CAN ID : 0x160

- Noeud Interface Utilisateur (Utilisation d'ESP) :
  - Développer une interface utilisateur pour surveiller et contrôler le système.
  - Afficher les données des autres noeuds (panneaux solaires, batterie, température, vent, onduleur).
  - Permettre le contrôle global du système via CAN.
  - Si le système de protection contre le vent est activé, il doit arrêté le système (SYSTEME INACTIF).
  - 
  - Message sortant CAN ID : 0x120

Chaque groupe devra concevoir, développer et intégrer son propre noeud dans le système global de gestion d'énergie solaire autonome.
Tous les groupes devront participer à l'intégration de leur noeud dans le système.

### ID des messages


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

