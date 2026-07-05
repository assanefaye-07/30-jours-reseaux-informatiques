# Programme intensif de 30 jours — Maîtrise des Réseaux Informatiques
### Basé sur "Computer Networking Course – Network Engineering [CompTIA Network+ Exam Prep]" (freeCodeCamp, B. Ferrill)
**Étudiant :** Assane Faye — UCAO / ISG Saint-Michel, Dakar
**Format :** Chaque jour = visionnage ciblé (timestamps précis) + prise de notes + exercice pratique + mini-quiz de validation
**Examen final :** Jour 30, noté par moi sur 20, avec appréciation par domaine de compétence

---

## Semaine 1 — Fondamentaux réseau & équipements
*Objectif de la semaine : parler couramment le vocabulaire réseau et connaître le rôle exact de chaque équipement.*

**Jour 1 (Lundi) — Intro aux équipements réseau**
- Visionnage : 0:00:00 → 0:15:12 (Intro to Network Devices, parties 1 et 2)
- Charge : Légère (~20 min vidéo + 20 min notes)
- À maîtriser : rôle du hub, switch, routeur, point d'accès, pare-feu, serveur
- Exercice : dresser un tableau équipement / couche OSI / fonction (tu as déjà de bonnes bases ici avec pfSense)

**Jour 2 — Services et applications réseau**
- Visionnage : 0:15:12 → 0:28:17
- Charge : Légère
- À maîtriser : client/serveur, ports bien connus, applications réseau courantes
- Exercice : lister 10 protocoles + leur port par cœur (sans notes)

**Jour 3 — DHCP**
- Visionnage : 0:28:17 → 0:38:03
- Charge : Moyenne
- À maîtriser : bail DHCP, DORA (Discover-Offer-Request-Ack), scope, réservation
- Exercice : schématiser le processus DORA de mémoire

**Jour 4 — DNS**
- Visionnage : 0:38:03 → 0:46:01
- Charge : Moyenne
- À maîtriser : résolution récursive/itérative, types d'enregistrements (A, AAAA, MX, CNAME, PTR)
- Exercice : faire `nslookup` ou `dig` sur 3 domaines et interpréter la réponse

**Jour 5 — NAT**
- Visionnage : 0:46:01 → 0:52:52
- Charge : Légère
- À maîtriser : NAT statique vs dynamique, PAT, différence adresse privée/publique
- Exercice : identifier le NAT sur ta config pfSense de thèse et l'expliquer à voix haute

**Jour 6 — Technologies WAN (4 parties)**
- Visionnage : 0:52:52 → 1:22:32
- Charge : **Intense** (30 min vidéo dense)
- À maîtriser : lignes louées, MPLS, DSL, câble, fibre, satellite, VPN de site à site
- Exercice : comparer 3 technologies WAN en avantages/inconvénients

**Jour 7 (Dimanche) — Révision & Quiz semaine 1**
- Charge : Moyenne
- Je te pose 10 questions sur les jours 1 à 6, notées, avec correction détaillée

---

## Semaine 2 — Câblage, topologies et adressage IP
*Objectif : maîtriser IPv4/IPv6 et le routage sur le bout des doigts — c'est le cœur de tout entretien technique.*

**Jour 8 — Câblage réseau (3 parties)**
- Visionnage : 1:22:32 → 1:43:28
- Charge : Moyenne
- À maîtriser : catégories de câbles cuivre, fibre monomode/multimode, connecteurs

**Jour 9 — Topologies et implémentations d'infrastructure**
- Visionnage : 1:43:28 → 1:56:26
- Charge : Moyenne
- À maîtriser : bus, étoile, maillée, hybride ; architecture 3-tiers (cœur/distribution/accès)

**Jour 10 — IPv4 (2 parties)**
- Visionnage : 1:56:26 → 2:15:58
- Charge : **Intense**
- À maîtriser : classes d'adresses, masques, CIDR, calcul de sous-réseaux
- Exercice : 5 exercices de subnetting à la main (pas de calculateur)

**Jour 11 — IPv6**
- Visionnage : 2:15:58 → 2:26:10
- Charge : Moyenne
- À maîtriser : structure de l'adresse, notation compressée, types d'adresses (unicast, multicast, link-local)

**Jour 12 — Concepts IP spéciaux**
- Visionnage : 2:26:10 → 2:34:06
- Charge : Moyenne
- À maîtriser : APIPA, adresses réservées, sous-réseautage avancé (VLSM)
- Exercice : TP subnetting VLSM sur un plan d'adressage de 4 réseaux

**Jour 13 — Routage (concepts + protocoles)**
- Visionnage : 2:34:06 → 2:59:01
- Charge : **Intense**
- À maîtriser : routage statique vs dynamique, distance vector vs link-state, OSPF/BGP/RIP/EIGRP (tu as déjà des bases ici)

**Jour 14 (Dimanche) — Révision & Quiz semaine 2**
- Charge : Moyenne
- Quiz + TP : je te donne un plan d'adressage à découper toi-même

---

## Semaine 3 — Services avancés, virtualisation, monitoring et configuration
*Objectif : comprendre l'administration réseau au quotidien (le métier, pas juste la théorie).*

