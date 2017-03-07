mise en ligne
======

Importance de faire héberger dans la même zone géographique que utilisateurs.


Quelques Exemples d'Hebergeurs
=====
* 1&1
* OVH 
* LWS hostinger
* orange
* wordpress.fr
* sfr
* hebergeur discount
* O2 switch
* oxito
* Nextwab

rq: certains ont leurs propres serveurs d'autres les louent  
Si on passe par un hebergeur on peut passer par un serveur virtuel dédié (cf machine virtuelle sur pc) mais pas par serveur dédié.  


Self hosting
====


Avantages
----
* admin
* 100% des ressources
* accès physique
inconvéniants
-----
* ordinateur à reserver pour cette tâche
* puissance de calcul moindre par rapport à un serveur
* nécessite une bonne connexion internet
* disponibilité (si coupure courant ou téléphone plus de serveur)
* coût en electricité

Mutualisé
====


Avantages
----
* Pas de maj à effectuer
* Pas de sécurisation à faire
* ressources supplémentaires à certains moments (ressouces partagées donc possibilité ultiliser % des ressources d'autres sites qui n'utilisent pas les leurs)
* 100% configurés
* certains serveurs mutualisé gratuits en echange bandeau pub 


inconvéniants
-----
* ressources partagées
* ressources partagées
* pas de choix os
* pas de choix de version (ex: php)
* pas de choix ip donc on peut se retrouver sur ip spam (Moins de 5000 mail/heure pour ne pas être bloqué) ou site bloqué car un des 
sites hebergés exerce activité illégale par exemple
* restriction mail Moins de 5000 mail/heure
* Attaques dead os 
* si un site piraté possibilté d'attaque sur tous les autres (ex : WHOIS sur site A donne ip qui permettera de chercher des failles sur d'autres sites hebergés pour remonter au site A)

Virtuel Dédié ou Virtuel Mutualisé
====


Avantages
----
* cf mutualisé
* mais on ne peut pas bénéficier de la portion de ressources des autres sites hébergés


inconvéniants
-----
* cf mutualisé
* mais moins de risque de piratage

Dédié
====


Avantages
----
* admin (avec tt les droits),ssh  
* 100% des ressources  
* 99.99% accessible (redemarrage serveur)
* plusieurs sites (possibilité de limiter la bande passante)


inconvéniants
-----
* Demande des connaissances
* maintenance
* besoin de sécuriser
* configuration mysql ftp... en cmd
* pas d'accès physique
* responsabilité nous incombe si piratage  


Rq : mutualisé tend à disparaitre au profit de virtuel mutualisé.  
virtuel mutualisé : puissance répartie entre les différents sites.  
self hosting : intranet (exemple caisse leclerc)  

chaque point de connexion a une adresse ip  
seft hosting mutualisé une seule ip pour plusieurs sites  
serveur dédié une ip par site pour 10 à 21 euros par mois  


VPN se connecte à un autre serveur pour aller d'un point A à un point B

Dans tout les cas besoin nom de domaine ou de sous domaine dans certains cas sous domaine gratuit en echange bandeau de pub  

Dédié : surveillance firewall physique (interface qui bloque certaines ip)

mise en œuvre
======
* whois.net permet de voir qui possède un nom de domaine
* aller sur site fournisseur (ex lws)
rq : serveur asp.net : serveur windows (virtualisation de windows, peu répendu)
 * serveur vps dédié ou dédié mutualisé
 * ISPconfig
 * options dite hebergeur
  * gestion domaine (site hebergeur) 
     * type de redirection pr referencement
     * Mx identification du serveur
     * cname adresse ip où site hebergé
     * dans config avancé box NAT/PAT 
	   * rediriger flux externe sur port identique de l'équipement ex : box fabrik
           * rq: ip fournisseur perso ip dynamique demander à passer dynamique en perso ip livebox pro fixe
           * dyndns service payant pour fai qui ne gèrent pas adresse ip fixe
  * .com et .fr ne donnent pas les mêmes obligations (mentions légales nom dev hebergeur... tt site avec cookie mention cookie tt site qui récolte data doit faire déclaration cnil (quelles data pk option pr suppr réponse cnil sous 48h))
  * garder dns par défault (attaques dead os + configuration à revoir fréquemment à cause de modifications des normes)
  * .asso .org que si asso ou organisme précis
  * il est interdit de faire de la spéculation sur un nom de domaine (on ne peut pas acheter nom de domaine pour le revendre plus cher
  * On peut acheter un nom de domaine et le mettre aux enchères
  * si renouvellement en retard on peut perdre son nom de domaine



