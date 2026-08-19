# Jour 21 — Révision, TP & Bilan de la Semaine 3
 
📅 Date : 19/08/2026
⏱️ Temps passé : ~1h30 (révision + quiz + TP)
🎯 Charge de travail : Intense
 
## Périmètre couvert
Semaine 3 complète : 2:59:01 → 4:53:17
- Jour 15 : Communications unifiées, virtualisation, SAN
- Jour 16 : Cloud & implémentation réseau
- Jour 17 : Monitoring réseau
- Jour 18 : Gestion de configuration & segmentation (VLAN)
- Jour 19 : Patchs & configuration des switches
- Jour 20 : Infrastructure WLAN
## Résultats des quiz de la semaine
 
| Jour | Thème | Score | Statut |
|---|---|---|---|
| 15 | Communications unifiées, virtualisation, SAN | 2/3 | ✅ Acquis |
| 16 | Cloud & implémentation réseau | 2,5/3 | ✅ Acquis |
| 17 | Monitoring réseau | 2/3 | ✅ Acquis |
| 18 | Gestion de config & VLAN | 3/3 | ✅ Sans-faute |
| 19 | Patchs & configuration switches | 3/3 | ✅ Sans-faute |
| 20 | Infrastructure WLAN | 3/3 | ✅ Sans-faute |
 
**Moyenne de la semaine : ~2,6/3 (≈ 86%)** — meilleure série de la fin de semaine (3 sans-fautes consécutifs : Jours 18, 19, 20)
 
## Points forts confirmés
- SIP/RTP et lien concret avec le projet Asterisk (métaphore "standard téléphonique / voix")
- SAN vs NAS avec exemples professionnels (cluster de bases de données)
- VLAN, port security, mode access/trunk — avec notions avancées maîtrisées (VLAN hopping, err-disabled)
- Sécurité Wi-Fi (WEP vs WPA2/WPA3, RC4 vs AES-CCMP) à un niveau très solide
- Roaming Wi-Fi relié correctement à SIP/RTP et à la notion de jitter (Jour 17)
- Contrôleur WLAN et gestion centralisée (rogue AP, équilibrage de charge)
## Points à retravailler avant la Semaine 4
- **Virtualisation** : bien distinguer VMware Workstation (Type 2, hébergé) de VMware ESXi (Type 1, bare-metal) — et retenir que le Type 1 est le plus performant, pas l'inverse
- **Jitter** : bien retenir que c'est un jitter **élevé** qui pose problème, pas faible
- **Cloud** : toujours donner un exemple concret ET une justification "pourquoi" (pas seulement la définition), notamment pour PaaS
## Exercice de synthèse
Rédige un paragraphe (5-6 phrases) qui explique, sans notes, comment un patch de sécurité identifié comme critique (par exemple sur un contrôleur WLAN) devrait être géré, de la détection à l'application — en citant le monitoring (Jour 17), la gestion de configuration (Jour 18), et le patch management (Jour 19).
 
```
Lorsqu’un patch de sécurité critique est identifié sur un contrôleur WLAN, la première étape consiste à le détecter grâce au monitoring, qui permet de repérer rapidement les vulnérabilités ou alertes remontées par les systèmes de supervision.
Ensuite, la gestion de configuration assure que l’inventaire des équipements est à jour et que l’on sait précisément quelles versions logicielles sont déployées, afin de cibler correctement les systèmes concernés. 
Vient alors le processus de patch management, où l’on évalue la criticité, planifie l’application du correctif et teste son impact potentiel sur la production.
Une fois validé, le patch est appliqué de manière contrôlée, souvent en dehors des heures de pointe pour limiter les perturbations.
 Enfin, un suivi post-déploiement est réalisé via le monitoring pour vérifier que la faille est bien corrigée et que le système reste stable.
 Ce cycle garantit une réponse rapide et structurée face aux menaces critiques.
```
 
## Auto-évaluation de la semaine
- [x] Je peux configurer un VLAN + port security sur un switch Cisco sans notes
- [x] Je peux expliquer la chaîne complète monitoring → détection → patch → validation
- [x] Je me sens prêt à passer à la sécurité réseau avancée (Semaine 4) sans lacune bloquante
## Lien avec mes projets précédents
- Comment le monitoring (Wazuh), la segmentation et le patch management s'articulent concrètement dans mon architecture de thèse :
