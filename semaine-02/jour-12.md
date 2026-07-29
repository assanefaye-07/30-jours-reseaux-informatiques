# Jour 12 — Concepts IP spéciaux & VLSM
 
📅 Date :29/07/2026
⏱️ Temps passé : ~40 min
🎯 Charge de travail : Moyenne
 
## 📺 Support suivi
- Vidéo : 2:26:10 → 2:34:06 (Special IP Concepts)
- Lien direct : https://youtu.be/qiQR5rTSshw?t=8770
## 🧠 Ce que j'ai appris
<!-- Résume avec tes propres mots -->
- Domaine de collision et domaine de broadcast
- Savoir les significations suivantes: Unicast (point à point), Multicast (un à un groupe désigné) et broadcast (tous les appareils du réseau local recoivent la transmission)
- IPv6 fait du unicast, du multicast et de l'anycast (atteindre l'hôte le plus proche en utilisant une IP partagé entre plusieurs noeuds)
## 🤔 Ce qui a coincé
- C'était des concepts déjà traité d'une part
## 🛠️ Exercice pratique — TP VLSM
 
Contrairement au subnetting classique (sous-réseaux égaux), le **VLSM (Variable Length Subnet Masking)** permet de créer des sous-réseaux de **tailles différentes**, adaptées au nombre réel d'hôtes de chaque segment — évite de gaspiller des adresses.
 
### Cas pratique
Tu disposes du bloc `192.168.100.0/24`. Découpe-le en VLSM pour ces besoins :
 
| Segment | Hôtes nécessaires | Masque à utiliser | Plage attribuée |
|---|---|---|---|
| LAN Interne | 100 hôtes |/25 |192.168.100.1 à 192.168.100.126 |
| DMZ | 50 hôtes |/26 |192.168.100.129/26 à 192.168.100.190 |
| LAN Management | 20 hôtes |/27 |192.168.100.193 à 192.168.100.222 |
| Lien point-à-point routeur 1 ↔ routeur 2 | 2 hôtes |/30 |192.168.100.225 – 192.168.100.226 |
 
**Méthode :** commence toujours par le segment qui a besoin du **plus grand nombre d'hôtes**, attribue-lui le premier bloc disponible, puis continue en ordre décroissant.
 
## 📊 Adresses réservées à connaître
| Adresse / Plage | Signification |
|---|---|
| 0.0.0.0 |Signifie toutes les adresses |
| 127.0.0.1 |adresse de loopback, du localhost |
| 169.254.0.0/16 |Adresse APIPA DHCP, la machine s'auto-configure une adresse |
| 255.255.255.255 |Adresse de broadcast permettant d'envoyer des paquets à tous les hôtes du réseau local |
| 10.0.0.0/8, 172.16.0.0/12, 192.168.0.0/16  |Plage d'adresse privé, et bien sûr non routable |
 
## ✅ Auto-évaluation
- [x] Je peux expliquer ce concept à voix haute sans notes
- [x] Je peux faire un découpage VLSM complet sans calculateur en ligne
- [x] Je vois le lien avec un projet que j'ai déjà fait (thèse, VoIP, cloud...)
## 🔗 Lien avec mes projets précédents
- Application du VLSM à mon architecture de thèse à 4 zones (WAN, DMZ, LAN Management, LAN Interne) :
