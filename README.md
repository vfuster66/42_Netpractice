# 42-Netpractice

### TCP/IP
```
Ensemble de protocoles de communication utilisé pour interconnecter des appareils sur Internet.
TCP (Transmission Control Protocol) assure la livraison fiable des données.
IP (Internet Protocol) gère l'acheminement des paquets de données.
```

### Masque sous-reseau
```
Définit la taille d'un réseau et séparent l'adresse IP en réseau et en partie hôte.
Cela aide à organiser un grand réseau en plus petits sous-réseaux pour améliorer la gestion et la sécurité.
```

### CIDR(Classless Inter-Domain Routing)
```
Méthode pour allouer des adresses IP et router les messages.
Remplace l'ancien système de classes d'adresses IP, permettant une allocation plus flexible et efficace des adresses IP.

    /32 : 255.255.255.255 (Un seul hôte)
    /31 : 255.255.255.254 (Deux hôtes)
    /30 : 255.255.255.252 (Quatre hôtes)
    /29 : 255.255.255.248 (Huit hôtes)
    /28 : 255.255.255.240 (Seize hôtes)
    /27 : 255.255.255.224 (32 hôtes)
    /26 : 255.255.255.192 (64 hôtes)
    /25 : 255.255.255.128 (128 hôtes)
    /24 : 255.255.255.0 (256 hôtes)
    /23 : 255.255.254.0 (512 hôtes)
    /22 : 255.255.252.0 (1024 hôtes)
    /21 : 255.255.248.0 (2048 hôtes)
    /20 : 255.255.240.0 (4096 hôtes)
    /19 : 255.255.224.0 (8192 hôtes)
    /18 : 255.255.192.0 (16384 hôtes)
    /17 : 255.255.128.0 (32768 hôtes)
    /16 : 255.255.0.0 (65536 hôtes)
    /15 : 255.254.0.0 (131072 hôtes)
    /14 : 255.252.0.0 (262144 hôtes)
    /13 : 255.248.0.0 (524288 hôtes)
    /12 : 255.240.0.0 (1048576 hôtes)
    /11 : 255.224.0.0 (2097152 hôtes)
    /10 : 255.192.0.0 (4194304 hôtes)
    /9 : 255.128.0.0 (8388608 hôtes)
    /8 : 255.0.0.0 (16777216 hôtes)

Chaque "slash" suivi d'un nombre indique combien de bits du masque de sous-réseau sont définis sur 1.
Plus le nombre après le slash est élevé, plus le nombre d'hôtes dans le sous-réseau est petit.
```

### Adresse IP
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

### Trouver l'adresse reseau
```
    Exemple 1 :
        Adresse IP : 192.168.100.14
        Masque de sous-réseau : 255.255.255.0 (en binaire : 11111111.11111111.11111111.00000000)
        L'adresse réseau sera 192.168.100.0, car la partie hôte (les derniers 8 bits) est mise à zéro.

    Exemple 2 :
        Adresse IP : 10.0.5.25
        Masque de sous-réseau : 255.255.0.0 (en binaire : 11111111.11111111.00000000.00000000)
        L'adresse réseau sera 10.0.0.0, car les 16 derniers bits (partie hôte) sont mis à zéro.

Dans ces exemples, l'opération de "ET logique" entre l'adresse IP et le masque de sous-réseau détermine
quelle partie de l'adresse IP appartient au réseau et met les autres bits (de la partie hôte) à zéro
pour obtenir l'adresse réseau.
```

### Switch
```
Appareil de réseau utilisé pour connecter plusieurs appareils dans un réseau local (LAN).
Reçoit des paquets de données d'un appareil et les transmet uniquement à l'appareil de destination,
améliorant ainsi l'efficacité et la sécurité du réseau.
```

### Routeur
```
Dispositif de réseau qui connecte plusieurs réseaux, typiquement un réseau local (LAN)
et un réseau étendu (WAN) comme Internet.
Dirige le trafic de données en déterminant le meilleur chemin pour chaque paquet de données, grâce à des tables de routage.
Joue un rôle crucial dans le transfert de données entre différents réseaux et assure la sécurité en filtrant le trafic.
Peut également attribuer des adresses IP locales aux appareils du réseau.
```

### Table de routage
```
Ensemble de règles dans un routeur qui détermine le chemin le plus approprié pour acheminer les paquets de données vers leur destination.
Chaque entrée de la table de routage contient au moins la destination (souvent une plage d'adresses IP), le masque de sous-réseau,
la passerelle (le prochain saut vers la destination), et parfois l'interface réseau à utiliser.
La table de routage est utilisée pour décider si un paquet doit être envoyé à un autre réseau ou s'il appartient au réseau local.
```
