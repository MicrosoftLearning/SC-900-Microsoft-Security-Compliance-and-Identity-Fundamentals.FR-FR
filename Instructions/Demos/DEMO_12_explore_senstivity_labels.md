<!---
---
Démonstration : Titre : « Étiquettes de confidentialité dans Microsoft Purview » Parcours d’apprentissage/Module/Unité : « Parcours d’apprentissage : Décrire les fonctionnalités des solutions de conformité Microsoft ; Module 3 : Décrire les fonctionnalités de protection des informations, de gestion du cycle de vie des données et de gouvernance des données dans Microsoft Purview ; Unité 4 : Décrire les étiquettes de confidentialité »
---
--->

# Démo : Étiquettes de confidentialité dans Microsoft Purview

Cette démonstration correspond au contenu Learn suivant :

- Parcours d’apprentissage : Décrire les fonctionnalités des solutions de conformité Microsoft
- Module : Décrire les fonctionnalités de protection des informations, de gestion du cycle de vie des données et de gouvernance des données dans Microsoft Purview
- Unité : Décrire les étiquettes de confidentialité

## Scénario de démonstration

Dans cette démo, vous présentez les fonctionnalités des étiquettes de confidentialité.  Vous passez en revue les paramètres des étiquettes de confidentialité existantes et la stratégie correspondante pour publier l’étiquette.   Ensuite, vous voyez comment appliquer une étiquette et observez son impact du point de vue de l’utilisateur.  **REMARQUE** : la première fois que vous utilisez Word en ligne avec votre locataire Microsoft 365, l’option Sensibilité peut apparaître sur le ruban au bout de 15 minutes.  Les présentateurs doivent exécuter la partie 2 de la démonstration avant la classe afin que le délai soit suffisant pour que l’option s’affiche.

### Partie 1 de la démonstration

Dans cette démonstration, vous présentez les paramètres d’une étiquette de confidentialité existante et la stratégie correspondante pour la publier.

1. Ouvrez l’onglet du navigateur menant sur la page d’accueil de Microsoft Purview.  Si vous l’avez précédemment fermé, ouvrez un onglet du navigateur et entrez **https://admin.microsoft.com** . Connectez-vous avec les identifiants d’administration du tenant (ou « locataire/abonné ») Microsoft 365 fournis par l’hôte de labo autorisé (ALH). Dans le volet de navigation gauche du Centre d’administration Microsoft 365, sélectionnez **Tout afficher**, puis **Conformité**.  Le navigateur ouvre une nouvelle page. Il s’agit de la page d’accueil du portail de conformité Microsoft Purview.  

1. Dans le volet de navigation de gauche, sous Solutions, développez **Protection des informations**, puis sélectionnez **Vue d’ensemble**.  La page de présentation contient des informations sur les principales étiquettes de confidentialité appliquées au contenu, les principales activités détectées, les emplacements où les étiquettes de confidentialité sont appliquées, etc.  
    1. Sur la page de présentation, vous pouvez voir une boîte d’information jaune indiquant que votre organisation n’a pas activé la possibilité de traiter le contenu des fichiers Office en ligne auxquels des étiquettes de confidentialité chiffrées ont été appliquées et qui sont stockés dans OneDrive et SharePoint.  Sélectionnez **Activer maintenant**.  Une fois cette opération effectuée, il peut y avoir un délai avant que le paramètre ne soit propagé à travers le système.

1. Dans le volet de navigation de gauche, sélectionnez **Étiquettes**.

1. Certaines étiquettes ont été préconfigurées dans votre tenant de labo Microsoft 365, pour votre commodité. Sélectionnez l’étiquette nommée **Confidentiel - Finance**.  Une fenêtre s’ouvre et fournit des informations sur cette étiquette.  Notez les paramètres de cette étiquette.  Sélectionnez **Modifier l’étiquette** (ou l’icône de crayon) en haut de la page pour afficher certains des paramètres de base. Si vous ne voyez pas cette option, sélectionnez les points de suspension.
    1. La procédure de configuration commence par l’attribution d’un nom et d’une description à votre étiquette.  Ne changez rien.  Sélectionnez **Suivant** au bas de la page.
    1. Vérifiez l’étendue de cette étiquette. Ne changez rien.  Sélectionnez **Suivant** au bas de la page.
    1. L’écran suivant vous permet de choisir les paramètres de protection des éléments étiquetés. Cette étiquette est configurée pour prendre en charge le marquage du contenu. Ne changez rien.  Sélectionnez **Suivant** au bas de la page.
        1. Sur la page de marquage du contenu, prenez note de l’encadré d’information situé en haut.  Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.
    1. Vous êtes à présent dans la fenêtre d’étiquetage automatique des fichiers et des e-mails.  Lisez la description de l’étiquetage automatique en haut de la page et l’encadré d’information en dessous.  Notez également que cette étiquette est configurée pour l’étiquetage automatique pour des conditions spécifiques. Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.
    1. Cette fenêtre définit les paramètres de protection des équipes, des groupes et des sites qui ont cette étiquette. Si cette option n’est pas activée, sélectionnez **Suivant** en bas de la page.
    1. Cette fenêtre est une fonctionnalité d’évaluation qui permet d’appliquer automatiquement cette étiquette aux ressources de données schématisées dans Mappage de données Microsoft Purview (telles que SQL, Synapse, etc.) qui contiennent les types d’informations sensibles que vous avez choisis.  La fonctionnalité n’est pas activée. Sélectionnez **Annuler** en bas de la page pour quitter l’assistant Configuration de l’étiquette et revenir à la page Protection des données.

