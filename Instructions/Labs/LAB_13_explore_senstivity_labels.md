---
lab:
  title: 'Explorer les étiquettes de confidentialité dans Microsoft Purview'
  module: 'Module 3 : Décrire la protection des informations et la gestion du cycle de vie des données dans Microsoft Purview'
---


# <a name="lab-explore-sensitivity-labels-in-microsoft-purview"></a>Labo : Explorer les étiquettes de confidentialité dans Microsoft Purview

Ce labo correspond au contenu Learn suivant :

- Parcours d’apprentissage : Décrire les fonctionnalités des solutions de conformité Microsoft
- Module : Décrire la protection des informations et la gestion de cycle de vie des données dans Microsoft Purview
- Unité : Décrire les étiquettes de confidentialité

## <a name="lab-scenario"></a>Scénario du labo

Dans ce labo, vous explorez les fonctionnalités des étiquettes de confidentialité.  Vous passez en revue les paramètres des étiquettes de confidentialité existantes et la stratégie correspondante pour publier l’étiquette.   Ensuite, vous voyez comment appliquer une étiquette et observez son impact du point de vue de l’utilisateur.

**Durée estimée** : 20-25 minutes

### <a name="task-1"></a>Tâche 1

Dans cette tâche, vous comprenez ce que vous pouvez faire avec les étiquettes de confidentialité en passant en revue les paramètres d’une étiquette de confidentialité existante et la politique correspondante pour la publier.

1. Ouvrez Microsoft Edge. Dans la barre d’adresse, entrez **admin.microsoft.com**.

1. Connectez-vous avec vos informations d’identification d’administrateur.
    1. Dans la fenêtre de connexion, entrez **admin@WWLxZZZZZZ.onmicrosoft.com** (où ZZZZZZ représente votre ID de locataire unique fourni par votre fournisseur d’hébergement de labo), puis sélectionnez **Suivant**.

    1. Entrez le mot de passe d’administrateur qui vous a été communiqué par votre fournisseur d’hébergement de labo. Sélectionnez **Connexion**.
    1. Lorsque vous êtes invité à rester connecté, sélectionnez **Oui**. Vous accédez ainsi à la page du Centre d’administration Microsoft 365.

1. Sélectionnez **Tout afficher** dans le volet de navigation gauche du centre d’administration Microsoft 365.

1. Sous les Centres d’administration, sélectionnez **Conformité**.  Le navigateur ouvre une nouvelle page. Il s’agit de la page d’accueil du portail de conformité Microsoft Purview.  

1. Dans le volet de navigation à gauche, sélectionnez **Protection des données**.

1. Dans la page de présentation, notez que la zone d’informations jaune indique que votre organisation n’a pas activé la possibilité de traiter le contenu des fichiers Office en ligne qui ont des étiquettes de confidentialité chiffrées, et qui sont stockées dans OneDrive et SharePoint.  Sélectionnez **Activer maintenant**.  Une fois activé, il peut y avoir un délai avant que le paramètre ne soit propagé à travers le système.  Consultez également les informations disponibles dans cette page de présentation.

1. Sélectionnez l’onglet **Étiquettes** en haut de la page.

1. Au milieu de la page, notez comment des étiquettes sont déjà créées.  Sélectionnez **Confidentiel - Finance**.  Une fenêtre avec des informations à propos de cette étiquette s’ouvre.  Remarquez comment cette étiquette est définie pour prendre en charge le chiffrement et le marquage de contenu.  Sélectionnez **Modifier l’étiquette** en haut de la page pour afficher certains des paramètres de base.  Quand vous parcourez les différents paramètres, ne changez RIEN.

1. Vous commencez la configuration en fournissant un nom et une description pour votre étiquette.  Ne changez rien.  Sélectionnez **Suivant** au bas de la page.

1. Notez l’étendue de cette étiquette.  L’étendue est définie sur **Éléments**.  Lisez la description, mais ne changez rien.  Sélectionnez **Suivant** au bas de la page.

1. Pour l’étendue sélectionnée, Éléments, vous pouvez choisir de chiffrer et/ou de marquer le contenu.  Notez que les paramètres de protection des fichiers et des e-mails sont définis à la fois pour le chiffrement et pour le marquage du contenu des fichiers.  Passez en revue la définition de chacun d’entre eux.  Ne changez rien.  Sélectionnez **Suivant** au bas de la page.

