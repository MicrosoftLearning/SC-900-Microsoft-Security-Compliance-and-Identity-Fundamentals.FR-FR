<!---
---
Démonstration : Titre : « Étiquettes de confidentialité dans Microsoft Purview » Parcours d’apprentissage/Module/Unité : « Parcours d’apprentissage : Décrire les fonctionnalités des solutions de conformité Microsoft ; Module 3 : Décrire les fonctionnalités de protection des informations, de gestion du cycle de vie des données et de gouvernance des données dans Microsoft Purview ; Unité 4 : Décrire les étiquettes de confidentialité »
---
--->

# Démonstration : Étiquettes de confidentialité dans Microsoft Purview

Cette démonstration correspond au contenu Learn suivant :

- Parcours d’apprentissage : Décrire les fonctionnalités des solutions de conformité Microsoft
- Module : Décrire les fonctionnalités de protection des informations, de gestion de cycle de vie des données et de gouvernance des données dans Microsoft Purview
- Unité : Décrire les étiquettes de confidentialité

## Scénario de la démonstration

Dans cette démo, vous présentez les fonctionnalités des étiquettes de confidentialité.  Vous passez en revue les paramètres des étiquettes de confidentialité existantes et la stratégie correspondante pour publier l’étiquette.   Ensuite, vous voyez comment appliquer une étiquette et observez son impact du point de vue de l’utilisateur.  **REMARQUE** : La première fois que vous utilisez Word en ligne avec votre locataire Microsoft 365, l’option Sensibilité peut apparaître sur le ruban au bout de 15 minutes.  Les présentateurs doivent exécuter la partie 2 de la démonstration avant la classe afin que le délai soit suffisant pour que l’option s’affiche.

### Partie 1 de la démonstration

Dans cette démonstration, vous présentez les paramètres d’une étiquette de confidentialité existante et la stratégie correspondante pour la publier.

1. Ouvrez l’onglet du navigateur pour la page d’accueil de Microsoft Purview.  Si vous l’avez précédemment fermé, ouvrez un onglet du navigateur et entrez **https://admin.microsoft.com** . Connectez-vous avec les identifiants d’administration du locataire Microsoft 365 fournis par l’hôte de labo autorisé (ALH). Dans le volet de navigation gauche du centre d’administration Microsoft 365, sélectionnez **Tout afficher**, puis **Conformité**.  Le navigateur ouvre une nouvelle page. Il s’agit de la page d’accueil du portail de conformité Microsoft Purview.  

1. Dans le volet de navigation de gauche, sous Solutions, développez **Protection des informations**, puis sélectionnez **Vue d’ensemble**.  La page de présentation contient des informations sur les principales étiquettes de confidentialité appliquées au contenu, les principales activités détectées, les emplacements où les étiquettes de confidentialité sont appliquées, etc.  
    1. Sur la page de présentation, vous pouvez voir une boîte d’information jaune indiquant que votre organisation n’a pas activé la possibilité de traiter le contenu des fichiers Office en ligne auxquels des étiquettes de confidentialité chiffrées ont été appliquées et qui sont stockés dans OneDrive et SharePoint.  Sélectionnez **Activer maintenant**.  Une fois activé, il peut y avoir un délai avant que le paramètre ne soit propagé à travers le système.

1. Dans le volet de navigation de gauche, sélectionnez **Étiquettes**.

