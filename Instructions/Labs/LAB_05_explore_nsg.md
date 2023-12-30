<!---
---
Labo : Titre : « Découvrir les groupes de sécurité réseau Azure » Parcours d’apprentissage/Module/Unité : « Parcours d’apprentissage : Décrire les fonctionnalités des solutions de sécurité Microsoft ; Module 1 : Décrire les fonctionnalités de sécurité de base dans Azure ; Unité 6 : Décrire les groupes de sécurité réseau Azure »
---
--->

# Labo : Explorer les groupes de sécurité réseau Azure (NSG)

Ce labo correspond au contenu Learn suivant :

- Parcours d’apprentissage : Décrire les fonctionnalités des solutions de sécurité Microsoft
- Module : Décrire les principales fonctionnalités de sécurité dans Azure
- Unité : Décrire les groupes de sécurité réseau Azure

## Scénario du labo

Dans ce labo, vous allez explorer la fonction des groupes de sécurité réseau dans Azure.  Pour cela, vous créerez un groupe de sécurité réseau (NSG), puis vous l’affecterez à l’interface d’une machine virtuelle préexistante.  Une fois la configuration terminée, vous examinerez les règles de trafic entrant et sortant par défaut, puis vous créerez des règles et les testerez.  Dans ce labo, la machine virtuelle que vous utiliserez avec le groupe de sécurité réseau a été créée pour vous. Vous commencerez donc par examiner certaines des informations associées à cette machine virtuelle.
  
**Durée estimée** : 30 à 45 minutes

### Tâche 1

Dans cette tâche, vous allez explorer certains des paramètres associés à la machine virtuelle qui a été créée spécifiquement pour ce labo.

1. Ouvrez Microsoft Edge.  Dans la barre d’adresse, entrez **https://portal.azure.com** .

1. Connectez-vous avec vos informations d’identification d’administrateur.
    1. Dans la fenêtre de connexion, entrez le nom d’utilisateur fourni par votre fournisseur d’hébergement de labo, puis sélectionnez **Suivant**.
    1. Entrez le mot de passe d’administrateur qui vous a été communiqué par votre fournisseur d’hébergement de labo. Cliquez sur **Connexion**.
    1. Si vous êtes invité à rester connecté, sélectionnez **Oui**.

1. En haut de la page, sous l’intitulé Services Azure, sélectionnez **Machines virtuelles**.  Si vous ne voyez pas cet élément dans la liste, dans la barre de recherche, dans la barre bleue en haut de la page à côté de l’intitulé Microsoft Azure, entrez **Machines virtuelles**, puis sélectionnez **Machines virtuelles** dans les résultats de la recherche.

1. Dans la page Machines virtuelles, sélectionnez la machine virtuelle appelée **SC900-WinVM**.

1. Vous êtes à présent dans la page SC900-WinVM.  Notez certaines des informations de base sur la machine virtuelle.

1. En haut de la page, sélectionnez **Connexion**.  Sélectionnez l’option **Vérifier l’accès**, qui est listée sous l’adresse IP.  Cette vérification est effectuée en utilisant le port 3389, qui est le port de la connectivité RDP.  Vous devez voir le message « Vérification impossible ».  Dans la zone Protocole RDP natif, cliquez sur **Sélectionner**.  Dans la fenêtre qui s’ouvre, sous « 1 Configurer les prérequis du protocole RDP natif », vous devez voir « Azure doit configurer certaines fonctionnalités pour se connecter à la machine virtuelle ».  Dans la tâche suivante, vous configurez un NSG pour autoriser explicitement la connexion RDP.


1. Dans le volet de navigation de gauche, sélectionnez **Réseau**.  
    1. La vue par défaut affiche les règles de port d’entrée.  Notez que l’interface réseau de cette machine virtuelle n’a aucun groupe de sécurité réseau configuré.  C’est la même chose si vous sélectionnez la vue des règles de port de sortie.
    1. Sélectionnez **Règles de sécurité effectives** en regard de l’intitulé Interface réseau.  Notez ce message : « Aucun groupe de sécurité réseau ou groupe de sécurité d'application n'est associé à l'interface réseau ».

