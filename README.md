# Apache2 DDoS Protection avec Flask et iptables

### Description
Ce projet propose une solution simple de protection contre les attaques DDoS (Distributed Denial of Service) pour les serveurs **Apache2** sous Linux. Il analyse les logs d'Apache pour détecter les tentatives d'attaques DDoS en fonction du nombre de requêtes provenant d'une même IP. Une interface web permet de visualiser les attaques détectées, ainsi que les IP bloquées par iptables.

### Fonctionnalités
- **Surveillance des logs d'Apache2** : Le script analyse les logs d'Apache en temps réel pour détecter les requêtes abusives.
- **Blocage automatique via iptables** : Lorsqu'une IP dépasse un certain seuil de requêtes par minute, elle est bloquée via iptables.
- **Déblocage automatique** : Les IP sont débloquées après un certain temps pour permettre une reprise du service.
- **Interface web avec Flask** : Une interface web simple permet de consulter les attaques et les IP bloquées.
- **Design Bootstrap** : Utilisation de Bootstrap pour un design moderne et responsive.

### Prérequis
1. Serveur Linux avec Apache2 installé.
2. Python 3.x
3. Les bibliothèques Python suivantes :
   - Flask
   - iptc (pour iptables)
   - collections, threading, logging (modules Python intégrés)

Installez les dépendances avec :
```bash
pip install flask python-iptables
