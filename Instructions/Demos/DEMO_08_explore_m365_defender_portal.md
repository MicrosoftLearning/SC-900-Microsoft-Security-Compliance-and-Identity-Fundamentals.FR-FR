<!---
---
Démonstration : Titre : « Portail Microsoft Defender » Module : « Parcours d’apprentissage : décrire les fonctionnalités des solutions de sécurité Microsoft ; Module 4 : décrire les fonctionnalités de protection contre les menaces de Microsoft Defender XDR ; Unité 7 : décrire le portail Microsoft Defender »
---
--->

# Démonstration : portail Microsoft Defender

Cette démonstration correspond au contenu Learn suivant :

- Parcours d’apprentissage : Décrire les fonctionnalités des solutions de sécurité Microsoft
- Module : décrire les fonctionnalités de protection contre les menaces de Microsoft Defender XDR
- Unité : décrire le portail Microsoft Defender

## Scénario de démonstration

Dans cette démonstration, vous allez présenter le fonctionnement du portail Microsoft Defender en explorant le contenu affiché sur la page d’accueil. Vous explorerez également les options du volet de navigation qui permettent d’accéder rapidement aux fonctionnalités de la solution de détection et de réponse étendues (XDR) de Microsoft : Microsoft Defender pour point de terminaison et Microsoft Defender pour Office 365 (messagerie et collaboration).  Enfin, vous présenterez comment le Niveau de sécurité Microsoft permet aux organisations d’améliorer leur posture de sécurité.

### Partie 1 de la démonstration

Explorez la page d’accueil de Microsoft Defender.

1. Ouvrez l’onglet du navigateur pour la page d’accueil de Microsoft Defender.  Si vous avez précédemment fermé le navigateur, ouvrez Microsoft Edge. Dans la barre d’adresse, entrez **https://admin.microsoft.com** , puis connectez-vous avec les informations d’identification d’administrateur du locataire Microsoft 365 fournies par votre hôte de laboratoire autorisé (ALH) pour accéder au centre d’administration Microsoft 365. Dans le volet de navigation de gauche du centre d’administration Microsoft 365, sélectionnez **Tout afficher**, puis **Sécurité**.  Une nouvelle page de navigateur s’ouvre sur la page d’accueil du portail Microsoft Defender.  

1. La page d’accueil du portail Microsoft Defender affiche les cartes les plus courantes dont les équipes de sécurité ont besoin. La composition des cartes et des données dépend du rôle de l’utilisateur. Faites défiler la page pour afficher l’ensemble des cartes par défaut pour votre rôle d’administrateur général.

1. Les carte affichées peuvent être personnalisées selon vos préférences.  Sélectionnez **+ Ajouter des cartes**. Une fenêtre s’ouvre et affiche toutes les cartes disponibles à ajouter à votre page d’accueil.  Toutes les cartes sont peut-être déjà affichées, auquel cas vous verrez la note « Vous avez déjà toutes les cartes sur votre page d’accueil ». Fermez la fenêtre en sélectionnant le **X** en haut à droite.

1. Sélectionner les points de suspension en haut à droite de n’importe quelle carte affiche l’option qui permet de supprimer la carte de la page d’accueil.  

1. Vous pouvez également déplacer les cartes. Pointez le curseur de votre souris sur la barre du titre d’une carte. Quand vous obtenez un curseur en forme de croix, sélectionnez la carte et déplacez-la à l’emplacement souhaité.  

1. Certaines cartes possèdent des boutons en bas celles-ci qui sont sélectionnables. Le titre de certaines cartes sert également de lien vers la page de la rubrique.  Par exemple, si vous cliquez sur le titre de la carte Niveau de sécurité Microsoft, cela vous dirige vers la page Niveau de sécurité Microsoft.  Vous allez aborder plus en détail le Niveau de sécurité Microsoft dans une section ultérieure de cette démonstration.

1. Ne fermez pas la fenêtre de navigateur.

### Partie 2 de la démonstration

Dans cette partie de la démonstration, vous allez explorer certaines des options disponibles dans le volet de navigation de gauche du portail Defender.  Par le biais du portail Microsoft Defender, Microsoft respecte son engagement à fournir une plateforme d’opérations de sécurité unifiée. Le portail Microsoft Defender regroupe dans un endroit central la protection, la détection, l’investigation et la réponse aux menaces dans votre organisation toute entière et dans tous ses composants. Il inclut un accès rapide aux solutions Microsoft Defender XDR, y compris Microsoft Defender for Endpoint, Microsoft Defender pour Office 365, Microsoft Defender for Cloud Apps, etc.  Explorez ces options en sélectionnant certains des liens.   Pour revenir à la page d’accueil du portail Microsoft Defender, sélectionnez **Accueil** dans le volet de navigation de gauche.

**REMARQUE : le but est de parcourir certaines des options du panneau de navigation, il ne s’agit pas d’une démonstration complète de toutes les options**.

