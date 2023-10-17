<!---
---
Labo : Titre : « Explorer le workflow eDiscovery (Standard) » Parcours d’apprentissage/Module/Unité : « Parcours d’apprentissage : Décrire les fonctionnalités de conformité Microsoft ; Module 5 : Décrire les fonctionnalités d’eDiscovery et d’audit de Microsoft Purview ; Unité 2 : Décrire les solutions eDiscovery dans Microsoft 365 »
---
--->

# Labo : Explorer le workflow eDiscovery (Standard)

Ce labo correspond au contenu Learn suivant :

- Parcours d’apprentissage : Décrire les fonctionnalités des solutions de conformité Microsoft
- Module : Décrire les fonctionnalités eDiscovery et d’audit de Microsoft Purview
- Unité : Décrire les solutions eDiscovery dans Microsoft Purview

## Scénario du labo

Dans ce labo, vous suivez les étapes nécessaires pour configurer eDiscovery, notamment configurer les autorisations de rôle, créer un cas eDiscovery, créer une conservation eDiscovery et créer une requête de recherche.  Remarque :  Pour obtenir une licence eDiscovery (Standard), l’organisation doit disposer de l’abonnement approprié et d’une licence par utilisateur. Si vous ne savez pas quelles licences prennent en charge eDiscovery (Standard), consultez [Bien démarrer avec eDiscovery (Standard) dans Microsoft Purview](https://docs.microsoft.com/microsoft-365/compliance/get-started-core-ediscovery?view=o365-worldwide).

**Durée estimée** : 25-30 minutes

### Tâche 1

Pour accéder à eDiscovery (Standard) ou être ajouté en tant que membre d’un cas eDiscovery, les autorisations appropriées doivent être accordées à l’utilisateur. Dans cette tâche, vous allez jouer le rôle d’administrateur et ajouter des utilisateurs spécifiques en tant que membres du groupe de rôles Gestionnaire eDiscovery.

1. Ouvrez l’onglet du navigateur pour la page d’accueil de Microsoft Purview.  Si vous l’aviez fermé, ouvrez un onglet du navigateur et entrez **https://admin.microsoft.com** . Connectez-vous avec les informations d’identification d’administrateur du locataire Microsoft 365 fournies par l’hébergeur de labo agréé. Dans le volet de navigation de gauche du Centre d’administration Microsoft 365, sélectionnez **Tout afficher**, puis **Conformité**.  Le navigateur ouvre une nouvelle page. Il s’agit de la page d’accueil du portail de conformité Microsoft Purview.  


1. Dans le volet de navigation de gauche, développez (sélectionnez la flèche vers le bas) **Rôles et étendues**, puis sélectionnez **Autorisations**.

1. Sous les solutions Microsoft Purview, sélectionnez **Rôles**.

1. Dans le champ de recherche, entrez **eDiscovery**, puis appuyez sur Entrée sur votre clavier.  Sélectionnez **Gestionnaire eDiscovery**.

1. Sélectionnez **Modifier**.  Notez qu’il y a deux sous-groupes, Gestionnaire eDiscovery et Administrateur eDiscovery.  
    1. La page « Gérer le gestionnaire eDiscovery » vous permet d’ajouter des utilisateurs au rôle de gestionnaire eDiscovery. Pour ce labo, nous allons ajouter des membres au sous-groupe Administrateur eDiscovery, donc sélectionnez **Suivant**.
    1. Dans la page « Gérer l’administrateur eDiscovery », sélectionnez **Sélectionner les utilisateurs**. Recherchez et sélectionnez **Administrateur MOD** et **Megan Bowen**, appuyez sur **Sélectionner** en bas de la page et sélectionnez **Suivant**, puis **Enregistrer**.
    1. Dans la page « Vous avez correctement mis à jour le groupe de rôles », sélectionnez **Terminé**.

1. Gardez cet onglet ouvert, car vous l’utilisez dans la prochaine tâche.

### Tâche 2

Dans cette tâche, vous allez jouer le rôle d’Administrateur eDiscovery (administrateur MOD est un type d’Administrateur eDiscovery) et créer un dossier pour commencer à utiliser eDiscovery (Standard).

1. Vous devez toujours être dans la page des rôles du portail de conformité. Si vous avez fermé l’onglet du navigateur de la tâche précédente, ouvrez un nouvel onglet de navigateur et entrez **compliance.microsoft.com**

1. Dans le volet de navigation de gauche, sous Solutions, développez **eDiscovery**, puis **Standard**.

1. En haut de la page eDiscovery (Standard), sélectionnez **+ Créer un dossier**.

1. Dans la fenêtre Nouveau dossier, donnez-lui le nom **SC900 Dossier test** avant de sélectionner **Enregistrer** en bas de la page.

1. Le dossier apparaît maintenant dans la liste.

1. Puisque vous l’avez créé et que vous disposez des privilèges d’Administrateur eDiscovery, vous pouvez commencer à travailler dessus.  

1. Gardez cet onglet ouvert, car vous l’utilisez dans la tâche suivante.

### Tâche 3

Maintenant que vous avez créé un cas eDiscovery (Standard), vous pouvez commencer à l’utiliser.  Dans cette tâche, vous créez une conservation eDiscovery pour le cas que vous avez créé.  En particulier, vous créez une conservation pour la boîte aux lettres Exchange d’Adele Vance.

1. Ouvrez l’onglet eDiscovery (Standard) dans votre navigateur.

1. Dans la page eDiscovery (Standard), sélectionnez le dossier créé dans l’onglet précédent, **SC900 Dossier test**.

1. Sur la page d’accueil du dossier, sélectionnez l’onglet **Conservation**, puis **+ Créer**.

1. Dans le champ Nom, entrez **Conservation test** et sélectionnez **Suivant**.

1. Dans la page Choisir les emplacements, sélectionnez le bouton bascule à côté de **Boîtes aux lettres Exchange** pour définir l’état sur **Activé**.  

1. Sélectionnez maintenant **Choisir des utilisateurs, des groupes ou des équipes**.  Dans la zone de recherche, saisissez **Adele**, puis appuyez sur Entrée. Dans les résultats de recherche, sélectionnez **Adele Vance**, puis **Terminé**.

1. Sur la page Choisir l’emplacement, sélectionnez **Suivant**.  Dans le cadre du labo, cette conservation ne contiendra aucun autre emplacement.

1. La page Conditions de requête vous permet de créer une conservation à partir de mots clés ou de conditions spécifiques. Sélectionnez **+ Ajouter une condition** pour voir les options disponibles.  Sélectionnez **Suivant**. Sans conditions, la conservation conserve tout le contenu à l’emplacement prévu.

1. Vérifiez les paramètres avant de sélectionner **Envoyer**. Après un moment, vous pouvez utiliser le bouton **Terminé**.  La Conservation test apparaît maintenant dans la liste.  Si vous ne la voyez pas tout de suite, pensez à **Actualiser**.

1. Gardez cet onglet ouvert, car vous l’utilisez dans la tâche suivante.

### Tâche 4

Une fois la conservation en place, vous créez une requête de recherche.  Quand votre recherche est terminée, eDiscovery prend en charge des actions, comme l’exportation et le téléchargement des résultats pour investigation ultérieure.   Remarque :  Les recherches associées à un dossier eDiscovery (Standard) ne sont pas listées dans la page de recherche de contenu du portail de conformité Microsoft Purview. Elles apparaissent seulement dans la page des recherches du dossier eDiscovery (Standard) associé.

1. Ouvrez l’onglet du Cas de test SC900 dans votre navigateur.

1. Dans la page Cas de test SC900, sélectionnez **Recherches**.

1. puis **+ Nouvelle recherche** sur la page suivante.

1. Dans le champ Nom, saisissez **Conservation test - Recherches ventes**, puis sélectionnez **Suivant** en bas de la page.

1. Dans la page Choisir les emplacements, sélectionnez **Emplacements en attente** et désélectionnez **Ajouter du contenu d’application pour les utilisateurs locaux**, car votre environnement de labo n’a pas d’utilisateurs locaux, puis sélectionnez **Suivant**.

1. La page des Conditions de requête vous permet de créer une recherche à partir de mots clés ou de conditions spécifiques. Saisissez **Ventes** dans le champ des mots clés, puis sélectionnez **Suivant**.

1. Vérifiez les paramètres avant de sélectionner **Envoyer**. Après un moment, vous pouvez utiliser le bouton **Terminé**.  La recherche apparaît dans la liste.  Si vous ne la voyez pas tout de suite, pensez à **Actualiser**.

1. Dans la fenêtre Recherches, sélectionnez celle que vous avez créée, **Conservation test - Recherches ventes**.  Une fenêtre s’affiche, dans laquelle l’onglet Résumé est ouvert.  Une fois la recherche terminée, l’état indique que celle-ci est terminée.  Vous voyez un onglet Statistiques de recherche (sinon, la recherche est peut-être encore en cours et peut prendre encore quelques minutes).  **Statistiques de recherche** que vous devez sélectionner. Déroulez ensuite le menu près du Contenu de la recherche.  Vous pouvez également afficher plus d’informations sur le rapport de condition et les emplacements principaux.  

1. En bas de la page, sélectionnez **Actions**.  Notez les options disponibles qui comprennent des options d’exportation (les options d’exportation ne peuvent pas être sélectionnées à partir de la plateforme lab fournie par l’hébergeur de labo autorisé, mais sont disponibles dans un environnement de production et considérées comme faisant partie du workflow standard). Sélectionnez **Fermer**.

1. Déconnectez-vous et fermez toutes les fenêtres ouvertes du navigateur.

### Révision

Dans ce labo, vous avez suivi les étapes nécessaires pour bien démarrer avec eDiscovery (Standard), notamment la configuration des autorisations de rôle pour eDiscovery et la création d’un cas eDiscovery.  Ce dernier vous a permis de suivre les éléments du workflow eDiscovery (Standard) en créant une conservation eDiscovery et une requête de recherche.
