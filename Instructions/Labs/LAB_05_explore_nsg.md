---
ms.openlocfilehash: d2377516343cb85c279c1a2d6347c59f573d73c7
ms.sourcegitcommit: 15658ca1c7bae8a4dbaa33ab6f897070bde521b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/12/2022
ms.locfileid: "147892195"
---
<a name="---"></a><!---
---
Labo : Titre : « Découvrir les groupes de sécurité réseau Azure » Parcours d’apprentissage/Module/Unité : « Parcours d’apprentissage : Décrire les fonctionnalités des solutions de sécurité Microsoft ; Module 1 : Décrire les fonctionnalités de sécurité de base dans Azure ; Unité 6 : Décrire les groupes de sécurité réseau Azure »
---
--->

# <a name="lab-explore-azure-network-security-groups-nsgs"></a>Labo : Découvrir les groupes de sécurité réseau Azure

Ce labo correspond au contenu Learn suivant :

- Parcours d’apprentissage : Décrire les fonctionnalités des solutions de sécurité Microsoft
- Module : Décrire les principales fonctionnalités de sécurité dans Azure
- Unité : Décrire les groupes de sécurité réseau Azure

## <a name="lab-scenario"></a>Scénario du labo

Dans ce labo, vous allez découvrir la fonction des groupes de sécurité réseau dans Azure.  Pour ce faire, vous allez créer la machine virtuelle sans groupe de sécurité réseau. Vous suivrez ensuite le processus de création d’un groupe de sécurité réseau et d’affectation de l’interface de la machine virtuelle à ce groupe de sécurité réseau.  Une fois la configuration effectuée, vous allez examiner les règles de trafic entrant et sortant par défaut et créer des règles.
  
**Durée estimée** : 15-20 minutes

### <a name="task-1"></a>Tâche 1

Dans cette tâche, vous allez créer une machine virtuelle Windows 10.

1. Ouvrez Microsoft Edge.  Dans la barre d’adresse, saisissez **portal.azure.com**.

1. Connectez-vous avec vos informations d’identification d’administrateur.
    1. Dans la fenêtre de connexion, entrez **admin@WWLxZZZZZZ.onmicrosoft.com** (où ZZZZZZ représente votre ID de locataire unique fourni par votre fournisseur d’hébergement de labo), puis sélectionnez **Suivant**.

    1. Saisissez le mot de passe d’administrateur communiqué par votre fournisseur d’hébergement de labo. Sélectionnez **Connexion**.
    1. Lorsque vous êtes invité à rester connecté, sélectionnez **Oui**.
1. Dans le coin supérieur gauche de l’écran, en regard de la mention Microsoft Azure, sélectionnez l’icône de menu Afficher le portail (les trois lignes horizontales également appelées icône Hamburger), puis sélectionnez **Tous les services**.  
1. Dans la fenêtre principale, sous Recommandés, sélectionnez Machines virtuelles.  Si aucune machine virtuelle ne figure dans la liste, saisissez-la dans la barre de recherche, puis sélectionnez-la dans les résultats de la recherche.
1. Dans le coin supérieur gauche de la page, sélectionnez **+ Créer** puis **Machine virtuelle Azure**.
1. Sous l’onglet Informations de base, remplissez les informations suivantes (laissez les paramètres par défaut pour les éléments non répertoriés) :
    1. Abonnement : vérifiez que le paramètre par défaut est Pass Azure - Parrainage.

    1. Groupe de ressources : sélectionnez **Créer nouveau** puis, dans le champ Nom, entrez **LabsSC900**, puis sélectionnez **OK**.
    1. Nom des machines virtuelles : entrez **SC900-WinVM**.
    1. Région : si le champ Région n’est pas prérempli, sélectionnez la région la plus proche de votre emplacement.
    1. Image : dans la liste déroulante, sélectionnez **Windows 10 Professionnel, version 21H2 – Gen 2**.
    1. Taille : sélectionnez **Afficher toutes les tailles** dans la liste déroulante, sélectionnez **B2s**, puis cliquez sur **Sélectionner** dans le bas de la page.
    1. Nom d’utilisateur :  Entrez un nom d’utilisateur de votre choix.  Prenez-en note, car vous en aurez besoin pour accéder à la machine virtuelle.
    1. Mot de passe :  Entrez un mot de passe de votre choix.  Prenez-en note, car vous en aurez besoin pour accéder à la machine virtuelle.
    1. Ports de trafic entrant publics : laissez la valeur par défaut **Autoriser les ports sélectionnés**.
    1. Sélectionnez les ports de trafic entrant : laissez la valeur par défaut **RDP 3389**.
    1. Licences : sélectionnez **Je confirme disposer d’une licence Windows 10 éligible avec des droits d’hébergement multilocataire** pour faire apparaître une coche dans la case.
    1. Sélectionnez **Suivant : Disques**.