1. La fenêtre de chiffrement affiche la configuration pour les paramètres de chiffrement.  Ne changez rien.  Passez en revue la zone d’informations sous Configuration des paramètres de chiffrement ainsi que les paramètres configurés. Notez comment l’accès utilisateur au contenu est défini pour ne jamais expirer.  Vous pouvez aussi attribuer des autorisations à des utilisateurs et groupes spécifiques afin qu’ils puissent interagir avec le contenu auquel cette étiquette est appliquée.  Le locataire est défini sous Utilisateurs et groupes. Ainsi, tous les utilisateurs de votre locataire peuvent afficher le contenu qui dispose de cette étiquette.  L’équipe responsable des finances apparaît également et ses membres disposent d’autorisations pour co-éditer.  Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.

1. Sur la page de marquage de contenu, remarquez la zone d’informations en haut de l’écran.  Les marquages de contenu seront appliqués aux documents, mais uniquement les en-têtes et les pieds de page seront appliqués aux e-mails. En d’autres termes, les filigranes ne sont pas appliqués aux e-mails.  Le marquage de contenu associé à cette étiquette est un filigrane qui indique HAUTEMENT CONFIDENTIEL.  Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.

1. Vous êtes à présent dans la fenêtre d’étiquetage automatique des fichiers et des e-mails.  Lisez la description de l’étiquetage automatique en haut de la page ainsi que la zone d’informations en dessous.  Notez également que cette étiquette est définie pour l’étiquetage automatique sous certaines conditions. Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.

1. La fenêtre suivante définit les paramètres de protection des groupes et des sites qui ont cette étiquette. Ce n’est pas activé, sélectionnez **Suivant** au bas de la page.

1. Cette fenêtre suivante est une fonctionnalité en préversion de l’étiquetage automatique des ressources de données schématisées. lisez la description.  La fonctionnalité n’est pas activée. Sélectionnez **Annuler** en bas de la page pour quitter l’assistant de configuration de l’étiquette et retourner à la page de protection des données.

1. En haut de la page de protection des données, sélectionnez **Stratégies d’étiquettes**.  C’est au travers des stratégies d’étiquettes que les étiquettes de confidentialité peuvent être publiées.  

1. Dans ce cas, sélectionnez **Stratégie d’étiquette de confidentialité globale**.  Une fenêtre avec des informations à propos de la stratégie s’ouvre.  Notez la description, il s’agit de la stratégie d’étiquette de confidentialité par défaut pour tous les utilisateurs et groupes. Cette stratégie permet de publier la plupart des étiquettes qui ont été préconfigurées pour ce locataire lab Microsoft 365 et qui sont listées sous l’onglet Étiquettes.  

1. Sélectionnez **Modifier** la stratégie en haut de la fenêtre.
    1. Lisez la description sous « Choisir les étiquettes de confidentialité à publier ».  Notez l’étiquette qui est indiquée.  Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.
    1. Lisez la description sous « Publier aux utilisateurs et groupes ».  Notez que cette étiquette est disponible pour tous les utilisateurs.  Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.
    1. Passez en revue les paramètres de stratégie.  Sélectionnez **Demander aux utilisateurs d’appliquer une étiquette à leurs e-mails et documents**. Vérifiez la description fournie. Sélectionnez **Suivant** au bas de la page.
    1. Lisez la description sous « Appliquer une étiquette par défaut aux documents ». Dans le champ Étiquette par défaut, sélectionnez la flèche vers le bas, puis **Général/Tous les employés (sans restriction)** .  Sélectionnez **Suivant** au bas de la page.
    1. Lisez la description sous « Appliquer une étiquette par défaut aux e-mails ». Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.
    1. Lisez la description sous « Appliquer une étiquette par défaut au contenu Power BI ». Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.
    1. La dernière option de configuration consiste à nommer votre stratégie.  Comme vous modifiez la stratégie, le champ de nom est grisé. Sélectionnez **Suivant** en bas de la page.
    1. Passez en revue les paramètres de stratégie, puis sélectionnez **Envoyer**, et **Terminé** pour revenir à la page Protection des informations.

1. Depuis la page de protection des données, sélectionnez l’étiquetage automatique.  Notez qu’il n’y a pas de stratégie d’étiquetage automatique configurée.  Ne modifiez pas les paramètres.  Si vous vous demandez pourquoi il n’y a pas de stratégie ici, alors que la configuration d’étiquette est définie sur l’étiquetage automatique des fichiers et des e-mails, revenez aux étapes où vous avez parcouru les paramètres de configuration d’étiquette, et passez en revue les zones Description et Informations associées à l’étiquetage automatique des fichiers et des e-mails.  Conseil :  Dans l’onglet d’étiquetage automatique pour le labo de confidentialité, il est indiqué :  « Afin d’appliquer automatiquement cette étiquette aux fichiers qui sont déjà enregistrés (dans SharePoint ou OneDrive) ou aux e-mails qui ont déjà été traités par Exchange, vous devez créer une stratégie d’étiquetage automatique. »

