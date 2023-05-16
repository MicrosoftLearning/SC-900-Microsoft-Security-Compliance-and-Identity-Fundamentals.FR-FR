---
demo:
  title: 'Groupes de sécurité réseau Azure'
  module: 'Module 1 : Décrire les fonctionnalités de sécurité de base dans Azure'
---


# <a name="demo-azure-network-security-groups-nsgs"></a>Démonstration : Groupes de sécurité réseau Azure

Cette démonstration correspond au contenu Learn suivant :

- Parcours d’apprentissage : Décrire les fonctionnalités des solutions de sécurité Microsoft
- Module : Décrire les principales fonctionnalités de sécurité dans Azure
- Unité : Décrire les groupes de sécurité réseau Azure

## <a name="demo-scenario"></a>Scénario de la démonstration

Dans cette démonstration, vous allez explorer la fonction des groupes de sécurité réseau dans Azure et appliquer un groupe de sécurité réseau à une machine virtuelle préalablement créée. Vous commencerez par présenter brièvement les informations relatives à la machine virtuelle qui a été précréée par l’hébergeur ALH (Authorized Lab Hoster). Ensuite, vous montrerez le processus de création d’un groupe de sécurité réseau (NSG), vous présenterez les règles de trafic entrant et sortant par défaut, vous créerez une règle RDP pour autoriser la connexion à la machine virtuelle et vous testerez cette règle.

### <a name="demo-part-1"></a>Partie 1 de la démonstration

Dans cette partie, vous allez explorer certains des paramètres associés à la machine virtuelle qui a été créée spécifiquement pour ce labo.

1. Ouvrez Microsoft Edge.  Dans la barre d’adresse, entrez **portal.azure.com**.

1. Connectez-vous avec vos informations d’identification d’administrateur.
    1. Dans la fenêtre de connexion, entrez le nom d’utilisateur fourni par votre fournisseur d’hébergement de labo, puis sélectionnez **Suivant**.
    1. Entrez le mot de passe d’administrateur qui vous a été communiqué par votre fournisseur d’hébergement de labo. Sélectionnez **Connexion**.
    1. Si vous êtes invité à rester connecté, sélectionnez **Oui**.

1. En haut de la page, sous l’intitulé Services Azure, sélectionnez **Machines virtuelles**.  Si vous ne voyez pas cet élément dans la liste, dans la barre de recherche, dans la barre bleue en haut de la page à côté de l’intitulé Microsoft Azure, entrez **Machines virtuelles**, puis sélectionnez **Machines virtuelles** dans les résultats de la recherche.

1. Dans la page Machines virtuelles, sélectionnez la machine virtuelle appelée **SC900-WinVM**.

1. Vous êtes à présent dans la page SC900-WinVM.  Notez le nom du groupe de ressources, LabsSC900, dans lequel réside la machine virtuelle.

1. En haut de la page, sélectionnez **Se connecter** puis, dans la liste déroulante, sélectionnez **RDP**. Notez que le prérequis concernant le port n’est pas respecté.  Pour satisfaire au prérequis, une règle de sécurité réseau de trafic entrant avec le port de destination 3389 utilisé par le protocole RDP doit être configurée.  Vous configurerez la règle à la prochaine étape quand vous créerez un groupe de sécurité réseau.

1. Dans le volet de navigation de gauche, sélectionnez **Réseau**.  
    1. La vue par défaut affiche les règles de port d’entrée.  Notez que l’interface réseau de cette machine virtuelle n’a aucun groupe de sécurité réseau configuré.  C’est la même chose si vous sélectionnez la vue des règles de port de sortie.
    1. Sélectionnez **Règles de sécurité effectives** en regard de l’intitulé Interface réseau.  Notez ce message : « Aucun groupe de sécurité réseau ou groupe de sécurité d'application n'est associé à l'interface réseau ».
1. Laissez cet onglet de navigateur ouvert.

### <a name="demo-part-2"></a>Partie 2 de la démonstration

Dans cette partie, vous allez créer un groupe de sécurité réseau, affecter l’interface réseau de la machine virtuelle à ce groupe de sécurité réseau et créer une règle de trafic RDP entrant.

1. Ouvrez l’onglet SC900-WinVM - Microsoft Azure dans votre navigateur.

1. Dans la barre de recherche bleue en haut de la page, entrez **Groupes de sécurité réseau**. Dans les résultats, sélectionnez **Groupes de sécurité réseau** (ne sélectionnez pas Groupes de sécurité réseau classiques).

1. En haut de la page Groupes de sécurité réseau, sélectionnez **+ Créer**.

1. Sous l’onglet de base de la page Créer un groupe de sécurité réseau, spécifiez les paramètres suivants :
    1. Abonnement : conservez la valeur par défaut (il s’agit de l’abonnement Azure fourni par l’hébergeur de labo autorisé)
    1. Groupe de ressources :  **LabsSC900**
    1. Nom :  **NSG-SC900**
    1. Région : laissez la valeur par défaut.
    1. Sélectionnez **Examiner et créer** puis sélectionnez **Créer**.

