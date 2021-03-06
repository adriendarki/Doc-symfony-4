# Doc-symfony-4

(docummentation en cours de réalisation.)

DOCUMENTATION SYMFONY 4 EN FRANCAIS
==================================

## Sommaire
 - [Installation ?](#Installation)
 - [IDE](#IDE) 
 - [Premier demarrage](#Premier-démmarage-de-symfony)
 - [Lexique](#les-commandes-toujours-utile)
 


##  Installation 


 Pour démarrer un bon projet symfony sans avoir d'installation sur  sont environnement de dev il vous faut :
 - [un serveur local](#Serveur)
 - [avoir composer](#Installer-composer)
 - [Framework Symfony 4](#Installer-symfony-4)


## Serveur
Dans un premier temps il vous faudra un serveur local pour cela vous pouvez télécharger XAMPP/LAMPP ou celui qui vous arrange le mieux !

pour ma part quand je suis sur windows j'utilise Xampp https://www.apachefriends.org/fr/index.html

télécharger le penser à prendre la derniere version en fonction de ce que vous develloper les versions de php vous limiterons mais je vous conseille de prendre la derniere version ! installer le et passe à l'etatpe suivant.


## Installer composer

 Par la suite, il faut se rendre sur  https://getcomposer.org/

 Deux possibilité  sois par l'installation windows sois en ligne de commande

  pour l'installation windows il suffit de téléchager le .exe 
  pour la manierere ligne de commande, il suffit de marquer ce code

<code>
    php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
    php -r "if (hash_file('sha384', 'composer-setup.php') === '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5') { echo 'Installer verified';
        } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
    php composer-setup.php
    php -r "unlink('composer-setup.php');" 
</code>

apres ça vous avez normalement composer sur votre machine ;) c'est le moment de passer à la deuxieme etape

## Installer symfony 4

 pour cela vous pouvez vous rendre sur le site de  https://symfony.com et aller dans la sessions setup (pensez à aller faire souvent un tour sur le site de symfony beaucoup de vos réponses ce trouve dans la documentation officiel de symfony!).

 ouvrer le dossier ou vous allez enregristrée votre projet

Exemple:
<code>
   C:\Users\adrie>cd /xampp/htdocs/adriendarki
</code>

Maintenant composer va enfin nous servir ! vous pouvez commencer l'installation avec la ligne de commande 
<code>
composer create-project symfony/website-skeleton nom de votre projet
</code>

Laisser quelques minutes votre cmd executer l'installation... bravo vous avez symfony 4 sur votre environnement ! Maintenant regardons l'IDE sinon aller directement à la partie suivant si vous en posserder déjà un.

##  IDE

si vous avez déjà un idée passer à la session suivant sinon poursuivez la lecture.

en terme IDE vous avez clairement le choix. Cependant pour ma pars j'en utilise deux ou trois uniquement. 2 pour du dev rapide/modifications rapide et un autre dedier au dev PUR.

- Pour les modifications rapide vous pouvez utiliser Sublime text ou visual studio code d'autre sont possible comme atom mais là ça reste un choix personnel prennez celui qui vous correspond le mieux !

- Pour le develloppement pur utilisé PHPSTORM actuellement c'est le meilleur du marché pour du dev symfony 3 et 4 !

## Premier démmarage de symfony

il est temps de démmarer notre projet !

ouvrez votre projet dans votre id pour cette manipulation vous avez deux possibilité sois faire entré le code dans le terminal sois dans le cmd (invité de commande). Je vous conseiller fortement de le faire dans le cmd ! vous comprendrez pourquoi dans la suite de la docummentation.

vous avez ouvert votre cmd ? bien maintenant vous aller pouvoir lancer le serveur interne du framework avec la commande

<code>
php bin/console server:run
</code>

en toute logique vous aller obtenir le message suivant:
<code>
 [OK] Server listening on http://127.0.0.1:8000
</code>
 rendez-vous à l'adresse 127.0.01:8000 . normalement vous aurez un beau message indiquant que votre installation à bien marcher 


super ! on attaque les premieres créations de Controller !


## les commandes toujours utile

Les indispensables.
<code>
php bin/console server:run
php bin/console make:controller ExempleController
php bin/console make:crud Post
php bin/console doctrine:database:create
php bin/console make:entity
</code>

les debugs 

<code>
php bin/console debug:router
php bin/console debug:twig
composer dump-autoload
</code>