1. Laissez cet onglet de navigateur ouvert.


### Tâche 2

Dans cette tâche, vous allez créer un groupe de sécurité réseau, affecter l’interface réseau de la machine virtuelle à ce groupe de sécurité réseau et créer une règle de trafic RDP entrant.

1. Sous l’onglet NSG ouvert, *cliquez avec le bouton droit* sur le lien **Accueil** en haut de la page et sélectionnez **Ouvrir le lien dans un nouvel onglet** pour ouvrir une autre page vers les services Azure.

1. Dans la barre de recherche bleue en haut de la page, entrez **Groupes de sécurité réseau** et, dans les résultats, sélectionnez **Groupes de sécurité réseau**. Ne sélectionnez pas *Groupes de sécurité réseau (classique)* .

1. En haut de la page Groupes de sécurité réseau, sélectionnez **+ Créer**.

1. Sous l’onglet Options de base de la page Créer un groupe de sécurité réseau, spécifiez les paramètres suivants :
    1. Abonnement : conservez la valeur par défaut (il s’agit de l’abonnement Azure fourni par l’hébergeur de labo autorisé)
    1. Groupe de ressources : **LabsSC900**
    1. Nom : **NSG-SC900**
    1. Région : laissez la valeur par défaut.
    1. Sélectionnez **Vérifier + créer**, puis sélectionnez **Créer**.

1. Une fois le déploiement effectué, sélectionnez **Accéder à la ressource**.

1. En haut de la page, sous la mention Informations de base, vous voyez des informations générales sur le groupe de sécurité réseau que vous avez créé.  Deux points sont à noter : il n’y a pas de règles de sécurité personnalisées et il n’y a pas de sous-réseaux ni d’interfaces réseau associés à ce groupe de sécurité réseau.  Il n’y a aucune règle de sécurité personnalisée, mais il y a des règles de trafic entrant et sortant par défaut qui sont incluses avec chaque groupe de sécurité réseau, comme indiqué sur la page.  Passez en revue les règles entrantes et sortantes. Les règles de trafic entrant par défaut refusent tout le trafic entrant qui ne provient pas d’un réseau virtuel ou d’un équilibreur de charge Azure.  Les règles de trafic sortant refusent tout le trafic sortant, à l’exception du trafic entre les réseaux virtuels et du trafic sortant vers Internet.

1. Dans le volet de navigation gauche de la page NSG-SC900, sous Paramètres, sélectionnez **Interfaces réseau**.
    1. Sélectionnez **Associer**.
    2. Dans le champ des associations d’interface réseau, sélectionnez la **flèche vers le bas**, sélectionnez **sc900-winvmXXX**, puis **OK** en bas de la fenêtre. Une fois que l’interface est associée au NSG, elle apparaît dans la liste.

1. Dans le volet de navigation gauche, sélectionnez **Règles de sécurité de trafic entrant**.

1. Les règles de trafic entrant par défaut refusent tout trafic entrant qui ne provient pas d’un réseau virtuel ou d’un équilibreur de charge Azure. Vous devez donc configurer une règle qui autorise le trafic RDP entrant (trafic sur le port 3389). N’oubliez pas que vous ne pouvez pas supprimer les règles par défaut. Toutefois, vous pouvez les remplacer en créant des règles dont la priorité est plus élevée.

1. En haut de la page, sélectionnez **Ajouter**. Sur la fenêtre Ajouter une règle de sécurité de trafic entrant, spécifiez les paramètres suivants :
    1. Source : **quelconque**
    1. Plages de ports sources : **\***
    1. Destination : **quelconque**
    1. Service : **RDP**
    1. Action : **Autoriser**
    1. Priorité : **1000**. Les règles avec les plus petits nombres ont une priorité plus élevée et sont traitées en premier.
    1. Nom : conservez le nom par défaut ou ajoutez votre propre nom descriptif.
    1. Notez la présence du signe d’avertissement en bas de la fenêtre.  Nous utilisons RDP uniquement à des fins de test et pour illustrer les fonctionnalités du groupe de sécurité réseau.
    1. Sélectionnez **Ajouter**