1. Vous êtes à présent au niveau de l’onglet Disques pour la configuration de la machine virtuelle.  Conservez tous les paramètres par défaut et sélectionnez **Suivant : Mise en réseau >** .
1. Vous êtes à présent au niveau de l’onglet Mise en réseau pour la configuration de la machine virtuelle.  Pour l’option du groupe de sécurité réseau de la carte réseau, sélectionnez **Aucun**. Laissez les valeurs par défaut pour tous les autres paramètres.  Remarque : sélectionner l’option Aucun à cette étape vous permet de traiter les étapes de création d’un groupe de sécurité réseau à partir de zéro ultérieurement.
1. En bas de la page, sélectionnez **Suivant : Vérifier + Créer>** . Une fois la validation réussie, sélectionnez **Créer**. Le déploiement de la machine virtuelle peut prendre plusieurs minutes.
1. Une fois le déploiement de la machine virtuelle effectué, sélectionnez **Accéder à la ressource**.
1. Vous êtes à présent sur la page SC900-WinVM.
1. En haut de la page, sélectionnez **Se connecter** puis, dans la liste déroulante, sélectionnez **RDP**.
1. Notez que le prérequis concernant le port n’est pas respecté.  Pour satisfaire au prérequis, une règle de sécurité réseau de trafic entrant avec le port de destination 3389 utilisé par le protocole RDP doit être configurée.  Vous effectuerez cette opération dans la prochaine étape quand vous allez créer un groupe de sécurité réseau.
1. Laissez cet onglet de navigateur ouvert.

### <a name="task-2"></a>Tâche 2

Créez un groupe de sécurité réseau, affectez l’interface réseau de la machine virtuelle à ce groupe de sécurité réseau et créez une règle de trafic RDP entrant.

1. Ouvrez l’onglet SC900-WinVM - Microsoft Azure dans votre navigateur.

1. Dans le coin supérieur gauche de la page, en regard de la mention Microsoft Azure, sélectionnez l’icône de menu Afficher le portail (les trois lignes horizontales également appelées icône Hamburger), puis sélectionnez **Tous les services**.
1. Dans la zone Filtrer les services, en regard de la mention Tous les services, saisissez **Groupes de sécurité réseau**. Dans les résultats, sélectionnez **Groupes de sécurité réseau** (ne sélectionnez pas Groupes de sécurité du réseau classique).
1. En haut de la page Groupes de sécurité réseau, sélectionnez **+ Créer**.
1. Sous l’onglet de base de la page Créer un groupe de sécurité réseau, spécifiez les paramètres suivants :
    1. Abonnement :  Pass Azure - Parrainage

    1. Groupe de ressources :  **LabsSC900**
    1. Nom :  **NSG-SC900**
    1. Région : laissez la valeur par défaut.
    1. Sélectionnez **Examiner et créer** puis sélectionnez **Créer**.
