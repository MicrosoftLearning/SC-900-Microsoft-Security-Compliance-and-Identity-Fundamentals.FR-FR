<!---
---
Démonstration : titre : « Explorer le workflow (standard) eDiscovery » Parcours d’apprentissage/module/unité : « Décrire les fonctionnalités de Microsoft Priva et Microsoft Purview ; Module 3 : décrire les solutions de conformité des données de Microsoft Purview ; Unité 2 : décrire eDiscovery »
---
--->

# Démo : Explorer le workflow eDiscovery (Standard)

Cette démonstration correspond au contenu Learn suivant :

- Parcours d’apprentissage : décrire les fonctionnalités de Microsoft Priva et Microsoft Purview
- Module : décrire les solutions de conformité des données de Microsoft Purview
- Unité : décrire eDiscovery

## Scénario de démonstration

Dans cette démo, vous suivez les étapes nécessaires pour configurer eDiscovery, notamment configurer les autorisations de rôle, créer un cas eDiscovery, créer une conservation eDiscovery et créer une requête de recherche.  REMARQUE : dans le portail Microsoft Purview, les mises à jour apportées à l’interface utilisateur sont déployées progressivement. Certains locataires de labo/démonstration peuvent ne pas encore afficher la dernière interface utilisateur. Toutes les étapes de labo sont donc affichées dans l’IU eDiscovery classique.

### Partie 1 de la démonstration

Pour accéder à eDiscovery (Standard) ou être ajouté en tant que membre d’un cas eDiscovery, les autorisations appropriées doivent être accordées à l’utilisateur. Dans cette partie de la démo, en tant qu’administrateur général, vous allez suivre le processus d’ajout d’utilisateurs spécifiques en tant que membres du groupe de rôles Gestionnaire eDiscovery.

1. Ouvrez l’onglet du navigateur pour accéder à **Microsoft Purview**. Si vous l’avez précédemment fermé, ouvrez un onglet de navigateur et saisissez **https://purview.microsoft.com** dans la barre d’adresses. Pour accéder au nouveau portail Microsoft Purview, sélectionnez la zone en regard du texte **J’accepte les conditions de divulgation de flux de données et les déclarations de confidentialité**, puis sélectionnez **Démarrer**.  
1. Dans le volet de navigation de gauche, sélectionnez **Paramètres**.
1. Dans le volet de navigation qui s’ouvre, sélectionnez **Rôles et étendues** pour développer l’option, puis sélectionnez **Groupes de rôles**.
1. Dans la zone de recherche située à droite de l’écran, recherchez le terme **eDiscovery**.  Sélectionnez **Gestionnaire eDiscovery**.
    1. Sélectionnez **Modifier**.
    1. Sélectionnez **Choisir des utilisateurs**.
    1. Recherchez l’administrateur MOD, sélectionnez la zone à côté de **Administrateur MOD**, puis cliquez sur le bouton **Sélectionner** en bas de la page.
    1. Sélectionnez **Suivant**, puis **Enregistrer**. Enfin, sélectionnez **Terminé**.

1. Gardez cet onglet de navigateur ouvert.

### Partie 2 de la démonstration

Dans cette partie, vous allez créer un cas pour commencer à utiliser eDiscovery (standard).

1. Dans le volet de navigation de gauche, sélectionnez **Solutions**, **eDiscovery**, puis **Dossiers standard**.

1. En haut de la page eDiscovery (Standard), sélectionnez **+ Créer un dossier**.

1. Dans la fenêtre Nouveau cas, entrez un nom de cas, **Cas test SC900**, puis sélectionnez **Enregistrer** en bas de la page.

1. Le cas devrait maintenant apparaître dans la liste.

1. En tant que créateur du cas et du fait que vous disposez des privilèges d’administrateur eDiscovery, vous pouvez commencer à travailler dessus.  

1. Gardez cet onglet de navigateur ouvert.

### Partie 3 de la démonstration

Maintenant que vous avez créé un cas eDiscovery (Standard), vous pouvez commencer à l’utiliser.  Dans cette partie, vous créez une conservation eDiscovery pour le cas que vous avez créé.  En particulier, vous créez une conservation pour la boîte aux lettres Exchange d’Adele Vance.

1. Sur la page eDiscovery (Standard), sélectionnez le dossier créé : **SC900 Dossier test**.

