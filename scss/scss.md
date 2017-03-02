<center>http://sass-lang.com/guide</center>
install
======
		sudo apt-get gem
		sudo apt-get ruby
		sudo su -c "gem install sass"



 


Création dossier de travail
=====

dossier travail  
* style
  * sass    
       * style.scss
  * css
* index.html


Pour regarder tt un dossier et écrire dans les fichier css correspondant auto en modif scss  
cmd dans dossier style	  


		sass --watch --sourcemap=none sass:css

* commandes possibles pour changer mise en forme
		sass --watch --sourcemap=none --style compressed sass:css
		sass --watch --sourcemap=none --style EXPENDED sass:css
		

* aide 

		sass -?


commentaire sur plusieurs lignes apparait dans css mais les // ne sont visibles que dans le scss  

possibilité de:
====

* déclarer une variable 


		$default_color: red;
		et de s'en servir où l'on veut
		body{
			background-color: $default_color;
		}

* selectionner enfants en les écrivant dans les parents


		body{
			a{
				background-color: $default_color;
			}
			}

* réaliser des opérations sur les variables si unités compatibles 
* selectionner ttes les actions associées à un element et leur donner style
  * Attention utiliser & avant :action

			#articlecool{
				 &:hover{
					color: black;
					}
				}
* Regrouper les sous-propriétés dans une accolade de propriété

		Propriété:{
			souspropriété1: attribut;
			souspropriété2: attribut;
		}

ex Propriété= font souspropriété1=family souspropriété2: size
* un fichier css par classe
 * avec des classes communes regroupées :
       * dans le fichier css link dans html écrire (où menu = fichier avec css commun)


		@import 'menu';
       * si on marque _menu dans l'import et qu'on renomme menu.scss par _menu.scss le contenu de _menu.scss sera placé à l'endroit définit par l'import dans le fichier css mais pas de fichier menu.css généré

* reprendre les attributs d'un element grâce à @extend
			
			.danger{
				height: 50px;
				width: 100px;
				border: 1px solid black;
				background-color: red;
			}

			.success{
				@extend .danger;
				background-color:red;
	
			}
 * ce code génère un css avec .success qui a les même attr que .danger sauf pour la couleur
* Modification d'une même variable:
  * prend en compte le dernier état de la variable en amont du code
* Possibilité de faire des fonctions dans le scss
 * exemple
 
		@function calculhauteur( $largeur, $multiplicateur ){

			@return $largeur*$multiplicateur;
		}


		.success{
			@extend .danger;
			background-color:$color;
			width: calculhauteur( 100px, 6 );
	
		}


