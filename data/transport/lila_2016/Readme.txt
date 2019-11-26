		*			BASE ATC			*
		*	- BASE D'ARRETS de TRANSPORT COLLECTIF -	* 
		*********************************************************
	
Ce répertoire contient les couches d'arrêts pour le réseau de TC concerné, ainsi qu'un fichier de méta-données.

Ces fichiers ont été produits par le Cerema à partir des données fournies par le producteur (le producteur des données est renseigné dans les méta-données). 
Les données ont été reformatées pour être conformes au modèle d'arrêt partagé proposé par l'AFIMB, et plusieurs indicateurs ont été calculés.

Chaque couche comporte 4 fichiers .SHP, .SHX, .PRJ, .DBF (ce dernier contenant le tableau des données), plus le cas échéant un fichier .CPG (pour l'encodage).

Ces données sont diffusées via le site http://www.territoires-ville.cerema.fr et [utilisables par les services du MEDDE et le Cerema pour leurs besoins d'études] (selon licence).



Contenu du répertoire:

1) couche quays (Zones d'embarquement, notées ZE)
--> contient les arrêts physiques, décrits par les attributs du modèle d'arrêt partagé, auxquels sont ajoutés les indicateurs suivants:
	- NbHab_300m: Nb d'habitants dans un rayon de 300m autour de l'arrêt physique
	- Min_Time: horaire du premier passage à cet arrêt (en hh:mm:ss)
	- Max_Time: horaire du dernier passage à cet arrêt (en hh:mm:ss)
	- Amplitude: Amplitude des horaires des lignes passant par cet arrêt (en hh:mm:ss)
	- NbPas_PNTE: Nombre de passages des lignes à cet arrêt en période de PoiNTE  ( 07h30 - 9h29  /   16h30 - 19h59 ) 
	- NbPas_INTR: Nombre de passages des lignes à cet arrêt en période INTeRmédiaire ( 09h30 - 16h29 )
	- NbPas_CRSE: Nombre de passages des lignes à cet arrêt en période CReuSE     ( 00h00 - 7h29  /   20h00 - 23h59 )
	- NbPas_Tot: Nombre de passages des lignes à cet arrêt sur la journée complète


2) couche stopplaces (Lieux d'arrêt monomodaux, notés LAM)
--> contient les arrêts commerciaux, décrits par les attributs du modèle d'arrêt partagé, auxquels est ajouté l'indicateur suivant:
	- NbHab_300m: Nb d'habitants dans un rayon de 300m autour de l'arrêt commercial



3) fichier de métadonnées :
	- métadonnées en tant que telles
	- comptages (nombre de ZE, nombre de LAM, nombre de lignes TC)
	- indicateurs de qualité des données :
		* ratio du nombre de ZE sur le nombre de LAM (théoriquement proche de 2)
		* nombre d'arrêts dont les coordonnées sont [0,0]
		* nombre de LAM qui ont les mêmes coordonnées qu'une ZE (théoriquement limité aux arrêts dont le sens opposé de la ligne utilise un autre itinéraire)


Contact : dd.dtectv@cerema.fr
		