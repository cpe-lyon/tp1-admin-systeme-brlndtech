# Compte rendu TP 1 - Linux | Geoffrey Sauvageot-Berland

## Partie 1 | 

### Q1 : A l’aide du manuel, identifiez le rôle de la commande which ? 

-> La commande which permet de connaître l'emplacement d'un programme.

 which  renvoie  le chemin des fichiers (ou liens) qui seraient exécutés
       dans l'environnement courant si ses arguments avaient été donnés  comme
       commandes  dans un interpréteur de commandes strictement conforme à PO‐
       SIX. Pour ce faire, which cherche dans la variable  PATH  les  fichiers
       exécutables  correspondant  aux  noms des arguments. which ne normalise
       pas les chemins.

### Q2 : Quand on consulte cette page, comment peut-on rechercher, par exemple, le mot option? 

-> <code> man which </code>
   <code> / option </code>

   " si une option non valable est spécifiée. " 

### Q3 Comment quitte-t-on le manuel ?

-> Simplement en tappant sur q ou ctrl c 

### Q4 : Chaque section du manuel a une première page, qui présente le contenu de la section. Aﬀicher la première page de la section 6; de quoi parle cette section?

man 6 intro 

## Partie 2 | 

### Q1-5
<code> -bash: cd: /root: Permission denied </code>
Nous sommes connécté en utilisateur standard, il faut se connecter en root pour pouvoir accéder à son dossier (/root) 

### Q6 

Le mot de passe de l'utilisateur actuel est demandé <...>
Mais ils nous ai impossible d'accéder au dossier /root, car nous devons nous connecter en root; 

### Q7-8 revenez dans votre dossier personnel  à l’aide de la commande rm, essayez de supprimer Fichier1, puis Dossier1  que se passe-t-il? 

le fichier va pouvoir se supprimer, mais le dossier non CAR pour supprimer un dossier il faut passer par la commande rm -r (repository) Dossier1

### Q9 

<code> rm -r <dossier> </code>

### Q10 

Bizarrement ça marche 

### Q11 

<code> cd Dossier2 </code> <br>
<code> rm -r * </code>