1. Une fois le déploiement effectué, sélectionnez **Accéder à la ressource**.
1. Notez les règles de trafic entrant et sortant par défaut dans le groupe de sécurité réseau.  Bien que le groupe de sécurité réseau ait été créé et qu’il dispose des règles par défaut pour filtrer le trafic, aucune interface ne lui a été associée.
1. Dans le volet de navigation de gauche de la page NSG-SC900, sous Paramètres, sélectionnez **Interfaces réseau**.
1. Sélectionnez **+ Associer**, au-dessus de la zone de recherche.
1. Un champ à droite de la page permet de sélectionner l’interface réseau à associer au groupe de sécurité réseau. Sélectionnez la flèche de la liste déroulante vers le bas, puis sélectionnez **sc900-winvmXXX** (la valeur XXX est spécifique à l’interface réseau de votre machine virtuelle), puis sélectionnez **OK** en bas de la fenêtre.
1. Une fois l’interface associée au groupe de sécurité réseau, elle s’affiche dans la liste.
1. Dans le volet de navigation gauche, sélectionnez **Règles de sécurité de trafic entrant**.
1. Les règles de trafic entrant par défaut refusent tout trafic entrant qui ne provient pas d’un réseau virtuel ni d’un équilibreur de charge Azure. Vous devez donc configurer une règle pour autoriser le trafic RDP entrant (trafic sur le port 3389). N’oubliez pas que vous ne pouvez pas supprimer les règles par défaut. Toutefois, vous pouvez les remplacer en créant des règles dont la priorité est plus élevée.
1. En haut de la page, sélectionnez **Ajouter** :
1. Sur la fenêtre Ajouter une règle de sécurité de trafic entrant, spécifiez les paramètres suivants :
    1. Source :  **Any**

    1. Plages de ports sources : **\***
    1. Destination :  **Any**
    1. Service :  **RDP**
    1. Action :  **Autoriser**
    1. Priorité :  **300** ; Remarque : Les règles avec les nombres les plus petits ont une priorité plus élevée et sont traitées en premier.
    1. Nom :  **AllowRDP**
1. Sélectionnez **Ajouter**
1. Une fois la règle provisionnée, elle s’affiche dans la liste des règles de trafic entrant (vous devez peut-être actualiser l’écran).
1. Vérifiez maintenant que vous pouvez vous connecter à la machine virtuelle à l’aide de RDP.  Sélectionnez le champ de recherche en haut de la page, à côté de l’indication Microsoft Azure, pour afficher les services récents.  Sélectionnez **Machines virtuelles**.
1. Sélectionnez la machine virtuelle **SC900-WinVM**.
1. En haut de la page, sélectionnez **Se connecter** puis, dans la liste déroulante, sélectionnez **RDP**.
1. Vérifiez que l’adresse IP est paramétrée sur Adresse IP publique, conservez le numéro de port par défaut et sélectionnez **Télécharger le fichier DRP**.
1. Ouvrez le fichier téléchargé et sélectionnez **Se connecter**.
1. Vous serez invité à saisir vos informations d’identification.  Entrez le nom d’utilisateur et le mot de passe que vous avez utilisés quand vous avez créé la machine virtuelle.
1. Une fenêtre de connexion de bureau à distance s’ouvre et indique que l’identité de l’ordinateur distant ne peut pas être vérifiée.  Voulez-vous quand même vous connecter ?  Sélectionnez **Oui**.
1. Vous êtes maintenant connecté à la machine virtuelle. Dans le cas présent, vous avez pu vous connecter à la machine virtuelle, car la règle de trafic entrant que vous avez créée autorise le trafic entrant vers la machine virtuelle via RDP.
1. Laissez la machine virtuelle ouverte. Vous allez l’utiliser pour la tâche suivante.

### <a name="task-3"></a>Tâche 3

Les règles de trafic sortant par défaut de groupe de sécurité réseau autorisent le trafic Internet sortant, ce qui vous permettra de vérifier que vous pouvez vous connecter à Internet.  Vous allez ensuite créer une règle de trafic sortant personnalisée pour bloquer le trafic Internet sortant et tester cette règle.