1. **Gestion de l’exposition** - Les options répertoriées fournissent une vue unifiée de la posture de sécurité pour les ressources et les charges de travail de l’entreprise.
    1. **Surface d’attaque** - Vous pouvez afficher la carte de la surface d’attaque pour votre organisation. Les chemins d’attaque génèrent automatiquement des chemins d’attaque en fonction des données collectées parmi les ressources et les charges de travail. Il simule des scénarios d’attaque et identifie les vulnérabilités et faiblesses qu’un attaquant pourrait exploiter.
    1. **Informations de sécurité** - Les informations d’exposition dans la gestion de l’exposition pour la sécurité Microsoft agrègent en continu les données et les informations de la posture de sécurité issues des charges de travail et des ressources dans un seul pipeline.
    1. **Niveau de sécurité** - Le niveau de sécurité fournit une décomposition du score, des actions d’amélioration qui peuvent améliorer le score de l’organisation et une comparaison du score de sécurité de l’organisation par rapport à des organisations similaires.
    1. **Connecteurs de données** - Ici, vous pouvez connecter des sources de données pour une expérience de gestion de l’exposition plus riche et plus centralisée.
1. **Investigation et réponse** - Ici, vous pouvez voir plusieurs options :
    1. **Incidents et alertes** - Ici, vous pouvez consulter les incidents ou les alertes individuelles des différentes solutions Defender XDR (Defender pour Identity, Defender for Cloud Apps et Defender pour Office 365) et d’autres solutions Microsoft, y compris Microsoft Sentinel, Microsoft Defender pour le cloud, Microsoft Entra et Microsoft Purview.
    1. **Recherche de menaces** - Ici, vous pouvez créer des règles de détection personnalisées et rechercher des menaces spécifiques dans votre environnement.
    1. **Actions et requêtes** - Le centre d’actions unifié regroupe les actions de correction de Microsoft Defender for Endpoint et de Microsoft Defender for Office 365. Il liste les actions de correction en cours et terminées pour vos appareils, contenu de collaboration et e-mails et identités dans un seul et même endroit. Dans les organisations Microsoft 365 avec des boîtes aux lettres Exchange Online, les administrateurs peuvent utiliser la page Soumissions du portail Microsoft Defender pour envoyer des messages, des URL et des pièces jointes à Microsoft pour les analyser.
    1. **Catalogue de partenaires** - Le catalogue de partenaires liste les partenaires technologiques et les services professionnels pris en charge qui peuvent aider votre organisation à améliorer ses fonctionnalités de détection, d’investigation et de renseignement sur les menaces de sa plateforme.
1. **Renseignement sur les menaces** - À partir de l’onglet Renseignement sur les menaces, les utilisateurs peuvent accéder au renseignement sur les menaces Microsoft Defender et aux fonctionnalités prises en charge par la solution, notamment l’analyse des menaces, les profils de renseignement, l’explorateur de renseignements et les projets de renseignement.
1. **Ressources** - L’onglet Ressources vous permet de consulter et de gérer l’inventaire des ressources protégées et découvertes de votre organisation (appareils et identités).
1. **Microsoft Sentinel** - Certaines fonctionnalités de Microsoft Sentinel sont disponibles dans la section Microsoft Sentinel du portail Defender.  Cela nécessite de configurer l’intégration via la page Paramètres.
1. **Identités** - Le nœud Identités est mappé aux fonctionnalités associées à Microsoft Defender pour Identity. Le tableau de bord fournit des informations essentielles et des données en temps réel sur la détection et la réponse pour les menaces d’identité. La page Problèmes d’intégrité liste les problèmes d’intégrité actuels de votre déploiement et de vos capteurs Defender pour Identity en vous avertissant de tout problème dans votre déploiement Defender pour Identity. La page Outils liste des informations supplémentaires pour vous aider à gérer votre environnement Microsoft Defender pour Identity.
1. **Points de terminaison** - Le nœud Points de terminaison dans le volet de navigation de gauche du portail Microsoft Defender est mappé aux fonctionnalités associées à Microsoft Defender for Endpoint.
    1. Gestion des menaces et des vulnérabilités : gérez des vulnérabilités et d’autres sources à risque sur les appareils. Vous pouvez, à partir d’ici, accéder au tableau de bord de gestion des vulnérabilités, des suggestions, des corrections, des faiblesses et bien plus encore.
    1. API et partenaires - Ici, vous pouvez sélectionner les applications connectées et l’explorateur d’API.
    1. Gestion de la configuration - Ici, vous pouvez afficher le tableau de bord de gestion de la configuration des appareils.  Vous pouvez également définir des stratégies de point de terminaison et suivre un déploiement.
