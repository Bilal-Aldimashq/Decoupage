# Découpage réseaux
_______
### Découpage réseaux symétrique
_______
Réseaux: 172.16.1.0/24    
Le Pôle informatique: 50 équipements au total; Découpage symétrique donc on se base sur le plus grand sous réseaux    
Le Pôle développement: 12 équipements au total  
Le Pôle Administratif: 20 équipements au total  
Le Pôle Technicien: 15 équipements au total  
50 équipements--> 2^6 = 64-2 (adressage réseaux et diffusion) = 62  
**CIDR** = 32 - 6 (car 2^6)=**26**

|  Pôles | Adresse réseaux | Adresse de broadcast | Adresse de début de plage | Adresse de fin de plage|
|:-------------:|:---------------:|:--------------------:|:-------------------------:|:----------------------:|
|**Pôle informatique**| 172.16.1.0/26   | 172.16.1.63    |       172.16.1.1        |            172.16.1.62|
|**Pôle dévellopement**| 172.168.1.64/26| 172.16.1.127   |       172.16.1.65     |      172.16.1.126|
|**Pôle administratif**  | 172.16.1.128/26 | 172.16.1.191  |     172.16.1.129      |   172.16.1.190   |
|**Pôle technicien**   | 172.16.1.192/26  |  172.16.1.255   | 172.16.1.193      |     172.16.1.255    |


_______________

### Découpage asymétrique
___________
Réseaux: 172.16.1.0/24      
Le Pôle informatique: 50 équipements au total: 2^6 = 64-2 ( Adressage réseaux et diffusion)= 62; CIDR= 32-6= 26     
Le Pôle Administratif: 20 équipements au total: 2^5= 32-2= 30; CIDR= 32-5= 27    
Le Pôle Technicien: 15 équipements au total: 2^5= 32-2= 30; CIDR= 32-5= 27    
Le Pôle développement: 12 équipements au total: 2^4 = 16-2= 14; CIDR= 32-4= 28  


 |  Pôles | Adresse réseaux | Adresse de broadcast | Adresse de début de plage | Adresse de fin de plage|
|:--------------------:|:---------------:|:--------------------:|:-------------------------:|:----------------------:|
|**Pôle informatique** | 172.16.1.0/26   |  172.16.1.63   |        172.16.1.1   |     172.16.1.62   |
|**Pôle administratif**  | 172.16.1.64/27  | 172.16.1.95  |    172.16.1.65   |    172.16.1.94  |
|**Pôle technicien**  | 172.16.1.95/27  | 172.16.1.127 |  172.16.1.96  |    172.16.1.126  |
|**Pôle développement**   | 172.16.1.128/28  |  172.16.1.143  | 172.16.1.129  |   172.16.1.142  |
