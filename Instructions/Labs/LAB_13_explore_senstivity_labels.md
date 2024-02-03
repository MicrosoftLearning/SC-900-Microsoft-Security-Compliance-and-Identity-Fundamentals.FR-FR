<!---
---
Labo : Titre : « Explorer les étiquettes de confidentialité dans Microsoft Purview » Parcours d’apprentissage/Module/Unité : « Parcours d’apprentissage : Décrire les fonctionnalités des solutions de conformité Microsoft ; Module 3 : Décrire la protection des informations et la gestion du cycle de vie des données dans Microsoft Purview ; Unité 4 : Décrire les étiquettes de confidentialité »
---
--->

# Labo : Explorer les étiquettes de confidentialité dans Microsoft Purview

Ce labo correspond au contenu Learn suivant :

- Parcours d’apprentissage : Décrire les fonctionnalités des solutions de conformité Microsoft
- Module : Décrire la protection des informations et la gestion de cycle de vie des données dans Microsoft Purview
- Unité : Décrire les étiquettes de confidentialité

## Scénario du labo

Dans ce labo, vous explorez les fonctionnalités des étiquettes de confidentialité.  Vous passez en revue les paramètres des étiquettes de confidentialité existantes et la stratégie correspondante pour publier l’étiquette.   Ensuite, vous voyez comment appliquer une étiquette et observez son impact du point de vue de l’utilisateur.

**Durée estimée** : 20 à 25 minutes

### Tâche 1

Dans cette tâche, vous comprendrez le rôle des étiquettes de confidentialité en créant une étiquette et en élaborant une stratégie pour la publier.

1. Ouvrez l’onglet du navigateur menant sur la page d’accueil de Microsoft Purview.  Si vous l’avez précédemment fermé, ouvrez un onglet du navigateur et entrez **https://admin.microsoft.com** . Connectez-vous avec les identifiants d’administration du tenant (ou « locataire/abonné ») Microsoft 365 fournis par l’hôte de labo autorisé (ALH). Dans le volet de navigation gauche du Centre d’administration Microsoft 365, sélectionnez **Tout afficher**, puis **Conformité**.  Le navigateur ouvre une nouvelle page. Il s’agit de la page d’accueil du portail de conformité Microsoft Purview.

1. Dans le volet de navigation de gauche, sous Solutions, développez **Protection des informations**, puis sélectionnez **Vue d’ensemble**. Notez l’avertissement en haut de la page et faites défiler vers le bas pour afficher les informations disponibles.
   1. Sur la page de présentation, vous pouvez voir une boîte d’information jaune indiquant que votre organisation n’a pas activé la possibilité de traiter le contenu des fichiers Office en ligne auxquels des étiquettes de confidentialité chiffrées ont été appliquées et qui sont stockés dans OneDrive et SharePoint.  Sélectionnez **Activer maintenant**.  Une fois cette opération effectuée, il peut y avoir un délai pour que le paramètre se propage dans le système et des étapes supplémentaires doivent être effectuées pour protéger Teams, les sites SharePoint et les groupes Microsoft 365.

1. Dans le volet de navigation de gauche, sélectionnez **Étiquettes**.
   1. Sur la page Étiquettes, vous pouvez voir une boîte d’information jaune indiquant que votre organisation n’a pas activé la possibilité de traiter le contenu des fichiers Office en ligne auxquels des étiquettes de confidentialité chiffrées ont été appliquées et qui sont stockés dans OneDrive et SharePoint.  Sélectionnez **Activer maintenant**.  Une fois cette opération effectuée, il peut y avoir un délai pour que le paramètre se propage dans le système et des étapes supplémentaires doivent être effectuées pour protéger Teams, les sites SharePoint et les groupes Microsoft 365.

1. Certaines étiquettes ont été préconfigurées dans votre locataire de labo Microsoft 365, pour votre commodité. Sélectionnez l’étiquette nommée **Confidentiel - Finance**.  Une fenêtre s’ouvre et fournit des informations sur cette étiquette.  Notez les paramètres de cette étiquette.  Sélectionnez **Modifier l’étiquette** (ou l’icône de crayon) en haut de la page pour afficher certains des paramètres de base. Si vous ne voyez pas cette option, sélectionnez les points de suspension.
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

