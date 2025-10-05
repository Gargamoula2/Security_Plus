[[Security+]]
#### **1. Définition**  
- **ACL (Access Control List)** : Liste de règles définissant les permissions d'accès à une ressource (fichier, réseau, périphérique).  
- **Objectif** : Contrôler qui peut **lire, écrire, exécuter** ou **accéder** à une ressource.  

---

#### **2. Types d'ACL**  

| **Type**                    | **Description**                                                             | **Exemple**                                              |
| --------------------------- | --------------------------------------------------------------------------- | -------------------------------------------------------- |
| **ACL Réseau**              | Filtrage des paquets basé sur des règles (IP, port, protocole).             | Bloquer le trafic SSH depuis une IP étrangère.           |
| **ACL Système de Fichiers** | Gère les droits d'accès aux fichiers/dossiers (lecture/écriture/exécution). | `chmod 750 script.sh`                                    |
| **ACL Router/Firewall**     | Règles de trafic entrant/sortant (ex : NAT, filtrage).                      | Autoriser le trafic HTTP uniquement vers le serveur web. |

---

#### **3. Composants d'une ACL Réseau**  
- **Source/Destination** : Adresse IP, plage d’IP.  
- **Port/Protocole** : TCP/UDP, numéro de port (ex : 80 pour HTTP).  
- **Action** : `PERMIT` (autoriser) ou `DENY` (refuser).  
- **Ordre des règles** : Les ACL sont évaluées **de haut en bas** (la première règle correspondante est appliquée).  

**Exemple (Cisco Router)** :  
```bash
access-list 100 deny tcp 192.168.1.0 0.0.0.255 any eq 22  
access-list 100 permit ip any any  
```  
→ Bloque le SSH depuis le réseau `192.168.1.0/24`, autorise tout le reste.  

---

#### **4. Bonnes Pratiques**  
- **Principe du moindre privilège** : Ne donner que les accès nécessaires.  
- **Ordre logique** : Placer les règles les plus spécifiques en haut.  
- **Journalisation (Logging)** : Logger les accès refusés pour analyse.  
- **Révision régulière** : Supprimer les règles obsolètes.  

---

#### **5. ACL vs RBAC (Role-Based Access Control)**  
| **Critère**     | **ACL**                      | **RBAC**                                      |
| --------------- | ---------------------------- | --------------------------------------------- |
| **Granularité** | Gestion par ressource/règle. | Gestion par rôle utilisateur.                 |
| **Évolutivité** | Complexe à grande échelle.   | Adapté aux grandes organisations.             |

---

**À retenir** :  
- **ACL réseau** = Pare-feu basique.  
- **ACL fichiers** = Sécurité Linux/Windows.  
- **Implicite DENY** : Si aucune règle ne correspond, l’accès est refusé.  

📌 **Exemple concret** :  
- Un serveur web :  
  - ACL réseau : `Autoriser TCP 443 (HTTPS), Refuser tout le reste`.  
  - ACL fichiers : `/var/www/` : RW pour l’utilisateur `www-data`, RX pour les autres.  