1. Certaines étiquettes ont été préconfigurées dans votre locataire de labo Microsoft 365, pour votre commodité. Développez l’étiquette **Hautement confidentielle** en sélectionnant le **>** , puis sélectionnez **Tous les employés**.  Une fenêtre avec des informations à propos de cette étiquette s’ouvre.  Remarquez comment cette étiquette est définie pour prendre en charge le chiffrement et le marquage de contenu.  Sélectionnez l’**icône de crayon** en haut de la page pour afficher certains des paramètres de base. Si vous ne voyez pas l’icône de crayon, sélectionnez les points de suspension.
    1. Vous commencez la configuration en fournissant un nom et une description pour votre étiquette.  Ne changez rien.  Sélectionnez **Suivant** au bas de la page.
    1. Notez l’étendue de cette étiquette.  L’étendue est définie sur Fichiers & E-mails.  Ne changez rien.  Sélectionnez **Suivant** au bas de la page.
    1. L’écran suivant vous permet de choisir les paramètres de protection des éléments étiquetés. Notez que cette étiquette est configurée pour prendre en charge le chiffrement et le marquage du contenu. Ne changez rien.  Sélectionnez **Suivant** au bas de la page.
        1. La fenêtre de chiffrement affiche la configuration pour les paramètres de chiffrement. Passez en revue les paramètres actuels, mais ne modifiez rien. Notez comment l’accès utilisateur au contenu est défini pour ne jamais expirer.  Vous pouvez aussi attribuer des autorisations à des utilisateurs et groupes spécifiques afin qu’ils puissent interagir avec le contenu auquel cette étiquette est appliquée.  Le locataire est défini sous Utilisateurs et groupes. Ainsi, tous les utilisateurs de votre locataire peuvent afficher le contenu qui dispose de cette étiquette.  L’équipe responsable des finances apparaît également et ses membres disposent d’autorisations pour co-éditer.  Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.
        1. Sur la page de marquage de contenu, remarquez la zone d’informations en haut de l’écran.  Les marquages de contenu seront appliqués aux documents, mais uniquement les en-têtes et les pieds de page seront appliqués aux e-mails. En d’autres termes, les filigranes ne sont pas appliqués aux e-mails.  Le marquage de contenu associé à cette étiquette est un filigrane.  Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.
    1. Vous êtes à présent dans la fenêtre d’étiquetage automatique pour les fichiers et les e-mails.  Lisez la description de l’étiquetage automatique en haut de la page ainsi que la zone d’informations en dessous.  Notez également que cette étiquette est définie pour l’étiquetage automatique sous certaines conditions. Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.
    1. La prochaine fenêtre définit les paramètres de protection pour les équipes, les groupes et les sites pour lesquels cette étiquette est appliquée. Ce n’est pas activé, sélectionnez **Suivant** au bas de la page.
    1. La fenêtre suivante est une fonctionnalité d’évaluation qui permet d’appliquer automatiquement cette étiquette aux ressources de données schématisées dans Mappage de données Microsoft Purview (telles que SQL, Synapse, etc.) qui contiennent les types d’informations sensibles que vous avez choisis.  La fonctionnalité n’est pas activée. Sélectionnez **Annuler** en bas de la page pour quitter l’assistant de configuration de l’étiquette et retourner à la page de protection des données.

1. Dans le volet de navigation de gauche, sélectionnez **Stratégies d’étiquette**.  C’est au travers des stratégies d’étiquettes que les étiquettes de confidentialité peuvent être publiées.  Le locataire Microsoft 365 a été configuré avec certaines stratégies d’étiquette, pour votre commodité.

1. Dans ce cas, sélectionnez **Stratégie d’étiquette de confidentialité globale**.  Une fenêtre avec des informations à propos de la stratégie s’ouvre.  Notez la description, cette stratégie d’étiquette a été configurée pour servir de stratégie d’étiquette de confidentialité par défaut pour tous les utilisateurs et groupes. Cette stratégie permet de publier la plupart des étiquettes qui ont été préconfigurées pour ce locataire lab Microsoft 365 et qui sont listées sous l’onglet Étiquettes.

1. Sélectionnez **Modifier la stratégie** la stratégie en haut de la fenêtre.
    1. Lisez la description sous « Choisir les étiquettes de confidentialité à publier ».  Notez les étiquettes répertoriées.  Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.
    1. La page suivante est un aperçu de l’attribution des unités d’administration. Sélectionnez **Suivant**.
    1. Lisez la description sous « Publier aux utilisateurs et groupes ».  Notez que cette étiquette est disponible pour tous les utilisateurs.  Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.
    1. Passez en revue les paramètres de stratégie.  Sélectionnez **Suivant** au bas de la page.
    1. Lisez la description sous « Appliquer une étiquette par défaut aux documents ». Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.
    1. Lisez la description sous « Appliquer une étiquette par défaut aux e-mails ». Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.
    1. Lisez la description sous « Paramètres par défaut pour les réunions et les événements de calendrier ». Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.
    1. Lisez la description sous « Appliquer une étiquette par défaut au contenu Power BI ». Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.
    1. La dernière option de configuration consiste à nommer votre stratégie.  Comme vous modifiez la stratégie, le champ de nom est grisé. Sélectionnez **Suivant** en bas de la page.
    1. Passez en revue les paramètres de stratégie. Étant donné que rien n’a été modifié, sélectionnez **Annuler** pour revenir à la page Stratégies d’étiquette.

1. Depuis la page de protection des données, sélectionnez l’étiquetage automatique. Passez en revue la description. Notez que vous créez des stratégies d’étiquette automatique pour appliquer automatiquement des étiquettes de confidentialité aux messages électroniques ou aux fichiers OneDrive et SharePoint qui contiennent des informations confidentielles. Si des stratégies d’étiquetage automatique sont configurées, sélectionnez-en une et passez en revue les informations de stratégie dans le volet d’informations.  Si aucune stratégie n’est répertoriée, vous pouvez choisir de parcourir les étapes pour en créer une, si le temps le permet.