1. Dans le volet de navigation de gauche, sélectionnez Accueil pour revenir au portail de conformité Microsoft Purview.

1. Laissez cette page ouverte, vous en avez besoin pour la tâche suivante.

### <a name="task-2"></a>Tâche 2

Dans cette tâche, vous suivez le processus d’application d’une étiquette du point de vue de l’utilisateur (dans notre cas, l’utilisateur est l’administrateur) et voyez comment elle marque le contenu.

1. Dans la page d’accueil du portail de conformité Microsoft Purview, sélectionnez l’icône **Lanceur d’application**, à côté de l’indication Contoso Electronics. Sélectionnez l’**icône Word**.  

1. Sous Créer, sélectionnez **Document vide**, puis entrez du texte sur la page.  En haut de la page, dans la barre bleue, sélectionnez la flèche vers le bas à côté de Document - Enregistré et, dans la zone du nom du fichier, entrez **Test-label** et appuyez sur **Entrer** sur votre clavier.

1. Dans la barre de menus supérieure, sélectionnez **Icône Sensibilité**, l’icône à droite de l’icône en forme de microphone (selon la taille de votre écran, vous devrez peut-être sélectionner les points de suspension, puis la sensibilité). Dans le menu déroulant, sélectionnez **Confidentiel - Finance**.  REMARQUE : si vous ne voyez pas immédiatement l’option Sensibilité, actualisez la page, mais comme il s’agit d’un environnement locataire de labo, les délais peuvent être plus longs que la normale (10 à 15 minutes).

1. Dans la barre de menu supérieure, sélectionnez **Affichage**, puis sélectionnez **Mode lecture**.

1. Notez comment le document inclut le filigrane.  

1. Fermez les onglets Microsoft Word qui sont ouverts dans votre navigateur pour quitter Word.

### <a name="task-3-optional"></a>Tâche 3 (facultative)

Souvenez-vous, dans la première partie de la démo, l’étiquette Confidentiel - Finance est configurée pour le chiffrement. Selon les autorisations configurées avec cette étiquette, les utilisateurs du locataire Contoso ont des autorisations de lecture pour n’importe quel document/e-mail qui a l’étiquette.  Dans cette section, vous envoyez le document que vous avez créé précédemment, qui comprend l’étiquette Confidentiel - Finance, à une adresse e-mail à laquelle vous avez accès (par exemple, une adresse e-mail personnelle ou votre e-mail Microsoft) et qui ne fait PAS partie du domaine WWLxZZZZ.OnMicrosoft.com.  

1. Dans la page d’accueil du portail de conformité Microsoft Purview, sélectionnez l’icône **Lanceur d’application**, à côté de l’indication Contoso Electronics. Sélectionnez l’**icône Outlook**.

1. Sélectionnez **Nouveau message** en haut à gauche de l’écran.  Saisissez une adresse e-mail à laquelle vous avez accès et qui ne fait pas partie du domaine WWLxZZZZ.OnMicrosoft.com et saisissez **Test** dans la ligne d’objet.

1. Sélectionnez **Joindre** (icône en forme de trombone).

1. Sélectionnez **OneDrive**.

1. Vérifiez que l’onglet **Récent** dans le volet de navigation de gauche est sélectionné.  À partir de la liste qui apparaît, sélectionnez le document que vous avez créé et auquel vous avez appliqué l’étiquette **Étiquette de test**. Sélectionnez **Suivant**, puis **Joindre en tant que copie**.  Appuyez sur **Envoyer**.

1. Consultez l’adresse e-mail à laquelle vous avez envoyé le document.  Notez que l’e-mail peut être envoyé directement dans votre dossier Courrier indésirable.  L’e-mail est envoyé, mais quand vous essayez d’ouvrir le fichier Word joint, qui a été étiqueté à l’origine comme Confidentiel - Finance, vous voyez une notification indiquant que vous n’avez pas l’autorisation d’ouvrir le document.

1. Fermez les onglets de votre navigateur.

### <a name="review"></a>Révision

Dans ce labo, vous explorez les fonctionnalités des étiquettes de confidentialité.  Vous passez en revue les paramètres des étiquettes de confidentialité existantes et la politique correspondante pour pouvoir les publier.   Ensuite, vous voyez comment appliquer une étiquette et observez son impact du point de vue de l’utilisateur.
