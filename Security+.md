[[Security+]]
## ***==Acronymes :==***
## 🔐 **Authentication & Access Control**

| Acronyme       | Signification                                            | Usage principal                                                                                                                                                                                                         |     |
| -------------- | -------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --- |
| **2FA**        | Two-factor Authentication                                | Ajout d’un deuxième facteur pour authentifier un utilisateur (ex : mot de passe + SMS)                                                                                                                                  |     |
| **[[AAA]]**    | Authentication, Authorization, and Accounting            | Cadre de gestion des accès : identifier, autoriser, journaliser                                                                                                                                                         |     |
| **[[ACL]]**    | Access Control List                                      | Liste définissant qui peut accéder à quoi sur un système ou un réseau                                                                                                                                                   |     |
| **DAC**        | Discretionary Access Control                             | Modèle où le propriétaire d’un objet définit les autorisations                                                                                                                                                          |     |
| **IAM**        | Identity and Access Management                           | Gestion centralisée des identités et des autorisations                                                                                                                                                                  |     |
| **MFA**        | Multifactor Authentication                               | Authentification par plusieurs types de facteurs (connaissance, possession, biométrie)                                                                                                                                  |     |
| **PAM**        | Privileged Access Management                             | Contrôle et journalisation des accès à privilèges élevés                                                                                                                                                                |     |
| **RBAC**       | Role-based Access Control                                | Attribution des droits selon le rôle de l'utilisateur                                                                                                                                                                   |     |
| **ABAC**       | Attributs-based Acces Control                            | Attribution des droits selon les attributs (localisation, heure...)                                                                                                                                                     |     |
| **SSO**        | Single Sign-on                                           | Permet de s’authentifier une fois pour accéder à plusieurs services                                                                                                                                                     |     |
| **CHAP**       | Challenge Handshake Authentication Protocol              | Protocole d’authentification réseau basé sur un défi/réponse                                                                                                                                                            |     |
| **PAP**        | Password Authentication Protocol                         | Protocole simple d’authentification (moins sécurisé, en clair)                                                                                                                                                          |     |
| **RADIUS**     | Remote Authentication Dial-in User Service               | Serveur d’authentification centralisé (souvent utilisé en entreprise)                                                                                                                                                   |     |
| **TACACS+**    | Terminal Access Controller Access Control System Plus    | Gère les accès privilégiés des administrateurs réseau (routeurs, switchs Cisco)                                                                                                                                         |     |
| **IEE 802.1X** | Port-Based Network Access Control                        | Protocole d’authentification qui contrôle l’accès à un réseau (filaire ou sans fil) avant d’autoriser une connexion.                                                                                                    |     |
| **LDAP**       | Lightweight Directory Access Protocol                    | Protocole d'annuaire utilisé dans l'IAM (avec Active Directory)                                                                                                                                                         |     |
| **NTLM**       | NT LAN Manager                                           | Authentification sur les réseaux Windows (Vulnérable aux attaques pass-the-hash, relay attacks, rainbow tables), est remplacé par **KERBEROS**                                                                          |     |
| **KERBEROS**   |                                                          | Protocole d’authentification réseau sécurisé, utilisé par défaut dans les domaines AD. Remplace NTLM                                                                                                                    |     |
| **JIT**        | Just-In-Time-Access                                      | Donner des droits d'accès élevés pendant une courte période pour un besoin éphémère                                                                                                                                     |     |
| **SCADA**      | supervisory control and data acquisition                 | Architecture de système de contrôle comprenant des ordinateurs, des communications de données en réseau et des interfaces graphiques utilisateur pour la supervision de haut niveau des machines et des processus.      |     |
| **IF**         | Identity Federation                                      | SSO entre plusieurs organisations ou domaines                                                                                                                                                                           |     |
| **MDM/MAM**    | Mobile Device Management / Mobile Application Management | Le MDM/MAM est une solution logicielle qui permet aux entreprises de gérer, surveiller et sécuriser les appareils mobiles (smartphones, tablettes, ordinateurs portables) utilisés dans un environnement professionnel. |     |