1. Une fois le déploiement effectué, sélectionnez **Accéder à la ressource**.

1. En haut de la page, sous la mention Informations de base, vous voyez des informations générales sur le groupe de sécurité réseau que vous avez créé.  Deux points sont à noter : il n’y a pas de règles de sécurité PERSONNALISÉES et il n’y a pas de sous-réseaux ni d’interfaces réseau associés à ce groupe de sécurité réseau.  Il n’y a aucune règle de sécurité personnalisée, mais il y a des règles de trafic entrant et sortant par défaut qui sont incluses avec chaque groupe de sécurité réseau, comme indiqué sur la page.  Passez en revue les règles entrantes et sortantes. Les règles de trafic entrant par défaut refusent tout le trafic entrant qui ne provient pas d’un réseau virtuel ou d’un équilibreur de charge Azure.  Les règles de trafic sortant refusent tout le trafic sortant, à l’exception du trafic entre les réseaux virtuels et du trafic sortant vers Internet.

1. Dans le volet de navigation gauche de la page NSG-SC900, sous Paramètres, sélectionnez **Interfaces réseau**.
    1. Sélectionnez **Associer**.
    1. Dans le champ de sélection des associations d’interface réseau, sélectionnez la **flèche vers le bas**, sélectionnez **sc900-winvmXXX**, puis sélectionnez **OK** en bas de la fenêtre. Une fois l’interface associée au groupe de sécurité réseau, elle s’affiche dans la liste.

1. Dans le volet de navigation gauche, sélectionnez **Règles de sécurité de trafic entrant**. Les règles de trafic entrant par défaut refusent tout trafic entrant qui ne provient pas d’un réseau virtuel ou d’un équilibreur de charge Azure. Vous devez donc configurer une règle qui autorise le trafic RDP entrant (trafic sur le port 3389). N’oubliez pas que vous ne pouvez pas supprimer les règles par défaut. Toutefois, vous pouvez les remplacer en créant des règles dont la priorité est plus élevée.

1. En haut de la page, sélectionnez **Ajouter**. Sur la fenêtre Ajouter une règle de sécurité de trafic entrant, spécifiez les paramètres suivants :
    1. Source :  **Any**
    1. Plages de ports sources : **\***
    1. Destination :  **Any**
    1. Service :  **RDP**
    1. Action :  **Autoriser**
    1. Priorité : **1000** ; Remarque : les règles avec les nombres les plus petits ont une priorité plus élevée et sont traitées en premier.
    1. Nom : conservez le nom par défaut ou ajoutez votre propre nom descriptif.
    1. Notez la présence du signe d’avertissement en bas de la fenêtre.  Nous utilisons RDP uniquement à des fins de test et pour illustrer les fonctionnalités du groupe de sécurité réseau.
    1. Sélectionnez **Ajouter**

1. Une fois la règle provisionnée, elle s’affiche dans la liste des règles de trafic entrant (vous devez peut-être actualiser l’écran). Un signe d’avertissement s’affiche sur la nouvelle règle ajoutée.  Comme nous l’avons dit plus haut, nous utilisons RDP uniquement à des fins de test et pour illustrer les fonctionnalités du groupe de sécurité réseau.

### <a name="demo-part-3"></a>Partie 3 de la démonstration

Après avoir créé le groupe de sécurité réseau, associé ce groupe à votre machine virtuelle et créé la règle RDP, vous allez montrer l’impact du groupe de sécurité réseau en testant la connexion RDP à la machine virtuelle.

1. Ouvrez l’onglet SC900-WinVM - Microsoft Azure dans votre navigateur. Si vous avez précédemment fermé l’onglet du navigateur, sélectionnez la barre de recherche bleue en haut de la page, sélectionnez Machines virtuelles, puis sélectionnez la machine virtuelle appelée **SC900-WinVM**.

1. Testez la règle de trafic entrant en vérifiant que vous pouvez vous connecter à la machine virtuelle à l’aide du RDP.
    1. Sélectionnez **Connecter** dans le volet de navigation à gauche.
    1. Vérifiez que l’adresse IP est paramétrée sur Adresse IP publique, conservez le numéro de port par défaut et sélectionnez **Télécharger le fichier DRP**.
    1. **Ouvrez** le fichier téléchargé et sélectionnez **Connecter**.
    1. Vous êtes invité à entrer vos informations d’identification. Entrez le nom d’utilisateur et le mot de passe que vous avez utilisés quand vous avez créé la machine virtuelle.  Si la fenêtre qui vous demande vos informations d’identification vous demande un code confidentiel, sélectionnez **Plus de choix**, puis **Utiliser un autre compte**.
    1. Une fenêtre de connexion de bureau à distance s’ouvre et indique que l’identité de l’ordinateur distant ne peut pas être vérifiée. Voulez-vous quand même vous connecter ? Sélectionnez **Oui**.
    1. Vous êtes maintenant connecté à la machine virtuelle. Mentionnez à l’apprenant que dans ce cas-ci, vous avez pu vous connecter à la machine virtuelle, car la règle de trafic entrant que vous avez créée autorise le trafic entrant pour la machine virtuelle via RDP.

