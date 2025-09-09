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

Dans ce labo, vous suivez les étapes nécessaires pour configurer eDiscovery, notamment configurer les autorisations de rôle, créer un cas eDiscovery, créer une conservation eDiscovery et créer une requête de recherche.  Note :  pour obtenir une licence eDiscovery, l’organisation doit disposer de l’abonnement approprié et d’une licence par utilisateur. Si vous ne savez pas quelles licences prennent en charge eDiscovery, consultez [Prise en main d’eDiscovery dans Microsoft Purview](https://docs.microsoft.com/microsoft-365/compliance/get-started-core-ediscovery?view=o365-worldwide).

**Durée estimée** : 45 minutes

### Tâche 1

Pour accéder à eDiscovery (Standard) ou être ajouté en tant que membre d’un cas eDiscovery, les autorisations appropriées doivent être accordées à l’utilisateur. Dans cette tâche, en tant qu’administrateur général, vous ajouterez des utilisateurs spécifiques en tant que membres du groupe de rôles Gestionnaire eDiscovery.

1. Vous devriez être sur la page d’accueil du portail Microsoft Purview.  Si vous l’avez précédemment fermé, ouvrez un onglet du navigateur et entrez **https://purivew.microsoft.com** .

1. Dans le volet de navigation de gauche, sélectionnez **Paramètres**, développez **Rôles et étendues**, puis sélectionnez **Groupes de rôles**.

1. Dans le champ de recherche, en haut à droite de la page, saisissez **eDiscovery**, puis appuyez sur Entrée.  Sélectionnez **Gestionnaire eDiscovery**.

1. Sélectionnez **Modifier**. Dans le cadre de ce labo, vous allez vous définir en tant qu’administrateur MOD en tant que gestionnaire et administrateur eDiscovery.  Dans la pratique, vous devez désigner des utilisateurs spécifiques pour des rôles spécifiques.
    1. La page « Gérer le Gestionnaire eDiscovery » vous permet d’ajouter des utilisateurs au rôle de Gestionnaire eDiscovery.
    1. Sélectionnez **Choisir des utilisateurs**. Recherchez et sélectionnez **Administrateur MOD**, appuyez sur **Sélectionner** en bas de la page, puis sélectionnez **Suivant**.
    1. Sur la page « Gérer le Gestionnaire eDiscovery », sélectionnez **Choisir des utilisateurs**. Recherchez et sélectionnez **Administrateur MOD**, appuyez sur **Sélectionner** en bas de la page, puis sélectionnez **Suivant** et **Enregistrer**.
    1. Sur la page « Vous avez mis à jour le groupe de rôles », sélectionnez **Terminé**.

1. Revenez à la page d’accueil de Microsoft Purview en sélectionnant **Accueil** dans le volet de navigation gauche.

1. Gardez cet onglet ouvert, car vous l’utilisez dans la prochaine tâche.

### Tâche 2

Dans cette tâche, vous allez jouer le rôle d’administrateur eDiscovery (administrateur MOD est un type d’administrateur eDiscovery) et créer un ticket pour commencer à utiliser eDiscovery.

1. Vous devriez être sur la page d’accueil du portail Microsoft Purview.

1. Dans le volet de navigation de gauche, sous Solutions, développez **eDiscovery**, puis sélectionnez **Cas**.

1. Dans la page Cas, sélectionnez **Créer un cas**.

1. Dans la fenêtre Nouveau cas, saisissez un nom de cas, **Cas test SC900**, puis sélectionnez **Créer**.

1. Le cas devrait maintenant apparaître dans la liste.

1. En tant que créateur du cas et du fait que vous disposez des privilèges d’administrateur eDiscovery, vous pouvez commencer à travailler dessus.  

1. Gardez cet onglet ouvert, car vous l’utilisez dans la tâche suivante.

### Tâche 3

Une fois un cas créé, vous pouvez commencer à travailler avec lui.  Vous pouvez notamment créer une requête de recherche pour rechercher des données et du contenu pertinents pour votre cas, appliquer une stratégie de mise en attente, créer un jeu de révisions et exporter des données. Dans cette tâche, vous allez explorer certaines de ces options.

1. Ouvrez l’onglet du Cas de test SC900 dans votre navigateur.

1. Dans la page Cas test SC900, sélectionnez **Créer une recherche**.

1. Dans le champ nom, saisissez **recherche de cas SC900**, puis sélectionnez **Créer**.

1. Sélectionnez **Ajouter des sources**. Notez les options de filtre et les paramètres par défaut. Dans la zone de recherche, saisissez **Pradeep**, puis appuyez sur Entrée. Dans les résultats de recherche, sélectionnez **Pradeep Gupta**, puis sélectionnez **Enregistrer et fermer**. Le générateur de conditions vous permet de générer une requête de recherche basée sur des mots clés ou des conditions spécifiques satisfaites. Dans la zone de mot clé, saisissez **Ventes**. À partir de là, vous pouvez sélectionner **Exécuter la requête**.  Cette opération peut prendre quelques minutes.

1. Comme les résultats de requête sont retournés sous la forme de statistiques, vous pouvez exporter les résultats.  Sélectionnez **Exporter** pour activer les options disponibles, puis sélectionnez **Annuler** (les options d’exportation ne peuvent pas être sélectionnées à partir de la plateforme d’activité fournie par l’hôte de l’activité autorisée, mais sont disponibles dans un environnement de production et font partie du flux de travail).

1. Vous pouvez les ajouter à un jeu à réviser pour un traitement ultérieur.  Sélectionnez **Ajouter au jeu à réviser**. Saisissez un nom pour le nouveau jeu à réviser, **`SC900-review-set`** laissez les paramètres par défaut, puis sélectionnez **Ajouter au jeu à réviser**.  Cette opération peut prendre plusieurs minutes.  Vous pouvez désormais passer en revue et prendre des mesures à partir du jeu à réviser, notamment l’étiquetage des éléments, l’interrogation du jeu à réviser, l’exécution d’analyses et bien plus encore.  Explorons à présent les différentes options.

1. Vous pouvez également créer des stratégies de mise en attente pour conserver le contenu pertinent pour votre cas. Sélectionnez **Stratégies de mise en attente**, puis **Nouvelle stratégie**.  Saisissez un nom de stratégie, **`SC900-hold`** puis sélectionnez **Créer.**  Comme dans la recherche, vous devez ajouter des sources de données pour la conservation et ajouter des mots clés et des conditions à utiliser dans la stratégie de mise en attente, puis vous pouvez sélectionner **Appliquer la conservation**.  Les actions que vous pouvez effectuer sur une stratégie de mise en attente incluent une nouvelle tentative, la désactivation et la suppression.

1. Déconnectez-vous et fermez toutes les fenêtres ouvertes du navigateur.

### Révision

Dans cette activité, vous avez appris les bases d’eDiscovery, notamment la configuration des autorisations pour chaque rôle et la création d’un cas eDiscovery.  Avec le cas, vous avez créé des options explorées disponibles dans le cadre du flux de travail eDiscovery, y compris une recherche eDiscovery, une stratégie de mise en attente, l’ajout des résultats de recherche à un jeu à réviser et l’exportation des résultats.
