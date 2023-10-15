<!---
---
Démonstration : Titre : « Groupes de sécurité réseau Azure » Parcours d’apprentissage/Module/Unité : « Parcours d’apprentissage : Décrire les fonctionnalités des solutions de sécurité Microsoft ; Module 1 : Décrire les fonctionnalités de sécurité de base dans Azure ; Unité 6 : Décrire les groupes de sécurité réseau Azure »
---
--->

# Démonstration : Groupes de sécurité réseau Azure

Cette démonstration correspond au contenu Learn suivant :

- Parcours d’apprentissage : Décrire les fonctionnalités des solutions de sécurité Microsoft
- Module : Décrire les principales fonctionnalités de sécurité dans Azure
- Unité : Décrire les groupes de sécurité réseau Azure

## Scénario de la démonstration

Dans cette démonstration, vous allez explorer la fonction des groupes de sécurité réseau dans Azure et appliquer un groupe de sécurité réseau à une machine virtuelle préalablement créée. Vous commencerez par présenter brièvement les informations relatives à la machine virtuelle qui a été précréée par l’hébergeur ALH (Authorized Lab Hoster). Ensuite, à l’aide d’un groupe de sécurité réseau qui a été configuré dans le cadre de la configuration pré-démonstration, vous allez montrer les paramètres essentiels d’un groupe de sécurité réseau et les règles de trafic entrant et sortant par défaut. Vous allez affecter une interface de machine virtuelle au groupe de sécurité réseau, créer une règle RDP pour autoriser la connexion à la machine virtuelle et enfin la tester.

### Partie 1 de la démonstration

Dans cette partie, vous allez afficher certains des paramètres associés à la machine virtuelle qui a été créée dans le cadre de la démonstration de configuration (DEMO_00_pre_demo_setup.md).

1. Ouvrez Microsoft Edge.  Dans la barre d’adresse, entrez **https://portal.azure.com** et connectez-vous avec les informations d’identification Azure fournies par l’hébergeur de labo agréé.  Cela vous amène à la page d’accueil des services Azure.

1. Dans la zone de recherche bleue en haut de la page, entrez **Machines virtuelles** et sélectionnez **Machines virtuelles** dans les résultats de la recherche.

1. Dans la page Machines virtuelles, sélectionnez la machine virtuelle appelée **SC900-WinVM**.  Cette machine virtuelle doit avoir été créée dans le cadre de la configuration pré-démonstration.  Si elle n’apparaît pas dans la liste, créez-la maintenant.

1. Vous êtes à présent dans la page SC900-WinVM.  Notez certaines des informations de base sur la machine virtuelle.

1. Dans le volet de navigation de gauche, sélectionnez **Réseau**.  
    1. La vue par défaut affiche les règles de port d’entrée.  Notez que l’interface réseau de cette machine virtuelle n’a aucun groupe de sécurité réseau configuré.  C’est la même chose si vous sélectionnez la vue des règles de port de sortie.
    1. Sélectionnez **Règles de sécurité effectives** en regard de l’intitulé Interface réseau.  Notez ce message : « Aucun groupe de sécurité réseau ou groupe de sécurité d'application n'est associé à l'interface réseau ».

1. Note pour le présentateur : Si vous essayez de vérifier l’état du port dans la page de connexion, vous recevez le message « Vérification impossible ».  Cela ne signifie pas nécessairement que les ports ne sont pas exposés.  Comme vous le remarquerez, lorsque vous effectuerez la même action avec le groupe de sécurité réseau affecté, vous obtiendrez « Non accessible » indiquant que le trafic sur ce port est bloqué.


1. Laissez cet onglet de navigateur ouvert.

### Partie 2 de la démonstration

Dans cette partie, vous allez affecter une interface au groupe de sécurité réseau et vous allez parler des règles de trafic entrant et sortant par défaut en montrant comment celles-ci fonctionnent.  Dans le cadre de la configuration pré-démonstration, une machine virtuelle doit affecter l’interface réseau de la machine virtuelle à ce groupe de sécurité réseau et créer une règle de trafic entrant pour le trafic RDP.

1. Ouvrez un nouvel onglet de navigateur pour vous connecter au portail Azure (portal.azure.com) et dans la barre de recherche bleue en haut de la page, entrez **Groupes de sécurité réseau**. Dans les résultats, sélectionnez **Groupes de sécurité réseau** (ne sélectionnez pas Groupes de sécurité réseau classiques).

