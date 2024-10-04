---
lab:
  title: Explorer eDiscovery
  module: Describe the data compliance solutions of Microsoft Purview
---

# Labo : Explorer eDiscovery

Ce labo correspond au contenu Learn suivant :

- Parcours d’apprentissage : décrire les fonctionnalités de Microsoft Priva et Microsoft Purview
- Module : décrire les solutions de conformité des données de Microsoft Purview
- Unité : décrire eDiscovery

## Scénario du labo

Dans ce labo, vous suivez les étapes nécessaires pour configurer eDiscovery, notamment configurer les autorisations de rôle, créer un cas eDiscovery, créer une conservation eDiscovery et créer une requête de recherche.  Remarque : la gestion des licences pour eDiscovery (Standard) nécessite l’abonnement à l’organisation et les licences par utilisateur appropriés. Si vous ne savez pas quelles licences prennent en charge eDiscovery (Standard), consultez [Bien démarrer avec eDiscovery (Standard) dans Microsoft Purview](https://docs.microsoft.com/microsoft-365/compliance/get-started-core-ediscovery?view=o365-worldwide).

**Durée estimée** : 45 minutes

### Tâche 1

Pour accéder à eDiscovery (Standard) ou être ajouté en tant que membre d’un cas eDiscovery, les autorisations appropriées doivent être accordées à l’utilisateur. Dans cette tâche, en tant qu’administrateur général, vous ajouterez des utilisateurs spécifiques en tant que membres du groupe de rôles Gestionnaire eDiscovery.

1. Ouvrez l’onglet du navigateur menant sur la page d’accueil de Microsoft Purview.  Si vous l’avez précédemment fermé, ouvrez un onglet du navigateur et entrez **https://admin.microsoft.com** . Connectez-vous avec les identifiants d’administration du tenant (ou « locataire/abonné ») Microsoft 365 fournis par l’hôte de labo autorisé (ALH). Si vous êtes déjà connecté en tant qu’administrateur, vous êtes invité à effectuer une seconde authentification, dans le cadre de l’authentification multifacteur. SI vous n’étiez pas déjà connecté en tant qu’administrateur, vous serez invité à terminer le processus d’inscription MFA. Suivez les invites à l’écran pour installer l’authentification multifacteur.

1. Dans le volet de navigation gauche du Centre d’administration Microsoft 365, sélectionnez **Tout afficher**, puis **Conformité**.  Une nouvelle page de navigateur s’ouvre sur la page d’accueil du portail Microsoft Purview.  

1. Dans le volet de navigation de gauche, sélectionnez **Paramètres**, développez **Rôles et étendues**, puis sélectionnez **Groupes de rôles**.

1. Dans le champ de recherche, en haut à droite de la page, saisissez **eDiscovery**, puis appuyez sur Entrée.  Sélectionnez **Gestionnaire eDiscovery**.

1. Sélectionnez **Modifier**. Dans le cadre de ce labo, vous allez vous définir en tant qu’administrateur MOD, en tant qu’administrateur eDiscovery et administrateur.  Dans la pratique, vous devez désigner des utilisateurs spécifiques pour des rôles spécifiques.
    1. La page « Gérer le Gestionnaire eDiscovery » vous permet d’ajouter des utilisateurs au rôle de Gestionnaire eDiscovery.
    1. Sélectionnez **Choisir des utilisateurs**. Recherchez et sélectionnez **Administrateur MOD**, appuyez sur **Sélectionner** en bas de la page, puis sélectionnez **Suivant**.
    1. Sur la page « Gérer le Gestionnaire eDiscovery », sélectionnez **Choisir des utilisateurs**. Recherchez et sélectionnez **Administrateur MOD**, appuyez sur **Sélectionner** en bas de la page, puis sélectionnez **Suivant** et **Enregistrer**.
    1. Sur la page « Vous avez mis à jour le groupe de rôles », sélectionnez **Terminé**.

1. Gardez cet onglet ouvert, car vous l’utilisez dans la prochaine tâche.

### Tâche 2

Dans cette tâche, vous allez jouer le rôle d’Administrateur eDiscovery (administrateur MOD est un type d’Administrateur eDiscovery) et créer un dossier pour commencer à utiliser eDiscovery (Standard).

1. Vous devez toujours être dans la page des rôles du portail de conformité. Si vous avez fermé l’onglet du navigateur de la tâche précédente, ouvrez un nouvel onglet de navigateur et entrez **compliance.microsoft.com** pour accéder au portail Microsoft Purview.

1. Dans le volet de navigation de gauche, sous Solutions, développez **eDiscovery**, puis sélectionnez **Dossiers standard**.

1. En haut de la page eDiscovery (Standard), sélectionnez **+ Créer un dossier**.

1. Dans la fenêtre Nouveau cas, entrez un nom de cas, **Cas test SC900**, puis sélectionnez **Enregistrer** en bas de la page.

1. Le cas devrait maintenant apparaître dans la liste.

1. En tant que créateur du cas et du fait que vous disposez des privilèges d’administrateur eDiscovery, vous pouvez commencer à travailler dessus.  

1. Gardez cet onglet ouvert, car vous l’utilisez dans la tâche suivante.

### Tâche 3

Maintenant que vous avez créé un cas eDiscovery (Standard), vous pouvez commencer à l’utiliser.  Dans cette tâche, vous créez une conservation eDiscovery pour le cas que vous avez créé.  En particulier, vous créez une conservation pour la boîte aux lettres Exchange d’Adele Vance.

1. Ouvrez l’onglet eDiscovery (Standard) dans votre navigateur.

1. Dans la page eDiscovery (Standard), sélectionnez le dossier créé dans l’onglet précédent, **SC900 Dossier test**.

1. À partir de la page d’accueil du cas, sélectionnez l’onglet **Conservation** puis **+Créer**.

1. Dans le champ Nom, entrez **Conservation test** et sélectionnez **Suivant**.

1. Dans la page Choisir les emplacements, sélectionnez le bouton bascule à côté de **Boîtes aux lettres Exchange** pour définir l’état sur **Activé**.  

1. Sélectionnez maintenant **Choisir des utilisateurs, des groupes ou des équipes**.  Dans la zone de recherche, saisissez **Adele**, puis appuyez sur Entrée. Dans les résultats de recherche, sélectionnez **Adele Vance**, puis **Terminé**.

1. Sur la page Choisir les emplacements, sélectionnez **Suivant**.  Pour des raisons de commodité avec le labo, aucun autre lieu ne sera inclus dans cette conservation.

1. La page Conditions de requête vous permet de créer une conservation à partir de mots clés ou de conditions spécifiques. Sélectionnez **+ Ajouter une condition** pour voir les options disponibles.  Cliquez sur **Suivant**. Sans aucune condition, la conservation préserve tout le contenu de l’emplacement spécifié.

1. Vérifiez vos paramètres et sélectionnez **Envoyer**, cela peut prendre une minute, puis sélectionnez **Terminé**.  La Conservation test devrait apparaître dans la liste.  Si ce n’est pas le cas, sélectionnez **Actualiser**.

1. Gardez cet onglet ouvert, car vous l’utilisez dans la tâche suivante.

### Tâche 4

Une fois la conservation en place, vous créez une requête de recherche.  Quand votre recherche est terminée, eDiscovery prend en charge des actions, comme l’exportation et le téléchargement des résultats pour investigation ultérieure.   Remarque : les recherches associées à un dossier eDiscovery (Standard) ne sont pas listées sur la page de recherche de contenu du portail de conformité Microsoft Purview. Elles apparaissent seulement dans la page des recherches du dossier eDiscovery (Standard) associé.

1. Ouvrez l’onglet du Cas de test SC900 dans votre navigateur.

1. Dans la page Cas de test SC900, sélectionnez **Recherches**.

1. Sur la page Recherche, sélectionnez **+ Nouvelle recherche**.

1. Dans le champ Nom, entrez **Conservation test - Recherches ventes**, puis sélectionnez **Suivant** en bas de la page.

1. Dans la page Choisir les emplacements, sélectionnez **Emplacements en attente** et désélectionnez **Ajouter du contenu d’application pour les utilisateurs locaux**, car votre environnement de labo n’a pas d’utilisateurs locaux, puis sélectionnez **Suivant**.

1. La page Conditions de requête vous permet de créer une recherche basée sur des mots-clés ou des conditions spécifiques qui sont remplies. Dans le champ Mot-clé, saisissez **Ventes**, puis sélectionnez **Suivant**.

1. Vérifiez vos paramètres et sélectionnez **Envoyer**, cela peut prendre une minute, puis sélectionnez **Terminé**.  La recherche devrait apparaître dans la liste.  Si ce n’est pas le cas, sélectionnez **Actualiser**.

1. Dans la fenêtre Recherches, sélectionnez celle que vous avez créée, **Conservation test - Recherches ventes**.  Une fenêtre qui s’ouvre avec l’onglet Résumé sélectionné.  Une fois la recherche terminée, l’état indique que celle-ci est terminée.  Vous voyez un onglet Statistiques de recherche (sinon, la recherche est peut-être encore en cours et peut prendre encore quelques minutes).  Sélectionnez l’onglet **Statistiques de recherche** et sélectionnez la liste déroulante située à côté de contenu de recherche.  Vous pouvez également obtenir plus d’informations sur le rapport de condition et les principaux emplacements.  

1. En bas de la page, sélectionnez **Actions**.  Notez les options disponibles qui comprennent des options d’exportation (les options d’exportation ne peuvent pas être sélectionnées à partir de la plateforme lab fournie par l’hébergeur de labo autorisé, mais sont disponibles dans un environnement de production et considérées comme faisant partie du workflow standard). Sélectionnez **Fermer**.

1. Déconnectez-vous et fermez toutes les fenêtres ouvertes du navigateur.

### Révision

Dans ce labo, vous avez suivi les étapes nécessaires pour bien démarrer avec eDiscovery (Standard), notamment la configuration des autorisations de rôle pour eDiscovery et la création d’un cas eDiscovery.  Ce dernier vous a permis de suivre les éléments du workflow eDiscovery (Standard) en créant une conservation eDiscovery et une requête de recherche.
