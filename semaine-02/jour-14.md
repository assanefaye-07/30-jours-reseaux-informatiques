# Jour 14 — Révision & Bilan de la Semaine 2
 
📅 Date : 31/07/2026
⏱️ Temps passé : ~1h (révision + quiz + TP)
🎯 Charge de travail : Intense
 
## 📺 Périmètre couvert
Semaine 2 complète : 1:22:32 → 2:59:01
- Jour 8 : Câblage réseau
- Jour 9 : Topologies & infrastructure
- Jour 10 : IPv4 & subnetting
- Jour 11 : IPv6
- Jour 12 : Concepts IP spéciaux & VLSM
- Jour 13 : Routage (concepts & protocoles)
## 📊 Résultats des quiz de la semaine
 
| Jour | Thème | Score | Statut |
|---|---|---|---|
| 8 | Câblage réseau | 3/3 | ✅ Sans-faute |
| 9 | Topologies & infrastructure | 2,5/3 (2e tentative) | ✅ Acquis après reprise |
| 10 | IPv4 & subnetting | 2,5/3 (2e tentative) | ✅ Acquis après reprise |
| 11 | IPv6 | 3/3 | ✅ Sans-faute |
| 12 | Concepts IP spéciaux & VLSM | 3/3 | ✅ Sans-faute |
| 13 | Routage (concepts & protocoles) | 2,5/3 | ✅ Acquis |
 
**Moyenne de la semaine : ~2,75/3 (≈ 92%)** — nette progression par rapport à la Semaine 1 (~70%)
 
## ✅ Points forts confirmés
- Câblage cuivre/fibre, connecteurs (sans-faute)
- IPv6 : compression, types d'adresses, raisons de sa création (sans-faute)
- VLSM : méthode rigoureuse, calculs exacts sur un cas réel à 4 zones (sans-faute)
- Subnetting classique après reprise — bonne maîtrise du calcul du bloc dans le bon octet
- Distance Vector vs Link-State, avec exemples concrets bien choisis
- Architecture 3-tiers après reprise (Accès/Distribution/Cœur)
- TP pratique Cisco (routage directement connecté) réalisé avec succès
## ⚠️ Points à retravailler avant la Semaine 3
- **Topologies** : bien distinguer bus / étoile / étoile étendue / maillage (le TP routeur correspond à une étoile étendue, pas un bus)
- **Subnetting** : rester rigoureux sur l'identification de l'octet concerné par le découpage selon le masque (`/17` à `/24` → 3ème octet, `/9` à `/16` → 2ème octet)
- **BGP** : bien retenir que c'est un protocole **policy-based** (accords commerciaux/politiques entre AS), pas juste un calcul de performance
## 🛠️ Exercice de synthèse
Rédige un paragraphe (5-6 phrases) qui explique, sans notes, comment un paquet part d'une machine dans un sous-réseau VLSM, traverse un routeur qui décide du meilleur chemin (statique ou dynamique), pour atteindre un sous-réseau différent.
 
```
[Lorsqu’un paquet est généré par une machine dans un sous‑réseau configuré avec VLSM, il est d’abord encapsulé avec son adresse IP source et destination. La machine vérifie sa table de routage locale pour savoir si la destination se trouve dans son propre sous‑réseau ou non. Si l’adresse appartient à un autre sous‑réseau, le paquet est envoyé vers la passerelle par défaut, généralement un routeur. Le routeur examine alors sa table de routage, qui peut être construite statiquement par l’administrateur ou dynamiquement grâce à des protocoles comme OSPF ou RIP, afin de déterminer le meilleur chemin. Une fois la décision prise, le paquet est transféré vers l’interface appropriée et continue son trajet à travers le réseau. Finalement, il atteint le sous‑réseau cible où la machine destinataire le reçoit et le traite.]
```
 
## ✅ Auto-évaluation de la semaine
- [x] Je peux faire un exercice de VLSM complet sans calculateur, sans erreur
- [x] Je peux expliquer la différence Distance Vector / Link-State avec un exemple chiffré
- [x] Je me sens prêt à passer à l'administration réseau (Semaine 3) sans lacune bloquante
## 🔗 Lien avec mes projets précédents
- Comment le VLSM et le routage s'articulent concrètement dans mon architecture de thèse (pfSense + zones réseau) :