1. Sélectionnez le groupe de sécurité réseau créé dans le cadre de la configuration pré-démonstration. Si vous ne l’aviez pas créé, faites-le maintenant. Sélectionnez **Créer un groupe de sécurité réseau** et spécifiez les paramètres suivants :
    1. Abonnement : conservez la valeur par défaut (il s’agit de l’abonnement Azure fourni par l’hébergeur de labo autorisé)
    1. Groupe de ressources : **LabsSC900** (le même groupe de ressources que celui utilisé par la machine virtuelle).
    1. Nom :  **NSG-SC900**
    1. Région : laissez la valeur par défaut.
    1. Sélectionnez **Examiner et créer** puis sélectionnez **Créer**.
    1. Une fois que le déploiement est terminé (l’opération est très rapide), sélectionnez **Accéder à la ressource**.

1. En haut de la page, sous la mention Informations de base, vous voyez des informations générales sur le groupe de sécurité réseau que vous avez créé.  Deux points sont à noter : il n’y a pas de règles de sécurité PERSONNALISÉES et il n’y a pas de sous-réseaux ni d’interfaces réseau associés à ce groupe de sécurité réseau.  Il n’y a aucune règle de sécurité personnalisée, mais il y a des règles de trafic entrant et sortant par défaut qui sont incluses avec chaque groupe de sécurité réseau, comme indiqué sur la page.  Passez en revue les règles entrantes et sortantes. Les règles de trafic entrant par défaut refusent tout le trafic entrant qui ne provient pas d’un réseau virtuel ou d’un équilibreur de charge Azure.  Les règles de trafic sortant refusent tout le trafic sortant, à l’exception du trafic entre les réseaux virtuels et du trafic sortant vers Internet.

1. Dans le volet de navigation gauche de la page NSG-SC900, sous Paramètres, sélectionnez **Interfaces réseau**.
    1. Sélectionnez **Associer**.
    1. Dans le champ de sélection des associations d’interface réseau, sélectionnez la **flèche vers le bas**, sélectionnez **sc900-winvmXXX**, puis sélectionnez **OK** en bas de la fenêtre. Une fois l’interface associée au groupe de sécurité réseau, elle s’affiche dans la liste.

1. Revenez sur la machine virtuelle en sélectionnant l’onglet du navigateur de la machine virtuelle.  Vous devriez voir qu’un groupe de sécurité réseau est désormais attaché à l’interface de la machine virtuelle.  La table des règles de port de trafic entrant s’affiche. Les règles de trafic entrant par défaut refusent tout le trafic entrant qui ne provient pas d’un réseau virtuel ou d’un équilibreur de charge Azure.  Pour tester cela, vous allez vérifier l’état sur le port RDP 3389.
    1. En haut de la page, sélectionnez **Se connecter**, puis **Vérifier l’accès** pour le port 3389 (RDP). Vous verrez « Non accessible ».  
    1. Bien que vous ne testiez que le port RDP 3389, tout trafic réseau entrant qui ne provient pas d’un autre réseau virtuel ou d’un autre équilibreur de charge est bloqué.  

1. Vous allez maintenant créer une règle pour autoriser le trafic entrant sur le port RDP.  Dans le volet de navigation de gauche, sélectionnez **Réseaux**. La table des règles de port de trafic entrant devrait s’afficher (l’onglet des règles de port de trafic entrant est souligné).  À droite de la page, sélectionnez **Ajouter une règle de port d’entrée**. Un point important à souligner est que vous ne pouvez pas supprimer les règles par défaut. Toutefois, vous pouvez les remplacer en créant des règles dont la priorité est plus élevée. Sur la fenêtre Ajouter une règle de sécurité de trafic entrant, spécifiez les paramètres suivants :
    1. Source :  **Any**
    1. Plages de ports sources : **\***
    1. Destination :  **Any**
    1. Service :  **RDP**
    1. Action :  **Autoriser**
    1. Priorité : **1000** ; Remarque : les règles avec les nombres les plus petits ont une priorité plus élevée et sont traitées en premier.
    1. Nom : conservez le nom par défaut ou ajoutez votre propre nom descriptif.
    1. Notez la présence du signe d’avertissement en bas de la fenêtre.  Nous utilisons RDP uniquement à des fins de test et pour illustrer les fonctionnalités du groupe de sécurité réseau.
    1. Sélectionnez **Ajouter**

1. Une fois la règle provisionnée, elle s’affiche dans la liste des règles de trafic entrant (vous devez peut-être actualiser l’écran).

### Partie 3 de la démonstration

Avec le groupe de sécurité réseau associé à votre machine virtuelle et la règle RDP créée, vous allez montrer l’impact du groupe de sécurité réseau en testant la connexion RDP à la machine virtuelle.

1. Ouvrez l’onglet SC900-WinVM - Microsoft Azure dans votre navigateur. 

1. Sélectionnez **Connecter** dans le volet de navigation à gauche.
    1. Vous pouvez simplement sélectionner **Vérifier l’accès**.  L’état devrait indiquer « Accessible ». Si vous avez le temps, vous pouvez également vous connecter à la machine virtuelle en ouvrant une instance Connexion Bureau à distance sur Windows.  Cette option ouvre la machine virtuelle si la connexion à celle-ci réussit.  Voici les étapes ci-dessous :
        1. Dans votre barre de recherche Windows, entrez **Connexion Bureau à distance** et sélectionnez **Ouvrir**.
        1. Dans le champ à côté de l’endroit où il est indiqué **Ordinateur**, entrez l’adresse IP publique de votre machine virtuelle.
        1. Une fois que vous avez entré l’adresse IP, le nom d’utilisateur doit apparaître sous le champ où vous avez entré l’adresse IP. Si ce n’est pas le cas, développez **Afficher les options**, entrez le nom d’utilisateur pour votre machine virtuelle, puis sélectionnez **Se connecter**.
        1. Une fenêtre de connexion de bureau à distance s’ouvre et indique que l’identité de l’ordinateur distant ne peut pas être vérifiée. Voulez-vous quand même vous connecter ? Sélectionnez **Oui**.
        1. Vous êtes maintenant connecté à la machine virtuelle. Mentionnez à l’apprenant que dans ce cas-ci, vous avez pu vous connecter à la machine virtuelle, car la règle de trafic entrant que vous avez créée autorise le trafic entrant pour la machine virtuelle via RDP.
        1. Réduisez la machine virtuelle en sélectionnant le trait de soulignement **_** dans l’onglet bleu qui affiche l’adresse IP de la machine virtuelle. Vous revenez dans la page SC900-WinVM | Connexion.

1. Dans le volet de navigation de gauche, sélectionnez **Réseaux**, puis, dans la fenêtre principale, sélectionnez **Règles de port de trafic sortant**.  Parlez des règles de trafic sortant par défaut. Les règles par défaut autorisent le trafic de réseau virtuel sortant de n’importe quel réseau virtuel vers n’importe quel autre réseau virtuel et autorisent le trafic Internet sortant. Tout autre type de trafic sortant est refusé.  Vous ne pouvez pas supprimer la règle par défaut, mais vous pouvez la remplacer en créant une règle avec une priorité plus élevée de la même façon que vous avez créé une règle de trafic entrant.

1. Si le temps le permet et que vous souhaitez montrer des étapes similaires pour le trafic sortant, suivez la partie facultative de la démonstration listée ci-dessous.  Sinon, quittez la machine virtuelle, mais laissez l’onglet Azure ouvert dans votre navigateur pour la prochaine démonstration.

### FACULTATIVE Partie 4 de la démonstration

Dans cette partie, vous allez montrer les règles de trafic sortant actuelles du groupe de sécurité réseau qui autorisent le trafic Internet sortant de la machine virtuelle.  Ensuite, vous allez créer une règle pour bloquer le trafic Internet sortant de la machine virtuelle. Enfin, vous montrerez l’impact de la règle nouvellement créée en essayant d’accéder à Internet à partir de la machine virtuelle.

1. Ouvrez la machine virtuelle que vous avez réduite à l’étape précédente. Ici, vous allez montrer la connectivité Internet sortante vers Internet, qui est activée par l’une des règles de trafic sortant par défaut. Une fois que la machine virtuelle est ouverte et que vous vous êtes connecté en tant qu’utilisateur, sélectionnez **Microsoft Edge** pour ouvrir le navigateur.  Étant donné que c’est la première fois que vous ouvrez Microsoft Edge, il est possible qu’une fenêtre contextuelle s’affiche. Sélectionnez **Démarrer sans vos données**, sélectionnez **Continuer sans ces données**, puis sélectionnez **Confirmer et commencer la navigation**.
    1. Entrez **www.bing.com** dans la barre d’adresse du navigateur et vérifiez que vous pouvez vous connecter au moteur de recherche.
    1. Une fois que vous avez vérifié votre accès à www.bing.com, fermez la fenêtre du navigateur dans la machine virtuelle, mais laissez la machine virtuelle allumée.

1. Réduisez la machine virtuelle en sélectionnant le trait de soulignement **_** dans l’onglet bleu qui affiche l’adresse IP de la machine virtuelle. Vous revenez dans la page SC900-WinVM | Connexion.  

1. Dans le volet de navigation de gauche, sélectionnez **Réseau**.

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

1. Laissez l’onglet Azure ouvert dans votre navigateur pour la prochaine démonstration Azure.

### Révision

Lors de cette démonstration, vous avez présenté les informations et les paramètres permettant d’associer un groupe de sécurité réseau, y compris le processus pour associer une interface au groupe de sécurité réseau. Ensuite, vous avez présenté les règles de trafic entrant et sortant par défaut. Enfin, vous avez expliqué les étapes de la création d’une nouvelle règle.
