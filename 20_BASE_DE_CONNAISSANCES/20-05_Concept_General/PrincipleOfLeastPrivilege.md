---
aliases:
  - Principe du Moindre Privilège
  - Principle of Least Privilege
archetype: concept-general
source:
  - 
cssclasses:
  - max
---

# Principe du Moindre Privilège

## 📥 Définition en une phrase
> Le Principe du Moindre Privilège est un [[SecurityControl|contrôle de sécurité]] fondamental qui stipule qu'un [[Account|utilisateur]], un programme ou un processus ne doit disposer que des privilèges minimum nécessaires pour accomplir sa tâche spécifique et rien de plus.

## 🧠 Concepts Clés / Piliers
*   **Minimisation des Droits**: Accorder uniquement les [[Authorization|autorisations]] essentielles pour la fonction requise, réduisant ainsi la [[AttackSurface|surface d'attaque]] et les dommages potentiels en cas de [[SystemCompromise|compromission du système]].
*   **Accès Juste-à-Temps (JIT)**: Les privilèges élevés ne sont accordés que pour la durée nécessaire à l'exécution d'une tâche spécifique et sont révoqués immédiatement après.
*   **Séparation des Tâches**: Diviser les responsabilités pour s'assurer qu'aucune seule entité ne possède tous les privilèges nécessaires pour exécuter une [[Task|tâche]] complète ou critique, réduisant le risque de fraude ou d'erreur.

## 💡 Importance en Cybersécurité
> Ce principe est vital pour la [[Cybersecurity|cybersécurité]] car il limite l'étendue des dommages qu'une [[ThreatActor|menace]] ou un [[Malware|logiciel malveillant]] peut causer s'il parvient à obtenir l'[[UnauthorizedAccess|accès non autorisé]] à un [[System|système]] ou à une [[Resource|ressource]]. En restreignant les privilèges, il diminue la probabilité de [[DataBreach|fuites de données]], de [[PrivilegeEscalation|d'escalade de privilèges]] et la propagation d'[[Attack|attaques]] au sein d'un [[EnterpriseNetwork|réseau d'entreprise]]. Il incarne une approche proactive de la [[SecurityByDesign|sécurité dès la conception]].

## 🔗 Notes Connexes
*   [[AccessControl|Contrôle d'accès]]
*   [[Authorization|Autorisation]]
*   [[PrivilegeEscalation|Escalade de Privilèges]]
*   [[SecurityByDesign|Sécurité dès la conception]]
*   [[Threat|Menace]]