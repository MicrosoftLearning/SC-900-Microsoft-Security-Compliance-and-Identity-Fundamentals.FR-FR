<!---
---
Labo : Titre : « Explorer les étiquettes de confidentialité dans Microsoft Purview » Parcours d’apprentissage/Module/Unité : « Parcours d’apprentissage : Décrire les fonctionnalités des solutions de conformité Microsoft ; Module 3 : Décrire la protection des informations et la gestion du cycle de vie des données dans Microsoft Purview ; Unité 4 : Décrire les étiquettes de confidentialité »
---
--->

# Labo : Explorer les étiquettes de confidentialité dans Microsoft Purview

Ce labo correspond au contenu Learn suivant :

- Parcours d’apprentissage : Décrire les fonctionnalités des solutions de conformité Microsoft
- Module : Décrire la protection des informations et la gestion de cycle de vie des données dans Microsoft Purview
- Unité : Décrire les étiquettes de confidentialité

## Scénario du labo

Dans ce labo, vous explorez les fonctionnalités des étiquettes de confidentialité.  Vous passez en revue les paramètres des étiquettes de confidentialité existantes et la stratégie correspondante pour publier l’étiquette.   Ensuite, vous voyez comment appliquer une étiquette et observez son impact du point de vue de l’utilisateur.

**Durée estimée** : 20-25 minutes

### Tâche 1

Dans cette tâche, vous comprenez ce que vous pouvez faire avec les étiquettes de confidentialité en passant en revue les paramètres d’une étiquette de confidentialité existante et la politique correspondante pour la publier.

1. Ouvrez l’onglet du navigateur pour la page d’accueil de Microsoft Purview.  Si vous l’avez précédemment fermé, ouvrez un onglet du navigateur et entrez **https://admin.microsoft.com** . Connectez-vous avec les identifiants d’administration du locataire Microsoft 365 fournis par l’hôte de labo autorisé (ALH). Dans le volet de navigation gauche du centre d’administration Microsoft 365, sélectionnez **Tout afficher**, puis **Conformité**.  Le navigateur ouvre une nouvelle page. Il s’agit de la page d’accueil du portail de conformité Microsoft Purview.   

1. Dans le volet de navigation de gauche, sous Solutions, développez **Protection des informations**, puis sélectionnez **Vue d’ensemble**. Notez l’avertissement en haut de la page et faites défiler vers le bas pour afficher les informations disponibles.
   1. Sur la page de présentation, vous pouvez voir une boîte d’information jaune indiquant que votre organisation n’a pas activé la possibilité de traiter le contenu des fichiers Office en ligne auxquels des étiquettes de confidentialité chiffrées ont été appliquées et qui sont stockés dans OneDrive et SharePoint.  Sélectionnez **Activer maintenant**.  Une fois cette opération effectuée, il peut y avoir un délai pour que le paramètre se propage dans le système et des étapes supplémentaires doivent être effectuées pour protéger Teams, les sites SharePoint et les groupes Microsoft 365.

1. Dans le volet de navigation de gauche, sélectionnez **Étiquettes**.
   1. Sur la page Étiquettes, vous pouvez voir une boîte d’information jaune indiquant que votre organisation n’a pas activé la possibilité de traiter le contenu des fichiers Office en ligne auxquels des étiquettes de confidentialité chiffrées ont été appliquées et qui sont stockés dans OneDrive et SharePoint.  Sélectionnez **Activer maintenant**.  Une fois cette opération effectuée, il peut y avoir un délai pour que le paramètre se propage dans le système et des étapes supplémentaires doivent être effectuées pour protéger Teams, les sites SharePoint et les groupes Microsoft 365.