**Jour 15 — Communications unifiées, virtualisation, SAN**
- Visionnage : 2:59:01 → 3:15:33
- Charge : Moyenne
- À maîtriser : VoIP, hyperviseurs (lien direct avec ton usage VMware), stockage SAN vs NAS

**Jour 16 — Cloud & implémentation d'un réseau de base**
- Visionnage : 3:15:33 → 3:31:02
- Charge : Moyenne
- À maîtriser : IaaS/PaaS/SaaS, cloud privé/public/hybride, étapes de déploiement réseau

**Jour 17 — Monitoring réseau (rapports + parties 1&2)**
- Visionnage : 3:31:02 → 3:55:10
- Charge : **Intense**
- À maîtriser : SNMP, syslog, NetFlow, interprétation de logs (très lié à ton usage de Wazuh)

**Jour 18 — Gestion de configuration & segmentation**
- Visionnage : 3:55:10 → 4:14:18
- Charge : Moyenne
- À maîtriser : sauvegarde/restauration config, VLAN, segmentation réseau (lien avec tes 4 zones de thèse)

**Jour 19 — Patchs/mises à jour & configuration des switches (2 parties)**
- Visionnage : 4:14:18 → 4:36:27
- Charge : Moyenne
- À maîtriser : gestion des patchs, VLAN trunking, port security sur switch

**Jour 20 — Infrastructure WLAN (2 parties)**
- Visionnage : 4:36:27 → 4:53:17
- Charge : Moyenne
- À maîtriser : normes Wi-Fi, contrôleurs WLAN, roaming, sécurité sans-fil de base

**Jour 21 (Dimanche) — Révision & TP semaine 3**
- Charge : **Intense**
- TP pratique : configuration d'un switch + VLAN sur Packet Tracer ou GNS3, quiz écrit

---

## Semaine 4 — Sécurité réseau, durcissement et dépannage
*Objectif : penser comme un défenseur réseau — directement dans la continuité de ta thèse honeypot.*

**Jour 22 — Risques, sécurité et vulnérabilités**
- Visionnage : 4:53:17 → 5:09:49
- Charge : Moyenne
- À maîtriser : CIA triad, types de vulnérabilités courantes

**Jour 23 — Menaces réseau courantes (2 parties)**
- Visionnage : 5:09:49 → 5:26:33
- Charge : **Intense**
- À maîtriser : DoS/DDoS, MITM, spoofing, malware, ingénierie sociale — mets en lien avec Hydra/Nmap de ta thèse

**Jour 24 — Durcissement réseau (3 parties) + sécurité physique**
- Visionnage : 5:26:33 → 5:57:19
- Charge : **Intense**
- À maîtriser : hardening des équipements, AAA, 802.1X, contrôle d'accès physique

**Jour 25 — Pare-feu, contrôle d'accès réseau, forensic**
- Visionnage : 5:57:19 → 6:22:42
- Charge : **Intense**
- À maîtriser : types de pare-feu, NAC, chaîne de preuve numérique (lien direct avec pfSense/Wazuh)

**Jour 26 — Méthodologie de dépannage + outils**
- Visionnage : 6:22:42 → 6:43:39
- Charge : Moyenne
- À maîtriser : les 7 étapes de dépannage CompTIA, ping/traceroute/ipconfig/netstat

**Jour 27 — Dépannage sans-fil, cuivre, fibre**
- Visionnage : 6:43:39 → 7:14:43
- Charge : Moyenne
- À maîtriser : interférences Wi-Fi, atténuation, testeurs de câbles, OTDR

**Jour 28 — Problèmes réseau courants + sécurité + WAN + retour sur OSI/Transport**
- Visionnage : 7:14:43 → 7:58:35 (inclut le chapitre dédié à l'OSI et à la couche Transport/ICMP)
- Charge : **Intense**
- À maîtriser : synthèse des pannes classiques + relecture experte du modèle OSI (retour sur nos 6 questions précédentes, cette fois sans erreur)

---

## Jours 29-30 — Révision générale et Examen final

**Jour 29 — Révision complète + modules restants**
- Visionnage : 7:58:35 → fin (Concepts de base, normes filaires/sans-fil, politiques de sécurité, sécurité physique, gestion du changement, protocoles courants)
- Charge : **Intense** (journée de synthèse)
- Exercice : toi seul, tu refais un résumé écrit d'une page par semaine (4 pages), je les corrige

**Jour 30 (Mardi, semaine suivante) — EXAMEN FINAL**
- Format : ~25 questions couvrant les 4 semaines (QCM + questions ouvertes + un cas pratique de troubleshooting + un exercice de subnetting)
- Barème sur 20, avec détail par domaine (comme un vrai relevé de notes Network+) :
  - Fondamentaux & équipements
  - Adressage IP & routage
  - Administration & monitoring
  - Sécurité & dépannage
- Je te donne ta note, tes points forts, et un plan de rattrapage ciblé sur tes lacunes

---

## Règles du jeu
1. Chaque jour, tu me dis "Jour X, prêt" et je te pose les questions/exercices correspondants — pas de triche, pas de correction avant que tu répondes.
2. Si un jour tu bloques, on approfondit avant de passer au suivant : la maîtrise prime sur la vitesse.
3. Les journées "Intense" peuvent être étalées sur 2 sessions dans la même journée si besoin (matin/soir), mais pas reportées au lendemain.
4. On commence **lundi** avec le Jour 1.