1. Dans le volet de navigation de gauche, sélectionnez **Stratégies des étiquettes**.  C’est par le biais des stratégies des étiquettes que les étiquettes de confidentialité peuvent être publiées.  Le tenant Microsoft 365 a été configuré avec certaines stratégies d’étiquette, pour votre commodité.

1. Sélectionnez **Stratégie Confidentiel - Finance**.  Une fenêtre s’ouvre et fournit des informations sur la stratégie. Sélectionnez **Modifier la stratégie** la stratégie en haut de la fenêtre.  Ici, parcourez les paramètres sans rien changer.
    1. Passez en revue la description de « Choisir les étiquettes de confidentialité à publier ».  Notez l’étiquette répertoriée.  Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.
    1. Passez en revue la description de « Attribuer des unités d’administration ». Les unités d’administration sont définies sur le répertoire complet, ne modifiez aucun paramètre. Cliquez sur **Suivant**.  
    1. Passez en revue la description de « Publier pour les utilisateurs et les groupes ».  Notez que cette étiquette est disponible pour tous les utilisateurs.  Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.
    1. Vérifiez les paramètres de stratégie. Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.
    1. Passez en revue la description de « Appliquer une étiquette par défaut aux documents ». Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.
    1. Passez en revue la description de « Appliquer une étiquette par défaut aux e-mails » et de « Hériter de l’étiquette des pièces jointes ». Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.
    1. Passez en revue la description de « Appliquer une étiquette par défaut aux réunions et aux événements du calendrier ». Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.
    1. Passez en revue la description de « Appliquer une étiquette par défaut au contenu de Power BI ». Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.
    1. La dernière option de configuration consiste à nommer votre stratégie.  Comme vous modifiez la stratégie, le champ de nom est grisé. Sélectionnez **Suivant** en bas de la page.
    1. Vérifiez les paramètres de stratégie. Sélectionnez **Annuler** pour abandonner les modifications et revenir à la page Stratégies d’étiquette.

1. Depuis le volet de navigation à gauche, dans Protection des données, sélectionnez Étiquetage automatique. Passez en revue la description. Notez que vous créez des stratégies d’étiquetage automatique pour appliquer automatiquement des étiquettes de confidentialité aux messages électroniques ou aux fichiers OneDrive et SharePoint qui contiennent des informations sensibles. Si des stratégies d’étiquetage automatique sont configurées, sélectionnez-en une et passez en revue les informations de stratégie dans le volet d’informations.  Si aucune stratégie n’est répertoriée, vous pouvez choisir de parcourir les étapes pour en créer une, si le temps le permet.

1. Dans le volet de navigation de gauche, sélectionnez Accueil pour revenir au portail de conformité Microsoft Purview.

1. Gardez cet onglet de navigateur ouvert.

### Partie 2 de la démonstration

Dans cette étape, vous présentez le processus d’application d’une étiquette du point de vue de l’utilisateur (dans notre exemple, l’utilisateur est l’administrateur).  Pour voir l’impact de l’application de l’étiquette, vous sélectionnez l’étiquette Confidentiel - Finance, car elle applique un filigrane.

1. Dans la page d’accueil du portail de conformité Microsoft Purview, sélectionnez l’icône **Lanceur d’application**, à côté de l’indication Contoso Electronics. Sélectionnez l’**icône Word**.  

1. Sélectionnez **Document vierge**, puis saisissez du texte sur la page.  Dans la barre bleue en haut de la page, sélectionnez la flèche vers le bas à côté de Document - Enregistré et, dans la zone du nom du fichier, entrez **Test-label** et appuyez sur la touche **Entrer** de votre clavier.

1. À l’extrême droite de la barre de menus supérieure (également appelée ruban), vous trouverez une flèche vers le bas. Sélectionnez-la, puis **Ruban classique**.  Cela facilite l’identification de l’icône de confidentialité. Sélectionnez **Sensibilité** en regard de l’icône du micro. À partir du menu déroulant, sélectionnez **Confidentiel – Finance**.  

1. Dans la barre de menu supérieure, sélectionnez **Affichage**, puis **Mode lecture**.

1. Remarquez que le document inclut le filigrane.  

1. Fermez les onglets Microsoft Word ouverts sur votre navigateur pour quitter Word.

1. Conservez l’onglet du navigateur Microsoft Purview ouvert pour la prochaine démonstration.

### Révision

Dans cette démonstration, vous avez découvert comment afficher les paramètres qui peuvent être configurés pour les étiquettes de confidentialité et les paramètres des stratégies pour publier des étiquettes de confidentialité. Vous avez également montré comment appliquer une étiquette.
