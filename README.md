<div align="center">

<a href="https://github.com/0xCyberLiTech">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=32&pause=1000&color=D14A4A&center=true&vCenter=true&width=650&lines=SUPERVISION+AVEC+CHECKMK+OMD;Installation+%26+Configuration;Tutoriels+%26+Fichiers+d'Exemple" alt="Typing SVG" />
</a>

<p align="center">
  <em>Tutoriels et configurations pour la supervision avec Checkmk OMD.</em><br>
  <b>📊 Monitoring – 📈 Performance – ⚙️ Fiabilité</b>
</p>

</div>

---

### 👨‍💻 **À propos de moi.**

> Bienvenue dans mon **laboratoire numérique personnel** dédié à l’apprentissage et à la vulgarisation de la cybersécurité.  
> Passionné par **Linux**, la **cryptographie** et les **systèmes sécurisés**, je partage ici mes notes, expérimentations et fiches pratiques.  
>  
> 🎯 **Objectif :** proposer un contenu clair, structuré et accessible pour étudiants, curieux et professionnels de l’IT.  
> 🔗 [Mon GitHub principal](https://github.com/0xCyberLiTech)

<p align="center">
  <a href="https://skillicons.dev">
    <img src="https://skillicons.dev/icons?i=linux,debian,bash,docker,nginx,git,vim" alt="Skills" />
  </a>
</p>

[![🔗 Profil GitHub](https://img.shields.io/badge/Profil-GitHub-181717?logo=github&style=flat-square)](https://github.com/0xCyberLiTech)
[![📦 Dernière version](https://img.shields.io/github/v/release/0xCyberLiTech/Checkmk?label=version&style=flat-square&color=blue)](https://github.com/0xCyberLiTech/Checkmk/releases/latest)
[![📄 CHANGELOG](https://img.shields.io/badge/📄%20Changelog-Checkmk-blue?style=flat-square)](https://github.com/0xCyberLiTech/Checkmk/blob/main/CHANGELOG.md)
[![📂 Dépôts publics](https://img.shields.io/badge/Dépôts-publics-blue?style=flat-square)](https://github.com/0xCyberLiTech?tab=repositories)
[![👥 Contributeurs](https://img.shields.io/badge/👥%20Contributeurs-cliquez%20ici-007ec6?style=flat-square)](https://github.com/0xCyberLiTech/Checkmk/graphs/contributors)

---

### 🎯 **Objectif de ce dépôt.**

> Ce dépôt a pour vocation de centraliser un ensemble de notions clés en supervision informatique. Il s’adresse aux passionnés, étudiants et professionnels souhaitant mieux comprendre les enjeux de la
> surveillance des systèmes d'information, apprendre à mettre en place des outils de monitoring efficaces et se familiariser avec les concepts et bonnes pratiques pour maintenir la performance et la stabilité de
> leurs environnements IT.

---

### 🧭 **Sommaire :**

---

<div align="center" style="margin-bottom: 10px;">

Légende des couleurs des boutons :

🟢 **Actif** – Dépôt totalement accessible  
🟠 **Partiel** – Dépôt partiellement accessible  
🔴 **Inactif** – Dépôt inaccessible ou indisponible

</div>

---

<div align="center">

| Catégorie | Sujet | Accès Rapide |
|:---:|:---|:---:|
| **Tuto** | Installation de checkmk OMD | [<img src="https://img.shields.io/badge/EXPLORER-red?style=for-the-badge&logo=github&logoColor=white">]() |
| **Tuto** | Configuration de checkmk OMD | [<img src="https://img.shields.io/badge/EXPLORER-red?style=for-the-badge&logo=github&logoColor=white">]() |
| **Tuto** | Configuration d'un dashboard sur checkmk OMD | [<img src="https://img.shields.io/badge/EXPLORER-red?style=for-the-badge&logo=github&logoColor=white">]() |

</div>

---

# 🔍 Checkmk / OMD – Présentation

**Checkmk** est une **solution de supervision IT** puissante et modulaire, utilisée pour surveiller des systèmes, réseaux, applications et infrastructures cloud. Elle est conçue pour offrir **des performances élevées**, une **installation simplifiée** et une **visualisation claire** de l'état de vos systèmes.

**OMD** (Open Monitoring Distribution) est l’environnement dans lequel **Checkmk** (et d’autres outils de supervision) s’exécutent. Il fournit une structure packagée pour installer, gérer et faire fonctionner Checkmk facilement, avec tous ses composants intégrés.

---

## 🧩 Composants clés d’une instance Checkmk OMD

Une instance OMD contient :

- **Checkmk Core** (CMC ou Nagios Core) : moteur de supervision.  
- **Livestatus** : interface rapide pour interroger l'état des services.  
- **Web GUI (Multisite)** : interface web centralisée de configuration et de visualisation.  
- **RRDTool ou Graphite** : pour les graphes de performance.  
- **Apache intégré** : serveur web préconfiguré pour l’accès à l’interface.  
- **NagVis** : cartes personnalisées (en option).  
- **MK Livestatus** : interface socket pour outils externes.  

---

## 🚀 Fonctionnalités de Checkmk via OMD

- Découverte automatique des services et hôtes.
- Surveillance des ressources système (CPU, RAM, disques, processus).
- Supervision réseau (ping, ports, SNMP, etc.).
- Prise en charge d’agents Checkmk sur hôtes surveillés.
- Supervision distribuée (remote sites, via agents ou SNMP).
- Gestion des alertes (e-mail, webhook, scripts…).
- Extensible via des **plug-ins** et des **scripts personnalisés**.
- Support des conteneurs, du cloud, de Kubernetes, etc.

---

## 🛠️ Avantages d’OMD avec Checkmk

- **Installation rapide** : tout-en-un dans une instance OMD.
- **Isolation par instance** : chaque instance a son propre environnement (utile pour tests, production, etc.).
- **Facilité de mise à jour** : possibilité de migrer d’une version à l’autre.
- **Simplicité de gestion** : via la CLI `omd` (start/stop/status/update/backup…).

---

## 📦 Exemple de commandes OMD

```bash
omd create monsite      # Crée une nouvelle instance Checkmk
omd start monsite       # Démarre l’instance
omd stop monsite        # Stoppe l’instance
omd update monsite      # Met à jour vers une nouvelle version de Checkmk
omd status monsite      # Affiche le statut des services de l’instance
```

---

## 📚 Versions de Checkmk

Checkmk est disponible en plusieurs éditions :

- **Raw Edition (CRE)** – gratuite, open source, basée sur Nagios Core.  
- **Enterprise Edition (CEE)** – version commerciale avec CMC, haute performance, et plus de fonctionnalités (graphes, alerting avancé, reporting…).  
- **Managed Services Edition (CME)** – pour les MSPs, avec gestion multi-clients.

---

<p align="center">
  <b>🔒 Un guide proposé par <a href="https://github.com/0xCyberLiTech">0xCyberLiTech</a> • Pour des tutoriels accessibles à tous. 🔒</b>
</p>
