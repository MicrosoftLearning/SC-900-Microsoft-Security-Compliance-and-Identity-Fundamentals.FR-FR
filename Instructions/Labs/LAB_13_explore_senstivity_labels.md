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

Dans ce labo, vous explorez les fonctionnalités des étiquettes de confidentialité.  Vous passez en revue les paramètres des étiquettes de confidentialité existantes et la stratégie correspondante pour publier l’étiquette. Ensuite, vous voyez comment appliquer une étiquette et observez son impact du point de vue de l’utilisateur.

**Durée estimée** : 45 minutes

### Tâche 1

Dans cette tâche, vous comprendrez le rôle des étiquettes de confidentialité en créant une étiquette et en élaborant une stratégie pour la publier.

1. Ouvrez l’onglet du navigateur menant sur la page d’accueil de Microsoft Purview.  Si vous l’avez précédemment fermé, ouvrez un onglet du navigateur et entrez **`https://admin.microsoft.com`** . Connectez-vous avec les identifiants d’administration du tenant (ou « locataire/abonné ») Microsoft 365 fournis par l’hôte de labo autorisé (ALH).

1. Dans le volet de navigation de gauche du centre d’administration Microsoft 365, sélectionnez **Tout afficher**, puis **Microsoft Purview**.  Une nouvelle page de navigateur s’ouvre sur la page d’accueil du portail Microsoft Purview.

1. Dans le volet de navigation de gauche, sélectionnez **Solutions**, puis sélectionnez **Protection des données**.  Vous arrivez alors à la page de présentation. Faites défiler vers le bas pour afficher les informations disponibles.

1. Dans le volet de navigation de gauche, sélectionnez **Étiquettes de confidentialité**.
1. Vous voyez une bannière jaune indiquant que votre organisation n’a pas activé la capacité à traiter du contenu dans des fichiers Office en ligne qui disposent d’étiquettes de confidentialité chiffrées appliquées et qui sont enregistrées dans OneDrive et SharePoint.  Sélectionnez **Activer maintenant**.

1. Certaines étiquettes ont été préconfigurées dans votre locataire de labo Microsoft 365, pour votre commodité. Développez l’étiquette nommée **Hautement confidentiel**, puis choisissez **Tous les employés**.  Une fenêtre s’ouvre et fournit des informations sur cette étiquette.  Notez les paramètres de cette étiquette.  Sélectionnez **Modifier l’étiquette**. Si vous ne voyez pas cette option, sélectionnez les points de suspension.
    1. La configuration commence par des détails de base pour l’étiquette.  Ne changez rien.  Sélectionnez **Suivant** au bas de la page.
    1. Vérifiez l’étendue de cette étiquette. Ne changez rien.  Sélectionnez **Suivant** au bas de la page.
    1. L’écran suivant vous permet de choisir les paramètres de protection des éléments étiquetés. Cette étiquette définit qui peut accéder aux éléments étiquetés et les consulter, et applique également un marquage de contenu.  Sélectionnez **Suivant** pour afficher les détails.
        1. Contrôle d’accès : Passez en revue les paramètres, sans rien modifier.  Cliquez sur **Suivant**.
        1. Marquage du contenu : Notez que l’étiquette applique un pied de page.  Sélectionnez ensuite **Suivant**.
        1. Étiquetage automatique pour les fichiers et les e-mails : Lisez la description de l’étiquetage automatique en haut de la page ainsi que la zone d’informations en dessous.  Notez également que cette étiquette est définie pour l’étiquetage automatique lorsque des numéros de carte de crédit sont détectés. Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.
    1. Définition des paramètres de protection pour les groupes et les sites : Passez en revue les options pour les paramètres de protection et les paramètres d’application automatique.  Aucune configuration n’est présente dans cette fenêtre.  Ne changez rien. Sélectionnez **Suivant** au bas de la page.
    1. Vérification des paramètres et finalisation : Passez vos paramètres en revue.  Aucune modification n’ayant été faite, sélectionnez **Annuler**.

1. Dans le panneau de navigation de gauche, développez **Stratégies**, puis **Publication de stratégies des étiquettes**.  C’est par le biais des stratégies des étiquettes que les étiquettes de confidentialité peuvent être publiées.  Le tenant Microsoft 365 a été configuré avec certaines stratégies d’étiquette, pour votre commodité. Sélectionnez **Stratégie hautement confidentielle**.  Une fenêtre s’ouvre et fournit des informations sur la stratégie. Sélectionnez **Modifier la stratégie** la stratégie en haut de la fenêtre.  Ici, parcourez les paramètres sans rien changer.
    1. Choix des étiquettes de niveau de confidentialité à publier :  Notez les étiquettes répertoriées.  Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.
    1. Attribution des unités administratives : Les unités d’administration sont définies sur le répertoire complet, ne modifiez aucun paramètre. Cliquez sur **Suivant**.  
    1. Publication auprès des utilisateurs et groupes :  Notez que cette étiquette est disponible pour tous les utilisateurs.  Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.
    1. Paramètres de stratégie : Notez les options disponibles. Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.
    1. Paramètres par défaut pour les documents : Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.
    1. Paramètres par défaut pour les e-mails : Passez en revue les options et notez que les e-mails peuvent hériter de l’étiquette d’une pièce jointe prioritaire, si cette option est configurée. Cliquez sur **Suivant**.
    1. Paramètres par défaut pour les réunions et événements de calendrier : Passez en revue les options et notez la possibilité d'appliquer l'héritage entre les réunions Teams et les artefacts. Ne modifiez pas les paramètres.  Cliquez sur **Suivant**.
    1. Paramètres par défaut pour le contenu Fabric et Power BI : Ne modifiez pas les paramètres.  Cliquez sur **Suivant**.
    1. Nommage de votre stratégie : Vous êtes en mode édition ; le champ du nom est donc verrouillé (grisé).  Sélectionnez **Suivant**.
    1. Vérification et finalisation : Aucune modification n’étant intervenue, sélectionnez **Annuler**.

