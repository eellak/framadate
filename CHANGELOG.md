# Changelog de framadate

## 1.1.19

23-12-2021

### Fixed

- Remove the X-Mailer header in e-mails, as this causes some email servers to see emails sent by Framadate as spam

## 1.1.18
20-12-2021

### Changed
- Dependency updates
- Replace abandonned SimpleMDE with EasyMDE fork

### Fixed
- Enforce the instance expiration limits when editing the poll expiration date once created, from poll admin
- Fixed some HTML markup validity

### Translations
- Fixed a missing french language key
- Enable Catalan language

## 1.1.17
18-10-2021
### Added

- Allow to export to ICS the best choices

### Changed

- Allow configuring AuthType for MailService

### Security

- Fix an XSS possibility in the result graph

## 1.1.16
22-03-2021
### Changed

- **Framadate now requires the `mbstring` PHP extension.** Make sure it's installed and activated before updating.

### Fixed

- Handle poll creator names being too long properly


## 1.1.15
22-03-2021
### Security

- Fixed cross-site scripting (XSS) attacks in poll description markdown preview. All administrators are encouraged to upgrade, especially if you have sensitive services and data on the same domain name.
  This was reported by @martgil
  https://framagit.org/framasoft/framadate/framadate/-/issues/546

## 1.1.14
08-03-2021
### Fixed

- Avoid error with a name too long https://framagit.org/framasoft/framadate/framadate/-/issues/530

## 1.1.13
08-03-2021
### Fixed

- Fixed error when closing a poll https://framagit.org/framasoft/framadate/framadate/-/issues/532

## 1.1.12
18-12-2020

### Changed

* Framadate now requires PHP 7.3

## 1.1.11
18-12-2020
### Fixed

- Fixed translations keys missing into emails https://framagit.org/framasoft/framadate/framadate/-/issues/463

### Translations

- Added Catalan translation

## 1.1.10

### Fixed
* Remove .git folder inside releases.
* Create releases through CI

## 1.1.9

### Fixed
- Fixes session issue https://framagit.org/framasoft/framadate/framadate/issues/255
- Fixes bug when editing column https://framagit.org/framasoft/framadate/framadate/issues/379
- Fix mail subject escaping https://framagit.org/framasoft/framadate/framadate/issues/375

## 1.1.8
### Fixed
- Stop creating `tpl_c` directory in releases and add a `.gitkeep`
- Show database connection issue details on installation panel
- Set the proper file rights on release packages
- Added `session.cookie_httponly = 1` to local php.ini file

## 1.1.7
### Fixed

- Fix issue with maximum number of participants https://framagit.org/framasoft/framadate/issues/353 (thanks to @lohmeyer for reporting it)

## 1.1.6

### Fixed

- Bump dependencies, including PHPMailer to version 6.x
- Fix an small issue with Smarty template

## 1.1.5
### Fixed