---

## 🔒 **Encryption & Cryptography**
 
| Acronyme      | Signification                                | Usage principal                                                                                                                                            |
| ------------- | -------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **3DES**      | Triple Data Encryption Standard              | Ancien algorithme de chiffrement symétrique                                                                                                                |
| **AES**       | Advanced Encryption Standard                 | Chiffrement symétrique rapide et sécurisé (standard actuel)                                                                                                |
| **AES-256**   | AES avec clé de 256 bits                     | Version plus sécurisée d’AES                                                                                                                               |
| **[[ECDHE]]** | Elliptic Curve Diffie-Hellman Ephemeral      | Utilisé pour générer des clés basées sur courbes elliptiques de manière éphémères                                                                          |
| **HMAC**      | Hashed Message Authentication Code           | Vérifie l'intégrité et l’authenticité des messages                                                                                                         |
| **PKI**       | Public Key Infrastructure                    | Ensemble de services pour la gestion des [[Certificats]] et des clés publiques                                                                             |
| **RSA**       | Rivest, Shamir, & Adleman                    | Algorithme de chiffrement asymétrique                                                                                                                      |
| **SHA**       | Secure Hashing Algorithm                     | Famille de fonctions de hachage cryptographique                                                                                                            |
| **SSL**       | Secure Sockets Layer                         | Ancien protocole de chiffrement pour sécuriser les communications                                                                                          |
| **TLS**       | Transport Layer Security                     | Successeur de SSL, utilisé pour HTTPS                                                                                                                      |
| **PFS**       | Perfect Forward Secrecy                      | Propriété empêchant le déchiffrement rétroactif des sessions (utilise **[[ECDHE]]**)                                                                       |
| **DKIM**      | DomainKeys Identified Mail                   | Vérifie qu’un e-mail a bien été envoyé depuis un domaine autorisé                                                                                          |
| **S/MIME**    | Secure/Multipurpose Internet Mail Extensions | Chiffrement et signature d’e-mails                                                                                                                         |
| **SED**       | Self-encrypting Drives                       | Disques durs avec chiffrement intégré matériellement                                                                                                       |
| **EFS**       | Windows Encrypting File System               | Chiffre un ou plusieurs fichiers                                                                                                                           |
| **BitLocker** |                                              | Chiffre l'ensemble du disque dur ou de la partition, OS inclus                                                                                             |
| **MD5**       | Message-Digest 5                             | Hash function producing 128 bits. Depracted/Unsafe                                                                                                         |
| **CRC**       | Contrôle de redondance cyclique              | Détecte des erreurs de transmission ou de transfert par ajout, combinaison et comparaison de données redondantes obtenues grâce à une procédure de hachage |

---

## 🌐 **Network Security**

| Acronyme         | Signification                                     | Usage principal                                                         |
| ---------------- | ------------------------------------------------- | ----------------------------------------------------------------------- |
| **BGP**          | Border Gateway Protocol                           | Routage entre grandes organisations ou fournisseurs (Internet)          |
| **DNS**          | Domain Name System                                | Résout les noms de domaine en adresses IP                               |
| **DNSSEC**       | DNS Security Extensions                           | Ajoute l’authenticité et l’intégrité aux réponses DNS                   |
| **[[DoS - DDoS]]** | Denial of Service / Distributed DoS               | Attaques visant à rendre un service indisponible                        |
| **IDS/IPS**      | Intrusion Detection/Prevention System             | Surveille (IDS) ou bloque (IPS) les activités malveillantes réseau      |
| **NAC**          | Network Access Control                            | Contrôle les connexions au réseau en fonction de politiques de sécurité |
| **NAT**          | Network Address Translation                       | Traduction des adresses IP internes vers une IP publique                |
| **VPN**          | Virtual Private Network                           | Tunnel sécurisé pour accéder à distance à un réseau                     |
| **WAF**          | Web Application Firewall                          | Filtre les requêtes HTTP pour protéger les applis web                   |
| **WPA/WEP**      | Wi-Fi Protected Access / Wired Equivalent Privacy | Protocoles de sécurité pour les réseaux Wi-Fi                           |
| **IPSec**        | Internet Protocol Security                        | Chiffrement de bout en bout au niveau IP, souvent pour les VPN          |
| **SD-WAN**       | Software-defined Wide Area Network                | Gestion intelligente du trafic réseau sur des WANs                      |

