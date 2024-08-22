 ## MAC-Spoofer ## 


## mac spoofer c'est quoi ?
Usurpation d'adresse MAC
L'usurpation d'adresse MAC est une méthode qui permet de changer l'identifiant unique, connu sous le nom d'adresse de contrôle d'accès au média (MAC), attribué à un contrôleur d'interface réseau (NIC) sur un appareil. Chaque NIC possède une adresse MAC attribuée par le fabricant, qui identifie de manière unique l'appareil sur un réseau. En changeant l'adresse MAC, les utilisateurs peuvent masquer leur véritable identité sur le réseau, permettant une opération anonyme ou le contournement des restrictions réseau. Cela peut être réalisé soit par le biais de logiciels spécifiques, soit en ajustant manuellement les paramètres réseau de l'appareil.

## Comment ça fonctionne?

Vérification des droits administratifs : Le script vérifie d'abord s'il dispose des privilèges administratifs, nécessaires pour modifier les paramètres réseau. Si ce n'est pas le cas, il en fait la demande.
Menu de sélection : Le script énumère ensuite tous les contrôleurs d'interface réseau (NIC) de votre système et les affiche dans une liste. Vous pouvez sélectionner le NIC que vous souhaitez modifier en entrant son numéro correspondant.
Menu d'actions : Une fois un NIC sélectionné, le script affiche une liste d'actions que vous pouvez effectuer : usurper l'adresse MAC, revenir à l'adresse MAC d'origine, ou définir une adresse MAC personnalisée. Vous pouvez sélectionner l'action que vous souhaitez effectuer en entrant son numéro correspondant.
Exécution de l'action : En fonction de votre sélection, le script effectuera l'action correspondante :
Usurper l'adresse MAC : Le script génère une adresse MAC aléatoire et l'attribue au NIC sélectionné.
Revenir à l'adresse MAC d'origine : Le script supprime l'adresse MAC personnalisée du NIC sélectionné, ce qui le fait revenir à son adresse MAC d'origine.
Définir une adresse MAC personnalisée : Le script vous invite à entrer une adresse MAC personnalisée, qu'il attribue ensuite au NIC sélectionné.
Après avoir effectué l'action, le script revient au menu de sélection, vous permettant d'effectuer des actions sur d'autres NIC ou sur le même NIC à nouveau.

## Lectures complémentaires
- [Connaissances techniques générales](https://wikipedia.org/wiki/MAC_address)
- [Différences entre CurrentControlSet, ControlSet001 et ControlSet002](https://stackoverflow.com/questions/291519/how-does-currentcontrolset-differ-from-controlset001-and-controlset002)
- [Problèmes avec les NIC sans fil sous Windows 7 et solutions de contournement](https://blog.technitium.com/2011/05/tmac-issue-with-wireless-network.html)

- Remarque importante sur le registre Windows
Dans le registre Windows, la clé HKLM\SYSTEM\CurrentControlSet\Control\Class\{4d36e972-e325-11ce-bfc1-08002be10318} est cruciale pour la gestion et le stockage des informations des adaptateurs réseau. Chaque sous-clé de cette classe correspond à un adaptateur réseau spécifique installé sur le système.

Identifiant de classe (CLSID) : {4d36e972-e325-11ce-bfc1-08002be10318} est un identifiant de classe (CLSID) associé à la classe "Adaptateurs réseau" dans le gestionnaire de périphériques Windows.
Sous-clés et indices : Sous cette clé de classe, vous trouverez des sous-clés avec des indices numériques, chacune représentant un adaptateur réseau différent. Par exemple, HKLM\SYSTEM\CurrentControlSet\Control\Class\{4d36e972-e325-11ce-bfc1-08002be10318}\0000 représente le premier adaptateur réseau.
Valeurs des clés :
NetCfgInstanceId : Contient un identifiant unique pour l'adaptateur réseau.
DriverDesc : Fournit une description lisible par l'homme ou le nom de l'adaptateur réseau.
NetworkAddress : Stocke l'adresse MAC de l'adaptateur réseau.

Guides visuels
Récupération et affichage des légendes des NIC :

![Récupération et affichage des légendes des NIC :
](https://github.com/Scrut1ny/Windows-MAC-Address-Spoofer/assets/53458032/982813d4-da4d-4631-84c6-f9480c1dcff9)

Affichage des sous-clés du registre (également appelées Indexes à partir d'une légende) sous le CLSID :

![Affichage des sous-clés du registre (également appelées Indexes à partir d'une légende) sous le CLSID :](https://github.com/Scrut1ny/Windows-MAC-Address-Spoofer/assets/53458032/02dc8ed8-1bd9-43d4-8cd1-464da63a5b43)
