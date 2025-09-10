<!---
---
Démonstration : Titre : « Étiquettes de confidentialité dans Microsoft Purview » Parcours d’apprentissage/module/unité : « Parcours d’apprentissage : décrire les fonctionnalités de Microsoft Priva et de Microsoft Purview ; Module 2 : décrire les solutions de sécurité des données de Microsoft Purview ; Unité 4 : décrire les étiquettes et les stratégies de confidentialité dans Microsoft Purview Information Protection »
---
--->

# Démo : Étiquettes de confidentialité dans Microsoft Purview

Cette démonstration correspond au contenu Learn suivant :

- Parcours d’apprentissage : décrire les fonctionnalités de Microsoft Priva et Microsoft Purview
- Module : décrire les solutions de sécurité des données de Microsoft Purview
- Unité : décrire les étiquettes et les stratégies de confidentialité dans Microsoft Purview Information Protection

## Scénario de démonstration

Dans cette démo, vous présentez les fonctionnalités des étiquettes de confidentialité.  Vous passez en revue les paramètres des étiquettes de confidentialité existantes et la stratégie correspondante pour publier l’étiquette.   Ensuite, vous voyez comment appliquer une étiquette et observez son impact du point de vue de l’utilisateur.  **REMARQUE** : la première fois que vous utilisez Word en ligne avec votre locataire Microsoft 365, l’option Sensibilité peut apparaître sur le ruban au bout de 15 minutes.  Les présentateurs doivent exécuter la partie 2 de la démonstration avant la classe afin que le délai soit suffisant pour que l’option s’affiche.

### Partie 1 de la démonstration

Dans cette démonstration, vous présentez les paramètres d’une étiquette de confidentialité existante et la stratégie correspondante pour la publier.

1. Normalement, vous vous trouvez toujours sur la page d’accueil du portail Microsoft Purview. Dans le cas contraire, ouvrez un nouvel onglet dans le navigateur Microsoft Edge. Dans la barre d’adresse, saisissez **https://purview.microsoft.com**, puis cliquez sur **Prise en main**.  

1. Depuis la page d’arrivée du nouveau portail Microsoft Purview, sélectionnez la vignette **Afficher toutes les solutions**, puis la vignette **Protection des données**. Vous pouvez également sélectionner **Solutions** dans le volet de navigation de gauche, puis **Information Protection**.

1. Vous accédez alors à la page Vue d’ensemble. Dans le volet de navigation de gauche, sélectionnez **Étiquettes de confidentialité**. Si une bannière jaune s’affiche, indiquant que votre organisation n’a pas activé la possibilité de traiter le contenu des fichiers Office en ligne protégés par des étiquettes de confidentialité chiffrées et stockées dans OneDrive ou SharePoint,  sélectionnez **Activer maintenant**.

1. Certaines étiquettes ont été préconfigurées dans votre locataire de labo Microsoft 365, pour votre commodité. Développez l’étiquette nommée **Hautement confidentiel**, puis choisissez **Tous les employés**.  Une fenêtre s’ouvre et fournit des informations sur cette étiquette.  Notez les paramètres de cette étiquette.  Sélectionnez **Modifier l’étiquette**. Si vous ne voyez pas cette option, sélectionnez les points de suspension.
    1. La configuration commence par des détails de base pour l’étiquette.  Ne changez rien.  Sélectionnez **Suivant** au bas de la page.
    1. Vérifiez l’étendue de cette étiquette. Ne changez rien.  Sélectionnez **Suivant** au bas de la page.
    1. L’écran suivant vous permet de choisir les paramètres de protection des éléments étiquetés. Cette étiquette définit qui peut accéder aux éléments étiquetés et les consulter, et applique également un marquage de contenu.  Sélectionnez **Suivant** pour afficher les détails.
        1. Contrôle d’accès : passez en revue les paramètres, sans rien modifier.  Cliquez sur **Suivant**.
        1. Marquage du contenu : Notez que l’étiquette applique un pied de page.  Sélectionnez ensuite **Suivant**.
        1. Étiquetage automatique pour les fichiers et les e-mails : Lisez la description de l’étiquetage automatique en haut de la page ainsi que la zone d’informations en dessous.  Notez également que cette étiquette est définie pour l’étiquetage automatique lorsque des numéros de carte de crédit sont détectés. Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.
    1. Définition des paramètres de protection pour les groupes et les sites : Passez en revue les options pour les paramètres de protection et les paramètres d’application automatique.  Aucune configuration n’est présente dans cette fenêtre.  Ne changez rien. Sélectionnez **Suivant** au bas de la page.
    1. Vérification des paramètres et finalisation : Passez vos paramètres en revue.  Aucune modification n’ayant été faite, sélectionnez **Annuler**.

