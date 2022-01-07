---
lab:
    title: 'Découvrir les étiquettes de confidentialité dans Microsoft 365'
    module: 'Module 4, leçon 2 : Décrire les fonctionnalités des solutions de conformité Microsoft : Décrire les fonctionnalités de protection et de gouvernance des informations de Microsoft 365'
---


# Labo : Découvrir les étiquettes de confidentialité dans Microsoft 365

## Scénario du labo
Dans ce labo, vous allez découvrir les possibilités offertes par les étiquettes de confidentialité.  Vous expliquerez les paramètres des étiquettes de confidentialité existantes qui ont été créées et la stratégie correspondante pour publier l’étiquette.   Ensuite, vous verrez comment appliquer une étiquette et l’effet de celle-ci, depuis la perspective d’un utilisateur.


**Durée estimée** : 20-25 minutes

#### Tâche 1 : Dans cette tâche, vous allez comprendre le potentiel des étiquettes de confidentialité. Pour ce faire, vous allez parcourir les paramètres d’une étiquette de confidentialité existante, ainsi que la politique correspondante pour pouvoir la publier.

1. Ouvrez Microsoft Edge. Saisissez **admin.microsoft.com** dans la barre d’adresse.

1. Connectez-vous avec vos informations d’identification d’administrateur.
    1. Dans la fenêtre de connexion, saisissez **admin@WWLxZZZZZZ.onmicrosoft.com** (ZZZZZZ représente votre ID de locataire unique fourni par votre fournisseur d’hébergement de labo), puis sélectionnez **Suivant**.
    
    1. Saisissez le mot de passe d’administrateur qui doit vous être fourni par votre fournisseur d’hébergement de labo. Sélectionnez **Se connecter**.
    1. Lorsque vous êtes invité à rester connecté, sélectionnez **Oui**. Vous accédez ainsi à la page du Centre d’administration Microsoft 365.

1. Sélectionnez **Tout afficher** dans le volet de navigation gauche du centre d’administration Microsoft 365.

1. Sous les Centres d’administration, sélectionnez **Conformité**.  Le navigateur ouvre une nouvelle page : il s’agit de la page d’accueil du Centre de conformité Microsoft 365.  

1. Dans le volet de navigation de gauche, sélectionnez **Protection des données**.

1. Sélectionnez l’onglet **Étiquettes** en haut de la page.

1. La zone d’informations jaune indique que votre organisation n’a pas activé la capacité à traiter du contenu dans des fichiers Office en ligne qui disposent d’étiquettes de confidentialité chiffrées appliquées et qui sont enregistrées dans OneDrive et SharePoint.  Sélectionnez Activer maintenant.  Une fois activé, il peut y avoir un délai avant que le paramètre ne soit propagé à travers le système.


1. Au milieu de la page, vous remarquerez que trois étiquettes ont déjà été créées.  Sélectionnez **Confidentiel - Finance**.  Une fenêtre avec des informations à propos de cette étiquette s’ouvre.  Remarquez comment cette étiquette est définie pour prendre en charge le chiffrement et le marquage de contenu.  Sélectionnez Modifier l’étiquette en haut de la page pour afficher quelques paramètres de configuration de base.

1. Vous commencez la configuration en fournissant un nom et une description pour votre étiquette.  Ne changez rien.  Sélectionnez **Suivant** au bas de la page.

1. Notez l’étendue de cette étiquette.  L’étendue est définie sur Fichiers et e-mails, ce qui vous permet de configurer les paramètres de chiffrement et de marquage de contenu afin de protéger les e-mails et les fichiers du bureau étiquetés.  Ne changez rien.  Sélectionnez **Suivant** au bas de la page.

1. Pour l’étendue sélectionnée, Fichiers et e-mails, vous pouvez décider de chiffrer et/ou de marquer le contenu.  Notez comment les paramètres de protection pour les fichiers et les e-mails sont définis à la fois pour le chiffrement et pour le marquage du contenu des fichiers.  Passez en revue la définition de chacun d’entre eux.  Ne changez rien.  Sélectionnez **Suivant** au bas de la page.

