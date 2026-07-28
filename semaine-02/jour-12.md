# Jour 12 — Concepts IP spéciaux & VLSM
 
📅 Date : À COMPLÉTER
⏱️ Temps passé : ~40 min
🎯 Charge de travail : Moyenne
 
## 📺 Support suivi
- Vidéo : 2:26:10 → 2:34:06 (Special IP Concepts)
- Lien direct : https://youtu.be/qiQR5rTSshw?t=8770
## 🧠 Ce que j'ai appris
<!-- Résume avec tes propres mots -->
-
-
-
## 🤔 Ce qui a coincé
-
## 🛠️ Exercice pratique — TP VLSM
 
Contrairement au subnetting classique (sous-réseaux égaux), le **VLSM (Variable Length Subnet Masking)** permet de créer des sous-réseaux de **tailles différentes**, adaptées au nombre réel d'hôtes de chaque segment — évite de gaspiller des adresses.
 
### Cas pratique
Tu disposes du bloc `192.168.100.0/24`. Découpe-le en VLSM pour ces besoins :
 
| Segment | Hôtes nécessaires | Masque à utiliser | Plage attribuée |
|---|---|---|---|
| LAN Interne | 100 hôtes | | |
| DMZ | 50 hôtes | | |
| LAN Management | 20 hôtes | | |
| Lien point-à-point routeur 1 ↔ routeur 2 | 2 hôtes | | |
 
**Méthode :** commence toujours par le segment qui a besoin du **plus grand nombre d'hôtes**, attribue-lui le premier bloc disponible, puis continue en ordre décroissant.
 
## 📊 Adresses réservées à connaître
| Adresse / Plage | Signification |
|---|---|
| 0.0.0.0 | |
| 127.0.0.1 | |
| 169.254.0.0/16 | |
| 255.255.255.255 | |
| 10.0.0.0/8, 172.16.0.0/12, 192.168.0.0/16 | |
 
## ✅ Auto-évaluation
- [ ] Je peux expliquer ce concept à voix haute sans notes
- [ ] Je peux faire un découpage VLSM complet sans calculateur en ligne
- [ ] Je vois le lien avec un projet que j'ai déjà fait (thèse, VoIP, cloud...)
## 🔗 Lien avec mes projets précédents
- Application du VLSM à mon architecture de thèse à 4 zones (WAN, DMZ, LAN Management, LAN Interne) :
