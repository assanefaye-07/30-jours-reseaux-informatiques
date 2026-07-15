# Jour 7 — Révision & Bilan de la Semaine 1
 
📅 Date : 13/07/2026
⏱️ Temps passé : ~1h (révision + quiz)
🎯 Charge de travail : Moyenne
 
## 📺 Périmètre couvert
Semaine 1 complète : 0:00:00 → 1:22:32
- Jour 1 : Équipements réseau
- Jour 2 : Services et applications réseau
- Jour 3 : DHCP
- Jour 4 : DNS
- Jour 5 : NAT
- Jour 6 : Technologies WAN
## 📊 Résultats des quiz de la semaine
 
| Jour | Thème | Score | Statut |
|---|---|---|---|
| 1 | Équipements réseau | 2,5/3 | ✅ Acquis |
| 2 | Services & applications | 2/3 | ✅ Acquis |
| 3 | DHCP | 2,5/3 (2e tentative) | ✅ Acquis après reprise |
| 4 | DNS | 1,5/3 | ⚠️ À consolider |
| 5 | NAT | 2/3 | ✅ Acquis |
| 6 | Technologies WAN | 2/3 | ✅ Acquis |
 
**Moyenne de la semaine : ~2,1/3 (≈ 70%)**
 
## ✅ Points forts confirmés
- Rôle et couche OSI des équipements réseau (switch, pare-feu, AP)
- Processus DORA (DHCP) après reprise — broadcast jusqu'à l'Ack, réservation MAC↔IP
- PAT et raison d'être du NAT (pénurie IPv4)
- MPLS vs ligne louée, VPN site-à-site
## ⚠️ Points à retravailler avant la Semaine 2
- **DNS** : enregistrement MX (mail), cas d'usage concrets des enregistrements, notion de **TTL** et son rôle dans la propagation
- **NAT** : ne pas confondre SNAT/DNAT (direction de traduction) avec NAT statique/dynamique (mode d'attribution)
- **VPN remote access** : bien retenir que c'est **1 utilisateur** (pas 1 réseau entier) qui se connecte via un client logiciel
- **DSL/câble/fibre** : tableau comparatif débit/latence à revoir, notamment pourquoi la fibre gagne aussi en latence
## 🛠️ Exercice de synthèse
Rédige un paragraphe (5-6 phrases) qui explique, sans notes, comment une machine de ton LAN interne obtient une IP (DHCP), résout un nom de domaine (DNS), et sort vers Internet (NAT) — en une seule chaîne logique cohérente.
 
```
 Dans un réseau avec un serveur DHCP pour obtenir un IP de façon dynamique, la machine utilise le processus DORA.
 Un paquet Discover est lancé par la machine en mode broadcast sur le port 68 , le serveur répond avec une offre (DHCP offer) d'IP avec ses paramètres réseaux sur le port 67, La machine choisit une offre (DHCP Request) d'IP.
 Enfin le server confirme cette offre pour la machine avec un DHCP Acknowlegment.
 Le DNS est "l'annuaire d'internet" il permet de transformer les noms de domaines compréhensible par les humains en IP que les machines utilisent pour communiquer.
 Y'a les requêtes récursives (la machine demande une URL et celle-ci est affiché à l'écran sans que l'user ne fasse rien) et les requêtes itératives (les serveurs qui ne sait pas demandent à l'autre jusqu'à la résolution du nom de domaine). Le NAT permet de traduire les adresses privées qui ne sont pas routable sur Internet en adresse IP publique routable sur Internet. Le PAT est une technologie NAT permettant à plusieurs appareils d'utiliser la même IP public mais sur des ports différents. C'est utilser par nos box internet à la maison
```
 
## ✅ Auto-évaluation de la semaine
- [✅] Je peux enchaîner DHCP → DNS → NAT dans un seul récit cohérent sans notes
- [✅] Je peux citer les 6 thèmes de la semaine sans regarder le planning
- [✅] Je me sens prêt à passer à l'adressage IP (Semaine 2) sans lacune bloquante
## 🔗 Lien avec mes projets précédents
- Comment ces 6 notions s'articulent concrètement dans mon architecture de thèse (pfSense + zones réseau) :
