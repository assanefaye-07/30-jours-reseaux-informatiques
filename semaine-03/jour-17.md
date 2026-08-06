# Jour 17 — Monitoring réseau
 
📅 Date : 06/08/2026
⏱️ Temps passé : ~45 min
🎯 Charge de travail : Intense
 
## 📺 Support suivi
- Vidéo : 3:31:02 → 3:55:10 (Analyzing Monitoring Reports + Network Monitoring parties 1&2)
- Lien direct : https://youtu.be/qiQR5rTSshw?t=12662
## 🧠 Ce que j'ai appris
<!-- Résume avec tes propres mots -->
- Les baselines (les référentiels de performance) CPU, bande passante, mémoire des équipements et stockage 
- Logs enregistrent les activités du réseau
- Les outils de monitoring (Logs et events viewer, Syslog, SIEM (SEM and SIM),SNMP (Simple Network Management Protocol))
## 🤔 Ce qui a coincé
- À comprendre au maximum car très important dans les réseaux modernes

## 📊 Schéma (si pertinent)
```mermaid
graph LR
    A[Équipements réseau] -->|SNMP / Syslog| B[Serveur de monitoring]
    B --> C[Tableau de bord / Alertes]
    C --> D[Administrateur réseau]
```
 
## ✅ Auto-évaluation
- [x] Je peux expliquer ce concept à voix haute sans notes
- [x] Je peux l'appliquer dans un cas pratique différent de l'exemple du cours
- [x] Je vois le lien avec un projet que j'ai déjà fait (thèse, VoIP, cloud...)
## 🔗 Lien avec mes projets précédents
- Comment Wazuh (utilisé dans ma thèse) s'inscrit dans cette logique de monitoring — quels types de logs collecte-t-il ?
- Différence entre ce que fait Wazuh et ce que fait Suricata en matière de surveillance :
