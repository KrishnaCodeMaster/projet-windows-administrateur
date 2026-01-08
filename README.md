# 🏢 Projet Infrastructure Active Directory Multi-Sites

## 📋 Vue d'ensemble

Déploiement d'une infrastructure Active Directory enterprise-grade avec réplication multi-sites, gestion centralisée des stratégies de groupe (GPO) et haute disponibilité.

### 🎯 Objectifs du projet
- Architecture Active Directory distribuée sur 3 sites géographiques (France, Pologne, Chine)
- Réplication intelligente avec contrôleur RODC (Read-Only Domain Controller)
- Automatisation des déploiements via GPO
- Sécurisation et standardisation des environnements utilisateurs

---

## 🏗️ Architecture technique

### Infrastructure réseau
```
pastascaduta.lan
├── 🇫🇷 Site France (AD-PARIS)     → Contrôleur principal
├── 🇵🇱 Site Pologne (AD-POLOGNE)  → Contrôleur secondaire  
└── 🇨🇳 Site Chine (RODC-CHINE)    → Contrôleur lecture seule
```

### Technologies utilisées
- **Active Directory Domain Services (AD DS)** - Administration centralisée
- **DNS** - Résolution de noms et équilibrage de charge
- **Group Policy Objects (GPO)** - Déploiement automatisé
- **IIS** - Serveur web multi-sites
- **Windows Server 2025** - Infrastructure système

---

## ⚙️ Composants implémentés

### 1. Configuration Active Directory
- ✅ Création du domaine `pastascaduta.lan`
- ✅ Déploiement de 3 contrôleurs de domaine
- ✅ RODC configuré pour le site distant (Chine)
- ✅ Réplication des mots de passe sécurisée

### 2. Topologie de sites
- ✅ 3 sites AD distincts avec liens inter-sites
- ✅ Coûts de réplication optimisés (400)
- ✅ Planification horaire (20h-6h)
- ✅ Intervalle de réplication : 180 minutes

### 3. Stratégies de groupe (GPO)

#### 🔐 Sécurité
- **Politique de mots de passe renforcée**
  - Complexité obligatoire
  - Durée de vie : 30 jours (utilisateurs) / 0 jours (IT)
  - Longueur minimale : 8 caractères

#### 📦 Déploiement d'applications
- Installation automatique de **7-Zip** (via MSI)
- Suggestion d'installation de **Notepad++**

#### 🎨 Standardisation environnement
- Fond d'écran commun déployé automatiquement
- Mappage réseau automatique (lecteur A:)

#### 🛡️ Restrictions de sécurité
- Désactivation de l'invite de commande (sauf groupe IT)
- Blocage du Panneau de configuration (sauf groupe IT)
- Filtrage de sécurité différencié par groupe

### 4. Services DNS
- ✅ Zones de recherche configurées
- ✅ Équilibrage de charge round-robin
- ✅ Enregistrements A pour les contrôleurs principaux

---

## 💡 Points forts du projet

### 🎓 Compétences démontrées

#### Architecture système
- Conception d'infrastructure distribuée multi-sites
- Gestion de la haute disponibilité et tolérance aux pannes
- Optimisation de la topologie réseau

#### Administration Windows Server
- Déploiement et configuration Active Directory
- Maîtrise des GPO et stratégies de sécurité
- Gestion des rôles FSMO et réplication

#### Sécurité informatique
- Implémentation RODC pour sites distants
- Politiques de mots de passe conformes aux standards
- Ségrégation des privilèges (utilisateurs vs IT)

#### Automatisation
- Déploiement centralisé d'applications
- Configuration standardisée des postes
- Gestion des accès et permissions

---

## 📊 Statistiques du projet

| Métrique | Valeur |
|----------|--------|
| **Serveurs déployés** | 3 |
| **GPO configurées** | 6 |
| **Sites AD** | 3 |
| **Utilisateurs types** | 2 groupes (Standard/IT) |
| **Liens de réplication** | 3 (FR-PL, FR-CN, PL-CN) |

---

## 🚧 Perspectives d'amélioration

### Objectifs techniques non finalisés
- **VPN site-à-site** : Configuration avancée en cours
- **IIS multi-sites** : Binding DNS à finaliser
- **Certificats SSL** : Sécurisation HTTPS

### Prochaines étapes
1. Finaliser la configuration VPN PPTP/L2TP
2. Implémenter HTTPS sur IIS avec certificats
3. Déployer WSUS pour gestion centralisée des mises à jour
4. Mettre en place la sauvegarde automatisée AD

---

## 🎯 Cas d'usage professionnel

Cette architecture répond aux besoins d'entreprises :
- **Multi-sites géographiques** avec connexions WAN limitées
- **Environnements sécurisés** nécessitant contrôle centralisé
- **Déploiements standardisés** sur parc informatique étendu
- **Conformité réglementaire** avec traçabilité des accès

---

## 📝 Note sur le développement

Projet réalisé en solo dans un contexte de charge de travail importante. Démontre la capacité à :
- Gérer un projet technique complexe de manière autonome
- Prioriser les fonctionnalités critiques
- Documenter les limitations techniques rencontrées
- Maintenir un niveau de qualité professionnel malgré les contraintes

---

## 🔗 Documentation technique

Pour plus de détails sur l'implémentation, consulter le document PDF joint avec captures d'écran des configurations.

---

**Technologies** : Active Directory • Windows Server 2025 • DNS • GPO • PowerShell • IIS • Virtualisation  
**Compétences** : Administration système • Architecture réseau • Sécurité • Automatisation
