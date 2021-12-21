# pearOS-plymouth
Default plymouth of pearOS

Forked from : https://github.com/navisjayaseelan/apple-mac-plymouth

## Screenshot :

![screenshot](https://user-images.githubusercontent.com/74509560/146959907-1058b28a-4e4f-4cfe-85df-c9f629323a32.png)

##How to install


    Pour choisir un thème,

    tapez :

    'sudo update-alternatives --config default.plymouth'

    Vous avez alors un écran de ce type :

     'Il existe 6 choix pour l'alternative default.plymouth (qui fournit /usr/share/plymouth/themes/default.plymouth).
     
      Sélection   Chemin                                                 Priorité  État
    ------------------------------------------------------------
    * 0            /usr/share/plymouth/themes/ubuntu-logo/ubuntu-logo.plymouth   100       mode automatique
      1            /usr/share/plymouth/themes/fade-in/fade-in.plymouth           10        mode manuel
      2            /usr/share/plymouth/themes/glow/glow.plymouth                 10        mode manuel
      3            /usr/share/plymouth/themes/script/script.plymouth             10        mode manuel
      4            /usr/share/plymouth/themes/solar/solar.plymouth               10        mode manuel
      5            /usr/share/plymouth/themes/spinfinity/spinfinity.plymouth     10        mode manuel
      6            /usr/share/plymouth/themes/ubuntu-logo/ubuntu-logo.plymouth   100       mode manuel'

Appuyez sur <Entrée> pour conserver la valeur par défaut[*] ou choisissez le numéro sélectionné :

    Faites votre choix en tapant un numéro au clavier.
    Pour prendre en compte les changements :

    sudo update-initramfs -u

    Redémarrez.

Admirez !

Il est possible de visualiser le thème Plymouth sans redémarrer. Pour cela,

    il faut lancer le démon Plymouthd (à chaque nouvelle visualisation) avec la commande :

    sudo plymouthd

    Puis lui demander de visualiser le thème actuel:

    sudo plymouth --show-splash

    Pour quitter, il suffit d'un simple :

    sudo plymouth quit

Pour tout faire en une fois, lancer le démon, avoir un aperçu de 20 secondes, puis quitter l'aperçu, on peut aussi lancer la commande :

sudo plymouthd && sudo plymouth --show-splash && sleep 20 && sudo plymouth quit