1. Dans le volet de navigation de gauche, sélectionnez Accueil pour revenir au portail de conformité Microsoft Purview.

1. Laissez cet onglet de navigateur ouvert.

### Partie 2 de la démonstration

Dans cette étape, vous présentez le processus d’application d’une étiquette du point de vue de l’utilisateur (dans notre exemple, l’utilisateur est l’administrateur).  Pour voir l’impact de l’application de l’étiquette, vous sélectionnez l’étiquette Confidentiel - Finance, car elle applique un filigrane.

1. Dans la page d’accueil du portail de conformité Microsoft Purview, sélectionnez l’icône **Lanceur d’application**, à côté de l’indication Contoso Electronics. Sélectionnez l’**icône Word**.  

1. Sélectionnez **Document vierge**, puis saisissez du texte sur la page.  Dans la barre bleue en haut de la page, sélectionnez la flèche vers le bas à côté de Document - Enregistré et, dans la zone du nom du fichier, entrez **Test-label** et appuyez sur la touche **Entrer** de votre clavier.

1. Dans la barre de menus en haut, sélectionnez l’**icône de confidentialité** (icône à droite de l’icône de micro). Si vous ne voyez pas immédiatement cette option, actualisez la page. Dans le menu déroulant, sélectionnez **Confidentiel - Finance**.   REMARQUE : si vous ne voyez pas immédiatement l’option Sensibilité, actualisez la page, mais comme il s’agit d’un environnement locataire de labo, les délais peuvent être plus longs que la normale (10 à 15 minutes).
1. 
1. Dans la barre de menu supérieure, sélectionnez **Affichage**, puis sélectionnez **Mode lecture**.

1. Notez comment le document inclut le filigrane.  

1. Fermez les onglets Microsoft Word qui sont ouverts dans votre navigateur pour quitter Word.

1. Conservez l’onglet du navigateur Microsoft Purview ouvert pour la prochaine démonstration.

### Partie 3 de la démonstration (facultative)

Souvenez-vous, dans la première partie de la démo, l’étiquette Confidentiel - Finance est configurée pour le chiffrement. Selon les autorisations configurées avec cette étiquette, les utilisateurs du locataire Contoso ont des autorisations de lecture pour n’importe quel document/e-mail qui a l’étiquette.  Dans cette section, vous envoyez le document que vous avez créé précédemment, qui comprend l’étiquette Confidentiel - Finance, à une adresse e-mail à laquelle vous avez accès (une adresse e-mail personnelle ou votre e-mail Microsoft) et qui ne fait PAS partie du domaine WWLxZZZZ.OnMicrosoft.com.  

1. Dans la page d’accueil du portail de conformité Microsoft Purview, sélectionnez l’icône **Lanceur d’application**, à côté de l’indication Contoso Electronics. Sélectionnez l’**icône Outlook**

1. Sélectionnez **Nouveau message** en haut à gauche de l’écran.  Saisissez une adresse e-mail à laquelle vous avez accès et qui ne fait pas partie du domaine WWLxZZZZ.OnMicrosoft.com et saisissez **Test** dans la ligne d’objet.

1. Dans le ruban supérieur, sélectionnez l’icône de trombone, puis, dans la liste déroulante, sous Fichiers suggérés, sélectionnez le document que vous avez créé à l’étape précédente, **Étiquette de test** pour le joindre à l’e-mail.

1. Appuyez sur **Envoyer** pour envoyer l’e-mail.

1. Consultez l’adresse e-mail à laquelle vous avez envoyé le document.  Notez que l’e-mail peut être envoyé directement dans votre dossier Courrier indésirable.  L’e-mail est envoyé, mais quand vous essayez d’ouvrir le fichier Word joint, qui a été étiqueté à l’origine comme Confidentiel - Finance, vous voyez une notification indiquant que vous n’avez pas l’autorisation d’ouvrir le document.

1. Fermez Outlook.

1. Conservez l’onglet du navigateur Microsoft Purview ouvert pour la prochaine démonstration.


### Révision

Dans cette démonstration, vous avez montré les paramètres qui peuvent être configurés pour les étiquettes de confidentialité et les paramètres des stratégies pour publier des étiquettes de confidentialité. Vous avez également présenté comment appliquer une étiquette et l’effet de celle-ci, depuis la perspective d’un utilisateur.