1. Certaines étiquettes ont été préconfigurées dans votre locataire de labo Microsoft 365, pour votre commodité. Développez l’étiquette **Hautement confidentielle** en sélectionnant le **>** , puis sélectionnez **Tous les employés**.  Une fenêtre avec des informations à propos de cette étiquette s’ouvre.  Remarquez comment cette étiquette est définie pour prendre en charge le chiffrement et le marquage de contenu.  Sélectionnez l’**icône de crayon** en haut de la page pour afficher certains des paramètres de base. Si vous ne voyez pas l’icône de crayon, sélectionnez les points de suspension.
    1. Vous commencez la configuration en fournissant un nom et une description pour votre étiquette.  Ne changez rien.  Sélectionnez **Suivant** au bas de la page.
    1. Notez l’étendue de cette étiquette.  L’étendue est définie sur Fichiers & E-mails.  Ne changez rien.  Sélectionnez **Suivant** au bas de la page.
    1. L’écran suivant vous permet de choisir les paramètres de protection des éléments étiquetés. Notez que cette étiquette est configurée pour prendre en charge le chiffrement et le marquage du contenu. Ne changez rien.  Sélectionnez **Suivant** au bas de la page.
        1. La fenêtre de chiffrement affiche la configuration pour les paramètres de chiffrement. Passez en revue les paramètres actuels, mais ne modifiez rien. Notez que l’accès utilisateur au contenu est défini de manière à ne jamais expirer et à toujours permettre l’accès hors ligne.  Vous pouvez aussi attribuer des autorisations à des utilisateurs et groupes spécifiques afin qu’ils puissent interagir avec le contenu auquel cette étiquette est appliquée.  Le locataire est défini sous Utilisateurs et groupes. Ainsi, tous les utilisateurs de votre locataire peuvent afficher le contenu qui dispose de cette étiquette.  Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.
        1. Sur la page de marquage de contenu, remarquez la zone d’informations en haut de l’écran.  Les marquages de contenu seront appliqués aux documents, mais uniquement les en-têtes et les pieds de page seront appliqués aux e-mails. En d’autres termes, les filigranes ne sont pas appliqués aux e-mails.  Le marquage de contenu associé à cette étiquette est un pied de page.  Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.
    1. Vous êtes à présent dans la fenêtre d’étiquetage automatique pour les fichiers et les e-mails.  Lisez la description de l’étiquetage automatique en haut de la page ainsi que la zone d’informations en dessous.  Notez également que cette étiquette est définie pour l’étiquetage automatique sous certaines conditions. Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.
    1. La prochaine fenêtre définit les paramètres de protection pour les équipes, les groupes et les sites pour lesquels cette étiquette est appliquée. Ce n’est pas activé, sélectionnez **Suivant** au bas de la page.
    1. La fenêtre suivante est une fonctionnalité d’évaluation qui permet d’appliquer automatiquement cette étiquette aux ressources de données schématisées dans Mappage de données Microsoft Purview (telles que SQL, Synapse, etc.) qui contiennent les types d’informations sensibles que vous avez choisis.  La fonctionnalité n’est pas activée. Sélectionnez **Annuler** en bas de la page pour quitter l’assistant de configuration de l’étiquette et retourner à la page de protection des données.

1. Dans le volet de navigation de gauche, sélectionnez **Stratégies d’étiquette**.  C’est au travers des stratégies d’étiquettes que les étiquettes de confidentialité peuvent être publiées.  Le locataire Microsoft 365 a été configuré avec certaines stratégies d’étiquette, pour votre commodité.

1. Dans ce cas, sélectionnez **Stratégie d’étiquette de confidentialité globale**.  Une fenêtre avec des informations à propos de la stratégie s’ouvre.  Notez la description, cette stratégie d’étiquette a été configurée pour servir de stratégie d’étiquette de confidentialité par défaut pour tous les utilisateurs et groupes. Cette stratégie permet de publier la plupart des étiquettes qui ont été préconfigurées pour ce locataire lab Microsoft 365 et qui sont listées sous l’onglet Étiquettes.  