1. Dans la machine virtuelle, sélectionnez **Edge** pour ouvrir le navigateur.  
1. Entrez **www.bing.com** dans la barre d’adresse du navigateur et confirmez que vous pouvez vous connecter au moteur de recherche.
1. Fermez le navigateur de votre machine virtuelle, mais gardez la machine virtuelle ouverte. Vous l’utiliserez dans les étapes ultérieures.
1. Revenez au portail Azure et ouvrez l’onglet SC900-WinVM - Microsoft Azure dans votre navigateur.
1. Dans le volet de navigation à gauche, sous Paramètres, sélectionnez **Mise en réseau**.
1. Sélectionnez l’onglet **Règles de port de trafic sortant**.  Les règles de trafic sortant par défaut s’affichent.  Notez la règle par défaut « AllowInternetOutBound ». Cette règle autorise l’ensemble du trafic Internet sortant. Vous ne pouvez pas supprimer la règle par défaut, mais vous pouvez la remplacer par une règle de priorité plus élevée. À droite de la page, sélectionnez **Ajouter une règle de port de trafic sortant**.
1. Sur la page Ajouter une règle de sécurité de trafic sortant, spécifiez les paramètres suivants :
    1. Source :  **Any**

    1. Plages de ports source : **\***
    1. Destination :  **Balise du service**
    1. Balise d’identification de destination :  **Internet**
    1. Service :  **Personnaliser** (conservez la valeur par défaut)
    1. Plages de ports de destination : * (veillez à placer un astérisque dans le champ Plages de ports de destination)
    1. Protocole : **Any**
    1. Action : **Deny**
    1. Priorité :  **4000**
    1. Nom :  **DenyInternet**
1. Sélectionnez **Ajouter**
1. Une fois que la règle est créée, elle apparaîtra dans la liste des règles de trafic sortant.  Elle apparaît dans la liste, mais son application prendra quelques minutes (attendez quelques minutes avant de passer aux étapes suivantes).  
1. Revenez à votre machine virtuelle
1. Ouvrez le navigateur Edge dans votre machine virtuelle et entrez **www.bing.com**. La page ne doit pas s’afficher.  Remarque : si vous pouvez vous connecter à Internet et que vous avez vérifié que tous les paramètres de la règle de trafic sortant ont été correctement définis, c’est probablement car il faut quelques minutes pour que la règle prenne effet.  Fermez le navigateur, patientez quelques minutes, puis réessayez.
1. Fermez la connexion au bureau à distance en sélectionnant le **X** en haut au centre de la page où l’adresse IP est affichée.  Une fenêtre contextuelle indique que Votre session à distance sera déconnectée. Sélectionnez **OK**.
1. Dans cette tâche, vous avez configuré une règle de trafic sortant dans votre groupe de sécurité réseau pour bloquer le trafic Internet sortant.

### <a name="tear-down"></a>Destruction

Les machines virtuelles sont des ressources facturées, et bien que le coût d’exécution des machines virtuelles dans cette démonstration soit minuscule, il est recommandé de supprimer le groupe de ressources contenant la machine virtuelle et les ressources associées à la fin du cours.

1. Ouvrez l’onglet SC900-WinVM - Microsoft Azure dans votre navigateur.

1. En haut à gauche de la page, sélectionnez **Tous les services**.
1. Dans la zone Filtrer les services, en regard de la zone Tous les services, saisissez **Groupes de ressources** puis, dans la liste des résultats, sélectionnez **Groupes de ressources**.
1. Sélectionnez **LabsSC900**.
1. Dans la partie supérieure centrale de la page LabsSC900, sélectionnez **Supprimer le groupe de ressources**.
1. Dans la fenêtre qui s’ouvre, saisissez le nom du groupe de ressources, **LabsSC900**, pour confirmer la suppression du groupe de ressources et de toutes ses ressources, puis sélectionnez **Supprimer** au bas de la page.
1. La suppression de toutes les ressources et du groupe de ressources peut prendre quelques minutes.
1. Fermez tous les onglets ouverts du navigateur.

### <a name="review"></a>Révision

Ce labo vous a présenté le processus de configuration d’un groupe de sécurité réseau, en associant ce groupe de sécurité réseau à l’interface réseau d’une machine virtuelle et en ajoutant de nouvelles règles au groupe de sécurité réseau en vue d’autoriser le trafic RDP entrant et de bloquer le trafic Internet sortant.
