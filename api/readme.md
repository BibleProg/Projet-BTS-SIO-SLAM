---
description: |
    API documentation for modules: gsb.

lang: en

classoption: oneside
geometry: margin=1in
papersize: a4

linkcolor: blue
links-as-notes: true
...


    
# Module `gsb` {#id}






    
## Functions


    
### Function `Insert_CR` {#id}




>     def Insert_CR()


fonction pour cr�er un compte rendu, la route attend un JSON 

method:
    POST


Param
-----=
JSON : contient les informations du compte rendu, il doit comporter les champs ["Medecin", "Date", "Motif", "Bilan", "Medoc"]


Returns
-----=
<code>HTTP CODE</code>
:   201, 400



    
### Function `connexion` {#id}




>     def connexion(
>         db_name
>     )


Fonction de connexion � la base de donn�e, elle est appel� � chaque nouvelle connexion.

!!! Le driver ODBC SQLite3 est necessaire � son execution.

!!! La base de donn�e doit imp�rativement se trouver dans ./BDD/


Args
-----=
**```db_name```** :&ensp;<code>string</code>
:   le nom de la base de donn�e � laquelle se connecter



Returns
-----=
<code>object</code>
:   objet pyodbc



    
### Function `cr_by_medecin` {#id}




>     def cr_by_medecin(
>         Id
>     )


Recherche de compte rendu par medecin.


Args
-----=
**```Id```** :&ensp;<code>int</code>
:   id du medecin



Returns
-----=
<code>string</code>
:   JSON contenant toutes les informations du compte rendu ainsi que les �chantillons associ�s



    
### Function `cr_by_visiteur` {#id}




>     def cr_by_visiteur()


Recherche de compte rendu par visiteur.


Returns
-----=
<code>string</code>
:   JSON contenant toutes les informations du compte rendu ainsi que les �chantillons associ�s



    
### Function `fake_cr` {#id}




>     def fake_cr(
>         Id=0
>     )


Genere 50 faux comptes rendus

    
### Function `fake_prat` {#id}




>     def fake_prat()


G�n�re 50 faux particiens

    
### Function `fake_visiteur` {#id}




>     def fake_visiteur()


G�n�re 50 faux visiteurs

    
### Function `get_session` {#id}




>     def get_session()


Check si l'utilisateur s'est connect� avant d'acc�der � une ressource (fonction appel�e � chaque route).


Returns
-----=
<code>bool</code>
:   l'utilisateur est bien connect�


<code>erreur</code>
:   code http 401



    
### Function `hashpass` {#id}




>     def hashpass(
>         password
>     )


Affiche le hash d'une chaine de charat�re


Args
-----=
password(string): mot de passe � asher

Returns
-----=
<code>string</code>
:   le mot de passe ash�



    
### Function `hello` {#id}




>     def hello()


S'execute lorsqu'on appelle la racine du serveur.
Redirige vers la route /links.

    
### Function `list_routes` {#id}




>     def list_routes()


Liste les routes existantes dans l'API.


Returns
-----=
Un DOM HTML.

    
### Function `log` {#id}




>     def log(
>         text,
>         loglevel=0
>     )


Fonction de logging.


Args
-----=
**```text```** :&ensp;<code>string</code>
:   le message du log



    
### Function `medecin` {#id}




>     def medecin(
>         Id
>     )


Execute une recherche de praticien.


Args
-----=
**```Id```** :&ensp;<code>int</code>
:   id du praticien concern�



Returns
-----=
<code>string</code>
:   JSON avec toutes les informations du praticien



    
### Function `medecin_all` {#id}




>     def medecin_all()


Execute une recherche sur tout les praticiens.


Returns
-----=
<code>string</code>
:   JSON avec toutes les informations de tous les praticiens



    
### Function `medicament` {#id}




>     def medicament(
>         Id
>     )


Execute une recherche de m�dicament.


Args
-----=
**```Id```** :&ensp;<code>int</code>
:   id du m�dicament concern�



Returns
-----=
<code>string</code>
:   JSON avec toutes les informations du m�dicament



    
### Function `medicaments` {#id}




>     def medicaments()


Execute une recherche sur tout les m�dicaments.


Returns
-----=
<code>string</code>
:   JSON avec toutes les informations de tous les m�dicaments



    
### Function `ping` {#id}




>     def ping()


Appel�e pour tester la connexion � l'API

    
### Function `query` {#id}




>     def query(
>         sql,
>         arg=[],
>         many=False
>     )


Fonction g�n�rale utilis�e pour executer les requt�tes sql sur la base de donn�e


Args
-----=
sql  (string): Ordre SQL � executer
arg  (list, optional): Liste des arguments de la requ�te SQL
**```many```** :&ensp;<code>bool</code>, optional
:   booleen qui indique si il faut executer la requete pour chaques �l�ments de arg



Returns
-----=
<code>dict</code>
:   Retourne un dictionnaire avec le nom des champs de la table en cl� et la valeur du champ en valeur.


<code>bool</code>
:   Si il n'y a aucun r�sultat � la requ�te retourne False



    
### Function `remove_accents` {#id}




>     def remove_accents(
>         input_str
>     )


Purge une chaine de caract�res en enlevants les accents.


Args
-----=
**```input_str```** :&ensp;<code>string</code>
:   la chaine � purger



Returns
-----=
<code>string</code>
:   input_str sans accents



    
### Function `se_connecter` {#id}




>     def se_connecter()


Route utilis�e pour s'authentifier aupr�s de l'API


Returns
-----=
<code>HTTP CODE</code>
:   200, 401



    
### Function `secteur_by_visiteur` {#id}




>     def secteur_by_visiteur(
>         Id
>     )


Recherche de Secteur par visiteur.


Args
-----=
**```Id```** :&ensp;<code>int</code>
:   id du visiteur



Returns
-----=
<code>integer</code>
:   id du secteur





-----
Generated by *pdoc* 0.10.0 (<https://pdoc3.github.io>).