---

## 🛡️ **Threats & Attacks**

|Acronyme|Signification|Usage principal|
|---|---|---|
|**APT**|Advanced Persistent Threat|Attaque discrète et soutenue, souvent menée par un acteur étatique|
|**CSRF**|Cross-site Request Forgery|Exploite la confiance d’un site envers l’utilisateur authentifié|
|**MITM**|Man-in-the-Middle|Interception ou altération de communications|
|**SQLi**|SQL Injection|Insertion de commandes SQL malveillantes dans une requête|
|**XSS**|Cross-site Scripting|Injection de scripts malveillants dans une page web|
|**RAT**|Remote Access Trojan|Logiciel malveillant permettant un accès à distance non autorisé|
|**PUP**|Potentially Unwanted Program|Logiciel indésirable, souvent installé sans le consentement complet|
|**IoC**|Indicators of Compromise|Signes qu’un système pourrait être compromis|
|**ATT&CK**|Adversarial Tactics, Techniques, and Common Knowledge|Base de données MITRE des tactiques et techniques utilisées par les attaquants|

---

## 📏 **Security Frameworks & Standards** 

| Acronyme       | Signification                                | Usage principal                                                    |
| -------------- | -------------------------------------------- | ------------------------------------------------------------------ |
| **CIA**        | Confidentiality, Integrity, Availability     | Principes de base de la sécurité de l’information                  |
| **GDPR**       | General Data Protection Regulation           | Règlement européen sur la protection des données personnelles      |
| **ISO**        | International Standards Organization         | Organisation de normalisation (ex : ISO 27001)                     |
| **NIST**       | National Institute of Standards & Technology | Établit des standards de sécurité (ex : SP 800-53)                 |
| **PCI DSS**    | Payment Card Industry Data Security Standard | Norme pour sécuriser les paiements par carte bancaire              |
| **SOC**        | Security Operations Center                   | Équipe chargée de surveiller et répondre aux incidents de sécurité |
| **SIEM**       | Security Information and Event Management    | Outil centralisant et analysant les logs pour détecter des menaces |
| **Volatility** |                                              | Framework open-source de forensic mémoire                          |

---

## ☁️ **Cloud & Virtualization**

| Acronyme           | Signification                                 | Usage principal                                                                              |
| ------------------ | --------------------------------------------- | -------------------------------------------------------------------------------------------- |
| **CASB**           | Cloud Access Security Broker                  | Intermédiaire entre utilisateurs et services cloud pour appliquer les politiques de sécurité |
| **IaaS/PaaS/SaaS** | Infrastructure/Platform/Software as a Service | Modèles de services cloud                                                                    |
| **PaaS**           | Platform as a Service                         | Fourniture d’une plateforme de développement (runtime, bases de données) sans gérer l’infra  |
| **SaaS**           | Software as a Service                         | Accès à des applications complètes via un navigateur sans gestion de l’infrastructure        |
| **Xaas**           | Anything as a Service                         | Terme englobant tous les services fournis à la demande via le cloud                          |
| **SDN**            | Software-defined Networking                   | Gestion centralisée et automatisée du réseau via logiciel                                    |
| **VLAN**           | Virtual Local Area Network                    | Séparation logique de réseaux au sein d’un même réseau physique                              |
| **VM**             | Virtual Machine                               | Système d’exploitation isolé fonctionnant dans un environnement virtuel                      |
| **VDI**            | Virtual Desktop Infrastructure                | Accès à des postes de travail virtuels centralisés dans un datacenter                        |

---

## 🧯 **Incident Response & Recovery**