1. La fenêtre de chiffrement affiche la configuration pour les paramètres de chiffrement.  Ne changez rien.  Passez en revue la zone d’informations sous Configuration des paramètres de chiffrement ainsi que les paramètres configurés. Notez comment l’accès utilisateur au contenu est défini pour ne jamais expirer.  Vous pouvez aussi attribuer des autorisations à des utilisateurs et groupes spécifiques afin qu’ils puissent interagir avec le contenu auquel cette étiquette est appliquée.  Le locataire est défini sous Utilisateurs et groupes. Ainsi, tous les utilisateurs de votre locataire peuvent afficher le contenu qui dispose de cette étiquette.  L’équipe responsable des finances apparaît également et ses membres disposent d’autorisations pour co-éditer.  Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.

1. Sur la page de marquage de contenu, remarquez la zone d’informations en haut de l’écran.  Les marquages de contenu seront appliqués aux documents, mais uniquement les en-têtes et les pieds de page seront appliqués aux e-mails. En d’autres termes, les filigranes ne sont pas appliqués aux e-mails.  Le marquage de contenu associé à cette étiquette est un filigrane comportant la mention « HAUTEMENT CONFIDENTIEL ».  Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.

1. Vous êtes à présent dans la fenêtre d’étiquetage automatique pour les fichiers et les e-mails.  Lisez la description de l’étiquetage automatique en haut de la page ainsi que la zone d’informations en dessous.  Notez également que cette étiquette est définie pour l’étiquetage automatique sous certaines conditions. Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.

1. La prochaine fenêtre définit les paramètres de protection pour les équipes, les groupes et les sites pour lesquels cette étiquette est appliquée. Ce n’est pas activé, sélectionnez **Suivant** au bas de la page. 

1. La prochaine fenêtre est un aperçu de la fonctionnalité qui permet d’appliquer automatiquement cette étiquette aux colonnes de la base de données d’Azure (comme SQL, Synapse, etc.) qui contiennent les types d’informations sensibles que vous choisissez.  Cette fonctionnalité n’est pas activée. Sélectionnez **Annuler** en bas de la page pour quitter l’assistant de configuration de l’étiquette et retourner à la page de protection des données. 

1. En haut de la page de protection des données, sélectionnez **Stratégies d’étiquettes**.  C’est au travers des stratégies d’étiquettes que les étiquettes de confidentialité peuvent être publiées.  

1. Sélectionnez **Confidentiel-Stratégie financière**.  Une fenêtre avec des informations à propos de la stratégie s’ouvre.  Cette stratégie sert à publier les étiquettes Confidentiel-Stratégie financière et à protéger les données qui contiennent les données financières pour Contoso.  Remarquez également comment cette stratégie est publiée pour tous.  

1. Sélectionnez **Modifier** la stratégie en haut de la fenêtre.

1. Lisez la description sous « Choisir les étiquettes de confidentialité à publier ».  Notez l’étiquette qui est indiquée.  Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.

1. Lisez la description sous « Publier aux utilisateurs et groupes ».  Notez que cette étiquette est disponible pour tous les utilisateurs.  Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.

1. Passez en revue les paramètres de stratégie.  Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.
    1. Lisez la description affichée sous la zone « Appliquer une étiquette par défaut aux documents ».  Notez qu’il n’y a pas d’étiquette par défaut. Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.
    1. Lisez la description affichée sous la zone « Appliquer une étiquette par défaut aux e-mails ».  Utilisez la flèche de la liste déroulante de la zone de saisie pour afficher les options disponibles. Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.
    1. Lisez la description affichée sous la zone « Appliquer une étiquette par défaut au contenu Power BI ».  Notez qu’il n’y a pas d’étiquette par défaut. Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.

1. La dernière option de configuration consiste à nommer votre stratégie.  Ne modifiez pas les paramètres.  Sélectionnez **Annuler** en bas de la page pour quitter la configuration de la stratégie et retourner à la page de protection des données.

1. Depuis la page de protection des données, sélectionnez l’étiquetage automatique.  Il n’y a pas de stratégie d’étiquetage automatique configurée.  Ne modifiez pas les paramètres.  Si vous vous demandez pourquoi il n’y a pas de stratégie ici, alors que la configuration d’étiquette est définie sur étiquetage automatique pour les fichiers et les e-mails, revenez aux étapes où vous avez parcouru les paramètres de configuration d’étiquette. Passez en revue les descriptions et les zones d’informations associées à l’étiquetage automatique pour les fichiers et les e-mails.  Astuce :  Dans l’onglet d’étiquetage automatique pour le labo de confidentialité, il est indiqué :  « Afin d’appliquer automatiquement cette étiquette aux fichiers qui sont déjà enregistrés (dans SharePoint ou OneDrive) ou aux e-mails qui ont déjà été traités par Exchange, vous devez créer une stratégie d’étiquetage automatique. »

