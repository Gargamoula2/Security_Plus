[[Security+]]
#### **1. Niveaux de Chiffrement**

|**Niveau**|**Description**|**Exemple d'Utilisation**|**Outils/Technologies**|
|---|---|---|---|
|**Full-Disk (FDE)**|Chiffre l'intégralité du disque dur, y compris le système d'exploitation.|Protéger les données en cas de vol d'ordinateur portable.|BitLocker (Windows), FileVault (macOS), LUKS (Linux).|
|**Partition**|Chiffre une partition spécifique du disque (pas tout le disque).|Isoler des données sensibles sur une partie du stockage.|VeraCrypt, dm-crypt (Linux).|
|**File**|Chiffre des fichiers individuels.|Envoyer un document confidentiel par email.|PGP/GPG, 7-Zip (AES).|
|**Volume**|Chiffre un volume logique (ex : disque externe, clé USB).|Sécuriser une clé USB contenant des données médicales.|BitLocker To Go, VeraCrypt.|
|**Database**|Chiffre une base de données entière (tables, schémas).|Protéger les données clients dans un SGBD.|TDE (Transparent Data Encryption) dans SQL Server, Oracle.|
|**Record**|Chiffre des enregistrements ou champs spécifiques dans une base de données.|Masquer les numéros de sécurité sociale (SSN) dans une table.|Chiffrement au niveau colonne (SQL), MongoDB Field-Level Encryption.|

---

#### **2. Comparaison des Niveaux**

|**Critère**|**Full-Disk**|**Partition/Volume**|**File/Record**|
|---|---|---|---|
|**Granularité**|Élevée (tout le disque)|Moyenne (section)|Fine (fichier/champ)|
|**Performance**|Impact modéré|Impact variable|Faible impact|
|**Cas d'Usage**|Vol de périphérique|Données isolées|Données spécifiques|

---

#### **3. Bonnes Pratiques**

- **Full-Disk** : Essentiel pour les appareils mobiles (PC portables).
    
- **File/Record** : Idéal pour les données hautement sensibles (ex : PII).
    
- **Database** : Combiner TDE (chiffrement global) et chiffrement au niveau champ pour une défense en profondeur.



**À retenir** :

- **Full-Disk** = Sécurité globale.
    
- **File/Record** = Précision.
    
- **Database** = Protection des SGBD.
    

📌 **Exemple concret** : Un hôpital utilise :

- **Full-Disk** sur les postes administratifs.
    
- **Record** pour les dossiers patients.
    
- **Volume** sur les clés USB des médecins.