1. Une fois la règle provisionnée, elle s’affiche dans la liste des règles de trafic entrant (vous devez peut-être actualiser l’écran).

1. Laissez cet onglet de navigateur ouvert.  

### Tâche 3

Dans cette tâche, vous allez tester la nouvelle règle de groupe de sécurité réseau entrante pour vérifier que vous pouvez établir une connexion Bureau à distance (RDP) à la machine virtuelle.  Une fois connecté à la machine virtuelle, vous vérifiez la connectivité sortante vers Internet à partir de la machine virtuelle.

1. Ouvrez l’onglet SC900-WinVM - Microsoft Azure dans votre navigateur. Si vous aviez fermé l’onglet du navigateur, ouvrez un nouvel onglet de navigateur, entrez **https://portal.azure.com** , puis sélectionnez **Machines virtuelles** et la machine virtuelle **SC900-WinVM**.

1. Sélectionnez **Se connecter** dans le volet de navigation de gauche.

1. Sélectionnez **vérifier l’accès** (vérifiez que le port est défini sur 3389).  L'état doit être « Accessible ».

1. Connectez-vous maintenant directement à la machine virtuelle en cliquant sur **Sélectionner** dans la zone qui indique le protocole RDP natif.
   
    1. Dans la fenêtre Protocole RDP natif qui s’ouvre, sélectionnez **Télécharger le fichier RDP**.
    1. Si un avertissement de téléchargement s’affiche, sélectionnez **Conserver** puis, dans la fenêtre contextuelle qui s’affiche, sélectionnez **Ouvrir le fichier**.
    1. Dans la fenêtre Connexion Bureau à distance qui s’ouvre, sélectionnez **Connexion**.
    1. Vous êtes invité à entrer vos informations d’identification.  Entrez le nom d’utilisateur et le mot de passe (consultez l’onglet des ressources dans le panneau d’instructions du labo).
    1. Une fenêtre de connexion Bureau à distance s’ouvre et indique que *L’identité de l’ordinateur distant ne peut pas être vérifiée. Voulez-vous vous connecter quand même ?*  Sélectionnez **Oui**.

1. Vous êtes maintenant connecté à la machine virtuelle. Dans ce cas-ci, vous avez pu vous connecter à la machine virtuelle, car la règle de trafic entrant que vous avez créée autorise le trafic entrant pour la machine virtuelle via RDP.  Au bout de quelques secondes dans l’écran d’accueil, vous pouvez voir une fenêtre vous permettant de choisir les paramètres de confidentialité de votre appareil. Sélectionnez **Accepter**.  Si la fenêtre Réseaux s’affiche, sélectionnez **Non**.

1. Dès que la machine virtuelle est opérationnelle, testez la connectivité sortante vers Internet à partir de cette machine.
    1. Dans la machine virtuelle ouverte, sélectionnez **Microsoft Edge** pour ouvrir le navigateur.  Étant donné que c’est la première fois que vous ouvrez Microsoft Edge, il est possible qu’une fenêtre contextuelle s’affiche. Sélectionnez **Démarrer sans vos données**, sélectionnez **Continuer sans ces données**, puis sélectionnez **Confirmer et commencer la navigation**.
    1. Entrez **www.bing.com** dans la barre d’adresse du navigateur et vérifiez que vous pouvez vous connecter au moteur de recherche.
    1. Une fois que vous avez vérifié votre accès à www.bing.com, fermez la fenêtre du navigateur dans la machine virtuelle, mais laissez la machine virtuelle allumée.

1. Réduisez la machine virtuelle en sélectionnant le trait de soulignement **_** sous l’onglet bleu qui affiche l’adresse IP de la machine virtuelle. Vous revenez dans la page SC900-WinVM \| Connexion.

