# Test de Packer

Suivez ces étapes pour tester Packer sur votre système Windows :

1. **Création d'un fichier de configuration :**
   - Créez un fichier de configuration Packer en utilisant JSON ou HCL (HashiCorp Configuration Language).
   - Exemple (fichier `exemple.json` en JSON) :
     ```json
     {
       "builders": [
         {
           "type": "virtualbox-iso",
           "iso_url": "path/to/os_image.iso",
           "iso_checksum": "checksum",
           "boot_command": [
             "<esc><wait>",
             "<esc><wait>",
             "<enter><wait>"
           ],
           "vm_name": "packer-example",
           "guest_os_type": "Windows2016_64"
         }
       ],
       "provisioners": [
         {
           "type": "shell",
           "script": "script.ps1"
         }
       ]
     }
     ```

4. **Validation du fichier de configuration :**
   - Utilisez la commande suivante pour valider votre fichier de configuration :
     ```bash
     packer validate exemple.json
     ```

5. **Construction de l'image :**
   - Utilisez la commande suivante pour commencer le processus de construction de l'image :
     ```bash
     packer build exemple.json
     ```
   - Packer créera une machine virtuelle, appliquera les configurations spécifiées, puis générera une image.

6. **Vérification du résultat :**
   - Une fois le processus terminé, vérifiez l'image générée dans votre environnement cible.

Vous avez maintenant testé avec succès Packer sur votre système Windows. N'hésitez pas à explorer davantage les fonctionnalités de Packer en consultant la documentation officielle. Bonne utilisation !