1. Dans le volet de navigation de gauche, développez **Stratégies**, puis **Publication de stratégies des étiquettes**.  C’est par le biais des stratégies des étiquettes que les étiquettes de confidentialité peuvent être publiées.  Le tenant Microsoft 365 a été configuré avec certaines stratégies d’étiquette, pour votre commodité. Sélectionnez **Stratégie hautement confidentielle**.  Une fenêtre s’ouvre et fournit des informations sur la stratégie. Sélectionnez **Modifier la stratégie** la stratégie en haut de la fenêtre.  Ici, parcourez les paramètres sans rien changer.
    1. Choix des étiquettes de niveau de confidentialité à publier :  Notez les étiquettes répertoriées.  Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.
    1. Attribution des unités administratives : Les unités d’administration sont définies sur le répertoire complet, ne modifiez aucun paramètre. Cliquez sur **Suivant**.  
    1. Publication auprès des utilisateurs et groupes :  Notez que cette étiquette est disponible pour tous les utilisateurs.  Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.
    1. Paramètres de stratégie : Notez les options disponibles. Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.
    1. Paramètres par défaut pour les documents : Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.
    1. Paramètres par défaut pour les e-mails : Passez en revue les options et notez que les e-mails peuvent hériter de l’étiquette d’une pièce jointe prioritaire, si cette option est configurée. Cliquez sur **Suivant**.
    1. Paramètres par défaut pour les réunions et événements de calendrier : Passez en revue les options et notez la possibilité d’hériter d’une étiquette entre une réunion d'équipe et ses éléments associés. Ne modifiez pas les paramètres.  Cliquez sur **Suivant**.
    1. Paramètres par défaut pour le contenu Fabric et Power BI : Ne modifiez pas les paramètres.  Cliquez sur **Suivant**.
    1. Nommage de votre stratégie : Vous êtes en mode édition ; le champ du nom est donc verrouillé (grisé).  Sélectionnez **Suivant**.
    1. Vérification et finalisation : Aucune modification n’étant intervenue, sélectionnez **Annuler**.

1. Depuis le volet de navigation à gauche, dans Protection des données, sélectionnez Étiquetage automatique. Passez en revue la description. Notez que vous créez des stratégies d’étiquetage automatique pour appliquer automatiquement des étiquettes de confidentialité aux messages électroniques ou aux fichiers OneDrive et SharePoint qui contiennent des informations sensibles. Si des stratégies d’étiquetage automatique sont configurées, sélectionnez-en une et passez en revue les informations de stratégie dans le volet d’informations.  Si aucune stratégie n’est répertoriée, vous pouvez choisir de parcourir les étapes pour en créer une, si le temps le permet.

1. Dans le volet de navigation de gauche, sélectionnez Accueil pour revenir au portail Microsoft Purview.

1. Gardez cet onglet de navigateur ouvert.

### Partie 2 de la démonstration

Dans cette étape, vous allez appliquer une étiquette de confidentialité à un document Microsoft Word, puis visualiser le marquage de contenu (pied de page) généré par cette étiquette. REMARQUE : Lorsque vous utilisez Microsoft Word en ligne, il se peut que vous rencontriez un délai avant que l’option de sélection des étiquettes de confidentialité n’apparaisse sur le ruban supérieur.  Il est recommandé d’effectuer tous les labos restants, puis de revenir à cette tâche.

1. Vous devriez encore être sur la page d’accueil du portail Microsoft Purview. 
1. Dans le portail Microsoft Purview, sélectionnez **l’icône du lanceur d’applications**, à côté du texte Microsoft Purview. Sélectionnez l’**icône Word**.  

1. Sous Créer, sélectionnez **Document vide**, puis entrez du texte sur la page.  En haut de la page, en regard de l’icône Word, sélectionnez **Document** et attribuez le nom **Test-label** au fichier, puis appuyez sur **Entrer** sur votre clavier.

1. À l’extrême droite de la barre de menus supérieure (également appelée ruban), vous trouverez une flèche vers le bas. Sélectionnez-la, puis **Ruban classique**.  Cela facilite l’identification de l’icône de confidentialité. Sélectionnez **Sensibilité** en regard de l’icône du micro. Dans le menu déroulant, sélectionnez **Hautement confidentiel** puis **Tous les employés**.  

1. Dans la barre de menu supérieure, sélectionnez **Affichage**, puis **Mode lecture**.

1. Notez que le document comporte désormais le pied de page « Classé Hautement confidentiel ».  

1. Fermez les onglets Microsoft Word ouverts dans votre navigateur pour quitter Word, mais gardez l’onglet de la page d’accueil Microsoft Purview ouvert.

### Révision

Dans cette démonstration, vous avez découvert comment afficher les paramètres qui peuvent être configurés pour les étiquettes de confidentialité et les paramètres des stratégies pour publier des étiquettes de confidentialité. Vous avez également montré comment appliquer une étiquette.