|Acronyme|Signification|Usage principal|
|---|---|---|
|**CERT**|Computer Emergency Response Team|Équipe spécialisée dans la réponse aux incidents de sécurité|
|**IRP**|Incident Response Plan|Plan détaillant les étapes à suivre en cas d’incident|
|**DRP**|Disaster Recovery Plan|Plan de reprise après sinistre (ex. panne, incendie)|
|**BCP**|Business Continuity Planning|Maintien des opérations critiques malgré une crise|
|**RPO/RTO**|Recovery Point/Time Objective|Limites acceptables de perte de données / temps d’arrêt|

---

## 🧱 **Hardware & Physical Security**

| Acronyme           | Signification                  | Usage principal                                                                                                                                                   |
| ------------------ | ------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **HSM**            | Hardware Security Module       | Matériel dédié à la gestion sécurisée des clés cryptographiques                                                                                                   |
| **TPM**            | Trusted Platform Module        | Composant matériel pour stocker des clés de chiffrement (ex : chiffrement disque)                                                                                 |
| **Secure Enclave** |                                | Zone physique sécurisée à l’intérieur d’un composant informatique (souvent un processeur) qui stocke et traite des données sensibles à l’abri du reste du système |
| **CCTV**           | Closed-circuit Television      | Surveillance vidéo locale pour la sécurité physique                                                                                                               |
| **FDE**            | Full Disk Encryption           | Chiffrement de l’intégralité d’un disque dur [[Niveau d'encryption]]                                                                                              |
| **SED**            | Self-encrypting Drives         | Disques durs avec chiffrement intégré matériellement [[Niveau d'encryption]]                                                                                      |
| **EFS**            | Windows Encrypting File System | Chiffre un ou plusieurs fichiers [[Niveau d'encryption]]                                                                                                          |
| **BitLocker**      |                                | Chiffre l'ensemble du disque dur ou de la partition, OS inclus [[Niveau d'encryption]]                                                                            |

---

## 📦 **Miscellaneous**

| Acronyme           | Signification                                                      | Usage principal                                                      |
| ------------------ | ------------------------------------------------------------------ | -------------------------------------------------------------------- |
| **BYOD/CYOD/COPE** | Bring/Choose Your Own Device / Corporate Owned, Personally Enabled | Politiques de gestion des appareils mobiles                          |
| **DLP**            | Data Loss Prevention                                               | Outils et techniques pour empêcher la fuite de données sensibles     |
| **PII/PHI**        | Personally Identifiable Information / Personal Health Information  | Données sensibles à protéger (fichiers médicaux ou d'identité)       |
| **SOAR**           | Security Orchestration, Automation, Response                       | Automatisation de la détection, réponse et remédiation aux incidents |
## 📊 **Vulnerability & Compliance Automation**

| Acronyme  | Signification                                         | Usage principal                                                  |
| --------- | ----------------------------------------------------- | ---------------------------------------------------------------- |
| **SCAP**  | Security Content Automation Protocol                  | Framework NIST pour l’automatisation des évaluations de sécurité |
| **CVE**   | Common Vulnerabilities and Exposures                  | Identifiants publics des vulnérabilités                          |
| **CVSS**  | Common Vulnerability Scoring System                   | Score de sévérité des vulnérabilités (0–10)                      |
| **OVAL**  | Open Vulnerability and Assessment Language            | Décrit des conditions de sécurité pour l’analyse automatique     |
| **XCCDF** | Extensible Configuration Checklist Description Format | Représente les checklists de configuration                       |
| **STIG**  | Security Technical Implementation Guide               | Guides de configuration sécurisée, souvent militaires            |
| **FISMA** | Federal Information Security Management Act           | Loi US encadrant la gestion de la sécurité de l’information      |
| **RMF**   | Risk Management Framework                             | Cadre NIST pour la gestion du risque et de la conformité         |

---

## 🧠 **Security Operations / Tools**

| Acronyme | Signification                      | Usage principal                                                              |
| -------- | ---------------------------------- | ---------------------------------------------------------------------------- |
| **EDR**  | Endpoint Detection and Response    | Surveillance avancée d'endpoints et réponse aux incidents                    |
| **UEBA** | User and Entity Behavior Analytics | Analyse des comportements suspects des utilisateurs/systèmes                 |
| **MDR**  | Managed Detection and Response     | Services externalisés de détection/traitement des menaces                    |
| **NGFW** | Next-Generation Firewall           | Pare-feu avec fonctions avancées (filtrage applicatif, inspection TLS, etc.) |
| **UTM**  | Unified Threat Management          | Appareil regroupant pare-feu, antivirus, IDS/IPS, etc.                       |

---

## 🧮 **Risk & Governance**

|Acronyme|Signification|Usage principal|
|---|---|---|
|**MTTR**|Mean Time To Repair|Temps moyen pour réparer un système après incident|
|**MTBF**|Mean Time Between Failures|Fiabilité estimée d’un système|
|**ALE**|Annualized Loss Expectancy|Coût annuel attendu d’un risque|
|**SLE**|Single Loss Expectancy|Perte attendue pour un seul incident|
|**ARO**|Annualized Rate of Occurrence|Fréquence annuelle estimée d’un événement|
|**BIA**|Business Impact Analysis|Analyse de l’impact potentiel d’un incident sur l’entreprise|

---

## 🧾 **Policy, Legal, and Privacy**

| Acronyme           | Signification                                          | Usage principal                                                                                      |
| ------------------ | ------------------------------------------------------ | ---------------------------------------------------------------------------------------------------- |
| **HIPAA**          | Health Insurance Portability and Accountability Act    | Réglementation US sur les données de santé                                                           |
| **SOX**            | Sarbanes-Oxley Act                                     | Loi US sur la conformité financière, incluant des exigences de sécurité                              |
| **FERPA**          | Family Educational Rights and Privacy Act              | Protection des données des étudiants aux États-Unis                                                  |
| **COPPA**          | Children’s Online Privacy Protection Act               | Règlement US sur la vie privée des enfants en ligne                                                  |
| **CCPA**           | California Consumer Privacy Act                        | Loi californienne sur la confidentialité (semblable au RGPD)                                         |
| **RGPD**           | Règlement Général sur la Protection des Données        | Données personnelles – **Union Européenne**, norme de référence mondiale                             |
| **PCI DSS**        | Payment Card Industry Data Security Standard           | Protection des données de **cartes bancaires** (monde entier, imposé par les fournisseurs de cartes) |
| **ISO/IEC 27001**  | International Organization for Standardization - 27001 | Norme internationale de gestion de la sécurité de l'information (ISMS)                               |
| **ISO/IEC 27701**  | Extension ISO 27001 sur la protection de la vie privée | Gestion des données personnelles, compatible avec RGPD et CCPA                                       |
| **NIST SP 800-53** | NIST Special Publication 800-53                        | Controles de securité pour les systèmes fédéraux (USA)                                               |
| **CSA CCM**        | Cloud Controls Matrix (Cloud Security Alliance)        | Cadre de sécurité pour les services cloud                                                            |
| **GLBA**           | Gramm-Leach-Bliley Act                                 | Confidentialité des données financières aux USA                                                      |

---

## 🧪 **Testing & Evaluation**

|Acronyme|Signification|Usage principal|
|---|---|---|
|**PT**|Penetration Testing|Simulation d’attaque pour tester la sécurité|
|**VA**|Vulnerability Assessment|Identification des failles sans exploitation active|
|**SOC 2**|Service Organization Control 2|Audit sur la sécurité et la confidentialité des services|
|**POC**|Proof of Concept|Démonstration de faisabilité (ex : exploit ou attaque réussie)|

---

## 🧯 **Incident Response Terms**

|Acronyme|Signification|Usage principal|
|---|---|---|
|**IOC**|Indicator of Compromise|Élément qui signale une infection ou intrusion probable|
|**TTP**|Tactics, Techniques, and Procedures|Méthodes typiques utilisées par les attaquants|
|**SIEM**|Security Information and Event Management|(Tu l’as déjà listé, mais c’est central ici aussi)|
## ==***Sécurité Physique :==***

## 🧱 **Physical Security Controls**

| Terme                                  | Traduction / Fonction                                                            |
| -------------------------------------- | -------------------------------------------------------------------------------- |
| **Tailgating**                         | Technique d'intrusion où une personne non autorisée suit une autre pour entrer   |
| **Mantrap**                            | Sas sécurisé à double porte empêchant l’entrée simultanée de plusieurs personnes |
| **Dumpster diving**                    | Recherche d’informations sensibles dans les poubelles                            |
| **Badging system**                     | Système d'accès utilisant des cartes ou badges d'identification                  |
| **Access control**                     | Contrôle d’accès physique ou logique basé sur autorisation                       |
| **Security guard**                     | Agent de sécurité physique contrôlant les accès et surveillant les lieux         |
| **Surveillance (CCTV)**                | Vidéosurveillance utilisée pour surveiller les zones sensibles                   |
| **Locked cabinet**                     | Armoire ou coffre sécurisé pour protéger les équipements ou documents            |
| **Air-gapped system**                  | Système totalement isolé des réseaux (aucune connexion Internet ou LAN)          |
| **Uninterruptible Power Supply (UPS)** | Alimentation de secours assurant la continuité du service en cas de panne        |
| **Fire suppression system**            | Système d’extinction automatique d’incendie (ex. gaz, mousse, sprinklers)        |

---

## ==***Termes Légaux :==***
| Acronyme | Signification                  | Description                                                                                                                                                                                                                                                                                |
| -------- | ------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **SLA**  | Service Level Agreement        | Contrat **formel** entre un fournisseur de services et un client, définissant le **niveau de service attendu** (disponibilité, temps de réponse, etc.).                                                                                                                                    |
| **MOU**  | Memorandum of Understanding    | Accord **non contraignant** entre deux parties pour **collaborer ou partager des ressources**. Moins formel qu’un contrat.                                                                                                                                                                 |
| **BPA**  | Business Partnership Agreement | Accord légal définissant la **relation entre deux entreprises partenaires**, incluant rôles, partages de revenus, responsabilités, etc.                                                                                                                                                    |
| **NDA**  | Non-disclosure agreement       | Contrat de **confidentialité** interdisant de divulguer des informations sensibles ou confidentielles.                                                                                                                                                                                     |
|          | Right to Audit clause          | Dans les contrats avec les fournisseurs, la clause de droit d'audit accorde à la partie acheteuse (« l’Acheteur ») le droit de réaliser des audits ou des évaluations des activités, des registres et de la performance du fournisseur afin de s'assurer du respect des termes du contrat. |



## ==***Protocoles Réseaux :==***

| Protocole  | Port par défaut     | Transport (TCP/UDP)                        | Usage principal                                  | Sécurité / Particularités                      |
| ---------- | ------------------- | ------------------------------------------ | ------------------------------------------------ | ---------------------------------------------- |
| **HTTP**   | 80                  | TCP                                        | Transfert de pages web non sécurisées            | Non chiffré, vulnérable à interception         |
| **HTTPS**  | 443                 | TCP                                        | Transfert web sécurisé (HTTP + TLS/SSL)          | Chiffrement, authentification serveur          |
| **FTP**    | 20 - 21             | TCP                                        | Transfert de fichiers                            | Non chiffré, vulnérable aux sniffers           |
| **SFTP**   | 22                  | TCP                                        | Transfert de fichiers sécurisé via SSH           | Chiffré, plus sûr que FTP                      |
| **SMTP**   | 25                  | TCP                                        | Envoi d’e-mails                                  | Souvent combiné avec TLS pour sécuriser        |
| **POP3**   | 110                 | TCP                                        | Récupération d’e-mails                           | Non sécurisé, POP3S sur 995 (TLS)              |
| **IMAP**   | 143                 | TCP                                        | Accès et gestion d’e-mails                       | Non sécurisé, IMAPS sur 993 (TLS)              |
| **DNS**    | 53                  | UDP (principal), TCP (pour transfert zone) | Résolution de noms de domaine                    | Peut être vulnérable sans DNSSEC               |
| **DHCP**   | 67/68               | UDP                                        | Attribution automatique d’adresses IP            | Important pour gestion réseau dynamique        |
| **SSH**    | 22                  | TCP                                        | Accès distant sécurisé                           | Chiffrement fort, remplace Telnet              |
| **Telnet** | 23                  | TCP                                        | Accès distant non sécurisé                       | Obsolète, transmet en clair                    |
| **RDP**    | 3389                | TCP                                        | Accès bureau à distance Microsoft                | Peut être sécurisé via VPN ou TLS              |
| **SNMP**   | 161/162             | UDP                                        | Gestion et monitoring des équipements réseau     | Versions 3+ avec chiffrement recommandé        |
| **LDAP**   | 389                 | TCP/UDP                                    | Accès aux annuaires d’entreprise                 | LDAPs (636) pour la sécurité via SSL/TLS       |
| **NTP**    | 123                 | UDP                                        | Synchronisation de l’heure réseau                | Peut être vecteur d’attaque si mal configuré   |
| **ICMP**   | N/A                 | Protocole IP                               | Contrôle et diagnostic réseau (ping, traceroute) | Utilisé pour tester la connectivité            |
| **BGP**    | 179                 | TCP                                        | Protocole de routage inter-domaines (Internet)   | Sensible aux attaques (ex : hijacking)         |
| **IPSec**  | N/A                 | IP (protocole 50/51)                       | Sécurisation du trafic IP (VPN)                  | Offre chiffrement et authentification          |
| **TLS**    | Variable (ex : 443) | TCP                                        | Sécurisation des communications                  | Successeur de SSL, protège la couche transport |

---
## ==***Gestion d'Incidents :==***

Les étapes dans l'ordre en cas d'incident type cyber-attaque :

**Préparation** : établir un plan d'incident-réponse et préparer les outils et ressources nécessaires
**Identification** :  détecter et confirmer la violation d'un protocole de sécurité
**Quarantaine** : isoler et restreindre les accès pour éviter la propagation
**Eradication** : supprimer la cause de l'incident (malware...) ou patcher les failles utilisées
**Réparation** : restaurer les systèmes affectés
**Tirer les conclusions** : analyser l'incident, localiser, interpréter et corriger


## ==***Fiches Techniques :==***

[[Honey Pot]]
[[DNS Hijacking]]
[[SSL TLS Downgrade]]
[[Zero Trust]]
[[Niveau d'encryption]]
[[Certificats]]
[[ACL]]
[[Stratégie de Sauvegarde et Récupération]]
[[Gap analysis]]
[[802.1X - RADIUS - TACACS+]]
[[Gestion risques, data et confidentialité, accords légaux, standards gouvernance et politique]]
## ==***Stade de Développement :==***

|**Stade**|**Objectif principal**|**Risques & Remarques**|
|---|---|---|
|**Development**|Écrire et construire le code.|- Failles fréquentes- Environnement peu sécurisé- Accès souvent large|
|**Test**|Vérifier les fonctionnalités, la sécurité, la performance.|- Données fictives ou anonymisées- Peut contenir du code non finalisé|
|**Staging / Pre-prod**|Réplication fidèle de la prod pour tests finaux|- Dernière étape avant déploiement- Doit être **quasi identique** à la prod|
|**Production**|Environnement actif utilisé par les utilisateurs finaux.|- Doit être **hautement sécurisé et stable**- Changements très contrôlés (Change Management)|
|**PoC (Proof of Concept)**|Démonstration technique de faisabilité ou prototype|- Code très instable- Non destiné à être mis en production|

## ==***Social Engineering :==***

| Technique            | Description                                                                                                                                                                          |
| -------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Diversion Theft**  | Créer une diversion pour profiter du désordre pour agir                                                                                                                              |
| **Hoaxes**           | Technique de manipulation où une personne ou un groupe diffuse de fausses informations dans le but de tromper, inquiéter, ou pousser les gens à agir d’une certaine manière          |
| **Shoulder Surfing** | Observer discrètement une personne qui rentre des informations confidentielles, ça peut etre en regardant par dessus son épaule ou par une caméra                                    |
| **Dumpster Diving**  | Fouiller les poubelles pour récupérer des informations qui n'auraient pas été détruites et jetées                                                                                    |
| **Eavesdropping**    | Ecouter discrètement une discussion qui ne nous concerne pas et qui pourraient révéler des informations confidentielles                                                              |
| **Baiting**          | Utiliser un leurre pour inciter une victime à faire une action qui compromet sa sécurité : brancher une clé USB malveillante, télécharger un fichier infecté, cliquer sur un lien... |
| **Piggybacking**     | Utiliser un leurre pour qu'une personne nous ouvre de son plein gré une porte verrouillée, exemple : se faire passer pour un livreur de pizzas qui doit livrer au 5ème étage.        |
| **Tailgating**       | Se glisser discrètement derrière une personne qui a déverrouillé une porte avec son badge                                                                                            |

| Technique          | Description                                                                                         |
| ------------------ | --------------------------------------------------------------------------------------------------- |
| **Spear phishing** | Cibler spécifiquement une personne définie pour du phishing                                         |
| **Whaling**        | Phishing mais qui cible spécifiquement des personnages avec beaucoup d'accès et beaucoup de pouvoir |


## ==***Contrôles de Sécurité :==***

| **Type de Security Control**             | **Définition**                                                         | **Exemples concrets**                                                                     |
| ---------------------------------------- | ---------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| **Preventive Security Control**          | Empêche les incidents avant qu'ils ne se produisent.                   | Pare-feu, contrôle d'accès, authentification à deux facteurs (2FA), mises à jour.         |
| **Detective Security Control**           | Détecte et alerte lorsqu’un incident survient.                         | IDS (Intrusion Detection System), journaux d’audit, caméras de surveillance.              |
| **Corrective Security Control**          | Rétablit les systèmes après un incident ou corrige les vulnérabilités. | Restaurations de sauvegardes, correctifs logiciels, procédures de réponse aux incidents.  |
| **Deterrent Security Control**           | Dissuade un acteur malveillant d’agir.                                 | Panneaux de vidéosurveillance, avertissements juridiques, présence de gardes de sécurité. |
| **Compensating Security Control**        | Remplace ou compense un contrôle manquant ou non applicable.           | Revue manuelle des logs en l’absence d’un SIEM, restrictions réseau en l'absence de 2FA.  |
| **Physical Security Control**            | Empêche l’accès physique non autorisé aux ressources.                  | Serrures, barrières, badges, cartes magnétiques, cages Faraday.                           |
| **Administrative (Managerial) Control**  | Définit les politiques, les procédures et les formations.              | Politique de sécurité, plan de continuité, formations de sensibilisation.                 |
| **Technical (Logical) Security Control** | Implémenté par des moyens technologiques.                              | Antivirus, chiffrement, contrôle d’accès basé sur les rôles (RBAC), DLP.                  |
| **[[Control Plane]]**                    | Cerveau du modèle Zero Trust                                           |                                                                                           |

| Catégories  |
| ----------- |
| Technical   |
| Managerial  |
| Operational |
| Physical    |

## ==***Gestion des données :==***

- **Data Controller** : décide pourquoi et comment les données sont traitées (ex. direction d’entreprise).

- **Data Custodian** : admin technique, gère la protection et la maintenance (sauvegardes, sécurité), typiquement technicien IT.

- **Data Subject** : la personne concernée par les données (le client, l’utilisateur).

- **Data Processor** : traite les données au nom du contrôleur (prestataire externe, sous-traitant).
---
- **Controller** = décide du _pourquoi_ et du _comment_.
    
- **Processor** = exécute pour le compte du controller, ne décide pas de l’usage final.
    
- **Custodian** = garde technique des données, gère la sécurité et la maintenance.
    
- **Subject** = personne concernée par les données.

![[Pasted image 20250812160016.png]]

[^1]: 