1. Depuis le volet de navigation de gauche, dans Protection des données, sélectionnez **Stratégies d’étiquetage automatique**. Passez en revue la description. Notez que vous créez des stratégies d’étiquette automatique pour appliquer automatiquement des étiquettes de confidentialité aux messages électroniques ou aux fichiers OneDrive et SharePoint qui contiennent des informations confidentielles. Aucune stratégie d’étiquette automatique n’a été préconfigurée dans notre locataire. Pour créer une nouvelle stratégie d’étiquette automatique, sélectionnez **Créer une stratégie d’étiquette automatique**.  Vous trouverez ici les étapes à suivre pour créer une nouvelle politique.
    1. Vous commencez par choisir les informations auxquelles vous souhaitez appliquer cette étiquette.  Notez les options disponibles.  Sélectionnez **Médical et Santé**, puis sélectionnez l’une des réglementations disponibles qui serviront de modèle.  Cliquez sur **Suivant**.
    1. Vous pouvez nommer votre stratégie d’étiquette automatique ou utiliser le nom par défaut.  Cliquez sur **Suivant**.
    1. Ensuite, vous choisissez une étiquette à appliquer automatiquement.  Sélectionnez **+ Choisir une étiquette**.  Sélectionnez une étiquette dans la liste, puis sélectionnez **Ajouter**.
    1. Vous pouvez attribuer les unités d’administration auxquelles cette stratégie s’applique.  Laissez la valeur par défaut sur Répertoire complet et sélectionnez **Suivant**.
    1. Choisissez les emplacements où vous souhaitez appliquer l'étiquette.  Vérifiez les informations fournies et les emplacements disponibles que vous pouvez sélectionner. Pour cet exercice, cochez la case à côté de **Échanger e-mail** puis sélectionnez **Suivant**.
    1. Vous pouvez configurer des règles communes ou avancées qui définissent le contenu auquel l’étiquette s’applique.  Laissez la valeur par défaut sur Règles communes et sélectionnez **Suivant**.
    1. Vous pouvez définir des règles pour le contenu dans tous les emplacements.  L’étiquette sera appliquée au contenu qui correspond aux règles définies sur cette page.  Pour le modèle que vous avez sélectionné, vous devriez voir un élément de ligne. Développez-le pour afficher les conditions qui s’appliquent.  Laissez tous les paramètres par défaut et sélectionnez **Suivant**.
    1. Des paramètres supplémentaires peuvent être configurés pour la messagerie. Conservez les valeurs par défaut, puis sélectionnez **Suivant**.
    1. Vous pouvez décider de tester la stratégie maintenant ou ultérieurement.  Sélectionnez **Laisser la stratégie désactivée**, puis sélectionnez **Suivant**.
    1. Passez en revue les paramètres. Dans le cadre de cet exercice, vous pouvez annuler sans créer la politique. Sélectionnez **Annuler**.

1. Dans le volet de navigation de gauche, sélectionnez **Accueil** pour revenir au portail Microsoft Purview.

1. Laissez cette page ouverte, vous en avez besoin pour la tâche suivante.

### Tâche 2

Dans cette tâche, vous allez suivre le processus d'application d'une étiquette de sensibilité à un document Microsoft Word, puis afficher le marquage de contenu (pied de page) généré par l'étiquette. REMARQUE : Lorsque vous utilisez Microsoft Word en ligne, il se peut que vous rencontriez un délai avant que l’option de sélection des étiquettes de confidentialité n’apparaisse sur le ruban supérieur.  Il est recommandé d’effectuer tous les labos restants, puis de revenir à cette tâche.

1. Vous devriez encore être sur la page d’accueil du portail Microsoft Purview. 
1. Dans le portail Microsoft Purview, sélectionnez **l’icône du lanceur d’applications**, à côté du texte Microsoft Purview. Sélectionnez l’**icône Word**.  

1. Sous Créer, sélectionnez **Document vide**, puis entrez du texte sur la page.  En haut de la page, en regard de l’icône Word, sélectionnez **Document** et attribuez le nom **Test-label** au fichier, puis appuyez sur **Entrer** sur votre clavier.

1. À l’extrême droite de la barre de menus supérieure (également appelée ruban), vous trouverez une flèche vers le bas. Sélectionnez-la, puis **Ruban classique**.  Cela facilite l’identification de l’icône de confidentialité. Sélectionnez **Sensibilité** en regard de l’icône du micro. Dans le menu déroulant, sélectionnez **Hautement confidentiel** puis **Tous les employés**.  

1. Dans la barre de menu supérieure, sélectionnez **Affichage**, puis **Mode lecture**.

1. Notez que le document comporte désormais le pied de page « Classé Hautement confidentiel ».  

1. Fermez les onglets Microsoft Word ouverts dans votre navigateur pour quitter Word, mais gardez l’onglet de la page d’accueil Microsoft Purview ouvert.

### Révision

Dans ce laboratoire, vous avez exploré les capacités des étiquettes de sensibilité.  Vous avez exploré les paramètres d'une étiquette de sensibilité existante et la politique correspondante pour publier l'étiquette.  Vous avez appliqué l'étiquette et, comme celle-ci comportait des marquages de contenu, vous avez pu voir ce marquage dans le document auquel vous avez appliqué l'étiquette.