1. Sélectionnez **Modifier la stratégie** la stratégie en haut de la fenêtre.
    1. Passez en revue la description de « Choisir les étiquettes de confidentialité à publier ».  Notez les étiquettes répertoriées.  Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.
    1. Passez en revue la description de « Attribuer des unités d’administration ». Les unités d’administration sont définies sur le répertoire complet, ne modifiez aucun paramètre. Sélectionnez **Suivant**.  
    1. Passez en revue la description de « Publier pour les utilisateurs et les groupes ».  Notez que cette étiquette est disponible pour tous les utilisateurs.  Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.
    1. Passez en revue les paramètres de stratégie. Sélectionnez **Exiger que les utilisateurs appliquent une étiquette à leurs e-mails et à leurs documents** et examinez la description fournie. Sélectionnez **Suivant** au bas de la page.
    1. Passez en revue la description de « Appliquer une étiquette par défaut aux documents ». Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.
    1. Passez en revue la description de « Appliquer une étiquette par défaut aux e-mails » et de « Hériter de l’étiquette des pièces jointes ». Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.
    1. Passez en revue la description de « Appliquer une étiquette par défaut aux réunions et aux événements du calendrier ». Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.
    1. Passez en revue la description de « Appliquer une étiquette par défaut au contenu de Power BI ». Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.
    1. La dernière option de configuration consiste à nommer votre stratégie.  Comme vous modifiez la stratégie, le champ de nom est grisé. Sélectionnez **Suivant** en bas de la page.
    1. Passez en revue les paramètres de stratégie. Sélectionnez **Annuler** pour abandonner les modifications et revenir à la page Stratégies d’étiquette.

1. Depuis la page de protection des données, sélectionnez l’étiquetage automatique. Passez en revue la description. Notez que vous créez des stratégies d’étiquette automatique pour appliquer automatiquement des étiquettes de confidentialité aux messages électroniques ou aux fichiers OneDrive et SharePoint qui contiennent des informations confidentielles. Aucune stratégie d’étiquette automatique n’a été préconfigurée dans notre locataire. Pour créer une nouvelle stratégie d’étiquette automatique, sélectionnez **Créer une stratégie d’étiquette automatique**.  Ici, vous allez suivre les étapes de création d’une nouvelle stratégie.
    1. Vous commencez par choisir les informations auxquelles vous souhaitez appliquer cette étiquette.  Notez les options disponibles.  Sélectionnez **Médical et santé**, puis sélectionnez l’un des modèles disponibles.  Sélectionnez **Suivant**.
    1. Vous pouvez nommer votre stratégie d’étiquette automatique ou utiliser le nom par défaut.  Sélectionnez **Suivant**.
    1. Vous pouvez attribuer les unités d’administration auxquelles cette stratégie s’applique.  Laissez la valeur par défaut sur Répertoire complet et sélectionnez **Suivant**.
    1. Notez les emplacements disponibles où vous souhaitez appliquer l’étiquette.  Conservez les valeurs par défaut, puis sélectionnez **Suivant**.
    1. Vous pouvez configurer des règles communes ou avancées qui définissent le contenu auquel l’étiquette s’applique.  Laissez la valeur par défaut sur Règles communes et sélectionnez **Suivant**.
    1. Vous pouvez définir des règles pour le contenu dans tous les emplacements.  L’étiquette sera appliquée au contenu qui correspond aux règles définies sur cette page.  Pour le modèle que vous avez sélectionné, vous devriez voir un élément de ligne. Développez-le pour afficher les conditions qui s’appliquent.  Laissez tous les paramètres par défaut et sélectionnez **Suivant**.
    1. Choisissez une étiquette à appliquer automatiquement en sélectionnant **Choisir une étiquette**.  Choisissez une étiquette, puis sélectionnez **Ajouter**. Sélectionnez **Suivant**.
    1. Des paramètres supplémentaires peuvent être configurés pour la messagerie. Conservez les valeurs par défaut, puis sélectionnez **Suivant**.
    1. Vous pouvez décider de tester la stratégie maintenant ou ultérieurement.  Sélectionnez **Laisser la stratégie désactivée**, puis sélectionnez **Suivant**.
    1. Passez en revue les paramètres et sélectionnez **Créer une stratégie**, puis sélectionnez **Terminé**.

1. Dans le volet de navigation de gauche, sélectionnez **Accueil** pour revenir au portail de conformité Microsoft Purview.

1. Laissez cette page ouverte, vous en avez besoin pour la tâche suivante.

### Tâche 2

Dans cette tâche, vous allez suivre le processus d’application d’une étiquette de confidentialité à un document Microsoft Word, puis afficher le marquage du contenu (filigrane) généré par l’étiquette. REMARQUE : Lorsque vous utilisez Microsoft Word en ligne, il se peut que vous rencontriez un délai avant que l’option de sélection des étiquettes de confidentialité n’apparaisse sur le ruban supérieur.  Il est recommandé d’effectuer tous les labos restants, puis de revenir à cette tâche.

