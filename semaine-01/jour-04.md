# Jour 4 — DNS
 
📅 Date : 09/07/2026
⏱️ Temps passé : ~35 min
🎯 Charge de travail : Moyenne
 
## 📺 Support suivi
- Vidéo : 0:38:03 → 0:46:01 (DNS)
- Lien direct : https://youtu.be/qiQR5rTSshw?t=2283
## 🧠 Ce que j'ai appris
<!-- Résume avec tes propres mots -->
- Le DNS et le FQDN (Fully Qualified Domain Name)
- les différents niveaux du DNS (Local serveur | Top Level Domain (TLD) | Root serveur (la racine))
- Les reponses faisant autorités et ne faisant pas autorité | Les types d'enregistrement (A, AAAA, CNAME, MX, PTR)
## 🤔 Ce qui a coincé
- Les requêtes récursives et itératives
## 🛠️ Exercice pratique réalisé
Requêtes DNS réelles avec `nslookup` ou `dig` sur 3 domaines, puis interprétation du résultat :
 
```bash
nslookup google.com
nslookup github.com
nslookup ucao.sn
```
 
Résultats obtenus :
```
[nslookup github.com
Serveur :   dns.google
Address:  8.8.8.8

Réponse ne faisant pas autorité :
Nom :    github.com
Address:  140.82.121.3]
```
 
Interprétation :
- C'est le serveur DNS de google que mon PC a interrogé avec son adresse 8.8.8.8
- Onvoit clairement "Réponse no faisant pas autorité" ce qui fait que c'est pas le serveur de Github qui répond mais google
- A la fin on voit les informations : github.com et son adresse IP qui en enregistrement A 
 
## 📊 Schéma (si pertinent)
Résolution DNS récursive vs itérative :
 
```mermaid
sequenceDiagram
    participant C as Client
    participant R as Résolveur (FAI/local)
    participant Root as Serveur racine
    participant TLD as Serveur TLD (.com)
    participant Auth as Serveur autoritaire
    C->>R: Requête récursive : www.exemple.com ?
    R->>Root: Requête itérative
    Root-->>R: Adresse du serveur .com
    R->>TLD: Requête itérative
    TLD-->>R: Adresse du serveur autoritaire
    R->>Auth: Requête itérative
    Auth-->>R: Adresse IP finale
    R-->>C: Réponse finale
```
 
## ✅ Auto-évaluation
- [✅] Je peux expliquer ce concept à voix haute sans notes
- [✅] Je peux l'appliquer dans un cas pratique différent de l'exemple du cours
- [✅] Je vois le lien avec un projet que j'ai déjà fait (thèse, VoIP, cloud...)
## 🔗 Lien avec mes projets précédents
- Types d'enregistrements DNS à retenir : A, AAAA, MX, CNAME, PTR, NS, TXT
- Lien avec mon projet Asterisk/VoIP (résolution de noms pour les trunks SIP) :
