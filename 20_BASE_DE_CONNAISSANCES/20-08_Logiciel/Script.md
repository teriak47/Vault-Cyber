---
tags:
  - outil
aliases:
  - Script informatique
  - Programme scripté
archetype: logiciel
site_web: 
cssclasses:
  - max
---

# Script (Programme scripté)

## 🎯 Objectif Principal
> Un script est une séquence de commandes ou d'instructions écrites dans un [[Programming|langage de programmation]] de script, conçue pour être exécutée par un interpréteur plutôt que d'être compilée en un exécutable autonome. Les scripts sont largement utilisés pour l'[[Automation|automatisation]] de tâches, l'administration de [[System|systèmes]] et le développement rapide de [[SoftwareApplication|logiciels]].

## ⚙️ Cas d'usage / Commandes Utiles

### Cas 1: Automatisation de tâches système
Description: Exécution d'un script shell pour automatiser des tâches récurrentes sur un [[OperatingSystem|système d'exploitation]] de type Unix/Linux (ex: sauvegardes, nettoyage de fichiers logs).
```bash
#!/bin/bash
# script_sauvegarde.sh
DATE=$(date +%Y%m%d)
tar -czf /var/backup/backup_$DATE.tar.gz /data/important
echo "Sauvegarde effectuée le $DATE"
```
Commande d'exécution:
```bash
chmod +x script_sauvegarde.sh
./script_sauvegarde.sh
```

### Cas 2: Exploitation de vulnérabilités
Description: Utilisation d'un [[Python]] script pour exploiter une [[Vulnerability|vulnérabilité]] dans une [[SoftwareApplication|application logicielle]], comme un [[CrossSiteScripting|XSS]] ou une injection [[SqlInjection|SQL]].
```python
# exploit_xss.py
import requests

target_url = "http://example.com/search"
payload = "<script>alert('XSS');</script>"
response = requests.get(target_url, params={"query": payload})

if payload in response.text:
    print("XSS détecté!")
else:
    print("Aucun XSS trouvé.")
```
Commande d'exécution:
```bash
python exploit_xss.py
```

## ⚠️ Points d'attention
*   **[[SecurityVulnerabilities|Vulnérabilités de sécurité]]**: Les scripts, s'ils ne sont pas correctement audités et sécurisés, peuvent introduire des [[Vulnerability|vulnérabilités]] dans un [[System|système]].
*   **Exécution de code arbitraire**: Les [[ThreatActor|acteurs de menace]] peuvent utiliser des scripts malveillants ([[Malware|logiciels malveillants]]) via des vecteurs comme le [[Phishing|hameçonnage]] ou les [[CrossSiteScripting|XSS]] pour exécuter du code à distance.
*   **Dépendances**: Les scripts peuvent dépendre de bibliothèques externes ou d'outils, ce qui peut créer une [[SoftwareSupplyChainSecurity|chaîne d'approvisionnement logicielle]] complexe et potentiellement vulnérable.
*   **Permission d'exécution**: Assurez-vous que les scripts exécutés ont le [[PrincipleOfLeastPrivilege|principe du moindre privilège]] appliqué.

## 🔗 Alternatives et Notes Connexes
*   Alternatives: [[SoftwareApplication|Application logicielle]], [[Programming|Programmation]], [[Automation|Automatisation]]
*   Contexte: [[Exploit|Exploit]], [[Vulnerability|Vulnérabilité]], [[Shellcode|Shellcode]], [[OperatingSystem|Système d'exploitation]]