1. Gardez l’onglet de navigateur ouvert, vous en avez besoin dans la prochaine tâche.

### Tâche 4

Dans la tâche précédente, vous avez vérifié que vous pouviez établir une connexion RDP à la machine virtuelle. Dans la machine virtuelle, vous avez également vérifié que vous pouvez établir une connexion sortante vers Internet.  Le trafic Internet sortant est autorisé, car les règles de trafic sortant par défaut des NSG l’autorisent.  Dans cette tâche, vous suivez le processus de création et de test d’une règle de trafic sortant personnalisée pour bloquer le trafic Internet sortant.

1. Vous êtes normalement dans la page SC900-WinVM \| Connexion. Dans le volet de navigation de gauche, sélectionnez **Réseau**. Si vous avez précédemment fermé l’onglet du navigateur, sélectionnez la barre de recherche bleue en haut de la page, sélectionnez Machines virtuelles, sélectionnez la machine virtuelle appelée **SC900-WinVM**, puis sélectionnez **Réseau**.

1. Sélectionnez l’onglet **Règles de port de trafic sortant**. Les règles de trafic sortant par défaut s’affichent.  Notez la règle par défaut « AllowInternetOutBound ». Cette règle autorise tout le trafic Internet sortant. Vous ne pouvez pas supprimer la règle par défaut, mais vous pouvez la remplacer en créant une règle de priorité plus élevée. À droite de la page, sélectionnez **Ajouter une règle de port de sortie**.

1. Sur la page Ajouter une règle de sécurité de sortie, spécifiez les paramètres suivants :
    1. Source : **quelconque**
    1. Plages de ports source : **\***
    1. Destination : **étiquette de service**
    1. Étiquette de service de destination : **internet**
    1. Service : **Personnalisé** (conserver la valeur par défaut)
    1. Plages de ports de destination : **\*** (veillez à placer un astérisque dans le champ des plages de ports de destination)
    1. Protocole : **quelconque**
    1. Action : **Deny**
    1. Priorité : **1000**
    1. Nom : conservez le nom par défaut ou ajoutez votre propre nom descriptif.
    1. Sélectionnez **Ajouter**

1. Une fois la règle configurée, elle apparaît dans la liste des règles de sortie.  Bien qu’elle apparaisse dans la liste, il faudra quelques minutes pour qu’elle prenne effet. (Attendez quelques minutes avant de passer aux étapes suivantes).  


1. Revenez dans votre machine virtuelle (l’icône RDP de la machine virtuelle doit s’afficher dans la barre des tâches en bas de la page).

1. Ouvrez le navigateur Microsoft Edge dans votre machine virtuelle et entrez **www.bing.com**. La page ne doit pas s’afficher. Si vous pouvez vous connecter à Internet et que vous avez vérifié que tous les paramètres de la règle de trafic sortant ont été correctement définis, c’est probablement parce qu’il faut quelques minutes pour que la règle prenne effet.  Fermez le navigateur, attendez quelques minutes et réessayez. Les abonnements Azure dans l’environnement lab peuvent avoir des délais plus longs que la normale.


1. Fermez la connexion bureau à distance en sélectionnant le **X** situé en haut du centre de la page où l’adresse IP est affichée.  Une fenêtre contextuelle s’affiche, indiquant « Votre session à distance sera déconnectée ». Cliquez sur **OK**.

1. En haut à gauche de la fenêtre, juste en dessous de la barre bleue qui indique Microsoft Azure, sélectionnez **Accueil** pour revenir à la page d’accueil des services Azure.

1. Gardez l’onglet Azure ouvert dans votre navigateur.

### Révision

Dans ce labo, vous avez suivi le processus de configuration d’un groupe de sécurité réseau (NSG), en associant ce NSG à l’interface réseau d’une machine virtuelle, et en ajoutant de nouvelles règles au NSG pour autoriser le trafic RDP entrant et bloquer le trafic Internet sortant.