1. Dans la page d’accueil du portail de conformité Microsoft Purview, sélectionnez l’icône **Lanceur d’application**, à côté de l’indication Contoso Electronics. Sélectionnez l’**icône Word**.  

1. Sous Créer, sélectionnez **Document vide**, puis entrez du texte sur la page.  En haut de la page, dans la barre bleue, sélectionnez la flèche vers le bas à côté de Document - Enregistré et, dans la zone du nom du fichier, entrez **Test-label** et appuyez sur **Entrer** sur votre clavier.

1. Dans la barre de menus supérieure, sélectionnez **Icône de confidentialité**, l’icône à droite de l’icône du microphone (selon la taille de votre écran, vous devrez peut-être sélectionner les points de suspension, puis Confidentialité). Dans la liste déroulante, sélectionnez **Hautement confidentiel**, puis **Tous les employés**.  REMARQUE : Lorsque vous utilisez Microsoft Word en ligne, il se peut que vous rencontriez un délai avant que l’option de sélection des étiquettes de confidentialité n’apparaisse sur le ruban supérieur.  Il est recommandé d’effectuer tous les labos restants, puis de revenir à cette tâche.

1. Dans la barre de menu supérieure, sélectionnez **Affichage**, puis sélectionnez **Mode lecture**.

1. Notez que le document inclut le pied de page « Classé comme hautement confidentiel ».  

1. Fermez les onglets Microsoft Word qui sont ouverts dans votre navigateur pour quitter Word.

### Tâche 3 (facultative)

Rappelez-vous, dans la première partie de la version de démonstration, que l’étiquette Hautement confidentiel - Tous les employés est configurée pour le chiffrement. Selon les autorisations configurées avec cette étiquette, les utilisateurs du locataire Contoso ont des autorisations de lecture pour n’importe quel document/e-mail qui a l’étiquette.  Dans cette section, vous enverrez le document que vous avez créé précédemment, qui comprend l’étiquette Hautement confidentiel - Tous les employés, à une adresse e-mail à laquelle vous avez accès (une adresse e-mail personnelle ou votre adresse e-mail Microsoft) et qui ne fait PAS partie du domaine WWLxZZZZ.OnMicrosoft.com.  

1. Dans la page d’accueil du portail de conformité Microsoft Purview, sélectionnez l’icône **Lanceur d’application**, à côté de l’indication Contoso Electronics. Sélectionnez l’**icône Outlook**.

1. Sélectionnez **Nouveau message** en haut à gauche de l’écran.  Saisissez une adresse e-mail à laquelle vous avez accès et qui ne fait pas partie du domaine WWLxZZZZ.OnMicrosoft.com et saisissez **Test** dans la ligne d’objet.

1. Sélectionnez **Joindre** (icône en forme de trombone).

1. Sélectionnez **OneDrive**.

1. Vérifiez que l’onglet **Récent** dans le volet de navigation de gauche est sélectionné.  À partir de la liste qui apparaît, sélectionnez le document **Test-label.docx** que vous avez créé et auquel vous avez appliqué l’étiquette Hautement confidentiel - Tous les employés. Sélectionnez la flèche déroulante vers le bas **Partager le lien**, puis sélectionnez **Joindre**.  Appuyez sur **Envoyer**.

1. Consultez l’adresse e-mail à laquelle vous avez envoyé le document.  Remarque : il se peut que l’e-mail soit envoyé dans votre dossier de courrier indésirable.  L’e-mail est envoyé avec succès, mais lorsque vous essayez d'ouvrir le fichier Word joint, qui était à l’origine intitulé Hautement confidentiel - Tous les employés, vous voyez apparaître une notification indiquant que vous n’avez pas l’autorisation d’ouvrir le document.

1. Fermez Outlook, mais gardez l’onglet du navigateur sur la page d’accueil de Microsoft Purview ouvert.

### Révision

Dans ce labo, vous explorez les fonctionnalités des étiquettes de confidentialité.  Vous allez passer en revue les paramètres des étiquettes de confidentialité existantes qui ont déjà été créées et la stratégie correspondante pour publier l’étiquette.   Ensuite, vous voyez comment appliquer une étiquette et observez son impact du point de vue de l’utilisateur.