1. **E-mail et collaboration** - C’est ici que vous trouverez la fonctionnalité Microsoft Defender for Office 365 qui vous permet de suivre et d’examiner les menaces dans les e-mails de vos utilisateurs, de surveiller des campagnes, etc.
1. **Applications cloud** - C’est ici que vous pouvez accéder à la fonctionnalité Microsoft Defender for Cloud Apps. Pour plus d’informations, consultez la démonstration sur Microsoft Defender for Cloud Apps.
1. **Optimisation SOC** - L’optimisation SOC vous fournit des moyens d’optimiser vos contrôles de sécurité, gagnant de la valeur issue des services de sécurité Microsoft à mesure que le temps se passe.
1. **Rapports** - Les rapports sont unifiés dans le portail Microsoft Defender. Les administrateurs peuvent commencer par un rapport général sur la sécurité et passer à des rapports spécifiques sur les points de terminaison, la messagerie et la collaboration, les applications cloud, l’infrastructure et les identités. Les liens ici sont générés dynamiquement en fonction de la configuration de la charge de travail.
1. **Hub d’apprentissage** - Le hub d’apprentissage vous relie à Microsoft Learn, où vous pouvez accéder à des cours de formation, des tutoriels, de la documentation et d’autres supports pertinents.
1. **Système** - Ceci inclut des sélections pour configurer les autorisations, voir l’intégrité des services, et les paramètres généraux.
    1. Autorisations - Ici, vous pouvez attribuer des autorisations de rôle pour les différentes solutions Microsoft Defender XDR.
    1. Paramètres - Ici, vous configurez les paramètres du portail Defender, de Defender XDR, des solutions qui font partie de Microsoft Defender XDR et de Microsoft Sentinel.  Explorer ceci à volonté.
1. **Personnaliser la navigation** - Ici, vous pouvez effectuer une sélection pour afficher ou masquer des éléments dans votre volet de navigation. Les autres administrateurs ne verront pas vos modifications.

### Partie 3 de la démonstration

Dans cette partie de la démonstration, vous présenterez comment le Niveau de sécurité Microsoft permet aux organisations d’améliorer leur posture de sécurité.

1. Dans le volet de navigation gauche, développez **Gestion de l’exposition**, puis sélectionnez **Niveau de sécurité**.

1. La page Niveau de sécurité Microsoft s’ouvre sur l’onglet Présentation. Le niveau de sécurité est une mesure de la posture de sécurité d’une organisation. Le niveau de sécurité de votre organisation est indiqué sous forme de pourcentage, ainsi que le nombre de points obtenus sur le total des points possibles, le tout par catégorie. Sélectionnez **Inclure**, en regard de l’emplacement indiquant Votre degré de sécurisation. Vous pouvez choisir la vue de votre score pour inclure le score réalisable, le score planifié et le score de licence actuel.

1. La page de présentation inclut aussi les meilleures actions recommandées, le score de comparaison, l’historique et les ressources.

1. Sélectionnez **Actions recommandées** en haut de la page.  Remarquez les informations disponibles pour chaque élément de la table.  

1. Sélectionnez les premiers éléments de la liste et passez en revue les informations disponibles. Dans la fenêtre qui s’ouvre, notez les options d’état disponibles. Sélectionnez l’onglet **Implémentation** pour afficher les informations relatives à l’implémentation. Sélectionnez le symbole **X** dans le coin supérieur droit pour fermer cette fenêtre.

1. Sélectionnez l’onglet **Historique** en haut de la page.  Pour chaque activité répertoriée, il existe une brève instruction qui fournit un contexte.  Sélectionnez un élément à partir du tableau d’historique.  En haut à droite de la page de détails, sous Historique, sélectionnez **X événements** (où X est un nombre).  La fenêtre d’historiques des actions s’ouvre et fournit plus d’informations.  Sélectionnez **Fermer** en bas de la page, puis sélectionnez le **X** dans le coin supérieur droit de la page des détails pour revenir à la page Historique.

1. En haut de la page, sélectionnez **Mesures et tendances**.  Notez les informations disponibles.  Dans le coin supérieur droit de la page, sélectionnez l’**icône du calendrier**.  Vous pouvez limiter la vue à une période personnalisée.  L’**icône de filtre** vous permet de filtrer l’affichage par identité, appareils et/ou applications.  Fermez la fenêtre.

1. Dans le volet de navigation de gauche, sélectionnez **Accueil** pour accéder à la page d’accueil de Microsoft Defender.

1. Gardez l’onglet du navigateur ouvert si vous prévoyez de suivre la démonstration suivante.

### Révision

Dans ce labo, vous avez exploré le portail Microsoft Defender en parcourant le contenu affiché sur la page d’accueil. Vous avez également exploré les options du volet de navigation qui fournissent un accès rapide aux fonctionnalités de Microsoft Defender XDR.  Enfin, vous avez montré comment le Niveau de sécurité Microsoft permet aux organisations d’améliorer leur posture de sécurité.
