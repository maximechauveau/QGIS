		*			BASE ATC			*
		*	- BASE D'ARRETS de TRANSPORT COLLECTIF -	* 
		*********************************************************
	
Ce r�pertoire contient les couches d'arr�ts pour le r�seau de TC concern�, ainsi qu'un fichier de m�ta-donn�es.

Ces fichiers ont �t� produits par le Cerema � partir des donn�es fournies par le producteur (le producteur des donn�es est renseign� dans les m�ta-donn�es). 
Les donn�es ont �t� reformat�es pour �tre conformes au mod�le d'arr�t partag� propos� par l'AFIMB, et plusieurs indicateurs ont �t� calcul�s.

Chaque couche comporte 4 fichiers .SHP, .SHX, .PRJ, .DBF (ce dernier contenant le tableau des donn�es), plus le cas �ch�ant un fichier .CPG (pour l'encodage).

Ces donn�es sont diffus�es via le site http://www.territoires-ville.cerema.fr et [utilisables par les services du MEDDE et le Cerema pour leurs besoins d'�tudes] (selon licence).



Contenu du r�pertoire:

1) couche quays (Zones d'embarquement, not�es ZE)
--> contient les arr�ts physiques, d�crits par les attributs du mod�le d'arr�t partag�, auxquels sont ajout�s les indicateurs suivants:
	- NbHab_300m: Nb d'habitants dans un rayon de 300m autour de l'arr�t physique
	- Min_Time: horaire du premier passage � cet arr�t (en hh:mm:ss)
	- Max_Time: horaire du dernier passage � cet arr�t (en hh:mm:ss)
	- Amplitude: Amplitude des horaires des lignes passant par cet arr�t (en hh:mm:ss)
	- NbPas_PNTE: Nombre de passages des lignes � cet arr�t en p�riode de PoiNTE  ( 07h30 - 9h29  /   16h30 - 19h59 ) 
	- NbPas_INTR: Nombre de passages des lignes � cet arr�t en p�riode INTeRm�diaire ( 09h30 - 16h29 )
	- NbPas_CRSE: Nombre de passages des lignes � cet arr�t en p�riode CReuSE     ( 00h00 - 7h29  /   20h00 - 23h59 )
	- NbPas_Tot: Nombre de passages des lignes � cet arr�t sur la journ�e compl�te


2) couche stopplaces (Lieux d'arr�t monomodaux, not�s LAM)
--> contient les arr�ts commerciaux, d�crits par les attributs du mod�le d'arr�t partag�, auxquels est ajout� l'indicateur suivant:
	- NbHab_300m: Nb d'habitants dans un rayon de 300m autour de l'arr�t commercial



3) fichier de m�tadonn�es :
	- m�tadonn�es en tant que telles
	- comptages (nombre de ZE, nombre de LAM, nombre de lignes TC)
	- indicateurs de qualit� des donn�es :
		* ratio du nombre de ZE sur le nombre de LAM (th�oriquement proche de 2)
		* nombre d'arr�ts dont les coordonn�es sont [0,0]
		* nombre de LAM qui ont les m�mes coordonn�es qu'une ZE (th�oriquement limit� aux arr�ts dont le sens oppos� de la ligne utilise un autre itin�raire)


Contact : dd.dtectv@cerema.fr
		