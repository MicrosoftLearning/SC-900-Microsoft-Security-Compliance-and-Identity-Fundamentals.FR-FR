<!---
---
Démonstration : titre : « Explorer eDiscovery » Parcours d’apprentissage/Module/Unité : « Décrire les fonctionnalités de Microsoft Priva et Microsoft Purview ; Module 3 : décrire les solutions de conformité des données de Microsoft Purview ; Unité 2 : décrire eDiscovery »
---
--->

# Démo : explorer eDiscovery (Standard)

Cette démonstration correspond au contenu Learn suivant :

- Parcours d’apprentissage : décrire les fonctionnalités de Microsoft Priva et Microsoft Purview
- Module : décrire les solutions de conformité des données de Microsoft Purview
- Unité : décrire eDiscovery

## Scénario de démonstration

Dans cette démo, vous suivez les étapes nécessaires pour configurer eDiscovery, notamment configurer les autorisations de rôle, créer un cas eDiscovery, créer une conservation eDiscovery et créer une requête de recherche.  REMARQUE : dans le portail Microsoft Purview, les mises à jour apportées à l’interface utilisateur sont déployées progressivement. Certains locataires de labo/démonstration peuvent ne pas encore afficher la dernière interface utilisateur. Toutes les étapes de labo sont donc affichées dans l’IU eDiscovery classique.

### Partie 1 de la démonstration

Pour accéder à eDiscovery ou être ajouté en tant que membre d’un cas eDiscovery, les autorisations appropriées doivent être affectées à l’utilisateur. Dans cette partie de la démo, en tant qu’administrateur général, vous allez suivre le processus d’ajout d’utilisateurs spécifiques en tant que membres du groupe de rôles Gestionnaire eDiscovery.

1. Ouvrez l’onglet du navigateur pour accéder à **Microsoft Purview**. Si vous l’avez précédemment fermé, ouvrez un onglet de navigateur, saisissez **https://purview.microsoft.com** dans la barre d’adresse, puis sélectionnez **Prise en main**.  
1. Dans le volet de navigation de gauche, sélectionnez **Paramètres**.
1. Dans le volet de navigation qui s’ouvre, sélectionnez **Rôles et étendues** pour développer l’option, puis sélectionnez **Groupes de rôles**.
1. Dans la zone de recherche située à droite de l’écran, recherchez le terme **eDiscovery**.  Sélectionnez **Gestionnaire eDiscovery**.
    1. Sélectionnez **Modifier**.
    1. Sélectionnez **Choisir des utilisateurs**.
    1. Recherchez l’administrateur MOD, sélectionnez la zone à côté de **Administrateur MOD**, puis cliquez sur le bouton **Sélectionner** en bas de la page.
    1. Sélectionnez **Suivant**, puis **Enregistrer**. Enfin, sélectionnez **Terminé**.

1. Gardez cet onglet de navigateur ouvert.

### Partie 2 de la démonstration

Dans cette section, vous allez, en tant qu’administrateur eDiscovery (l’administrateur MOD est un administrateur eDiscovery), créer un cas pour commencer à utiliser eDiscovery.

1. Normalement, vous vous trouvez sur la page d’accueil du portail Microsoft Purview.

1. Dans le volet de navigation de gauche, sous Solutions, développez **eDiscovery**, puis sélectionnez **Cas**.

1. Dans la page Cas, sélectionnez **Créer un cas**.

1. Dans la fenêtre Nouveau cas, saisissez un nom de cas, **Cas test SC900**, puis sélectionnez **Créer**.

1. Le cas devrait maintenant apparaître dans la liste.

1. En tant que créateur du cas et du fait que vous disposez des privilèges d’administrateur eDiscovery, vous pouvez commencer à travailler dessus.  

1. Gardez cet onglet ouvert, car vous l’utilisez dans la tâche suivante.

### Partie 3 de la démonstration

Une fois un cas créé, vous pouvez commencer à travailler avec lui. Vous pouvez notamment créer une requête de recherche pour rechercher des données et du contenu pertinents pour votre cas, appliquer une stratégie de mise en attente, créer un jeu à réviser et exporter des données. Dans cette tâche, vous allez explorer certaines de ces options. NOTE : il est recommandé d’effectuer au préalable la création d’une recherche et d’un jeu à réviser avant la démonstration, afin que les résultats soient disponibles immédiatement, car ces actions peuvent prendre plusieurs minutes.  

1. Ouvrez l’onglet du Cas de test SC900 dans votre navigateur.

1. Dans la page Cas test SC900, sélectionnez **Créer une recherche**.

1. Dans le champ nom, saisissez **recherche de cas SC900**, puis sélectionnez **Créer**.

1. Sélectionnez **Ajouter des sources**. Notez les options de filtre et les paramètres par défaut. Dans la zone de recherche, saisissez **`Pradeep`**, puis sélectionnez **Rechercher**. Dans les résultats de recherche, sélectionnez **Pradeep Gupta**, puis sélectionnez **Enregistrer et fermer**. Le générateur de conditions vous permet de générer une requête de recherche basée sur des mots clés ou des conditions spécifiques satisfaites. Dans la zone de mot clé, saisissez **Ventes**. Vous pouvez alors choisir d’**Exécuter la requête** depuis la fenêtre Choisir les résultats de la recherche. Pour le locataire de l’activité, seule la vue statistique des résultats de la recherche est disponible. Notez les options permettant de classer par indicateurs principaux. Sélectionnez **Exécuter la requête**.  Cette opération peut prendre quelques minutes.

1. Avec des résultats de requête retournés sous forme de statistiques, vous pouvez les résultats.  Dans le coin supérieur droit de l’écran (à côté de l’option « Ajouter au jeu à réviser »), sélectionnez **Exporter** pour afficher les options disponibles, puis sélectionnez **Annuler**.

1. Vous pouvez ajouter les résultats à un jeu à réviser pour un traitement ultérieur.  Sélectionnez **Ajouter au jeu à réviser**. Saisissez un nom pour le nouveau jeu à réviser, **`SC900-review-set`**, laissez les paramètres par défaut, puis sélectionnez **Ajouter au jeu à réviser**. Cette opération peut prendre plusieurs minutes. Une fois les résultats du jeu à réviser présentés, vous pouvez explorer les différentes options, notamment Analytique, Requête, Actions, Étiqueter des fichiers et Gérer.

1. Vous pouvez également créer des stratégies de conservation du contenu pertinent pour votre cas. Depuis la fenêtre Jeu à réviser, sélectionnez l’onglet **Conservation**.  Vous accédez ainsi à la fenêtre Stratégies de conservation. Sélectionnez **Nouvelle stratégie**.  Saisissez un nom de stratégie, **`SC900-hold`**, puis sélectionnez **Créer.**  Comme dans la recherche, vous devez ajouter des sources de données pour la conservation et ajouter des mots clés et des conditions à utiliser dans la stratégie de conservation, puis vous pouvez sélectionner **Appliquer la conservation**.  Les actions possibles sur une stratégie de conservation incluent la réexécution, la désactivation et la suppression.

1. Déconnectez-vous et fermez toutes les fenêtres ouvertes du navigateur.

### Révision

Dans cette démonstration, vous avez suivi les étapes nécessaires pour prendre en main eDiscovery. Elles incluent la configuration des autorisations de rôle et la création d’un cas eDiscovery.  Avec le cas créé, vous avez exploré les paramètres de création d’une recherche, d’exportation des résultats, d’ajout à un jeu à réviser et de création d’une conservation.