1. Dans le volet de navigation à gauche, sélectionnez Accueil pour retourner au Centre de conformité Microsoft 365.

1. Laissez cette page ouverte, vous en aurez besoin pour la tâche suivante.


#### Tâche 2 :  Cette tâche va vous apprendre le processus d’application d’une étiquette en tant qu’utilisateur (dans notre cas, l’utilisateur est aussi l’administrateur) et la façon dont elle marque le contenu.

1. Vérifiez tout d’abord qu’Office soit bien configuré sur votre machine virtuelle.  Pour ce faire, sélectionnez l’onglet **Centre d’administration Microsoft 365** dans votre navigateur.  Si cet onglet a été précédemment fermé, ouvrez un nouvel onglet dans le navigateur et saisissez **admin.microsoft.com**.
    1. Dans le volet de navigation de gauche, sélectionnez **Facturation** pour afficher toutes les options, puis sélectionnez **Vos produits**.
    1. Sur la page Vos produits, sélectionnez **Version d’évaluation de Microsoft 365 E5**
    1. Sur la page Version d’évaluation de Microsoft 365 E5, sélectionnez **Télécharger et installer le logiciel** et suivez les instructions présentées sur la page.

1. Dans le coin inférieur gauche de la machine virtuelle du labo, cliquez sur l’icône Windows, puis sélectionnez **Word** et puis **Nouveau document**.  Un nouveau document Word s’ouvre dans la version de bureau de Word.

1. Dans la barre de menu supérieure, sélectionnez **Sensibilité**. À partir du menu déroulant, sélectionnez **Confidentiel - Finance**.

1. Notez comment le document inclut le filigrane.  Le filigrane s’affiche en miniature et un texte en gris clair s’affiche verticalement sur la page. 

1. Enregistrez le fichier Word.

1. Fermez les onglets Microsoft Word qui sont ouverts dans votre navigateur pour quitter Word.

#### Tâche 3 (facultatif) : En plus du marquage de contenu, le paramètre de protection d’étiquette a été défini pour le chiffrement. Grâce à la configuration des autorisations qui ont été accordées pour cette étiquette, les membres du groupe responsable des finances peuvent co-éditer les documents qui disposent de cette étiquette et les utilisateurs dans le locataire Contoso peuvent les voir.  Dans cette tâche, vous allez envoyer ce document à une adresse e-mail à laquelle vous avez accès (c’est-à-dire une adresse personnelle) qui n’appartient PAS au domaine WWLxZZZZ.OnMicrosoft.com. Vous allez ensuite découvrir ce qui se passe quand vous essayez d’ouvrir la pièce jointe.  

1. Depuis la page d’accueil du Centre de conformité Microsoft 365, sélectionnez **l’icône du lanceur d’applications** à côté de Contoso Electronics. **Effectuez un clic droit sur l’icône Outlook** et sélectionnez **Ouvrir dans un nouvel onglet**.

1. En haut à gauche de l’écran, sélectionnez **Nouveau message**.  Saisissez une adresse e-mail à laquelle vous avez accès et qui ne fait pas partie du domaine WWLxZZZZ.OnMicrosoft.com et saisissez **Test** dans la ligne d’objet.

1. Sélectionnez **Joindre**.

1. Sélectionnez **Parcourir les emplacements cloud**.

1. À partir de la liste qui apparaît, sélectionnez le document que vous avez créé et auquel vous avez appliqué l’étiquette **Étiquette de test**. Sélectionnez **Suivant**, puis **Joindre en tant que copie**.  Appuyez sur **Envoyer**.

1. Connectez-vous au compte de messagerie à partir duquel vous avez envoyé le document, en utilisant le navigateur web de la machine virtuelle du labo.  Notez que l’e-mail peut être envoyé directement dans votre dossier Courrier indésirable.  Lorsque vous essayez d’ouvrir le fichier Word joint, une notification s’affiche et vous indique que vous ne disposez pas de l’autorisation pour ouvrir ce document.

1. Fermez les onglets de votre navigateur.


#### Révision
Dans ce labo, vous allez découvrir les possibilités offertes par les étiquettes de confidentialité.  Vous allez parcourir les paramètres d’étiquettes de confidentialité existantes, ainsi que la politique correspondante pour pouvoir les publier.   Ensuite, vous verrez comment appliquer une étiquette et l’effet de celle-ci, depuis la perspective d’un utilisateur.