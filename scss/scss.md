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


