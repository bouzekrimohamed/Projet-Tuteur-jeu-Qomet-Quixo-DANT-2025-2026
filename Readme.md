# DANT 2025–2026 — Projet tuteuré : QOMET / QUIXO

Logiciel de jeu permettant de jouer à **QOMET** (et optionnellement **QUIXO**) avec :
- **Mode local** (1v1 sur la même machine)
- **Mode réseau** (1v1 en ligne)
- **IA** (jouer contre l’ordinateur)
- **Interface graphique moderne** (thèmes / skins)
- (Optionnel) **Monétisation / gains** (à cadrer selon contraintes pédagogiques)

> Projet réalisé dans le cadre de l’UE **DANT 2025–2026**.

---

## Table des matières
- [Objectifs](#objectifs)
- [Fonctionnalités](#fonctionnalités)
- [Périmètre](#périmètre)
- [Technos envisagées](#technos-envisagées)
- [Architecture (proposition)](#architecture-proposition)
- [Installation](#installation)
- [Utilisation](#utilisation)
- [Réseau (proposition)](#réseau-proposition)
- [IA (proposition)](#ia-proposition)
- [Tests & qualité](#tests--qualité)
- [Gestion de projet](#gestion-de-projet)
- [Roadmap](#roadmap)
- [Auteurs](#auteurs)

---

## Objectifs
Développer une application **desktop** (Windows / Linux ?) proposant le jeu **QOMET** avec une UX moderne :
- interactions simples : **cliquer** / **glisser** pour déplacer,
- affichage clair de l’état du jeu,
- parties rapides et fluides,
- ajout progressif d’options (réseau, IA, thèmes…).

---

## Fonctionnalités

### Must-have (MVP)
- [ ] Moteur de règles complet **QOMET**
- [ ] Partie locale (2 joueurs)
- [ ] Interface graphique : plateau, pièces, tour par tour, reset, fin de partie
- [ ] Déplacements via **clic + glisser** (ou clics successifs)
- [ ] Journal des coups / historique simple

### Options demandées (à prioriser)
- [ ] **Jouer en réseau** (1v1)
- [ ] **Jouer contre une IA**
- [ ] **Interface moderne** + **plusieurs thèmes**
- [ ] **Jouer aussi à QUIXO** (mode séparé)
- [ ] (Optionnel) “Me faire gagner de l’argent” : **à définir** (modèle, contraintes, faisabilité)

### Bonus UX / Produit
- [ ] Menu principal (Local / Online / IA / Paramètres)
- [ ] Paramètres : thème, sons, pseudo, affichage
- [ ] Rejouer / sauvegarde des parties (optionnel)

---

## Périmètre
Le projet est découpé en **lots** pour sécuriser la livraison :

1. **MVP QOMET local** (règles + UI + interactions)  
2. **IA** (au moins un niveau simple, puis amélioration)  
3. **Réseau** (invitation + création/join de partie)  
4. **Thèmes / polish**  
5. **QUIXO** (si temps OK)  
6. **Monétisation** (uniquement si autorisé + cadré)

---

## Technos envisagées
D’après les notes :
- **Unity** (recommandé pour GUI moderne + export Windows/Linux)
- ou **Panda3D** (si orientation Python/3D)

> Décision finale à prendre au début du projet (impact direct sur réseau, UI, build, tests).

---

## Architecture (proposition)
Séparer strictement la logique de jeu de l’interface.

- **core/**  
  - règles QOMET (plateau, coups valides, victoire, etc.)
  - gestion du tour / état de partie
- **ui/**  
  - affichage, animations, drag & drop, menus, thèmes
- **ai/**  
  - IA niveau 1 (heuristique simple)
  - IA niveau 2 (minimax + élagage, si possible)
- **net/**  
  - création/join de partie
  - synchronisation des coups
  - lobby / invitation (email ou code)
- **tests/**  
  - tests unitaires des règles (coups valides, conditions victoire…)

---

## Installation

............a venirrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrrr