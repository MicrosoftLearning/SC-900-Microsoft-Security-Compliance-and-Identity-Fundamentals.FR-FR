---
Demo:
  title: Groupes de sécurité réseau Azure
  module: 'Module 3 Lesson 1: Describe the capabilities of Microsoft security solutions: Describe basic security capabilities in Azure.'
ms.openlocfilehash: dc653f2a9e6ee450b5693ad7bfbfe2208d5a7ea3
ms.sourcegitcommit: 25998048c2e354ea23d6f497205e8a062d34ac80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2022
ms.locfileid: "144557527"
---
# <a name="demo-azure-network-security-groups-nsgs"></a>Démonstration : Groupes de sécurité réseau Azure

## <a name="demo-scenario"></a>Scénario de la démonstration

Dans cette démonstration, vous présenterez les fonctionnalités d’un groupe de sécurité réseau dans Azure.  Afin de préparer la démonstration, vous créerez une machine virtuelle sans groupe de sécurité réseau. Vous créerez également un groupe de sécurité réseau sans interface ou sous-réseau associé.  Lors de cette démonstration, vous présenterez les règles de trafic entrant et sortant pour le groupe de sécurité réseau. Vous expliquerez ensuite comment attribuer l’interface virtuelle au groupe de sécurité réseau.  Après la configuration, vous testerez la connexion à la machine virtuelle à l’aide des règles de groupe de sécurité réseau par défaut, ainsi que les règles que vous créerez.
  
### <a name="pre-demo-setup-part-1"></a>Configuration à faire avant la démonstration, partie 1

 Il vous est recommandé en tant qu’instructeur d’effectuer ces actions **AVANT** l’heure de classe, car la création d’une machine virtuelle peut prendre plusieurs minutes. Lors de cette configuration, vous créez une machine virtuelle Windows 10.

1. Ouvrez l’onglet **Accueil - Microsoft Azure** dans votre navigateur.  Si vous avez fermé l’onglet, ouvrez une page du navigateur et saisissez portal.azure.com dans la barre d’adresse. Ensuite, reconnectez-vous.

1. Dans la barre de recherche, dans la barre bleue en haut de la page à côté de là où il est indiqué Microsoft Azure, saisissez **Machines virtuelles**, puis sélectionnez **Machines virtuelles** à partir des résultats de la recherche.  

1. En haut à gauche de la page, sélectionnez **+Ajouter**, puis **+Machines virtuelles**.

1. Sous l’onglet Informations de base, remplissez les informations suivantes (laissez les paramètres par défaut pour les éléments non répertoriés) :
    1. **Abonnement** : vérifiez que le paramètre par défaut est bien Pass Azure - Parrainage.
    1. **Groupe de ressources** : sélectionnez **Créer une nouvelle**, puis saisissez **LabsSC900-RG** dans le champ Nom et sélectionnez **OK**.
    1. **Nom des machines virtuelles** : entrez **SC900-WinVM**.
    1. **Région** : laissez la valeur par défaut.
    1. **Options de disponibilité** : vérifiez de bien sélectionner **Aucune redondance d’infrastructure requise**.  REMARQUE : il est très important que les options de disponibilité soient paramétrées sur Aucune redondance d’infrastructure requise. Dans le cas contraire, la démonstration ne fonctionnera pas comme prévu.  Disposer d’une option de disponibilité nécessite un groupe de sécurité réseau et nous créons volontairement une machine virtuelle sans groupe de sécurité réseau.
    1. **Image** : dans la liste déroulante, sélectionnez **Windows 10 Professionnel, Version 20H2 – Gen 1**.
    1. **Taille** : sélectionnez **Afficher toutes les tailles** dans le menu déroulant et sélectionnez **B2s**, puis cliquez sur **Sélectionner** dans le bas de la page.
    1. **Nom d’utilisateur** :  Entrez un nom d’utilisateur de votre choix.  Prenez-en note, car vous en aurez besoin pour accéder à la machine virtuelle.
    1. **Mot de passe** :  Entrez un mot de passe de votre choix.  Prenez-en note, car vous en aurez besoin pour accéder à la machine virtuelle.
    1. **Ports de trafic entrant publics** : vous pouvez laisser le paramètre par défaut (ce que vous sélectionnez ici n’a pas d’importance, car les paramètres du réseau vont remplacer ce que vous faites ici).
    1. **Licences** : sélectionnez **Je confirme disposer d’une licence Windows 10 éligible avec des droits d’hébergement multilocataire** pour faire apparaître une coche dans la case.
    1. Sélectionnez **Suivant : Disques**.

1. Vous êtes à présent au niveau de l’onglet Disques pour la configuration de la machine virtuelle.  Conservez tous les paramètres par défaut et sélectionnez **Suivant : Mise en réseau >** .

1. Vous êtes à présent au niveau de l’onglet Mise en réseau pour la configuration de la machine virtuelle.  Remplissez les informations suivantes (pour tous les éléments non répertoriés, laissez les paramètres par défaut) :
    1. Groupe de sécurité réseau de la carte réseau : sélectionnez **Aucun**.  Remarque : en sélectionnant Aucun, vous vous assurez que la carte réseau n’a pas de groupe de sécurité réseau.  Lors d’une tâche ultérieure de la démonstration, vous créerez un groupe de sécurité réseau et attribuerez la carte réseau de la machine virtuelle au groupe de sécurité réseau que vous avez créé.
    1. Puisque les autres paramètres de la machine virtuelle seront conservés par défaut, continuez et sélectionnez Suivant : **Vérifier + créer>** .

1. Vérifiez la configuration de votre machine virtuelle.  Quelques points à noter : Cette machine virtuelle dispose d’une adresse IP publique et d’aucun groupe de sécurité réseau de la carte réseau.  En ce qui concerne la sécurité, la machine virtuelle est exposée.  Nous verrons cela dans une tâche ultérieure. Sélectionnez **Create** (Créer).  Le déploiement de la machine virtuelle peut prendre plusieurs minutes.

1. Notez le nom de l’interface du réseau, **sc900-winvmXXX** (les XXX seront spécifiques à l’interface du réseau de votre machine virtuelle).

1. Une fois le déploiement de la machine virtuelle effectué, sélectionnez **Accéder à la ressource**.  Vous êtes à présent sur la page SC900-WinVM.  Notez l’adresse IP publique.

1. Dans le volet de navigation à gauche, sélectionnez **Mise en réseau** et notez l’interface du réseau, **sc900-winvmXXX** (les XXX seront spécifiques à l’interface du réseau de votre machine virtuelle).  Il ne doit pas y avoir de règle de trafic entrant ou sortant associée à l’interface.  

1. En haut de la page, sélectionnez **Connecter**, car il est important de vérifier que vous pouvez vous connecter à la machine virtuelle.
    1. En haut de la page, vérifiez que **RDP** est sélectionné (souligné).
    1. Vérifiez que l’adresse IP est paramétrée sur Adresse IP publique, conservez le numéro de port par défaut et sélectionnez **Télécharger le fichier DRP**.
    1. **Ouvrez** le fichier téléchargé et sélectionnez **Connecter** dans la fenêtre qui apparaît.
    1. Une fenêtre s’ouvre et vous demande vos informations d’identification. Si la fenêtre par défaut vous demande un code confidentiel, sélectionnez **Plus de choix**, puis **Utiliser un autre compte**.   Vous serez invité à saisir vos informations d’identification.  Entrez le nom d’utilisateur et le mot de passe que vous avez utilisés quand vous avez créé la machine virtuelle.
    1. Une fenêtre de connexion de bureau à distance s’ouvre et indique que l’identité de l’ordinateur distant ne peut pas être vérifiée.  Voulez-vous quand même vous connecter ?  Sélectionnez **Oui**.
    1. Vous êtes maintenant connecté à la machine virtuelle que vous venez de créer. Terminez la configuration de Windows. Bien que vous vous soyez connecté à la machine virtuelle via RDP et un port RDP couramment utilisé, cette machine virtuelle a tous les ports ouverts et rien ne filtre le trafic.  Fermez la connexion au bureau à distance en sélectionnant le **X** en haut au centre de la page où l’adresse IP est affichée.  Une fenêtre contextuelle indique que Votre session à distance sera déconnectée. Sélectionnez **OK**.

1. Vous êtes de retour sur la page SC900-WinVM dans le portail Azure.  Laissez cet onglet de navigateur ouvert pour la tâche suivante.

### <a name="pre-demo-setup-part-2"></a>Configuration à faire avant la démonstration, partie 2

Créez un groupe de sécurité réseau, mais n’assignez PAS l’interface du réseau de la machine virtuelle à ce groupe de sécurité réseau.  

1. Ouvrez l’onglet SC900-WinVM - Microsoft Azure dans votre navigateur.

1. Dans la barre de recherche, dans la barre bleue en haut de la page à côté de là où il est indiqué Microsoft Azure, saisissez **groupe de sécurité réseau**, puis sélectionnez **Groupes de sécurité réseau** à partir des résultats de la recherche.  Ne sélectionnez pas Groupes de sécurité réseau classique.

1. En haut de la page Groupes de sécurité réseau, sélectionnez **+ Créer**.

1. Sous l’onglet de base de la page Créer un groupe de sécurité réseau, spécifiez les paramètres suivants :
    1. Abonnement :  Pass Azure - Parrainage
    1. Groupe de ressources :  **LabsSC900-RG**
    1. Nom :  **NSG-SC900**
    1. Région : conservez la valeur par défaut **(USA) USA Est**
    1. Sélectionnez **Examiner et créer** puis sélectionnez **Créer**.

1. Une fois le déploiement terminé, sélectionnez **Accéder à la ressource** et assurez-vous que tout est correct.  Par défaut, il doit y avoir 3 règles de trafic entrant, 3 règles de trafic sortant et aucun sous-réseau et interface associé au groupe de sécurité réseau.  Retournez à la page **d’accueil** du portail Azure.  

### <a name="demo"></a>Démonstration

Montrez les paramètres pour un groupe de sécurité réseau.  Dans ce cas-ci, vous montrerez les fonctionnalités pour un groupe de sécurité réseau existant (celui que vous avez créé dans la configuration ci-dessus), qui n’a pas encore été attribué à une interface de machine virtuelle. Vous présenterez le processus pour associer une interface au groupe de sécurité réseau et le processus pour créer des règles de trafic entrant et sortant.

1. Ouvrez l’onglet du navigateur intitulé **Accueil-Microsoft Azure**.  Si vous avez fermé l’onglet, ouvrez une page du navigateur et saisissez portal.azure.com dans la barre d’adresse. Ensuite, reconnectez-vous.

1. Dans la barre de recherche, dans la barre bleue en haut de la page à côté de là où il est indiqué Microsoft Azure, saisissez **groupe de sécurité réseau**, puis sélectionnez **Groupes de sécurité réseau** à partir des résultats de la recherche.  Ne sélectionnez pas Groupes de sécurité réseau classique.

1. À partir de la page des groupes de sécurité réseau, sélectionnez le groupe de sécurité réseau que vous avez créé lors de la configuration, **NSG-SC900**.

1. L’onglet **Vue d’ensemble** du volet de navigation à gauche est mis en surbrillance.  Notez les règles de trafic entrant et sortant par défaut dans le groupe de sécurité réseau. Bien que le groupe de sécurité réseau ait été créé et qu’il dispose des règles par défaut pour filtrer le trafic, aucune interface ne lui a été associée. Vous pouvez voir cela en haut à droite de cette page où il est indiqué « Associé à : 0 sous-réseau, 0 interface réseau ».  Pour qu’un groupe de sécurité réseau fonctionne, il doit être attribué à quelque chose.  Ici, nous allons l’attribuer à l’interface du réseau de la machine virtuelle que nous avons créé plus tôt.

1. Dans le volet de navigation de gauche de la page NSG-SC900, sous Paramètres, sélectionnez **Interfaces réseau**.

1. Sélectionnez **+ Associer** au-dessus de la barre de recherche. Puis, à partir du menu déroulant, sélectionnez **sc900-winvmXXX** (les XXX seront spécifiques à l’interface réseau de votre machine virtuelle), puis sélectionnez **OK**. Pendant l’association de l’interface, une notification s’affiche en haut à droite de l’écran. Une fois l’interface associée au groupe de sécurité réseau, elle s’affiche dans la liste.

