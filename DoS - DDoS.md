[[Security+]]
### DDoS Amplifié (Amplification)

- **Principe** : L’attaquant envoie une petite requête à un serveur mal configuré ou un service ouvert, qui va lui renvoyer une réponse **beaucoup plus grande** que la requête initiale.
    
- **Effet** : Avec peu de trafic envoyé, l’attaquant provoque un **flux massif** vers la cible, en exploitant la différence de taille entre requête et réponse.
    
- **Exemple courant** : Utiliser des serveurs DNS ouverts pour envoyer une petite requête DNS, qui génère une grosse réponse vers la cible.
    
- **But** : Saturer la bande passante ou les ressources du serveur ciblé avec un trafic amplifié.


---

### DDoS Réfléchi (Reflection)

- **Principe** : L’attaquant envoie une requête à un serveur tiers en **usurpant l’adresse IP de la victime**.
    
- **Effet** : Le serveur tiers renvoie sa réponse directement à la victime (qui ne s’y attend pas), ce qui provoque une **attaque indirecte** via ces serveurs.
    
- **Souvent combiné avec amplification** : Les attaques dites "amplifiées réfléchies" utilisent la réflexion ET l’amplification pour maximiser l’impact.
    
- **Exemple** : Envoyer une requête DNS à un serveur DNS ouvert, mais avec l’IP source modifiée (spoofée) pour qu’elle pointe vers la cible. Le serveur DNS répond alors à la cible, non à l’attaquant.

---

### En résumé

|Attaque|Fonctionnement|Objectif|
|---|---|---|
|DDoS Amplifié|Exploiter un protocole qui renvoie une réponse plus grosse que la requête|Amplifier le volume de trafic|
|DDoS Réfléchi|Usurper l’IP de la victime pour faire renvoyer des réponses par des serveurs tiers|Faire arriver le trafic à la victime via des intermédiaires|