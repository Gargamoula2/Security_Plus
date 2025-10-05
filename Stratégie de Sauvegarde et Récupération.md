[[Security+]]
#### **1. Définition**

Les **sauvegardes (backups)** sont des copies sécurisées de données critiques, permettant leur récupération en cas de perte, corruption ou cyberattaque (ex : ransomware).

---

#### **2. Concepts Clés**

|**Terme**|**Description**|**Exemple/Best Practice**|
|---|---|---|
|**Onsite/Offsite**|- **Onsite** : Sauvegardes locales (ex : NAS). Rapide à restaurer, mais vulnérable aux désastres physiques (incendie).  <br>- **Offsite** : Sauvegardes externes (cloud, coffre-fort). Résilient mais dépendant de la connexion réseau.|Utiliser une combinaison **onsite (pour la rapidité) + offsite (pour la résilience)**.|
|**Frequency**|Fréquence des sauvegardes (horaire, quotidienne, hebdomadaire).  <br>- **RPO (Recovery Point Objective)** : Tolérance à la perte de données (ex : sauvegarde toutes les 24h = RPO de 24h).|Bases de données : sauvegarde **incrémentielle toutes les 4h**.|
|**Encryption**|Chiffrement des sauvegardes pour protéger contre les accès non autorisés.|Utiliser AES-256 pour les sauvegardes cloud.|
|**Snapshots**|Capture instantanée d'un système à un instant T (ex : état d'une VM).  <br>- Différent d'une sauvegarde : dépend du stockage source.|VMware/Kubernetes : snapshots **quotidiens** avec rétention de 7 jours.|
|**Recovery**|Processus de restauration des données.  <br>- **RTO (Recovery Time Objective)** : Temps maximal acceptable pour la récupération.|Test annuel de restauration pour valider les backups.|
|**Replication**|Copie en temps réel des données vers un autre système (haute disponibilité).  <br>- **Synchrone** : Écriture simultanée (ex : bases de données financières).  <br>- **Asynchrone** : Délai acceptable (ex : fichiers non critiques).|SQL Server Always-On (réplication synchrone).|
|**Journaling**|Journal des modifications (ex : bases de données, systèmes de fichiers). Permet une récupération précise.|MongoDB : **Oplog** pour restaurer jusqu'à une transaction spécifique.|

---

#### **3. Stratégies de Sauvegarde**

- **Full Backup** : Copie complète (longue mais simple à restaurer).
    
- **Incremental** : Sauvegarde uniquement les changements depuis la dernière backup (rapide, mais restauration complexe).
    
- **Differential** : Sauvegarde les changements depuis la dernière backup **complète** (équilibre entre stockage et temps de restauration).
    

**Exemple** :

- **Lundi** : Full Backup.
    
- **Mardi-Vendredi** : Incremental.
    
- **Restauration** : Nécessite la full + toutes les incrementales.
    

---

#### **4. Bonnes Pratiques**

- **Règle 3-2-1** :
    
    - 3 copies des données.
        
    - 2 supports différents (ex : disque + cloud).
        
    - 1 copie offsite.
        
- **Test régulier** des restaurations.
    
- **Air Gap** : Sauvegardes déconnectées du réseau (protection contre les ransomwares).


**À retenir** :

- **Onsite + Offsite** = Résilience.
    
- **RPO/RTO** = Critères de planification.
    
- **3-2-1 Rule** = Standard industriel.
    

📌 **Exemple concret** :  
Une banque utilise :

- **Réplication synchrone** pour les transactions.
    
- **Snapshots horaires** des VMs.
    
- **Sauvegardes chiffrées** air-gapped (hors réseau).