# Jour 10 — IPv4 & Subnetting
 
📅 Date : 27/07/2026
⏱️ Temps passé : ~50 min
🎯 Charge de travail : Intense
 
## 📺 Support suivi
- Vidéo : 1:56:26 → 2:15:58 (IPv4, parties 1 et 2)
- Lien direct : https://youtu.be/qiQR5rTSshw?t=7043
## 🧠 Ce que j'ai appris
<!-- Résume avec tes propres mots -->
- La définition, objectifs et le pourquoi des IPv4
- Les classes (A, B, C et D)
- FSLM (Fixed subnet lenght mask) et VSLM (Variable subnet lenght mask)
## 🤔 Ce qui a coincé
- Les exercices de subnetting quand c'est pas un mask générique (/8, /16, /24)
## 🛠️ Exercices de subnetting (à la main, sans calculateur)
 
### Rappel des classes d'adresses IPv4
| Classe | Plage | Masque par défaut |
|---|---|---|
| A | 1.0.0.0 – 126.255.255.255 | /8 |
| B | 128.0.0.0 – 191.255.255.255 | /16 |
| C | 192.0.0.0 – 223.255.255.255 | /24 | 
###Exercice 1
Nouveau masque : /26

Sous-réseau 1 : 192.168.1.0 (plage utilisable : 192.168.1.1 → 192.168.1.62, broadcast : 192.168.1.63)

Sous-réseau 2 : 192.168.1.64 (plage utilisable : 192.168.1.65 → 192.168.1.126, broadcast : 192.168.1.127)

Sous-réseau 3 : 192.168.1.128 (plage utilisable : 192.168.1.129 → 192.168.1.190, broadcast : 192.168.1.191)

Sous-réseau 4 : 192.168.1.192 (plage utilisable : 192.168.1.193 → 192.168.1.254, broadcast : 192.168.1.255)

###Exercice 2
Bits d’hôtes nécessaires : 9

Nouveau masque : /23

Nombre d’hôtes utilisables par sous-réseau : 510

###Exercice 3
Adresse réseau : 172.16.48.0

Adresse de broadcast : 172.16.63.255

Plage d’hôtes utilisables : 172.16.48.1 → 172.16.63.254

###Exercice 4
Nouveau masque : /27

Nombre de sous-réseaux : 8

Nombre d’hôtes utilisables par sous-réseau : 30
 
Formules qui pourront vous aider: 
Nombre de sous-réseau = 2 puissance bit(s) empruntés
Nombre d'hôte  = 2 puissance (bits restant - 2)
NB : Le - 2 signifie qu'il y'a deux adresses le broadcast et l'adresse réseau qui ne sont pas utilisable par les hôtes
## ✅ Auto-évaluation
- [x] Je peux faire un exercice de subnetting classique sans calculateur en ligne
- [x] Je peux expliquer le lien entre masque, nombre de sous-réseaux et nombre d'hôtes
- [x] Je vois le lien avec un projet que j'ai déjà fait (thèse, VoIP, cloud...)
## 🔗 Lien avec mes projets précédents
- Plan d'adressage utilisé (ou qui aurait dû être utilisé) dans mon architecture de thèse :