1. Depuis le volet de navigation à gauche, dans Protection des données, sélectionnez Étiquetage automatique. Passez en revue la description. Notez que vous créez des stratégies d’étiquette automatique pour appliquer automatiquement des étiquettes de confidentialité aux messages électroniques ou aux fichiers OneDrive et SharePoint qui contiennent des informations confidentielles. Aucune stratégie d’étiquette automatique n’a été préconfigurée dans notre locataire. Pour créer une nouvelle stratégie d’étiquette automatique, sélectionnez **Créer une stratégie d’étiquette automatique**.  Ici, vous allez suivre les étapes de création d’une nouvelle stratégie.
    1. Vous commencez par choisir les informations auxquelles vous souhaitez appliquer cette étiquette.  Notez les options disponibles.  Sélectionnez **Médical et santé**, puis sélectionnez l’un des modèles disponibles.  Cliquez sur **Suivant**.
    1. Vous pouvez nommer votre stratégie d’étiquette automatique ou utiliser le nom par défaut.  Cliquez sur **Suivant**.
    1. Vous pouvez attribuer les unités d’administration auxquelles cette stratégie s’applique.  Laissez la valeur par défaut sur Répertoire complet et sélectionnez **Suivant**.
    1. Notez les emplacements disponibles où vous souhaitez appliquer l’étiquette.  Conservez les valeurs par défaut, puis sélectionnez **Suivant**.
    1. Vous pouvez configurer des règles communes ou avancées qui définissent le contenu auquel l’étiquette s’applique.  Laissez la valeur par défaut sur Règles communes et sélectionnez **Suivant**.
    1. Vous pouvez définir des règles pour le contenu dans tous les emplacements.  L’étiquette sera appliquée au contenu qui correspond aux règles définies sur cette page.  Pour le modèle que vous avez sélectionné, vous devriez voir un élément de ligne. Développez-le pour afficher les conditions qui s’appliquent.  Laissez tous les paramètres par défaut et sélectionnez **Suivant**.
    1. Choisissez une étiquette à appliquer automatiquement en sélectionnant **Choisir une étiquette**.  Choisissez une étiquette, puis sélectionnez **Ajouter**. Cliquez sur **Suivant**.
    1. Des paramètres supplémentaires peuvent être configurés pour la messagerie. Conservez les valeurs par défaut, puis sélectionnez **Suivant**.
    1. Vous pouvez décider de tester la stratégie maintenant ou ultérieurement.  Sélectionnez **Laisser la stratégie désactivée**, puis sélectionnez **Suivant**.
    1. Passez en revue les paramètres et sélectionnez **Créer une stratégie**, puis sélectionnez **Terminé**.

1. Dans le volet de navigation de gauche, sélectionnez **Accueil** pour revenir au portail de conformité Microsoft Purview.

1. Laissez cette page ouverte, vous en avez besoin pour la tâche suivante.

### Tâche 2

Dans cette tâche, vous allez suivre le processus d’application d’une étiquette de confidentialité à un document Microsoft Word, puis afficher le marquage du contenu (filigrane) généré par l’étiquette. REMARQUE : Lorsque vous utilisez Microsoft Word en ligne, il se peut que vous rencontriez un délai avant que l’option de sélection des étiquettes de confidentialité n’apparaisse sur le ruban supérieur.  Il est recommandé d’effectuer tous les labos restants, puis de revenir à cette tâche.

1. Dans la page d’accueil du portail de conformité Microsoft Purview, sélectionnez l’icône **Lanceur d’application**, à côté de l’indication Contoso Electronics. Sélectionnez l’**icône Word**.  

1. Sous Créer, sélectionnez **Document vide**, puis entrez du texte sur la page.  En haut de la page, dans la barre bleue, sélectionnez la flèche vers le bas à côté de Document - Enregistré et, dans la zone du nom du fichier, entrez **Test-label** et appuyez sur **Entrer** sur votre clavier.

1. À l’extrême droite de la barre de menus supérieure (également appelée ruban), vous trouverez une flèche vers le bas. Sélectionnez-la, puis **Ruban classique**.  Cela facilite l’identification de l’icône de confidentialité. Sélectionnez **Sensibilité** en regard de l’icône du micro. À partir du menu déroulant, sélectionnez **Confidentiel – Finance**.  

1. Dans la barre de menu supérieure, sélectionnez **Affichage**, puis **Mode lecture**.

1. Remarquez que le document comporte le filigrane CONFIDENTIEL DONNÉES FINANCIÈRES.  

1. Fermez les onglets Microsoft Word ouverts dans votre navigateur pour quitter Word, mais gardez l’onglet de la page d’accueil Microsoft Purview ouvert.

### Révision

Dans ce labo, vous explorez les fonctionnalités des étiquettes de confidentialité.  Vous allez passer en revue les paramètres des étiquettes de confidentialité existantes qui ont déjà été créées et la stratégie correspondante pour publier l’étiquette.   Vous verrez ensuite comment appliquer une étiquette.
