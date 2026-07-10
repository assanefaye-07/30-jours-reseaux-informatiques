# Jour 5 — NAT (Network Address Translation)
 
📅 Date : 10/07/2026
⏱️ Temps passé : ~25 min
🎯 Charge de travail : Légère
 
## 📺 Support suivi
- Vidéo : 0:46:01 → 0:52:52 (NAT)
- Lien direct : https://youtu.be/qiQR5rTSshw?t=2761
## 🧠 Ce que j'ai appris
<!-- Résume avec tes propres mots -->
- Le NAT (SNAT: Static NAT | DNAT: Dynamic NAT) et son fonctionnment
- Le PAT (Port adress Translation: qui est utilsé par la majorité des box actuellement | Source NAT et Destination NAT)
- Les terminilogie (Inside local adress, inside global adress, outside local adress, outside global adress)
## 🤔 Ce qui a coincé
- J'ai souvent confondu certains termes (Static NAT et Source NAT, Dynamic NAT et destination NAT)
## 🛠️ Exercice pratique réalisé
Comparatif NAT statique / NAT dynamique / PAT (Port Address Translation) :
 
| Type | Principe | Cas d'usage |
|---|---|---|
| NAT statique |NAT static assigne une IP privée a une IP Publique unique |Sserveur WEb des entreprises |
| NAT dynamique |NAT dynamique assigne une ip privée à une IP publique de façon temporaire grâce à son pool d'adresse IP publique |Une entreprise qui configure plusieurs IP publique pour la sortie de ces machines sur Internet |
| PAT (NAT overload) |PAT plusieurs hôtes utilise la même IP publique pour sortir d'internet sur des ports différents |Box Internet actuel |
 
Identification sur ta config pfSense (thèse honeypot) :
- Pour qu'internet puisse atteindre mon honeypot, PfSense faisait du redirection de port 
- Mon LAN interne possedait des IP privées du coup Pfsense faisait aussi du PAT pour leur permettre de sortir sur internet avec l'IP publique du WAN
- Explique en une phrase pourquoi c'est nécessaire dans ton architecture
## 📊 Schéma (si pertinent)
```mermaid
graph LR
    A[Machine LAN<br/>IP privée 192.168.1.10] -->|NAT/PAT| B[Routeur/Pare-feu<br/>IP publique]
    B --> C[Internet]
```
 
## ✅ Auto-évaluation
- [✅] Je peux expliquer ce concept à voix haute sans notes
- [✅] Je peux l'appliquer dans un cas pratique différent de l'exemple du cours
- [✅] Je vois le lien avec un projet que j'ai déjà fait (thèse, VoIP, cloud...)
## 🔗 Lien avec mes projets précédents
- Différence entre adresse privée (RFC 1918) et adresse publique :
Les adresses de classe A (10.0.0.0/8), les adresses de classe B (172.16.0.0/16) et les adresses C (192.168.0.0/24) sont non routable sur Internet. Le NAT permet à ces IP privée d'accéder à Internet via des IP publiques
