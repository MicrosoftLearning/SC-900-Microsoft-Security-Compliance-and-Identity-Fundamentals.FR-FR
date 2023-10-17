<!---
---
Labo : Titre : « Découvrir Azure AD Authentication avec réinitialisation de mot de passe en libre-service » Parcours d’apprentissage/Module/Unité : « Parcours d’apprentissage : Décrire les fonctionnalités d’Azure Active Directory (Azure AD) - Solution Microsoft Entra ; Module 2 : Décrire les fonctionnalités d’authentification d’Azure AD ; Unité 4 : Décrire la réinitialisation de mot de passe en libre-service »
---
--->

# Labo : Réinitialisation de mot de passe en libre-service Microsoft Entra

Ce labo correspond au contenu Learn suivant :

- Parcours d’apprentissage : Décrire les fonctionnalités de Microsoft Entra
- Module : Décrire les fonctionnalités d’authentification de Microsoft Entra ID
- Unité : Décrire la réinitialisation du mot de passe en libre-service

## Scénario du labo

Dans ce labo, en tant qu’administrateur, vous allez suivre le processus d’ajout d’un utilisateur au groupe de sécurité SSPR, qui est déjà configuré dans votre locataire Microsoft 365. Une fois la réinitialisation de mot de passe en libre-service (SSPR) activée, vous adopterez le rôle d’un utilisateur, vous vous inscrirez à SSPR et vous réinitialiserez votre mot de passe.  Enfin, en tant qu’administrateur, vous serez en mesure de consulter les journaux d’audit, ainsi que les informations et données d’utilisation de SSPR.

**Durée estimée** : 15-20 minutes

### Tâche 1

Dans cette tâche, en tant qu’administrateur, vous allez parcourir certains des paramètres de configuration disponibles pour SSPR.

1. Ouvrez le navigateur Microsoft Edge. Dans la barre d’adresses, entrez **https://entra.microsoft.com** et connectez-vous avec les informations d’identification Microsoft 365 fournies par votre hôte de labo autorisé (ALH).
    1. Dans la fenêtre de connexion, entrez **admin@WWLxZZZZZZ.onmicrosoft.com** (où ZZZZZZ est votre ID de locataire unique communiqué par votre ALH), puis sélectionnez **Suivant**.
    1. Entrez le mot de passe d’administrateur qui vous a été communiqué par votre fournisseur d’hébergement de labo. Sélectionnez **Connexion**.
    1. Lorsque vous êtes invité à rester connecté, sélectionnez **Oui**.

1. Dans le volet de navigation de gauche, développez l’option **Protection**, puis sélectionnez **Réinitialisation de mot de passe**.  

1. Les propriétés de la réinitialisation de mot de passe en libre-service sont affichées. Sélectionnez l’icône d’informations en regard de l’emplacement de l’indication **Réinitialisation de mot de passe en libre-service activée** pour afficher la description. Assurez-vous que **Sélectionné** est surligné en bleu. Passez le curseur de la souris sur l’icône d’information à côté de l’indication **Sélectionner un groupe** et notez la description : « Définit le groupe d’utilisateurs qui sont autorisés à réinitialiser leurs propres mots de passe ». Vous devez inclure des utilisateurs dans le groupe : vous ne pouvez pas sélectionner des utilisateurs de manière individuelle. Notez qu’un groupe est déjà répertorié : SSPRSecurityGroupUsers (ce groupe a été préconfiguré dans le cadre de votre locataire Microsoft 365). Enfin, prenez note de la zone d’informations bleue indiquant « Ces paramètres ne s’appliquent qu’aux utilisateurs finaux de votre organisation. Les administrateurs bénéficient toujours du libre-service pour la réinitialisation de leur mot de passe et doivent utiliser deux méthodes d’authentification pour réinitialiser leur mot de passe. »

1. Dans le volet de navigation gauche de Réinitialisation du mot de passe, sélectionnez **Méthodes d’authentification**.

1. Dans l’option Nombre de méthodes requises pour réinitialiser, sélectionnez **1**. Notez la zone d’informations à l’écran.

