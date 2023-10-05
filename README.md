# Découpage réseaux
_______
###Découpage réseaux symétrique
_______
Réseaux: 172.16.1.0/24    
Le Pôle informatique: 50 équipements au total; Découpage symétrique donc on se base sur le plus grand sous réseaux    
Le Pôle développement: 12 équipements au total  
Le Pôle Administratif: 20 équipements au total  
Le Pôle Technicien: 15 équipements au total  
50 équipements--> 2^6 = 64-2 (adressage réseaux et diffusion) = 62  
**CIDR** = 64 - 6 (car 2^6)=**56**

|  Pôles | Adresse réseaux | Adresse de broadcast | Adresse de début de plage | Adresse de fin de plage|
|:-------------:|:---------------:|:--------------------:|:-------------------------:|:----------------------:|
|**Pôle informatique**| 172.16.1.0/27   | 172.16.1.63    |       172.16.1.1        |            172.16.1.62|
|**Pôle dévellopement**| 172.168.1.64/27| 172.16.1.127   |       172.16.1.65     |      172.16.1.126|
|
