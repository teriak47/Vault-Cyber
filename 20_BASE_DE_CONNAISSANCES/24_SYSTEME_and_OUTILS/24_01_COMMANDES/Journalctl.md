---
aliases:
  - journalctl
  - systemd logs
  - journal du système
  - system journal
  - logs systemd
  - journaux système
archetype: commandes
outil: journalctl
cssclasses:
  - max
tags:
  - commande
  - journalctl
  - administration/systeme
  - distribution/gnu-linux
  - log/gestion
  - filtrage
  - systemd
---

# Cheat Sheet : Journalctl

> [!tip] One-Liner Magique
> Afficher les logs du service Apache en temps réel, filtrés par les 10 dernières lignes et en couleur :
> `journalctl -u apache2.service -f -n 10 --color`

## 📜 Commandes Essentielles

| Action | Commande | Description |
|---|---|---|
| **Afficher tous les logs** | `journalctl` | Affiche tous les messages du journal, du plus ancien au plus récent. |
| **Afficher les logs les plus récents** | `journalctl -r` | Affiche les messages du journal dans l'ordre inverse (les plus récents en premier). |
| **Afficher les logs en temps réel** | `journalctl -f` | Suit les messages du journal en temps réel (comme `tail -f`). |
| **Afficher les logs du boot actuel** | `journalctl -b` | Affiche les logs depuis le dernier démarrage du système. |
| **Afficher les logs d'un boot précédent** | `journalctl -b -1` | Affiche les logs du démarrage précédent ( `-2` pour l'avant-dernier, etc.). |
| **Lister les boots disponibles** | `journalctl --list-boots` | Liste tous les identifiants de démarrage disponibles et leurs horodatages. |
| **Vérifier l'espace disque utilisé** | `journalctl --disk-usage` | Affiche la taille totale des fichiers journaux persistants. |

## 🔧 Options Avancées

*   `-u <UNIT>` ou `--unit=<UNIT>` : Filtrer les logs par unité `systemd` (ex: `nginx.service`, `user@1000.service`).
*   `-p <PRIORITY>` ou `--priority=<PRIORITY>` : Filtrer par niveau de priorité (0=emerg, 1=alert, ..., 7=debug). Peut être un chiffre ou un nom.
*   `--since=<DATE_TIME>` : Afficher les logs à partir d'une date/heure spécifique. (ex: "2023-11-25 08:00:00", "yesterday", "-1h").
*   `--until=<DATE_TIME>` : Afficher les logs jusqu'à une date/heure spécifique.
*   `-k` ou `--dmesg` : Affiche uniquement les messages du noyau (équivalent à `dmesg`).
*   `--no-hostname` : Ne pas afficher le nom d'hôte dans la sortie.
*   `-o <FORMAT>` ou `--output=<FORMAT>` : Change le format de sortie (ex: `short`, `verbose`, `json`, `json-pretty`, `export`, `cat`).
*   `-n <LINES>` ou `--lines=<LINES>` : Affiche les `N` dernières lignes (par défaut 10 si utilisé avec `-f`).
*   `--output-fields=<FIELDS>` : Limite les champs affichés pour les formats `json` et `export`.

## 📝 Exemples de Scripts / Pipelines

```bash
# Afficher les logs du service Nginx en temps réel
journalctl -u nginx.service -f

# Afficher les logs du service SSH depuis hier
journalctl -u sshd.service --since "yesterday"

# Afficher les logs du noyau (kernel) avec une priorité d'erreur ou plus élevée
journalctl -k -p err

# Afficher les logs avec une priorité 'warning' ou supérieure depuis les 30 dernières minutes
journalctl -p warning --since "-30min"

# Afficher tous les messages d'erreur du système
journalctl -p err

# Afficher les logs d'un utilisateur spécifique (ID 1000)
journalctl _UID=1000

# Exporter tous les logs du boot actuel au format JSON lisible
journalctl -b -o json-pretty > boot_logs.json

# Exporter les logs du service Docker des 2 dernières heures au format "export" (binaire)
journalctl -u docker.service --since "-2h" -o export > docker_logs_export

# Afficher les 20 dernières lignes des logs du service UFW (pare-feu)
journalctl -u ufw.service -n 20

# Filtrer les logs pour un chemin exécutable spécifique
journalctl _EXE=/usr/lib/systemd/systemd

# Afficher les logs d'un processus avec un PID spécifique
journalctl _PID=1234

# Combiner le filtrage par unité et priorité, puis les exporter au format texte brut
journalctl -u apache2.service -p warning --since "2023-01-01" --until "2023-01-31" -o cat > apache_warnings_january.txt
```