# Installation de Packer sur Windows

Suivez ces étapes simples pour installer Packer sur votre système Windows :

1. **Téléchargement de Packer :**
   - Rendez-vous sur le site officiel de Packer : [Lien Packer](https://www.packer.io/downloads)
   - Téléchargez le fichier exécutable : AMD64 ou 386

2. **Placement du fichier exécutable :**
   Une fois le téléchargement terminé, aller dans votre répertoire `Programmes`, créé un nouveau dossier ou vous allez placer l'exécutable
	
   - Une fois le téléchargement terminé, accédez à votre répertoire `Programmes`.
   - Créez un nouveau dossier où vous placerez l'exécutable Packer.

4. **Ajout au PATH :**
   Ajoutez le chemin du répertoire où Packer sera installé à votre variable d'environnement PATH. Cela permettra d'accéder à Packer de n'importe où dans votre ligne de commande.
	
   - Copiez le lien vers le dossier où se situe votre exécutable Packer (par exemple, `C:\Program Files\Packer`).
   - Dans la barre de recherche Windows, tapez `Modifier les variables d'environnement pour votre compte`.
   - Double-cliquez sur `Path`, puis cliquez sur "Nouveau" et ajoutez le chemin vers le dossier Packer que vous avez copié précédemment.

6. **Exécution de Packer :**
   - Terminez le processus d'installation en exécutant Packer.

7. **Vérification de l'installation :**
   - Ouvrez une nouvelle fenêtre de terminal (cmd) et tapez la commande suivante : `packer --version`
   - Vous devriez voir la version de Packer que vous venez d'installer s'afficher, confirmant ainsi que Packer est maintenant installé sur votre système Windows.

Vous avez maintenant réussi à installer Packer sur votre ordinateur Windows. 


# Installation de Packer sur Linux

Suivez ces étapes simples pour installer Packer sur votre système Linux :


1. **Téléchargement de Packer :**
   - Rendez-vous sur le site officiel de Packer : [Lien Packer](https://www.packer.io/downloads)
   - Téléchargez le fichier exécutable : AMD64 ou 386
   ou 
   - Via Packege manager:
	 ```
	 wget -O- https://apt.releases.hashicorp.com/gpg | sudo gpg --dearmor -o /usr/share/keyrings/hashicorp-archive-keyring.gpg
	 echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list
	 sudo apt update && sudo apt install packer
	 ```

2. **Vérification de l'installation :**
   - Après l'installation, vérifiez que Packer est correctement installé en tapant la commande : `packer --version`
   - Vous devriez voir la version de Packer s'afficher.
   
