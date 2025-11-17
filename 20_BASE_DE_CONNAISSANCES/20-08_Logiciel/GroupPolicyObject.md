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
> Un [[GroupPolicyObject|Objet de Stratégie de Groupe]] (GPO) est un ensemble de paramètres configurables qui contrôlent le comportement et la sécurité des [[Computer|ordinateurs]] et [[User|utilisateurs]] au sein d'un environnement [[Windows]] [[ActiveDirectory|Active Directory]]. Les GPO sont le mécanisme principal pour la [[CentralizedAdministration|gestion centralisée]] des [[OperatingSystem|systèmes d'exploitation]] Windows, permettant aux administrateurs de définir des politiques de [[Security|sécurité]], des configurations [[Software|logicielles]], des scripts de démarrage/fermeture et bien plus encore, garantissant ainsi la conformité et la stabilité de l'[[EnterpriseNetwork|entreprise]].

## ⚙️ Configuration
Les GPO ne sont pas des fichiers de configuration texte traditionnels mais des objets stockés dans [[ActiveDirectory]] et des fichiers dans le partage SYSVOL.
*   **Emplacements clés**:
    *   **Conteneurs d'objets de stratégie de groupe** (GPT) dans [[ActiveDirectory]] (stocke les métadonnées et la version de la GPO).
    *   **Modèles de stratégie de groupe** (GPT) dans le partage SYSVOL (stocke les fichiers de configuration réels, comme les modèles d'administration).
*   **Outils de gestion**:
    *   Console de Gestion des Stratégies de Groupe (GPMC.msc)
    *   Éditeur de Stratégie de Groupe Local (gpedit.msc) pour les GPO locales.
*   **Dépendances**:
    *   [[ActiveDirectory]] (pour les GPO de domaine).
    *   [[Windows]] [[OperatingSystem|systèmes d'exploitation]].

## 🔒 Sécurisation (Durcissement / Hardening)
La sécurisation des GPO est cruciale pour la [[Security|sécurité]] globale de l'[[Enterprise|entreprise]].
*   **Appliquer le [[PrincipleOfLeastPrivilege|principe du moindre privilège]]**: Limiter strictement qui peut créer, modifier ou lier des GPO. Les délégations de droits doivent être auditées et revues régulièrement.
*   **Contrôler l'accès aux GPO**: Restreindre l'accès en écriture au partage SYSVOL où les fichiers des GPO sont stockés. S'assurer que les groupes privilégiés ont seulement les droits nécessaires.
*   **Mettre en œuvre des paramètres de [[StrongPasswordPolicy|sécurité de mots de passe]] robustes**: Utiliser les GPO pour forcer des politiques de [[Password|mots de passe]] complexes, le [[AccountLockout|verrouillage de compte]] et l'expiration des mots de passe.
*   **Filtrage de sécurité des GPO**: Utiliser le filtrage de [[Security|sécurité]] pour s'assurer que les GPO ne s'appliquent qu'aux [[Computer|ordinateurs]] et [[User|utilisateurs]] cibles, afin d'éviter les applications involontaires ou les conflits.
*   **Utiliser les GPO pour les [[SecurityControl|contrôles de sécurité]] essentiels**: Déployer des configurations de [[Firewall|pare-feu]], [[Antivirus|logiciels antivirus]], et d'autres paramètres de [[Security|sécurité]] via GPO pour maintenir une posture de [[Security|sécurité]] cohérente.

## 🔍 Audit et Surveillance
La surveillance des GPO est essentielle pour détecter les [[ConfigurationDrift|dérives de configuration]] et les changements malveillants.
*   **Logs importants**:
    *   Journaux d'événements de [[Security|sécurité]] Windows (ID d'événements liés aux changements de GPO, échec d'application de GPO).
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
*   **Concept parent**: [[ActiveDirectory]]
*   **Technologie associée**: [[Windows]]
*   **Principe de gestion**: [[CentralizedAdministration|Administration Centralisée]]
*   **Application de directives**: [[SecurityPolicy|Politique de Sécurité]]
*   **Principe de sécurité**: [[PrincipleOfLeastPrivilege|Principe du Moindre Privilège]]