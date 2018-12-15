# Installer mon espace de travail de développement Full-Stack LAMP/JS sous Windows 10

*Ce cours est initialement destiné à des élèves d'un cursus "Développeur Intégrateur Web" en présentiel.*

Nous allons installer les outils nécessaires pour travailler de façon efficace sous Windows, avec un ensemble d'outils nous rapporchant d'un workflow sous Linux ou Mac en utilisant le sous-système Windows pour Linux (Windows Subsystem for Linux  - WSL).

# Outils

 - **Hyper** : Un terminal puissant et plein d'extensions (hyper.is)

# WSL et espace de travail (facultatif)
*L'installation de WSL reste facultative : la possibilité de travailler avec Linux sous Windows est extrêmement intéressante et vous familiarisera avec des notions importantes de l'écosystème du développement web. Néanmoins les outils que nous utilisons (Git, Node, npm, Apache, PHP, MySQL) sont tous disponibles sous Windows : vous ne profiterez pas d'un système Linux englobant le tout mais tout fonctionnera très bien aussi.*

## WSL
**Avant de commencer, assurez-vous d'avoir votre antivirus désactivé !**
 1. Ouvrir **PowerShell** (touche Windows => "Powershell") et **l'exécuter en tant qu'administrateur** (clic-droit, "Exécuter en tant qu'administrateur")
 2. **Saisir dans l'invite de commande** la ligne suivante :
 `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`
 3. Ouvrir **Microsoft Store**
 4. Rechercher et installer **Ubuntu**
 5. Lorsque Ubuntu est installé, une invite de commande doit s'ouvrir. Sinon, ouvrez Ubuntu depuis le menu Windows.
 6. L'invite de commande vous propose de créer un utilisateur. Saisissez un identifiant et un mot de passe : le mot de passe ne s'affiche pas, c'est normal ! C'est l'équivalent des "petites étoiles" des formulaires.

## Espace de travail
*Nous allons créer un alias vous permettant en une commande (`devws` comme "development workspace") d'accéder à votre dossier de travail depuis le terminal Ubuntu. **Il est extrêmement important de faire attention à chaque instant à ce que vous tapez : comme en programmation, à la moindre faute d'orthographe, d'accents, de majuscules, de guillemets et symboles spéciaux, cela ne marchera pas**.
Attention : n'écrivez pas les symboles `$` en début de ligne: ils signifient simplement qu'il s'agit d'une ligne de commande à taper dans un terminal.*
1.  A l'aide de **cd** et **ls**, retrouvez le chemin vers votre dossier de travail habituel. Habituellement, votre dossier personnel se trouve dans le chemin suivant :
`/mnt/c/Users/[nom_user]/[Documents, Desktop, etc.]`
2. Une fois le chemin trouvé et noté **sans aucune faute d'orthographe, d'accents, de majuscules**, saisissez :
$ `echo "alias devws='/mnt/c/Users/nom_user/Desktop/mon_workspace'" >> ~/.bash_aliases`
$ `source ~/.bashrc`  
3. Dorénavant, en saisissant "devws", vous accéderez à votre dossier de travail.

# Node.js  & npm
## Avec Linux
*Nous allons installer la dernière version LTS en date de Node.js. Pour tester l'installation de node.js et npm (qui s'installe en même temps), vous pourrez taper dans un terminal : `node -v && npm -v`, ce qui vous affichera vos versions installées de Node.js et de npm si tout s'est bien déroulé.**
$ `curl -sL https://deb.nodesource.com/setup_10.x | sudo -E bash -`
$ `sudo apt install -y nodejs`

## Avec Windows ou MacOS
**Si vous avez sauté l'étape WSL :** vous pouvez tout simplement installer le .exe ou .dmg en allant le télécharger sur https://nodejs.org. 

Pour travailler avec les commandes `node` et `npm`, vous ouvrirez une invite de commande (en saisissant "cmd" dans le menu Windows, en ouvrant un Terminal sous MacOS).

# Git
## Avec Linux
Git devrait déjà être installé ! Pour le vérifier : `git --version`. Sinon, `sudo apt install git`.

## Windows et MacOS
Installez avec l'exécutable depuis le site officiel : https://git-scm.com. Une fois installé, la commande `git` deviendra disponible dans l'invite de commande et dans le Terminal.

#  Angular & setup d'un projet Angular
Installer Angular :
$ `npm install -g @angular/cli`
*Une fois dans le dossier de travail dans lequel vous souhaitez installer votre projet Angular :*
$ `ng new monProjet`
$ `cd monProjet`

# PHP, Apache, MySQL
*à venir*

