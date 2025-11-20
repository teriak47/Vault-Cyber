---
tags:
  - logiciel
  - active-directory
  - politique/securite
  - gestion/acces
  - gestion/privileges
  - configuration
  - logiciel/windows
  - systeme/exploitation
  - controle/securite
  - gestion-centralisee
aliases:
  - Objet de Stratégie de Groupe
  - GPO
  - Group Policy Object
archetype: logiciel
version: 
cssclasses:
  - max
---

# Objet de Stratégie de Groupe (GPO)

## 🎯 Rôle et Fonction
> Un Objet de Stratégie de Groupe (GPO) est un ensemble de paramètres configurables qui contrôlent le comportement et la sécurité des ordinateurs et utilisateurs au sein d'un environnement Windows Active Directory. Les GPO sont le mécanisme principal pour la gestion centralisée des systèmes d'exploitation Windows, permettant aux administrateurs de définir des politiques de sécurité, des configurations logicielles, des scripts de démarrage/fermeture et bien plus encore, garantissant ainsi la conformité et la stabilité de l'entreprise.

## ⚙️ Configuration
Les GPO ne sont pas des fichiers de configuration texte traditionnels mais des objets stockés dans ActiveDirectory et des fichiers dans le partage SYSVOL.
*   **Emplacements clés**:
    *   **Conteneurs d'objets de stratégie de groupe** (GPT) dans ActiveDirectory (stocke les métadonnées et la version de la GPO).
    *   **Modèles de stratégie de groupe** (GPT) dans le partage SYSVOL (stocke les fichiers de configuration réels, comme les modèles d'administration).
*   **Outils de gestion**:
    *   Console de Gestion des Stratégies de Groupe (GPMC.msc)
    *   Éditeur de Stratégie de Groupe Local (gpedit.msc) pour les GPO locales.
*   **Dépendances**:
    *   ActiveDirectory (pour les GPO de domaine).
    *   Windows systèmes d'exploitation.

## 🔒 Sécurisation (Durcissement / Hardening)
La sécurisation des GPO est cruciale pour la sécurité globale de l'entreprise.
*   **Appliquer le principe du moindre privilège**: Limiter strictement qui peut créer, modifier ou lier des GPO. Les délégations de droits doivent être auditées et revues régulièrement.
*   **Contrôler l'accès aux GPO**: Restreindre l'accès en écriture au partage SYSVOL où les fichiers des GPO sont stockés. S'assurer que les groupes privilégiés ont seulement les droits nécessaires.
*   **Mettre en œuvre des paramètres de sécurité de mots de passe robustes**: Utiliser les GPO pour forcer des politiques de mots de passe complexes, le verrouillage de compte et l'expiration des mots de passe.
*   **Filtrage de sécurité des GPO**: Utiliser le filtrage de sécurité pour s'assurer que les GPO ne s'appliquent qu'aux ordinateurs et utilisateurs cibles, afin d'éviter les applications involontaires ou les conflits.
*   **Utiliser les GPO pour les contrôles de sécurité essentiels**: Déployer des configurations de pare-feu, logiciels antivirus, et d'autres paramètres de sécurité via GPO pour maintenir une posture de sécurité cohérente.

## 🔍 Audit et Surveillance
La surveillance des GPO est essentielle pour détecter les dérives de configuration et les changements malveillants.
*   **Logs importants**:
    *   Journaux d'événements de sécurité Windows (ID d'événements liés aux changements de GPO, échec d'application de GPO).
    *   Journaux des services de fichiers pour les modifications sur SYSVOL.
*   **Commandes d'audit**:
```bash
# Vérifier les GPO appliquées à l'ordinateur et à l'utilisateur
gpresult /r

# Vérifier l'état de la GPO et des informations de version (utilisé dans les scripts)
gpupdate /force

# Analyse de la configuration de sécurité effective via GPO (peut nécessiter des outils dédiés ou des scripts PowerShell)
Get-GPOReport -All -ReportType Html -Path "C:\temp\AllGPOs.html"
```
*   **Outils graphiques**:
    *   Console de Gestion des Stratégies de Groupe (GPMC.msc) pour l'analyse des résultats de stratégies et la modélisation.

## 🔗 Notes Connexes
*   **Concept parent**: ActiveDirectory
*   **Technologie associée**: Windows
*   **Principe de gestion**: Administration Centralisée
*   **Application de directives**: Politique de Sécurité
*   **Principe de sécurité**: Principe du Moindre Privilège