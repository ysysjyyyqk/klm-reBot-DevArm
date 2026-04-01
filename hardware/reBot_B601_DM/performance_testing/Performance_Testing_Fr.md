# 🧪 Référence de Test de Performance Physique reBot-DevArm

<p align="center">
  <img src="./images/v1.0.png" alt="reBot-DevArm Banner">
</p>

<p align="center">
  <strong>
    <a href="./Performance_Testing_zh.md">简体中文</a> &nbsp;|&nbsp;
    <a href="./Performance_Testing.md">English</a> &nbsp;|&nbsp;
    <a href="./Performance_Testing_JP.md">日本語</a>&nbsp;|&nbsp;
    <a href="./Performance_Testing_Fr.md">français</a>&nbsp;|&nbsp;
    <a href="./Performance_Testing_es.md">Español</a>
  </strong>
</p>

> [!NOTE]
> Ce document fournit des données de référence de test de performance pour le bras robotique reBot Arm B601-DM dans des conditions de travail normales et extrêmes.

> [!WARNING]
> **Avis de Différence de Version**: Ce test est basé sur le reBot Arm B601-DM équipé de **moteurs Damiao version V4**. **Les versions V3 et antérieures des moteurs présentent des différences de performance**. Les données de test sont fournies à titre indicatif ; veuillez vérifier les performances réelles par des tests.

---

## 💡 Résumé Rapide

**Raison d'Arrêt des Tests**: Tous les tests ont été arrêtés en raison de la **protection contre la surchauffe du moteur 2 (articulation du bras supérieur)**, et non d'une défaillance de la structure mécanique.

**Test de Mouvement Dynamique** (Durée d'un cycle de mouvement : 5s standard, mouvement de va-et-vient) :

| Plage de Portée | Charge | Durée | Raison d'Arrêt |
|----------|------|----------|----------|
| 5%~70% de la Portée Nominale | 1.5 kg | > 2 h | Température du moteur 2 à 90℃ |
| 5%~70% de la Portée Nominale | 2.5 kg | 40 min | Protection contre la surchauffe du moteur 2 |
| 5%~100% de la Portée Nominale | 1.5 kg | 45 min | Protection contre la surchauffe du moteur 2 |

**Test de Maintien Statique**:

| Position de Portée | Charge | Durée | Raison d'Arrêt |
|----------|------|----------|----------|
| 70% de la Portée Nominale | 1.5 kg | 18 min | Protection contre la surchauffe du moteur 2 |
| 100% de la Portée Nominale | 1.5 kg | 3 min | Protection contre la surchauffe du moteur 2 |

> 👉 **Conclusion Clé**: La résistance structurelle du manipulateur est suffisante. L'arrêt des tests était dû à la **protection contre la surchauffe du moteur 2**. La charge de travail recommandée est de **1.5 kg ou moins**, la portée de travail recommandée est **inférieure à 70%**, et il est conseillé d'ajouter des mesures de refroidissement actif.

---

## 📋 Table des Matières

- [⚡ Test de Performance en Conditions Extrêmes](#-test-de-performance-en-conditions-extrêmes)
- [📈 Courbe de Charge Officielle](#-courbe-de-charge-officielle)
- [📝 Conclusions et Recommandations](#-conclusions-et-recommandations)
- [🙋 Questions Fréquemment Posées (FAQ)](#-questions-fréquemment-posées-faq)
- [📅 Historique des Mises à Jour](#-historique-des-mises-à-jour)
- [📞 Support Technique](#-support-technique)

---

## ⚡ Test de Performance en Conditions Extrêmes

### Conditions de Test

**Test de Mouvement Dynamique**:
- Durée d'un cycle de mouvement : 5 s
- Mode de mouvement : Mouvement de va-et-vient
- Plage de portée de test : 5%~70% / 5%~100% de la portée nominale

**Test de Maintien Statique**:
- Position de test : Maintien de charge en position statique
- Portée de test : 70% / 100% de la portée nominale

### Résultats des Tests

#### 1. Test de Mouvement Dynamique

| Position de Test | Charge (kg) | Durée Maximale | Raison d'Arrêt |
|----------|-----------|--------------|----------|
| Portée 5%~70% | 1.5 | > 2 h | Protection contre la surchauffe du moteur 2 |
| Portée 5%~70% | 2.5 | 40 min | Protection contre la surchauffe du moteur 2 |
| Portée 5%~100% | 1.5 | 45 min | Protection contre la surchauffe du moteur 2 |

#### 2. Test de Maintien Statique

| Position de Test | Charge (kg) | Durée Maximale | Raison d'Arrêt |
|----------|-----------|--------------|----------|
| Portée 70% | 1.5 | 18 min | Protection contre la surchauffe du moteur 2 |
| Portée 100% | 1.5 | 3 min | Protection contre la surchauffe du moteur 2 |

---

## 📈 Courbe de Charge Officielle

![Courbe de Charge 12Nm](./images/12Nm.png)

<p align="center">Courbe de Charge du Moteur Série Damiao 43 Version 12Nm</p>

---

## 📝 Conclusions et Recommandations

### Recommandations d'Utilisation

1. **Conditions de Travail Recommandées**
   - Charge : < 1.5 kg
   - Rayon de travail : < 70% de la portée (450 mm)
   - Vitesse de mouvement : < 70% de la vitesse maximale
   - Température ambiante : 15 °C ~ 35 °C

2. **Recommandations de Refroidissement**
   - Lors d'un travail prolongé sous charge élevée, il est recommandé d'ajouter un refroidissement actif
   - Après 2 heures de travail continu, une pause de 10~15 minutes est recommandée
   - Évitez l'exposition directe au soleil et l'utilisation dans des espaces fermés

---

## 🙋 Questions Fréquemment Posées (FAQ)

<details>
<summary><b>Q1 : Les performances du manipulateur diminuent-elles dans des environnements à haute température ?</b></summary>

Oui. Lorsque la température ambiante dépasse 35 °C ou que la température du moteur dépasse 75 °C, il est recommandé de réduire la charge et la vitesse de mouvement pour garantir la précision et la durée de vie. L'utilisation continue à haute température n'est pas recommandée.

</details>

<details>
<summary><b>Q2 : Les données de test sont-elles applicables à toutes les versions ?</b></summary>

Ce test est basé sur le reBot Arm B601-DM équipé de **moteurs Damiao version V4**. **Les versions V3 et antérieures des moteurs présentent des différences de performance**, les données de test sont donc fournies à titre indicatif.

</details>

---

## 📅 Historique des Mises à Jour

| Version | Date | Contenu de la Mise à Jour | Auteur |
|------|------|----------|------|
| v1.0 | 2026.04.01 | Version initiale, publication des données de test de performance de base | SeeedStudio AI Robotics Team |

---

## 📞 Support Technique

Si vous avez des questions relatives aux tests de performance, n'hésitez pas à nous contacter :

- **Support Technique**: yaohui.zhu@seeed.cc
- **Discord**: [Rejoindre la Communauté](https://discord.gg/AbGuqJhDpQ)
- **Wiki**: [Consulter la Base de Connaissances](https://wiki.seeedstudio.com/robotics_page/)

---

<p align="center">
  <strong>🤖 reBot-DevArm - Manipulateur Open Source pour Chaque Développeur</strong>
</p>
