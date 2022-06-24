---
lab:
  title: Explorer le workflow eDiscovery (Standard)
  module: 'Module 4 Lesson 5: Describe the capabilities of Microsoft compliance solutions: Describe the eDiscovery and audit capabilities of Microsoft Purview'
ms.openlocfilehash: da37016799bb1343013c1ace901137646c0c856b
ms.sourcegitcommit: 57e11f5a455d10c8ae3c95bb8a9487b10af3d315
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/22/2022
ms.locfileid: "146542625"
---
# <a name="lab-explore-the-ediscovery-standard-workflow"></a>Labo : Explorer le workflow eDiscovery (Standard)

## <a name="lab-scenario"></a>Scénario du labo

Dans ce labo, vous allez apprendre à configurer eDiscovery et découvrir le workflow d’eDiscovery (Standard) en créant une conservation eDiscovery et une requête de recherche, puis en exportant les résultats de cette recherche.  Remarque :  Pour obtenir une licence eDiscovery (Standard), l’organisation doit disposer de l’abonnement approprié et d’une licence par utilisateur. Si vous ne savez pas quelles licences prennent en charge eDiscovery (Standard), consultez [Bien démarrer avec eDiscovery (Standard) dans Microsoft Purview](https://docs.microsoft.com/microsoft-365/compliance/get-started-core-ediscovery?view=o365-worldwide).

**Durée estimée** : 20-25 minutes

### <a name="task-1"></a>Tâche 1

Pour accéder à eDiscovery (Standard) ou être ajouté en tant que membre d’un cas eDiscovery, les autorisations appropriées doivent être accordées à l’utilisateur. Dans cette tâche, vous allez jouer le rôle d’administrateur et ajouter des utilisateurs spécifiques en tant que membres du groupe de rôles Gestionnaire eDiscovery.

 Ouvrez Microsoft Edge. Saisissez **admin.microsoft.com** dans la barre d’adresse.

1. Connectez-vous avec vos informations d’identification d’administrateur.
    1. Dans la fenêtre de connexion, entrez **admin@WWLxZZZZZZ.onmicrosoft.com** (où ZZZZZZ représente votre ID de locataire unique fourni par votre fournisseur d’hébergement de labo), puis sélectionnez **Suivant**.

    1. Saisissez le mot de passe d’administrateur communiqué par votre fournisseur d’hébergement de labo. Sélectionnez **Connexion**.
    1. Lorsque vous êtes invité à rester connecté, sélectionnez **Oui**. Vous accédez ainsi à la page du Centre d’administration Microsoft 365.

1. Sélectionnez **Tout afficher** dans le volet de navigation gauche du centre d’administration Microsoft 365.

1. Sous les Centres d’administration, sélectionnez **Conformité**.  Le navigateur ouvre une nouvelle page. Il s’agit de la page d’accueil du portail de conformité Microsoft Purview.  

1. Dans le volet de navigation de gauche, sélectionnez **Autorisations**.

1. Dans la page Autorisations et rôles, sous le portail de conformité, sélectionnez **Rôles**.

1. Dans le champ de recherche, entrez **eDiscovery**, puis sélectionnez l’icône de recherche (en forme de loupe).  Sélectionnez **Gestionnaire eDiscovery**.

1. Dans la fenêtre qui s’affiche, vous pouvez voir deux sous-groupes, Gestionnaire eDiscovery et Administrateur eDiscovery.  Lisez leurs descriptions.  Pour ce labo, nous allons ajouter des membres au sous-groupe Administrateur eDiscovery. Sélectionnez **Modifier** à côté d’Administrateur eDiscovery.  Nous recommandons d’attribuer le privilège minimum pour le rôle des utilisateurs.

1. Pour ajouter des membres à ce groupe de rôles, assurez-vous de vous trouver dans l’onglet **Sélectionner un administrateur eDiscovery**, puis choisissez l’option du même nom.

1. Sélectionnez **+ Ajouter** en haut de la page.

1. Dans la liste des noms, sélectionnez **Administrateur MOD**, **Megan Bowen**, puis **Ajouter** et **Terminé** en bas de la page.

1. Après avoir vérifié que les membres ajoutés ne comportent aucune erreur, sélectionnez **Enregistrer**.

1. En bas de la fenêtre eDiscovery, sélectionnez **Fermer**.

1. Conservez cet onglet ouvert pour l’utiliser lors de la prochaine tâche.

### <a name="task-2"></a>Tâche 2

Dans cette tâche, vous allez jouer le rôle d’Administrateur eDiscovery (administrateur MOD est un type d’Administrateur eDiscovery) et créer un dossier pour commencer à utiliser eDiscovery (Standard).

1. Vous devez toujours être dans la page des rôles du portail de conformité. Si vous avez fermé l’onglet du navigateur de la tâche précédente, ouvrez un nouvel onglet de navigateur et entrez **compliance.microsoft.com**

1. Dans le volet de navigation de gauche, sous Solutions, sélectionnez **eDiscovery**, puis **Standard**.

1. En haut de la page eDiscovery (Standard), sélectionnez **+ Créer un dossier**.

1. Dans la fenêtre Nouveau dossier, donnez-lui le nom **SC900 Dossier test** avant de sélectionner **Enregistrer** en bas de la page.

1. Le dossier apparaît maintenant dans la liste.

1. Puisque vous l’avez créé et que vous disposez des privilèges d’Administrateur eDiscovery, vous pouvez commencer à travailler dessus.  

1. Conservez cet onglet ouvert pour l’utiliser lors de la prochaine tâche.

### <a name="task-3"></a>Tâche 3

Maintenant que votre dossier eDiscovery (Standard) est créé, vous pouvez commencer à travailler dessus.  Dans cette tâche, vous allez y associer une conservation eDiscovery,  plus particulièrement pour la boîte aux lettres Exchange d’Adele Vance.

1. Ouvrez l’onglet eDiscovery (Standard) dans votre navigateur.

1. Dans la page eDiscovery (Standard), sélectionnez le dossier créé dans l’onglet précédent, **SC900 Dossier test**.

1. Sur la page d’accueil du dossier, sélectionnez l’onglet **Conservation**, puis **+ Créer**.

1. Dans le champ Nom, saisissez **Conservation test** avant d’utiliser le bouton Suivant.

1. Dans la page Choisir les emplacements, sélectionnez le bouton bascule en regard de **Boîtes aux lettres Exchange** pour définir l’état sur **Activé**, puis sélectionnez **Choisir les utilisateurs, groupes ou équipes**.  Dans la zone de recherche, saisissez **Adele**, puis appuyez sur Entrée. Sélectionnez **Adele Vance** dans les résultats de recherche, puis Choisir et enfin **Terminé**.

1. Sur la page Choisir l’emplacement, sélectionnez **Suivant**.  Dans le cadre du labo, cette conservation ne contiendra aucun autre emplacement.

1. La page des Conditions de requête vous permet de créer une conservation à partir de mots clés ou de conditions spécifiques. Sélectionnez **+ Conditions** pour afficher les options disponibles.  Sélectionnez **Suivant**. Sans conditions, la conservation conserve tout le contenu à l’emplacement prévu.

1. Vérifiez les paramètres avant de sélectionner **Envoyer**. Après un moment, vous pouvez utiliser le bouton **Terminé**.  La Conservation test apparaît maintenant dans la liste.  Si vous ne la voyez pas tout de suite, pensez à **Actualiser**.

1. Conservez cet onglet ouvert pour l’utiliser lors de la prochaine tâche.

### <a name="task-4"></a>Tâche 4

Une fois la conservation finalisée, vous créerez une requête de recherche.  Quand vous aurez terminé, vous exporterez et téléchargerez les résultats pour les étudier plus tard.   Remarque :  Les recherches associées à un dossier eDiscovery (Standard) ne sont pas listées dans la page de recherche de contenu du portail de conformité Microsoft Purview. Elles apparaissent seulement dans la page des recherches du dossier eDiscovery (Standard) associé.

1. Ouvrez l’onglet du dossier test SC900.

1. Sur la page Conservations du dossier, sélectionnez **Recherches**,

1. puis **+ Nouvelle recherche** sur la page suivante.

1. Dans le champ Nom, saisissez **Conservation test - Recherches ventes**, puis sélectionnez **Suivant** en bas de la page.

1. Dans la page Choisir les emplacements, sélectionnez **Emplacements en attente** et désélectionnez **Ajouter du contenu d’application pour les utilisateurs locaux**, car votre environnement de labo n’a pas d’utilisateurs locaux, puis sélectionnez **Suivant**.

1. La page des Conditions de requête vous permet de créer une recherche à partir de mots clés ou de conditions spécifiques. Saisissez **Ventes** dans le champ des mots clés, puis sélectionnez **Suivant**.

1. Vérifiez les paramètres avant de sélectionner **Envoyer**. Après un moment, vous pouvez utiliser le bouton **Terminé**.  La recherche apparaît dans la liste.  Si vous ne la voyez pas tout de suite, pensez à **Actualiser**.

1. Dans la fenêtre des Recherches, sélectionnez celle que vous venez de créer, **Conservation test - Recherches ventes**.  Une fenêtre s’affiche, dans laquelle l’onglet Résumé est ouvert.  Une fois la recherche terminée, l’état indique que celle-ci est terminée.  Si c’est bien le cas, s’affiche alors un onglet  **Statistiques de recherche** que vous devez sélectionner. Déroulez ensuite le menu près du Contenu de la recherche.  Vous pouvez également afficher plus d’informations sur le rapport de condition et les emplacements principaux.  

1. En bas de la page, sélectionnez **Actions**.  Examinez les options disponibles, puis sélectionnez **Exporter des résultats**.

    1. Dans la fenêtre qui s’affiche, conservez les paramètres par défaut et choisissez **Exporter** en bas de la page. Cela vous redirige automatiquement vers la fenêtre « Conservation test - Recherches ventes », Sélectionnez **fermer** en bas de la page.

    1. En haut de la page SC900-Dossier test, sélectionnez **Exportations**,
    1. puis **Conservation test - Recherches ventes_Export**.
    1. Dans la fenêtre qui s’ouvre, une clé d’exportation s’affiche. Sélectionnez **Copier dans le presse-papiers**.
    1. En haut, sélectionnez **Télécharger les résultats**. Une nouvelle page s’ouvre en même temps qu’une fenêtre contextuelle qui vous demande si vous voulez ouvrir ce fichier. Choisissez **Ouvrir**.
    1. Si vous réalisez cette action pour la première fois, il vous sera demandé d’installer l’outil d’exportation eDiscovery de Microsoft Office 365.  Sélectionnez **Installer**.
    1. Une fois cette opération terminée, l’outil d’exportation eDiscovery s’ouvre.  Dans le premier champ, collez la clé d’exportation que vous avez copiée précédemment (Ctrl + V sur votre clavier, ou clic droit puis coller avec votre souris).
    1. Dans le second champ, indiquez à quel emplacement vous souhaitez enregistrer le fichier d’exportation, puis sélectionnez **Démarrer**.  À la fin du téléchargement, **fermez** cet onglet.
    1. Cela vous redirige vers la fenêtre « Conservation test - Recherches ventes_Export ».  Sélectionnez **Fermer**.
    1. Vérifiez l’emplacement de votre téléchargement pour vous assurer que l’opération s’est bien déroulée.

### <a name="review"></a>Révision

Dans ce labo, vous avez appris les bases d’eDiscovery (Standard), notamment la configuration des autorisations pour chaque rôle et la création d’un dossier eDiscovery.  Ce dernier vous a permis de découvrir le workflow d’eDiscovery (Standard). Vous avez créé une conservation eDiscovery et une requête de recherche, avant d’exporter les résultats de cette recherche afin de les examiner plus tard.
