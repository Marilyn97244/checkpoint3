# Exercice 1 : Manipulations pratiques sur VM Windows 

## Partie 1 : Gestion des utilisateurs

- Q.1.1.1 Créer l'utilisateur Lionel Lemarchand avec les même attribut de société que Kelly Rhameur.
![Description de l'image](images/lionel.png)

![Description de l'image](images/lionel1.png)

![Description de l'image](images/lionel2.png)

![Description de l'image](images/lionel3.png)

![Description de l'image](images/lionel4.png)

![Description de l'image](images/exo1.2.png)


- Q.1.1.2 Créer une OU DeactivatedUsers et déplace le compte désactivé de Kelly Rhameur dedans.

  ![Description de l'image](images/OU1.png)

  ![Description de l'image](images/OU3.png)

  ![Description de l'image](images/OU5.png)



- Q.1.1.3 Modifier le groupe de l'OU dans laquelle était Kelly Rhameur en conséquence.

  ![Description de l'image]( images/SUPK.png)
  
  ![Description de l'image](images/KYL1.png)



- Q.1.1.4 Créer le dossier Individuel du nouvel utilisateur et archive celui de Kelly Rhameur en le suffixant par -ARCHIVE.

   ![Description de l'image](images/ARCHIVE.png)

## Partie 2 : Restriction utilisateurs

- Q.1.2.1 Faire en sorte que l'utilisateur Gabriel Ghul ne puisse se connecter que du lundi au vendredi, de 7h à 17h.

  ![Description de l'image](images/GABI1.png)


- Q.1.2.2 De même, bloquer sa connexion au seul ordinateur CLIENT01.

    ![Description de l'image](images/GABI2.png)
  
- Q.1.2.3 Mettre en place une stratégie de mot de passe pour durcir les comptes des utilisateurs de l'OU LabUsers.
Partie 3 : Lecteurs réseaux

  ![Description de l'image](images/durciMdp.png)

  ![Description de l'image](images/mdp1.png)

- Q.1.3.1 Créer une GPO Drive-Mount qui monte les lecteurs E: et F: sur les clients.

   ![Description de l'image](images/E.png)

   ![Description de l'image](images/F.png)

   ![Description de l'image](images/FE.png)

   ![Description de l'image](images/upd.png)

   ![Description de l'image](images/upd2.png)
  

# Exercice 2:Manipulations pratiques sur VM Linux

## Partie 1:Gestion des utilisateurs

 - Q.2.1.1 Sur le serveur, créer un compte pour ton usage personnel.
  ![Description de l'image](images/mdp.png)
   

 - Q.2.1.2 Quelles préconisations proposes-tu concernant ce compte ?

    - Minimum 12 caractères.
    - Mettre des majuscules, minuscules, chiffres, et caractères spéciaux
    - Ne pas donner des droits sudo
    - Utiliser une clé SSH pour l'accès distant


## Partie 2 : Configuration de SSH

 - Q.2.2.1 Désactiver complètement l'accès à distance de l'utilisateur root.

  ![Description de l'image]( images/root1.png)
  
  ![Description de l'image](images/root2.png)

- Q.2.2.2 Autoriser l'accès à distance à ton compte personnel uniquement.
  
 ![Description de l'image](images/root3.png)

 ![Description de l'image]( images/root4.png )

- Q.2.2.3 Mettre en place une authentification par clé valide et désactiver l'authentification par mot de passe
  
 ![Description de l'image](images/ssh1.png)

 ![Description de l'image](images/auth.png)
 
## Partie 3 : Analyse du stockage

- Q.2.3.1 Quels sont les systèmes de fichiers actuellement montés ?
- 
   ![Description de l'image](images/DF.png)

- Q.2.3.2 Quel type de système de stockage ils utilisent ?
  
 ![Description de l'image](images/lsblk.png)
 
- Q.2.3.3 Ajouter un nouveau disque de 8,00 Gio au serveur et réparer le volume RAID

- Q.2.3.4 Ajouter un nouveau volume logique LVM de 2 Gio qui servira à héberger des sauvegardes. Ce volume doit être monté automatiquement à chaque démarrage dans l'emplacement par défaut : /var/lib/bareos/storage.

- Q.2.3.5 Combien d'espace disponible reste-t-il dans le groupe de volume ?

## Partie 4 : Sauvegardes

- Q.2.4.1 Expliquer succinctement les rôles respectifs des 3 composants bareos installés sur la VM.

## Partie 5 : Filtrage et analyse réseau

- Q.2.5.1 Quelles sont actuellement les règles appliquées sur Netfilter ?

- Q.2.5.2 Quels types de communications sont autorisées ?

- Q.2.5.3 Quels types sont interdit ?

- Q.2.5.4 Sur nftables, ajouter les règles nécessaires pour autoriser bareos à communiquer avec les clients bareos potentiellement présents sur l'ensemble des machines du réseau local sur lequel se trouve le serveur.

## Partie 6 : Analyse de logs

- Q.2.6.1 Lister les 10 derniers échecs de connexion ayant eu lieu sur le serveur en indiquant pour chacun :

    La date et l'heure de la tentative
    L'adresse IP de la machine ayant fait la tentative


  