- Restrict custom poll URLs against app urls (thanks @mosterdt)
- Add a parameter to disable build-in font-awesome (thanks @mm)
- Fix an XSS security issue with time slots (thanks https://bitsoffreedom.nl for responsibly disclosing it).

## 1.1.4

### Fixed
* Add Fork-awesome, remove dependency to Font-Awesome Bootstrap CDN, add an option to disable it (https://framagit.org/framasoft/framadate/merge_requests/300 - @tcit)

## 1.1.3

### Fixed
* Fixing issue when no choice is selected introducted in https://framagit.org/framasoft/framadate/merge_requests/284 (https://framagit.org/framasoft/framadate/merge_requests/298 - @mm)

## 1.1.2

### Fixed
- Use Parsedown's Safe Mode

## 1.1.1

### Bug fixes

- Send email with correct vote address (thanks to @lohmeyer for finding it)

## 1.1.0

### Warning

**Framadate now requires PHP 5.6** to be used (it should still work under 5.4 but will not be supported anymore).

### Features

- Markdown editor for descriptions ! (@Antonin)
- Adding a maximum participants number (@SuperNach0)
- Allow setting SMTP config (Simon LEBLANC)
- Allow admins to give the vote link back to the voters (@mm, @tcit)
- Sending voters emails to remind themselves their voting url now works (@mm)

### Enhancements

- UI improvements for responsive design (@marjolaine-v)
- Better coherence for visible results and passwords (@TDavid)
- Added an edit button on the right when too many options (@SuperNach0)
- Emails with international characters are now allowed (added an unit test) (@mm)

### Translations

**New strings are available, don't hesitate to head to <https://trad.framasoft.org/zanata/project/view/framadate> to translate them into your language !**

### Fixed

- Reschedule function (https://framagit.org/framasoft/framadate/issues/203) (@TDavid)
- lang attribute must be a valid IETF language tag (@Rudloff)
- Fix datepicker js locale file path
- Fix everyone can always vote #267
- Fix MySQL error with `NO_ZERO_DATE` #224
- SimpleMDE Markdown Editor has been updated the latest version to remove console.log calls
- Fix width of `if need be` vote option and missing parenthesis
- Remove autocomplete on date fields
- Various fixes for value max error handling
- New error strings for bad formatted inputs (admin name, wrong value max option)
- Email is now a email field (better for virtual keyboards) and is html required as well as title
- Advanced settings for poll are now opened if there's error within them
- css fixes for pictures inside columns, and little space between editor and description text area (@marjolaine-v)
- released zip files now have proper chmod rights (@tcit)
- Best choices now work properly when there's no votes (@mm)
- Don't allow an existing name when updating a vote (@mm)
- Keep vote selections when there's an error on the name (@mm)
- Add a message ?? Your poll has been created ?? at the end of the poll form process (@mm)

### Documentation

- Move everything to wiki, translate everything to English

### Technical

- Continuous Integration handles the release process
- Translations with Zanata : https://trad.framasoft.org/zanata/project/view/framadate (@luc)
- Style fixes with PHP-CS
- Libraries updated
- Improved a few docs
- Use own Framadate Docker Image for CI
- https://beta.framadate.org now gets the latest translations for each deployment (@luc)
- A CI job tells if translations strings are up-to-date (@luc)

## 1.0.3

- Corrections de wording (fr / en)

## Version 1.0 (Erik - Markus - Ecmu - Julien - Imre - Luc - Pierre - Antonin - Olivier)
    - Am??lioration : Conserver les votes en cours lors que l'utilisateur envoie un commentaire
    - Am??lioration : Les mails sont envoy??s en multipart pour les lecteurs ne supportant pas HTML
    - Am??lioration : Masquer l'encart au dessus du tableau des votes, maintenant visible gr??ce ?? un bouton
    - Am??lioration : Les commentaires sont horodat??s
    - Am??lioration : Auto wrapping de la description du sondage
    - Am??lioration : Protection de sondages par mots de passe
    - Am??lioration : Un click dans les champs URL s??lectionne le contenu
    - Am??lioration : Choix du lien du sondage
    - Am??lioration : Possibilit?? de modifier un sondage apr??s expiration
    - Am??lioration : Confirmation demand??e pour supprimer une colonne
    - Am??lioration : Cr??ation d'une sondage par intervale de dates
    - Am??lioration : Possibilit?? de ne pas faire de choix sur une colonne
    - Am??lioration : Am??lioration du format des mails
    - Am??lioration : Am??lioration du mode o?? chaque votant ne peut modifier que son vote
    - Am??lioration : Fichier check.php pour v??rifier la possibilit?? d'installation
    - Am??lioration : Changements de libell??s
    - Am??lioration : Admin - Rechercher un sondage gr??ce ?? l'adresse mail
    - Am??lioration : Fluidification du d??filement de la page
    - Am??lioration : Simplification de l'??cran de cr??ation de sondage
    - Fix : Correction de traductions
    - Fix : Corrections diverses sur les dates et leurs formats
    - Fix : Impossible d'ajouter une colonne vide
    - Fix : Possibilit?? de supprimer des colonnes vides
    - Fix : Correction du formulaire de commentaires
    - Fix : Correction d'??chappements de caract??res
    - Fix : Rectification des contraintes sur les sondage expir??s
    - Fix : Interdiction d'exporter les r??sultats lorsque l'utilisateur ne peut pas les voir
    - Technique : Travail sur le service des notifications
    - Technique : Prise en compte de l'ent??te X-Forwarded-Proto
    - Technique : Utilisation de PHPMailer pour l'envoi de mails
    - Technique : Encore de la Smartization
    - Technique : Pas mal de nettoyage de code

## Version 0.9.6 (goofy-bz - Olivier - Quentin - Vincent)
    - Fix : Corrections mineures de langues
    - Am??lioration : Nouvelle langue - Occitan
    - Am??lioration : Blocage d'un vote si l'admin a chang?? les possibilit??s entre temps

## Version 0.9.5 (Olivier)
    - Fix : Corrections mineures de langues
    - Fix : Correction de la suppresion de votes
    - Am??lioration : Possibilit?? d'ajouter plus de "moments" ?? une date

## Version 0.9.4 (JosephK - Olivier - Nikos)
    - Fix : Correction de l'??chappement des tables Vote et Slot
    - Fix : Encodage des "actions" en base64 pour fonctionner avec l'UrlRewriting
    - Fix : Correction d'attributs "title"
    - Fix : Un seul jour est requis pour faire un sondage
    - Fix : Correction de l'UrlRewriting
    - Am??lioration : Traduction en Italien

## Version 0.9.3 (Antonin - Olivier - Nikos)
    - Fix : Traduction de textes en Italien
    - Fix : Emp??chement de la suppression de la derni??re colonne
    - Fix : Possiblit?? de supprimer des colonnes contenant des caract??res sp??ciaux (par exemple "&")
    - Fix : Correction de l'exemple d'URL rewriting (des efforts restent ?? faire)
    - Am??lioration : (Mode chacun son vote) Possiblit?? d'??diter son vote directement apr??s un vote
    - Am??lioration : Message plus parlant lors de la cr??ation d'une colonne
## Version 0.9.2 (Olivier)
    - Fix : Completion d'un manque de contr??le sur les ID
## Version 0.9.1 (JosephK - Olivier - Antonin - Michael - Paul)
    - Fix : Correction des lenteurs de d??filement
    - Fix : Arr??t du d??filement auto ?? gauche qu'on clique sur un choix
    - Fix : Traductions Fran??ais/Anglais/Allemand
    - Fix : Fin du tri automatique des colonnes (ex: 10h < 9h)
    - Fix : Option ?? la cr??ation masqu??e dans certains cas
    - Fix : Le nom peut maintenant contenir des caract??res sp??ciaux (ex: , - ')
    - Fix : Correction mineure de la doc d'installation
    - Fix : Interdiction du caract??re "," dans choix d'un vote
    - Fix : Correction de la suppression de choix contenant des caract??res sp??ciaux
    - Fix : Correction du contr??le pour emp??cher de supprimer le dernier choix d'un sondage
    - Fix : Taille du champs "Votre nom" agrandie
    - Technique : Ajout de logs
## Version 0.9 (JosephK - Olivier - Antonin - ...)
    - Technique : R??organisation des classes
    - Technique : D??coupage en MVC + Installation de Smarty
    - Technique : Refonte de l'acc??s aux donn??es + Remplacement de Adodb par PDO
    - Technique : D??finition claire des couches Service et Repository
    - Technique : Utilisation de la librairie open source o80-i18n pour la gestion des langue
    - Am??lioration : Refonte de l'administration
    - Am??lioration : Formulaire de recherche pour trouver des sondages
    - Am??lioration : Notification de l'utilisation si JAvascript ou les cookies sont d??sactiv??s
    - Am??lioration : D??coupage en 2 options pour recevoir ou non les nouveaux vote et commentaires
    - Am??lioration : Utilisation de jetons CSRF sur certaines actions
    - Am??lioration : Nouvelle option de sondage "Chaque participant peut modifier son propre vote"
    - Am??lioration : Nouvelle option de sondage "Vote cach??, seul le cr??ateur du sondage peu voir les r??sultats"
    - Am??lioration : Auto-cmopl??tion des champs de dates (15/5 peut devenir 15/05/2015 ou 15/05/2016 en fonction de la date actuelle)
    - Am??lioration : Nouvelle page pour retrouver ses sondages par mail
    - Am??lioration : Mise ?? jour des fichiers .md pour faciliter la collaboration
    - Am??lioration : Le nom de l'auteur et la date d'expiration sont modifiables
    - Am??lioration : Le nom de vote est modifiable
    - Am??lioration : Affichage du comptage des "Si n??cessaire" entre parenth??ses
    - Am??lioration : Page d'installation
    - Fix : Purge en 2 ??tapes ??? 1. Verrouillage du sondage ??? 2. 60 jours plus tard suppression du sondage
    - Fix : Date d'expiration qui devient nulle quand on ajoute une colonne
    - Fix : clic/focus sur oui/non/si n??cessaire ??? retour ?? gauche de la barre de scroll sur Chromium
    - Fix : Perte de ses votes quand le nom entr?? n'est pas valide
    - Fix : Certains sondages sont cr???? avec un ID d??j?? existant
    - Fix : 2 choix minimum sont n??cessaires pour cr??er un sondage
    - Fix : Ajout de la police d'??criture D??j?? Vu
    - Fix : M??morisation de la langue entre l'application et l'administration
    - Fix : Bug ?? la cr??ation d'un sondage sans Javascript ou sans Cookies
    - Fix : Erreur d'url avec les noms de domaine contenant "admin"
    - Fix : Mise ?? jour de la doc d'installation

## Version 0.8 (juillet 2014 Pascal Chevrel - Armony Altinier - JosephK)
	- Am??liorations sur l'accessibilit??
	- Am??liorations sur l'ergonomie
	- Am??liorations sur l'internationalisation (nombreuses phrases en fran??ais dans le code)
	- D??coupage chaines de langue pour virer le code html
	- Remise en place de l'export CSV
	- Remise en place de get_server_name() pour permettre l'installation dans un sous dossier, en https ou sur un port diff??rent
	- Ajout Authors.md + en-t??tes refaits
	- Fix bug changement de langues en mode URL rewriting (requ??te GET pass??e en formulaire POST)
	- Fix bug 2 boutons valider lorsqu'on ??dite un vote
	- Fix focus javascript sur "Votre nom"
	- Nettoyage + Bootstrap
	- Ajout vote Oui/Non/Si n??cessaire
	- Formulaire simplifi?? pour l'ajout de colonne date (horaire libre)
	- Restructuration
	- Fix (partiel) bug modification du premier vote en tapant Entr??e

## Version 0.7 (mars 2013)
	- Fix : le sondage supprim?? n'??tait pas forc??ment le sondage s??lectionn?? (cf??vrier)
	- Fix : suppression de STUDS_DIR pour ??viter toute confusion
	- Fix : corrections l'en-tete et de l'encodage des e-mails (cf??vrier)
	- Fix : rend Optionnelle l'utilisation de la variable "REMOTE_USER" (cf??vrier)
	- Am??lioration : ne faire apparaitre dans l'admin que les sondage actifs ou expir??s depuis x mois (pyg)
	- Am??lioration : ajout d'un champs date_creation dans la table "sondage" (pyg)
	- Am??lioration : permet de faire fonctionner gettext avec le serveur de dev de PHP5.4 + enl??ve code comment?? depuis des ann??es (pascalchevrel)
	- Fix : enl??ve les appels ?? get_server_name() partout sauf dans un appel ?? sendMail(), r????criture de la fonction pour cet usage (pascalchevrel)
	- Am??lioration : remplacement des define() par des const plus concis (pascalchevrel)
	- Am??lioration : possibilit?? de faire des liens directs vers les types de sondages ?? cr??er (pascalchevrel)
	- Am??lioration : meilleure int??gration de la framanav (pyg)
	- Am??lioration : nombreuses modifications CSS pour un meilleur affichage (pyg)

## Changelog des 22 et 23 juin (pyg@framasoft.net)
	- tr??s nombreuses modifications CSS
	- ajout de buttons.css pour des boutons plus propres
	- ajout de print.css pour une impression sans la classe "corps"
	- refonte de la page d'accueil
	- ajout de la framanav
	- qq retouches dans les fichiers .po
	- date de destruction pass??e de 2j ?? 30j
	- ajout de l'adresse ?? transmettre
	- ajout d'un bouton imprimer
	- g??n??ralisation des stripslashes
	- fix d'un bug sur une requete (suppression). Reste la seconde partie : https://github.com/leblanc-simon/OpenSondage/issues/8
	- modification du titre en image
	- ajout de htmlspecialchars_decode avec param ENT_QUOTES pour l'envoi des emails

## Changelog du 21 juin 2011 (pyg@framasoft.net)
	- tr??s nombreuses modifications CSS
	- modification adminstuds.php : ajout de classes aux formulaires et ajout de stripslashes ?? l'affichage
	- modification infos_sondages.php : simplification du tableau de choix, ajouts de CSS, ajouts de labels pour faciliter la selection

## Changelog version 0.6.7 (mai 2011)
	- fork du projet STUdS (https://sourcesup.cru.fr/projects/studs/) de la version trunk du 15 mai 2011)
    - reprise par Simon Leblanc
    - nettoyage du code (indentation, coh??rence de la convention de codage)
    - suppression des warning php
    - r??solution d'une faille de s??curit?? par injection SQL
    - r??solution d'une faille de s??curit?? par injection mail
    - correction dans le fichier de langue (merci ?? Julien Reitzel)
    - possibilit?? de mettre un texte libre pour les horaires
    - version Framasoft

# Les derni??res am??liorations de STUdS
	Changelog version 0.6.6 (XXX 2011) :
	- internationalisation avec gettext
	- abstraction de la base de donn??es avec ADOdb
	- support de mysql (fichier d'initialisation disponible)
	- meilleure compatibilit?? avec le mode strict de PHP
	- factorisation de code et de CSS
	- moins de boutons de formulaire, plus de liens <a href>

	Changelog version 0.6.5 (juin 2010) :
	- Changement de deux icones dans la creation d'un sondage.

	Changelog version 0.6.4 (mars 2010) :
	- Corrections de bug

	Changelog version 0.6.3 (janvier 2010) :
	- Corrections de bug

	Changelog version 0.6.2 (novembre 2009) :
	- Correction dans l'affichage des bandeaux,
	- Modification de la partie "A propos",
	- Pr??paration ?? l'authentification,
	- De UdSification de l'application dans certains fichiers.

	Changelog version 0.6.1 (octobre 2009) :
	- Corrections d'erreurs dans les traductions et d'oublis de traduction dans certaines pages.

	Changelog version 0.6 (ao??t 2009) :
	- Mise sous la licence CeCILL-B du code source de STUdS,
	- Passage de STUdS en encodage UTF8,
	- Ajout des icones des menus dans toutes les pages et non pas seulement sur la page d'accueil,
	- Correction d'un bug lors du rajout d'une colonne dans l'interface d'administration des sondages.

	Changelog version 0.5 (f??vrier 2009) :
	- Traduction de STUdS en anglais, allemand et espagnol,
	- Changement de la CSS avec ajout du logo de l'Universit?? de Strasbourg,
	- Possibilit?? d'ajouter un commentaire pour les sond??s.

	Changelog version 0.4 (janvier 2009) :
	- Possibilit?? de faire un export PDF pour envoyer la lettre de convocation ?? la date de r??union,
	- Possibilit?? de rajouter des colonnes dans la partie administration de sondage,
	- Correction de bugs d'affichage avec les caract??res ' et " .

	Changelog version 0.3 (novembre 2008) :
	- Possibilit?? de faire un export CSV pour exploiter le sondage dans un tableur,
	- Mise en place d'un repository Subversion pour partager les nouvelles versions de STUdS,
	- Am??lioration de la CSS pour un meilleur affichage,
	- Modification du code source pour le rendre portable vers une autre machine.

	Changelog version 0.2 (novembre 2008) :
	- Lors de la cr??ation d'un sondage DATE, classement des dates par ordre croissant,
	- Lors de la cr??ation d'un sondage DATE, accepter les horaires au format "8h" ou "8H",
	- Lors de la cr??ation d'un sondage DATE, possibilit?? de copier des horaires entre les dates,
	- Lors d'une modification de ligne, cocher les cases initialement choisies et non pas des cases vides,
	- Changement du format d'affichage des dates pour un formatage type : "Mardi 13/06",
	- Meilleure visualisation des choix les plus vot??s,
	- Possibilit?? pour l'administrateur du sondage de choisir de recevoir un mail d'alerte ?? chaque participation d'un sond??,
	- Remplacement des boutons de formulaire par des images moins aust??res,
	- Correction de quelques petits bugs d'affichage,
	- Possibilit?? de rajouter des cases suppl??mentaires lors de la cr??ation d'un sondage AUTRE,
	- Possibilit?? de rajouter des cases suppl??mentaires lors de la cr??ation d'un sondage DATE.