1. Étant donné que vous êtes déjà dans la machine virtuelle, vous pouvez afficher la connectivité Internet sortante vers Internet, qui est activée par l’une des règles de trafic sortant par défaut.
    1. Dans la machine virtuelle, sélectionnez **Microsoft Edge** pour ouvrir le navigateur.  Étant donné que c’est la première fois que vous ouvrez Microsoft Edge, il est possible qu’une fenêtre contextuelle s’affiche. Sélectionnez **Démarrer sans vos données**, sélectionnez **Continuer sans ces données**, puis sélectionnez **Confirmer et commencer la navigation**.
    1. Entrez **www.bing.com** dans la barre d’adresse du navigateur et vérifiez que vous pouvez vous connecter au moteur de recherche.
    1. Une fois que vous avez vérifié votre accès à www.bing.com, fermez la fenêtre du navigateur dans la machine virtuelle, mais laissez la machine virtuelle allumée.

1. Réduisez la machine virtuelle en sélectionnant le trait de soulignement **_** dans l’onglet bleu qui affiche l’adresse IP de la machine virtuelle. Vous revenez dans la page SC900-WinVM | Connexion.  

### <a name="optional-demo-part-4"></a>FACULTATIVE Partie 4 de la démonstration

Si vous avez le temps, vous pouvez créer une règle de groupe de sécurité réseau sortante pour bloquer le trafic Internet sortant à partir de la machine virtuelle.

1. Dans le volet de navigation de gauche, sélectionnez **Réseau**. Vous êtes normalement dans la page SC900-WinVM | Réseau.

1. Sélectionnez l’onglet **Règles de port de trafic sortant**. Les règles de trafic sortant par défaut s’affichent.  Notez la règle par défaut « AllowInternetOutBound ». Cette règle autorise l’ensemble du trafic Internet sortant. Vous ne pouvez pas supprimer la règle par défaut, mais vous pouvez la remplacer par une règle de priorité plus élevée. À droite de la page, sélectionnez **Ajouter une règle de port de trafic sortant**.

1. Sur la page Ajouter une règle de sécurité de trafic sortant, spécifiez les paramètres suivants :
    1. Source :  **Any**
    1. Plages de ports source : **\***
    1. Destination :  **Balise du service**
    1. Balise d’identification de destination :  **Internet**
    1. Service :  **Personnaliser** (conservez la valeur par défaut)
    1. Plages de ports de destination : * (veillez à placer un astérisque dans le champ Plages de ports de destination)
    1. Protocole : **Any**
    1. Action : **Deny**
    1. Priorité : **1000**
    1. Nom : conservez le nom par défaut ou ajoutez votre propre nom descriptif.
    1. Sélectionnez **Ajouter**

1. Une fois que la règle est créée, elle apparaîtra dans la liste des règles de trafic sortant.  Elle apparaît dans la liste, mais son application prendra quelques minutes (attendez quelques minutes avant de passer aux étapes suivantes).  

1. Revenez dans votre machine virtuelle (l’icône de la machine virtuelle doit s’afficher dans la barre des tâches en bas de la page).

1. Ouvrez le navigateur Microsoft Edge dans votre machine virtuelle et entrez **www.bing.com**. La page ne doit pas s’afficher.  Remarque : Si vous pouvez vous connecter à Internet et que vous avez vérifié que tous les paramètres de la règle de trafic sortant ont été correctement définis, c’est probablement dû au fait qu’il faut quelques minutes pour que la règle prenne effet.  Fermez le navigateur, patientez quelques minutes, puis réessayez.  Remarque : Les abonnements Azure dans l’environnement lab peuvent connaître des délais plus longs que d’habitude.

1. Fermez la connexion au bureau à distance en sélectionnant le **X** en haut au centre de la page où l’adresse IP est affichée.  Une fenêtre contextuelle s’affiche, indiquant « Votre session à distance sera déconnectée ». Sélectionnez **OK**.

1. Fermez tous les onglets ouverts du navigateur.

1. Une bonne pratique est généralement d’arrêter ou de désactiver la machine virtuelle pour éviter d’encourir des coûts, si elle est utilisée uniquement à des fins de démonstration ou de test. Dans ce cas, toutefois, ne désactivez PAS la machine virtuelle, car cela vous aidera à fournir les données de gestion de la posture de sécurité cloud lors de la démonstration de Microsoft Defender pour le cloud.  La machine virtuelle sera désactivée lorsque le labo sera annulé.

#### <a name="review"></a>Révision

Lors de cette démonstration, vous avez présenté les informations et les paramètres permettant d’associer un groupe de sécurité réseau, y compris le processus pour associer une interface au groupe de sécurité réseau. Ensuite, vous avez présenté les règles de trafic entrant et sortant par défaut. Enfin, vous avez expliqué les étapes de la création d’une nouvelle règle.
