
---

# Fonctionnement du protocole ARP

Le protocole ARP (Address Resolution Protocol) est utilisé dans les réseaux informatiques pour associer une adresse IP à une adresse MAC. Voici comment il fonctionne de manière générale :

## 1. Requête ARP

- Lorsqu'un appareil A souhaite communiquer avec un autre appareil B sur le réseau local et qu'il connaît l'adresse IP de B mais pas son adresse MAC, il envoie une requête ARP de type *ARP Request*.
- Cette requête contient l'adresse IP de B et l'adresse MAC de A.
- La requête ARP est diffusée sur le réseau local pour que tous les appareils puissent la recevoir.

## 2. Réponse ARP

- Lorsque l'appareil B reçoit la requête ARP, il vérifie si l'adresse IP à laquelle la requête est destinée correspond à la sienne.
- Si c'est le cas, l'appareil B répond avec un message ARP de type *ARP Reply*.
- Ce message contient son adresse IP et son adresse MAC.
- La réponse ARP est envoyée directement à l'appareil A qui a émis la requête ARP.

## 3. Mise en cache

- Une fois que l'appareil A reçoit la réponse ARP, il met à jour sa table ARP en associant l'adresse IP de B à son adresse MAC.
- Cette information est mise en cache pour une utilisation future afin d'éviter de devoir refaire la procédure ARP pour chaque communication ultérieure avec B.

## Conclusion

Le protocole ARP permet donc aux appareils d'un réseau local de résoudre les adresses IP en adresses MAC, facilitant ainsi la communication entre eux. Cependant, comme les informations ARP sont stockées en cache, il est important de garder à l'esprit que ces tables peuvent devenir obsolètes et nécessiter une mise à jour périodique.

---
