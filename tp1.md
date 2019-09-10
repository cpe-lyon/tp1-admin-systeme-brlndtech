# Compte rendu TP1  <img src="https://image.flaticon.com/icons/svg/518/518713.svg" height="50" alt="Zozor" /> | Geoffrey Sauvageot-Berland 

## Partie 1 | 

### **Q1 : A l’aide du manuel, identifiez le rôle de la commande which ?**

-> La commande which permet de connaître l'emplacement d'un programme.

 which  renvoie  le chemin des fichiers (ou liens) qui seraient exécutés
       dans l'environnement courant si ses arguments avaient été donnés  comme
       commandes  dans un interpréteur de commandes strictement conforme à PO‐
       SIX. Pour ce faire, which cherche dans la variable  PATH  les  fichiers
       exécutables  correspondant  aux  noms des arguments. which ne normalise
       pas les chemins.

### **Q2 : Quand on consulte cette page, comment peut-on rechercher, par exemple, le mot option ?**

-> <code> man which </code>
   <code> / option </code>

   " si une option non valable est spécifiée. " 

### **Q3 Comment quitte-t-on le manuel ?**

-> Simplement en tappant sur q ou ctrl c 

### **Q4 : Chaque section du manuel a une première page, qui présente le contenu de la section. Aﬀicher la première page de la section 6; de quoi parle cette section?**

man 6 intro 

## Partie 2 | 

### **Q1-5**
<code> -bash: cd: /root: Permission denied </code>
Nous sommes connécté en utilisateur standard, il faut se connecter en root pour pouvoir accéder à son dossier (/root) 

### **Q6 essayez la commande sudo cd /root; que se passe-t-il? Expliquez**

Le mot de passe de l'utilisateur actuel est demandé <...>
Mais ils nous ai impossible d'accéder au dossier /root, car nous devons nous connecter en root; 

### **Q7-8 revenez dans votre dossier personnel  à l’aide de la commande rm, essayez de supprimer Fichier1, puis Dossier1  que se passe-t-il?**

le fichier va pouvoir se supprimer, mais le dossier non CAR pour supprimer un dossier il faut passer par la commande rm -r (repository) Dossier1

### **Q9 quelle commande permet de supprimer un dossier?**

<code> rm -r dossier </code>

### **Q10 que se passe-t-il quand on applique cette commande à Dossier2? il dit que le dosssier n'est pas vide donc impossible a supprimer**

Bizarrement ça marche 

### **Q11 comment supprimer en une seule commande Dossier2 et son contenu**

<code> cd Dossier2 </code> <br>
<code> rm -r * </code>

## PARTIE 3 Commande Importante 

### **Q1 Quelle commande permet d’aﬀicher l’heure? A quoi sert la commandetime**

date 

### **Q2-6**

-> ls Cela permet de lister les fichiers / dossier <br>
-> la ------------------------- fichiers cachés <br>
-> La commande ls se situe dans /usr/bin/ls <br> 
-> ll --------------------------> fichiers / dossiers et leurs droits <br>


### **Q7 


<code> pwd </code>
Affiche le chemin courrant. 


### **Q8-9

<code> echo 'yo' > plop </code>

Cette commande permet de créer le fichier plop et d'inscrire dedant 'yo' ; 
Cette commande permet d'inscrire à la deuxième ligne 'yo'; 


### **Q10 A quoi sert la commande file ? Essayez la sur des fichiers de types différents.**

<code> man file </code> 

permet de déterminer le type de fichier ; 


### **Q11 Créez un fichier toto qui contient la chaîne Hello Toto ! ; créer ensuite un lien titi vers ce fichier avec la commande ln toto titi. Modifiez à présent le contenu de toto et affichez le contenu de titi : qu’observe-t-on ? Supprimez le fichier toto ; quelle conséquence cela a-t-il sur titi ?**

Supprimer le fichier toto rend le lien titi inutilisable.

### **Q12 Créez à présent un lien symbolique tutu sur titi avec la commande ln -s titi tutu. Modifiez lecontenu de titi ; quelle conséquence pour tutu ? Et inversement ? Supprimez le fichier titi ; quelle conséquence cela a-t-il sur tutu ?**

Lorsque que l'on écrit dans un des fichiers, l'autre contient la même chose.
Lorsque l'on supprime le fichier titi, le fichier tutu n'existe plus.

### **Q13 Affichez à l’écran le fichier /var/log/syslog. Quels raccourcis clavier permettent d’interrompre et reprendre le défilement à l’écran ?**

<code> cat /var/log/syslog  </code> <br> 

<code> ... Les logs </code>

la commande <code>:q </code>. Pour le reprendre il suffit de rappeler la commande avec la flèche du haut de notre clavier.


### **Q14 Affichez les 5 premières lignes du fichier /var/log/syslog, puis les 15 dernières, puis seulement les lignes 10 à 20.**

La commande <code>head -5 syslog</code> affiche les 5 première ligne du fichier /var/log/syslog. <br>
La commande <code>tail -15 syslog</code> affiche les 15 dernières ligne ---------------------- <br>
La commande <code>head -10 syslog | tail -n20</ code> ---------- seulement les ligne de 10 à 20. </code>

### **Q15 Que fait la commande dmesg | less ?**

via la commande  <code> Man </code >, nous apprenons que : dmesg - Afficher et contrôler le tampon circulaire du noyau <br>
---------------  <code> Man </code >, ------------------ : lass - Afficher plus au moins de contenue  


De manière plus clair : 

Elle affiche la mémoire tampon de message du noyau et la commande less ne charge pas le fichier dans son intégralité. <br>

C'est tj pas très clair mais bon ... 

### **Q16 : Affichez à l’écran le fichier /etc/passwd ; que contient-il ? Quelle commande permet d’afficher la page de manuel de ce fichier ?**

Le fichier <code>/etc/passwd</code> contient toutes les informatins concernant les utilisateurs (id,groupe... ). <br>
 <code>man -k passwd</code>.

### **Q17 : Affichez seulement la première colonne triée par ordre alphabétique inverse**


<code>sort -r </code>

#### **Q18 : Quelle commande nous donne le nombre d’utilisateurs ?**

<code>cat /etc/passwd | awk -F: '{print $ 1}'</code>

### **Q19 : Combien de pages de manuel comportent le mot-clé conversion dans leur description ?**

Il y a 4 pages de manuel comportant le mot-clé conversion dans leur description.

### **Q20 A l’aide de la commande find, recherchez tous les fichiers se nommant passwd présents sur la machine**

<code> cd / </code>

<code> find -name "passwd" ; </code>


### **Q21 Modifiez la commande précédente pour que la liste des fichiers trouvés soit enregistrée dans le fichier ~/list_passwd_files.txt et que les erreurs soient redirigées vers le fichier spécial /dev/null**

<code> echo find -name passwd >> ~/list_passwd_files.txt </code>

### **Q22 Dans votre dossier personnel, utilisez la commande grep pour chercher où est défini l’alias ll vu précédemment**
<code> cd sudo grep </code>


### **Q23 Utilisez la commande locate pour trouver le fichier history.log.**

<code> locate history.log </code>
<code> find -name "history.log" </code>

### 24.Créer un fichier dans votre dossier personnel puis utilisez locate pour letrouver. Apparaît-il?Pourquoi?

<code> touch fichier1 <br>
ls <br>
fichier <br>
locate fichier <br>
updatedb <br>
updatedb: can not open a temporary file for `/var/lib/mlocate/mlocate.db' <br>
</code>

Comme la bdd n'a pas été mis à jour via, le fichier n'est pas trouvé. 