1. Notez les différentes méthodes dont disposent les utilisateurs.  Les cases **E-mail** et **Téléphone mobile (SMS uniquement)** doivent déjà être cochées. Si ce n’est pas le cas, sélectionnez-les.

1. Dans le volet de navigation gauche de Réinitialisation du mot de passe, sélectionnez **Inscription**.  

1. Assurez-vous que le paramètre Exiger que les utilisateurs s’inscrivent quand ils se connectent ? est défini sur **Oui**.  Laissez le paramètre « Nombre de jours avant que les utilisateurs ne soient invités à reconfirmer leurs informations d’authentification » sur la valeur par défaut de 180.   Notez la zone d’informations sur la page.

1. Dans le volet de navigation gauche de Réinitialisation du mot de passe, sélectionnez **Notifications**.  

1. Assurez-vous que le paramètre Notifier les utilisateurs lors des réinitialisations de mot de passe ? est défini sur **Oui**.  Laissez le paramètre Notifier tous les administrateurs quand d’autres administrateurs réinitialisent leur mot de passe ? défini sur non.

1. Prenez note de la manière dont le volet de navigation de la réinitialisation de mot de passe inclut également des options servant à afficher les journaux d’audit ainsi que les informations et données d’utilisation.

1. Fermez la fenêtre de réinitialisation du mot de passe en sélectionnant le **X** dans le coin supérieur droit de la fenêtre. Vous revenez au centre d’administration Microsoft Entra.

1. Gardez la fenêtre Microsoft Entra ouverte.

### Tâche 2

Dans cette tâche, en tant qu’administrateur, vous ajoutez l’utilisateur que vous avez créé dans l’exercice de laboratoire précédent au groupe de sécurité SSPR.

