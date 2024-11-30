---
lab:
  title: "Explorer les étiquettes de confidentialité dans Microsoft\_Purview"
  module: Describe the data security solutions of Microsoft Purview
---

# Labo : Explorer les étiquettes de confidentialité dans Microsoft Purview

Ce labo correspond au contenu Learn suivant :

- Parcours d’apprentissage : décrire les fonctionnalités de Microsoft Priva et Microsoft Purview
- Module : décrire les solutions de sécurité des données de Microsoft Purview
- Unité : décrire les étiquettes et les stratégies de confidentialité dans Microsoft Purview Information Protection

## Scénario du labo

Dans ce labo, vous explorez les fonctionnalités des étiquettes de confidentialité.  Vous passez en revue les paramètres des étiquettes de confidentialité existantes et la stratégie correspondante pour publier l’étiquette.   Ensuite, vous voyez comment appliquer une étiquette et observez son impact du point de vue de l’utilisateur.

**Durée estimée** : 45 minutes

### Tâche 1

Dans cette tâche, vous comprendrez le rôle des étiquettes de confidentialité en créant une étiquette et en élaborant une stratégie pour la publier.

1. Ouvrez l’onglet du navigateur menant sur la page d’accueil de Microsoft Purview.  Si vous l’avez précédemment fermé, ouvrez un onglet du navigateur et entrez **`https://admin.microsoft.com`** . Connectez-vous avec les identifiants d’administration du tenant (ou « locataire/abonné ») Microsoft 365 fournis par l’hôte de labo autorisé (ALH).

1. Dans le volet de navigation gauche du Centre d’administration Microsoft 365, sélectionnez **Tout afficher**, puis **Conformité**.  Une nouvelle page de navigateur s’ouvre sur la page d’accueil du portail Microsoft Purview.

1. Dans le volet de navigation de gauche, sélectionnez **Solutions**, puis sélectionnez **Protection des données**.  Vous arrivez alors à la page de présentation. Faites défiler vers le bas pour afficher les informations disponibles.

1. Dans le volet de navigation de gauche, sélectionnez **Étiquettes de confidentialité**.
1. Vous voyez une bannière jaune indiquant que votre organisation n’a pas activé la capacité à traiter du contenu dans des fichiers Office en ligne qui disposent d’étiquettes de confidentialité chiffrées appliquées et qui sont enregistrées dans OneDrive et SharePoint.  Sélectionnez **Activer maintenant**.

1. Certaines étiquettes ont été préconfigurées dans votre locataire de labo Microsoft 365, pour votre commodité. Sélectionnez l’étiquette nommée **Confidentiel - Finance**.  Une fenêtre s’ouvre et fournit des informations sur cette étiquette.  Notez les paramètres de cette étiquette.  Sélectionnez **Modifier l’étiquette**. Si vous ne voyez pas cette option, sélectionnez les points de suspension.
    1. La configuration commence par des détails de base pour l’étiquette.  Ne changez rien.  Sélectionnez **Suivant** au bas de la page.
    1. Vérifiez l’étendue de cette étiquette. Ne changez rien.  Sélectionnez **Suivant** au bas de la page.
    1. L’écran suivant vous permet de choisir les paramètres de protection des éléments étiquetés. Cette étiquette est configurée pour prendre en charge le marquage du contenu. Ne changez rien.  Sélectionnez **Suivant** au bas de la page.
        1. Sur la page de marquage du contenu, prenez note de l’encadré d’information situé en haut.  Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.
    1. Vous êtes à présent dans la fenêtre d’étiquetage automatique des fichiers et des e-mails.  Lisez la description de l’étiquetage automatique en haut de la page et l’encadré d’information en dessous.  Notez également que cette étiquette est configurée pour l’étiquetage automatique pour des conditions spécifiques. Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.
    1. Cette fenêtre définit les paramètres de protection des groupes et des sites qui ont cette étiquette. Si cette option n’est pas activée, sélectionnez **Suivant** en bas de la page.
    1. Cette fenêtre est une fonctionnalité d’évaluation qui permet d’appliquer automatiquement cette étiquette aux ressources de données schématisées dans Mappage de données Microsoft Purview (telles que SQL, Synapse, etc.) qui contiennent les types d’informations sensibles que vous avez choisis.  La fonctionnalité n’est pas activée. Sélectionnez **Annuler** en bas de la page pour quitter l’assistant Configuration de l’étiquette et revenir à la page Protection des données.

1. Dans le panneau de navigation de gauche, développez **Stratégies**, puis **Publication de stratégies**.  C’est par le biais des stratégies des étiquettes que les étiquettes de confidentialité peuvent être publiées.  Le tenant Microsoft 365 a été configuré avec certaines stratégies d’étiquette, pour votre commodité.

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

1. Dans le volet de navigation de gauche, sélectionnez **Accueil** pour revenir au portail Microsoft Purview.

1. Laissez cette page ouverte, vous en avez besoin pour la tâche suivante.

### Tâche 2

Dans cette tâche, vous allez suivre le processus d’application d’une étiquette de confidentialité à un document Microsoft Word, puis afficher le marquage du contenu (filigrane) généré par l’étiquette. REMARQUE : Lorsque vous utilisez Microsoft Word en ligne, il se peut que vous rencontriez un délai avant que l’option de sélection des étiquettes de confidentialité n’apparaisse sur le ruban supérieur.  Il est recommandé d’effectuer tous les labos restants, puis de revenir à cette tâche.

1. Vous devriez encore être sur la page d’accueil du portail Microsoft Purview. 
1. Dans le portail Microsoft Purview, sélectionnez **l’icône du lanceur d’applications**, à côté du texte Microsoft Purview. Sélectionnez l’**icône Word**.  

1. Sous Créer, sélectionnez **Document vide**, puis entrez du texte sur la page.  En haut de la page, en regard de l’icône Word, sélectionnez **Document** et attribuez le nom **Test-label** au fichier, puis appuyez sur **Entrer** sur votre clavier.

1. À l’extrême droite de la barre de menus supérieure (également appelée ruban), vous trouverez une flèche vers le bas. Sélectionnez-la, puis **Ruban classique**.  Cela facilite l’identification de l’icône de confidentialité. Sélectionnez **Sensibilité** en regard de l’icône du micro. À partir du menu déroulant, sélectionnez **Confidentiel – Finance**.  

1. Dans la barre de menu supérieure, sélectionnez **Affichage**, puis **Mode lecture**.

1. Remarquez que le document comporte le filigrane CONFIDENTIEL DONNÉES FINANCIÈRES.  

1. Fermez les onglets Microsoft Word ouverts dans votre navigateur pour quitter Word, mais gardez l’onglet de la page d’accueil Microsoft Purview ouvert.

### Révision

Dans ce labo, vous explorez les fonctionnalités des étiquettes de confidentialité.  Vous allez passer en revue les paramètres des étiquettes de confidentialité existantes qui ont déjà été créées et la stratégie correspondante pour publier l’étiquette.   Vous verrez ensuite comment appliquer une étiquette.