1. Revenez à l’onglet **Vue d’ensemble**.  Remarquez qu’en haut à droite de la page vous verrez « Associé à : 0 sous-réseau, 1 interface réseau ». L’interface est maintenant attribuée au groupe de sécurité réseau. Mettez également en évidence les règles par défaut pour les apprenants. Pour le trafic entrant, seul le trafic qui provient des réseaux virtuels Azure et d’Azure Load Balancer seront autorisés. Tout autre trafic entrant dans la machine virtuelle sera refusé. Soulignez également les règles de trafic sortant par défaut.  Seuls le trafic sortant vers d’autres réseaux virtuels et le trafic Internet sortant sont autorisés.  Dans le cadre de la démonstration, il est recommandé de prendre une minute pour montrer que le trafic entrant est refusé.
    1. Dans la barre de recherche, en haut de la page, saisissez **Virtual Machines**, puis sélectionnez-le.
    1. Sur la page Machines virtuelles, sélectionnez **SC900-WinVM**.
    1. En haut de la page SC900-WinVM, sélectionnez **Connecter**, puis **RDP**.
    1. Vérifiez que l’adresse IP est paramétrée sur Adresse IP publique, conservez le numéro de port par défaut et sélectionnez **Télécharger le fichier DRP**.
    1. **Ouvrez** le fichier téléchargé et sélectionnez **Connecter**.
    1. Après une tentative de connexion de quelques secondes, vous verrez le message d’échec qui indique que le bureau à distance ne peut pas se connecter à l’ordinateur distant. Sélectionnez **OK**.

1. Maintenant que vous avez montré l’effet des règles de trafic entrant par défaut du groupe de sécurité réseau, vous souhaitez créer une nouvelle règle pour autoriser le trafic RDP entrant.  Expliquez que vous ne pouvez pas supprimer les règles par défaut existantes, vous ne pouvez qu’en créer de nouvelles avec une plus haute priorité.
    1. Dans le volet de navigation à gauche, sous Paramètres, sélectionnez **Mise en réseau**.  Vous êtes sur la page de mise en réseau de la machine virtuelle. Bien que vous puissiez créer ici une règle de trafic entrant et une règle de trafic sortant, revenez à la page des groupes de sécurité réseau. Après tout, la démonstration concerne le groupe de sécurité réseau.  Sélectionnez **NSG-SC900**. Il s’agit du lien au milieu de la fenêtre.

1. Vous êtes à présent sur la page de vue d’ensemble du groupe de sécurité réseau.  Remarquez les informations à propos du groupe de sécurité réseau. Sur la page des groupes de sécurité réseau, à partir du volet de navigation à gauche, sous paramètres, sélectionnez **Règles de sécurité de trafic** entrant, puis **+ Ajouter** en haut de la page. Sur la page Ajouter une règle de sécurité de trafic, parlez des différents paramètres. Il est recommandé de créer une règle pour autoriser le trafic RDP entrant, avec les paramètres suivants :
    1. Source : **Any**
    1. Plages de ports sources : **\***
    1. Destination : **Any**
    1. Service : **RDP**
    1. Action : **Autoriser**
    1. Priorité : **300** ; Remarque : Les règles avec les nombres les plus petits ont une priorité plus élevée et sont traitées en premier. La priorité pour cette nouvelle règle doit donc être plus élevée que la priorité pour la règle existante qui refuse tout trafic entrant.
    1. Nom : **AllowRDP**
    1. Sélectionnez **Ajouter**
    1. Une fois que la règle est créée, elle apparaîtra dans la liste des règles de trafic entrant.

1. Penchez-vous à présent sur les **Règles de sécurité de trafic sortant**.  Sélectionnez **+ Ajouter** en haut de la page et parlez des différents paramètres.  Je recommande de créer la règle. Les paramètres ci-dessous créent une règle pour refuser le trafic Internet sortant :
    1. Source : **Any**
    1. Plages de ports sources : **\***
    1. Destination : **Balise du service**
    1. Balise d’identification de destination : **Internet**
    1. Service : **Personnaliser** (conservez la valeur par défaut)
    1. Plages de ports de destination : **\*** (veillez à placer un astérisque dans le champ Plages de ports de destination).
    1. Protocole : **Any**
    1. Action : **Deny**
    1. Priorité : **4 000** (ce qu’il faut souligner ici, c’est que la priorité doit être plus élevée que la priorité pour la règle existante qui autorise le trafic Internet sortant).
    1. Nom : **DenyInternet**
    1. Sélectionnez **Ajouter**
    1. Une fois que la règle est créée, elle apparaîtra dans la liste des règles de trafic sortant.