1. Ouvrez l’onglet du navigateur pour la page d’accueil du centre d’administration Microsoft Entra **[entra.microsoft.com](https://entra.microsoft.com)** . Si nécessaire, développez **Identité**.

1. Dans le volet de navigation de gauche, sous « Identité », développez **Groupes**, puis sélectionnez **Tous les groupes**.

1. Une liste de groupes existants s’affiche. Dans le champ Rechercher des groupes, saisissez **SSPR**, puis sélectionnez **SSPRSecurityGroupUsers** dans les résultats de la recherche.  Vous accédez ainsi à l’option de configuration de ce groupe.

1. Dans le volet de navigation de gauche, sélectionnez **Membres**.

1. En haut de la page, sélectionnez **+ Ajouter des membres**.  

1. Dans la zone de recherche, entrez **Sara Perez**.  Une fois que l’utilisateur, **Sara Perez**, apparaît sous la zone de recherche, sélectionnez-le, puis appuyez sur **Sélectionner** en bas de la page.  Vous serez redirigé vers la page des membres.  Sélectionnez **Actualiser** en haut de la page. Vous devez maintenant voir Sara Perez répertoriée en tant que membre dans le groupe de sécurité SSPR.

1. Déconnectez-vous de tous les onglets de navigation en cliquant sur l’icône d’utilisateur à côté de l’adresse e-mail en haut à droite de l’écran. Ensuite, fermez toutes les fenêtres de navigation.

### Tâche 3

Dans cette tâche, vous adoptez le rôle de l’utilisateur, Sara Perez, et vous vous inscrivez à la réinitialisation de mot de passe en libre-service.  Cette tâche nécessite un appareil mobile sur lequel vous pouvez recevoir des SMS ou un compte e-mail personnel auquel vous avez accès.

1. Ouvrez Microsoft Edge et, dans la barre d’adresse, entrez **https://login.microsoft.com** .

1. Connectez-vous en tant que Sara Perez.

1. Une fenêtre contextuelle s’affiche pour indiquer que d’autres informations sont nécessaires.  La configuration demande que les membres du groupe SSPRSecurityGroupUsers s’inscrivent lorsqu’ils se connectent.  Sélectionnez le bouton **Suivant**.  Remarque :  Les administrateurs peuvent directement configurer les méthodes d’authentification lorsqu’ils ajoutent un utilisateur, plutôt que de demander aux utilisateurs de s’inscrire eux-mêmes. Pour ce faire, les administrateurs doivent connaître et définir les numéros de téléphone et les adresses e-mail dont se servent les utilisateurs pour effectuer la réinitialisation de mot de passe en libre-service, et réinitialiser le mot de passe d’un utilisateur.

1. La page « Sécuriser votre compte » s’ouvre.  La fenêtre qui s’affiche concerne la méthode d’authentification par téléphone. Si vous ne disposez pas d’un appareil mobile permettant de recevoir des SMS, passez à l’étape suivante.  Vous êtes invité à entrer un numéro de téléphone. Assurez-vous que l’option **Envoyez-moi un code par SMS** est activée.   Saisissez le numéro de téléphone sur lequel vous pouvez recevoir un code par SMS et appuyez sur le **bouton Suivant**.  Une nouvelle fenêtre s’ouvre, indiquant qu’un code a été envoyé au numéro de téléphone que vous avez entré.  Saisissez le code reçu et sélectionnez **Suivant**. Une fenêtre s’ouvre indiquant Opération réussie et votre méthode de connexion par défaut.  Sélectionnez **Terminé**.  
    1. Vous pouvez également définir une autre méthode, comme indiqué dans le coin inférieur gauche de la fenêtre.  Si vous choisissez de définir une méthode différente, sélectionnez **Je veux définir une méthode différente**. Ensuite, une fenêtre contextuelle s’affiche et vous demande : Quelle méthode souhaitez-vous utiliser ?  Dans la liste déroulante, sélectionnez votre méthode par défaut, **E-mail**, puis sélectionnez le bouton **Confirmer**.  Saisissez l’adresse e-mail que vous souhaitez utiliser, puis sélectionnez **Suivant**.  Une nouvelle fenêtre s’ouvre, indiquant qu’un code a été envoyé à l’adresse e-mail que vous avez entrée.  Accédez à l’adresse e-mail que vous avez saisie pour obtenir le code.  Saisissez le code reçu et sélectionnez **Suivant**. Une fenêtre s’ouvre indiquant Opération réussie et votre méthode de connexion par défaut.  Sélectionnez **Terminé**.

1. Vous pouvez maintenant terminer votre connexion. Si vous constatez que le délai de connexion a expiré, entrez à nouveau le mot de passe.

1. Déconnectez-vous de tous les onglets de navigation en cliquant sur l’icône d’utilisateur à côté de l’adresse e-mail en haut à droite de l’écran. Ensuite, fermez toutes les fenêtres de navigation.

### Tâche 4 (facultative)

Dans cette tâche, vous adoptez le rôle de l’utilisateur, Sara Perez, et vous réinitialisez votre mot de passe.

1. Ouvrez Microsoft Edge.

1. Dans la barre d’adresse, entrez **https://login.microsoftonline.com** .

1. Connectez-vous en tant que Sara Perez en saisissant votre adresse e-mail **sara@WWLxZZZZ.onmicrosoft.com** (où ZZZZZZ est votre ID de locataire unique fourni par le fournisseur d’hébergement de labo) et appuyez sur le bouton **Suivant**. Il se peut qu’une fenêtre Choisir un compte s’ouvre à la place. Dans ce cas, sélectionnez le compte de Sara Perez.

1. Dans la fenêtre Saisir le mot de passe, sélectionnez **J’ai oublié mon mot de passe**.

1. La fenêtre Réaccéder à votre compte s’ouvre.   Vérifiez que l’e-mail pour Sara Perez, sara@WWLxZZZZ.onmicrosoft.com, s’affiche dans la zone E-mail ou Nom d’utilisateur.  Si ce n’est pas le cas, saisissez-la.  

1. Dans la case vide, saisissez les caractères affichés dans l’image ou les mots que vous entendez. Une fois que vous les avez saisis, sélectionnez **Suivant**.

1. L’écran affiche Réaccéder à votre compte et indique Vérification étape 1 > choisir un nouveau mot de passe. Conservez le paramètre par défaut **Envoyer un SMS à mon téléphone mobile**.  Vous êtes invité à entrer votre numéro de téléphone mobile.  Une fois que vous l’avez entré, sélectionnez le bouton **Suivant**.  Si vous avez sélectionné la méthode par e-mail au moment de l’inscription, la fenêtre Réaccéder à votre compte indique ceci : Vous allez recevoir sur votre adresse de messagerie secondaire un e-mail contenant un code de vérification.  Sélectionnez **E-mail**.

1. Saisissez le code de vérification, puis appuyez sur **Suivant**.

1. Dans l’écran suivant, vous êtes invité à entrer un nouveau mot de passe et à le confirmer.  Saisissez-le et appuyez sur le bouton **Terminer**.

1. Un message indiquant que votre mot de passe a été réinitialisé s’affiche à l’écran.  Sélectionnez **cliquer ici** pour vous connecter avec votre nouveau mot de passe.

1. Dans la zone d’informations Choisir un compte, sélectionnez **sara@WWLxZZZZZZ.onmicrosoft.com** , saisissez votre nouveau mot de passe, puis appuyez sur le bouton **Se connecter**.  Si vous êtes invité à rester connecté, Sélectionnez **Non**.

1. Vous devez maintenant vous trouver dans le portail Office.

1. Déconnectez-vous en cliquant sur l’icône d’utilisateur à côté de l’adresse e-mail, dans le coin supérieur droit de l’écran, et en sélectionnant **Se déconnecter**. Ensuite, fermez toutes les fenêtres du navigateur.

### Tâche 5 (facultative)

Dans cette tâche, en tant qu’administrateur, vous allez brièvement consulter les journaux d’audit, ainsi que les informations et données d’utilisation associées à la réinitialisation du mot de passe.

1. Ouvrez Microsoft Edge.

1. Dans la barre d’adresses, entrez **https://entra.microsoft.com** et connectez-vous avec les informations d’identification Microsoft 365 fournies par votre hôte de labo autorisé (ALH).

1. Vous êtes dans le centre d’administration Microsoft Entra.  Dans le volet de navigation de gauche, développez l’option **Protection**, puis sélectionnez **Réinitialisation de mot de passe**.

1. Dans le volet de navigation de gauche, sélectionnez **Journaux d’audit**.  Notez les informations et les filtres disponibles.  Notez également que vous pouvez télécharger les journaux.  

1. Sélectionnez **Télécharger**.  Notez que vous pouvez formater le fichier téléchargé au format CSV ou JSON.  Fermez la fenêtre en sélectionnant le **X** dans le coin supérieur droit de l’écran.

1. Dans le volet de navigation de gauche, sélectionnez **Utilisation et informations**.

1. Notez les informations disponibles relatives à l’inscription.  Notez que l’actualisation de ces données peut prendre un certain temps, même après avoir effectué une actualisation. Il se peut donc qu’elles ne reflètent pas encore les données d’inscription ou d’utilisation de la tâche précédente.

1. En haut de la page, sélectionnez **Utilisation** pour consulter le nombre de réinitialisations de mot de passe en libre-service et de déverrouillages de comptes par méthode.  Notez que l’actualisation de ces données peut prendre un certain temps, même après avoir effectué une actualisation. Il se peut donc qu’elles ne reflètent pas encore les données d’utilisation de la tâche précédente.

1. Fermez les onglets de votre navigateur.

### Révision

Dans ce labo, vous avez suivi le processus d’activation de la réinitialisation du mot de passe en libre-service en tant qu’administrateur. Une fois la réinitialisation de mot de passe en libre-service (SSPR) activée, vous adopterez le rôle d’un utilisateur pour vous inscrire à SSPR et vous réinitialiserez votre mot de passe.  Enfin, en tant qu’administrateur, vous découvrez où accéder aux journaux d’audit, ainsi qu’aux informations et données d’utilisation de SSPR.