1. À partir de la page d’accueil du cas, sélectionnez l’onglet **Conservation** puis **+Créer**.

1. Dans le champ Nom, entrez **Conservation test** et sélectionnez **Suivant**.

1. Dans la page Choisir les emplacements, sélectionnez le bouton bascule à côté de **Boîtes aux lettres Exchange** pour définir l’état sur **Activé**.  

1. Sélectionnez maintenant **Choisir des utilisateurs, des groupes ou des équipes**.  Dans la zone de recherche, saisissez **Adele**, puis appuyez sur Entrée. Dans les résultats de recherche, sélectionnez **Adele Vance**, puis **Terminé**.

1. Sur la page Choisir les emplacements, sélectionnez **Suivant**.  Pour des raisons de commodité avec la démo, aucun autre lieu ne sera inclus dans cette conservation.

1. La page Conditions de requête vous permet de créer une conservation à partir de mots clés ou de conditions spécifiques. Sélectionnez **+ Ajouter une condition** pour voir les options disponibles.  Cliquez sur **Suivant**. Sans aucune condition, la conservation préserve tout le contenu de l’emplacement spécifié.

1. Vérifiez vos paramètres et sélectionnez **Envoyer**, cela peut prendre une minute, puis sélectionnez **Terminé**.  La Conservation test devrait apparaître dans la liste.  Si ce n’est pas le cas, sélectionnez **Actualiser**.

1. Gardez cet onglet de navigateur ouvert.

### Partie 4 de la démonstration

Une fois la conservation en place, vous créez une requête de recherche.  Quand votre recherche est terminée, eDiscovery prend en charge des actions, comme l’exportation et le téléchargement des résultats pour investigation ultérieure.   Remarque : les recherches associées à un dossier eDiscovery (Standard) ne sont pas listées sur la page de recherche de contenu du portail de conformité Microsoft Purview. Elles apparaissent seulement dans la page des recherches du dossier eDiscovery (Standard) associé.

1. Dans la page Cas de test SC900, sélectionnez **Recherches**.

1. Sur la page Recherche, sélectionnez **+ Nouvelle recherche**.

1. Dans le champ Nom, entrez **Conservation test - Recherches ventes**, puis sélectionnez **Suivant** en bas de la page.

1. Sur la page Choisir les emplacements, sélectionnez **Emplacements en attente** et désélectionnez **Ajouter du contenu d’application pour les utilisateurs locaux**, car votre environnement de labo n’a pas d’utilisateurs locaux. Sélectionnez ensuite **Suivant**.

1. La page Conditions de requête vous permet de créer une recherche basée sur des mots-clés ou des conditions spécifiques qui sont remplies. Dans le champ Mot-clé, saisissez **Ventes**, puis sélectionnez **Suivant**.

1. Vérifiez vos paramètres et sélectionnez **Envoyer**, cela peut prendre une minute, puis sélectionnez **Terminé**.  La recherche devrait apparaître dans la liste.  Si ce n’est pas le cas, sélectionnez **Actualiser**.

1. Dans la fenêtre Recherches, sélectionnez celle que vous avez créée, **Conservation test - Recherches ventes**.  Une fenêtre qui s’ouvre avec l’onglet Résumé sélectionné.  Une fois la recherche terminée, l’état indique que celle-ci est terminée.  Vous voyez un onglet Statistiques de recherche (sinon, la recherche est peut-être encore en cours et peut prendre encore quelques minutes).  Sélectionnez l’onglet **Statistiques de recherche** et sélectionnez la flèche vers le bas située à côté de contenu de recherche.  Vous pouvez également obtenir plus d’informations sur le rapport de condition et les principaux emplacements.  

1. En bas de la page, sélectionnez **Actions**.  Remarquez les options disponibles, notamment les options d’exportation. Sélectionnez **Fermer**.

1. Fermez tous les onglets ouverts du navigateur.

### Révision

Dans cette démo, vous avez suivi les étapes nécessaires pour bien démarrer avec eDiscovery (Standard), notamment la configuration des autorisations de rôle pour eDiscovery et la création d’un cas eDiscovery.  Ce dernier vous a permis de suivre les éléments du workflow eDiscovery (Standard) en créant une conservation eDiscovery et une requête de recherche.
