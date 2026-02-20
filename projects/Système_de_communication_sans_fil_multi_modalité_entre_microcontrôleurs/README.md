# Système de communication sans fil multi-modalité entre microcontrôleurs

Projet réalisé dans le cadre du module *Introduction aux Microcontrôleurs* | CY Cergy Paris Université

## Description

Ce projet consiste à concevoir et implémenter un système de communication sans fil entre deux microcontrôleurs STM32F4 via transmission de signaux sonores encodés en Morse.

L’objectif est de mettre en œuvre les principaux périphériques matériels du microcontrôleur (ADC, PWM, UART, GPIO, interruptions) afin de créer un système de transmission fiable et extensible.

---

## Objectifs pédagogiques

- Maîtriser la configuration des périphériques STM32
- Implémenter une communication UART fiable
- Générer un signal sonore via PWM
- Acquérir et traiter un signal analogique via ADC
- Implémenter un encodage/décodage Morse
- Tester la robustesse du système en environnement bruité

---

## Technologies utilisées

- STM32F4 (Nucleo-F446RE)
- STM32CubeIDE
- STM32CubeMX
- Langage C
- UART
- PWM
- ADC
- GPIO
- Interruptions
- SWV Data Trace (debug)

---

## Architecture du système

### Microcontrôleur 1 (Émetteur)
1. Réception d’un message via UART (depuis PC)
2. Encodage en code Morse
3. Génération du signal sonore via PWM (buzzer)

### Microcontrôleur 2 (Récepteur)
1. Acquisition du signal sonore via microphone (ADC)
2. Traitement et décodage Morse
3. Transmission du message décodé via UART vers PC

---

## Matériel utilisé

- 2 cartes STM32F4 (Nucleo-F446RE)
- Breadboard
- Buzzers
- Module microphone MAX9814
- Boutons poussoirs
- Câbles USB
- Jumper wires

---

## Tests & Validation

### Test de communication
- Envoi d’un message court ("SOS")
- Vérification de la réception correcte sur le second PC
- Résultat : transmission conforme

### Test en environnement bruité
- Ajout d’un bruit de fond (musique / voix)
- Évaluation de la robustesse
- Résultat : résistance à un bruit modéré

---

## Améliorations futures

- Ajout d’un filtre passe-bande pour réduire les interférences
- Communication bidirectionnelle temps réel
- Transmission multi-modalité :
  - Morse sonore (buzzer)
  - Morse lumineux (LED infrarouge)

---

## Compétences développées

- Programmation embarquée en C
- Configuration avancée des périphériques STM32
- Gestion des interruptions
- Traitement du signal
- Debug embarqué
- Validation expérimentale
- Travail en équipe

---

## Équipe

- Ines Boukais
- Rachel Bakhouche
- Andrew Makuisa
- Dan Agossa
- Mario Razafinony
- Nelly Sautron

---

## Slides
[📄 Voir les Slides](Slides.pdf)

---

## Conclusion

Ce projet illustre l’utilisation des microcontrôleurs pour concevoir un système de communication embarqué modulaire, robuste et extensible.  
Il démontre la maîtrise des interactions bas niveau entre matériel et logiciel dans un contexte réel.
