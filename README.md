# 42-Netpractice

## TCP/IP
```
Ensemble de protocoles de communication utilisé pour interconnecter des appareils sur Internet.
TCP (Transmission Control Protocol) assure la livraison fiable des données.
IP (Internet Protocol) gère l'acheminement des paquets de données.
```

## Masque sous-reseau
```
Définit la taille d'un réseau et séparent l'adresse IP en réseau et en partie hôte.
Cela aide à organiser un grand réseau en plus petits sous-réseaux pour améliorer la gestion et la sécurité.
```

## CIDR(Classless Inter-Domain Routing)
```
Méthode pour allouer des adresses IP et router les messages.
Remplace l'ancien système de classes d'adresses IP, permettant une allocation plus flexible et efficace des adresses IP.
```

## Adresse IP
```
Numéro unique attribué à chaque appareil sur un réseau.
Fonctionne comme une adresse postale, permettant de localiser et d'identifier les appareils sur le réseau.

Les adresses IP privées sont des plages d'adresses réservées pour être utilisées uniquement au sein de réseaux privés.
Elles ne sont pas routables sur Internet.
Voici les plages :
    10.0.0.0 à 10.255.255.255 : Cette plage est souvent utilisée dans les grands réseaux internes.

    172.16.0.0 à 172.31.255.255 : Plage intermédiaire, utilisée dans les réseaux de taille moyenne.

    192.168.0.0 à 192.168.255.255 : Couramment utilisée dans les réseaux domestiques et les petites entreprises.
```

## Trouver l'adresse reseau
```
    Exemple 1 :
        Adresse IP : 192.168.100.14
        Masque de sous-réseau : 255.255.255.0 (en binaire : 11111111.11111111.11111111.00000000)
        L'adresse réseau sera 192.168.100.0, car la partie hôte (les derniers 8 bits) est mise à zéro.

    Exemple 2 :
        Adresse IP : 10.0.5.25
        Masque de sous-réseau : 255.255.0.0 (en binaire : 11111111.11111111.00000000.00000000)
        L'adresse réseau sera 10.0.0.0, car les 16 derniers bits (partie hôte) sont mis à zéro.

Dans ces exemples, l'opération de "ET logique" entre l'adresse IP et le masque de sous-réseau détermine quelle partie de l'adresse IP
appartient au réseau et met les autres bits (de la partie hôte) à zéro pour obtenir l'adresse réseau.
```