1. Revenez maintenant à votre machine virtuelle et testez les règles.  En haut de la page, sélectionnez **SC900-VM**, au-dessus des règles de sécurité de trafic sortant.

1. Testez la règle de trafic entrant en vérifiant que vous pouvez vous connecter à la machine virtuelle à l’aide du RDP.
    1. Sélectionnez **Connecter** dans le volet de navigation à gauche.
    1. Vérifiez que l’adresse IP est paramétrée sur Adresse IP publique, conservez le numéro de port par défaut et sélectionnez **Télécharger le fichier DRP**.
    1. **Ouvrez** le fichier téléchargé et sélectionnez **Connecter**.
    1. Vous serez invité à saisir vos informations d’identification. Entrez le nom d’utilisateur et le mot de passe que vous avez utilisés quand vous avez créé la machine virtuelle.  Si la fenêtre qui vous demande vos informations d’identification vous demande un code confidentiel, sélectionnez **Plus de choix**, puis **Utiliser un autre compte**.
    1. Une fenêtre de connexion de bureau à distance s’ouvre et indique que l’identité de l’ordinateur distant ne peut pas être vérifiée. Voulez-vous quand même vous connecter ? Sélectionnez **Oui**.
    1. Vous êtes maintenant connecté à la machine virtuelle. Mentionnez à l’apprenant que dans ce cas-ci, vous avez pu vous connecter à la machine virtuelle, car la règle de trafic entrant que vous avez créée autorise le trafic entrant pour la machine virtuelle via RDP.

1. Testez maintenant la règle de groupe de sécurité réseau du trafic sortant.
    1. Ouvrez le navigateur Edge dans la machine virtuelle.
    1. Entrez **www.bing.com**. La page ne doit pas s’afficher. Remarque : si vous pouvez vous connecter à Internet et que vous avez vérifié que tous les paramètres de la règle de trafic sortant ont été correctement définis, c’est probablement car il faut quelques minutes pour que la règle prenne effet. Patientez quelques minutes, puis réessayez.

1. Fermez la connexion au bureau à distance en sélectionnant le **X** en haut au centre de la page où l’adresse IP est affichée. Une fenêtre contextuelle indique que Votre session à distance sera déconnectée. Sélectionnez **OK**.

1. Revenez à la page d’accueil du portail Azure en sélectionnant **Microsoft Azure** sur la barre bleue en haut de la page.

### <a name="tear-down"></a>Destruction

**IMPORTANT** : Lors de cette tâche, vous supprimerez le groupe de ressources et l’ensemble des ressources qu’il contient.   C’est important afin d’éviter des charges supplémentaires.

1. Ouvrez l’onglet SC900-WinVM - Microsoft Azure dans votre navigateur.

1. En haut à gauche de la page, sélectionnez **Tous les services**.

1. Dans la zone Filtrer les services, en regard de la zone Tous les services, saisissez **Groupes de ressources** puis, dans la liste des résultats, sélectionnez **Groupes de ressources**.

1. Sélectionnez **LabsSC900-RG**.

1. En haut au centre de la page LabsSC900-RG, sélectionnez **Supprimer le groupe de ressources**.

1. Dans la fenêtre qui s’ouvre, saisissez le nom du groupe de ressources, **LabsSC900-RG**, afin de confirmer la suppression du groupe de ressources et de toutes ses ressources. Sélectionnez ensuite **Supprimer** en bas de la page.

1. La suppression de toutes les ressources et du groupe de ressources peut prendre quelques minutes.

#### <a name="review"></a>Révision

Lors de cette démonstration, vous avez présenté les informations et les paramètres permettant d’associer un groupe de sécurité réseau, y compris le processus pour associer une interface au groupe de sécurité réseau. Vous avez présenté les règles de trafic entrant et sortant par défaut. Enfin, vous avez présenté les étapes de la création d’une nouvelle règle.
