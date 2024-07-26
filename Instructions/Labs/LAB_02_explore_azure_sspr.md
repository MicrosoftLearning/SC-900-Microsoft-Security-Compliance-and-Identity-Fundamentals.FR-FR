---
lab:
  title: Réinitialisation de mot de passe en libre-service Microsoft Entra
  module: Describe the authentication capabilities of Microsoft Entra ID
---

<!---
---
Labo : Titre : « Découvrir Azure AD Authentication avec réinitialisation de mot de passe en libre-service » Parcours d’apprentissage/Module/Unité : « Parcours d’apprentissage : Décrire les fonctionnalités d’Azure Active Directory (Azure AD) - Solution Microsoft Entra ; Module 2 : Décrire les fonctionnalités d’authentification d’Azure AD ; Unité 4 : Décrire le mot de passe en libre-service »
---
--->

# Lab : Réinitialisation de mot de passe en libre-service Microsoft Entra

Ce labo correspond au contenu Learn suivant :

- Parcours d’apprentissage : décrire les fonctionnalités de Microsoft Entra
- Module : décrire les fonctionnalités d’authentification de Microsoft Entra ID
- Unité : décrire la réinitialisation du mot de passe en libre-service

## Scénario du labo

Dans ce labo, vous, en tant qu’administrateur, allez suivre le processus d’ajout d’un utilisateur au groupe de sécurité SSPR, qui est déjà configuré dans votre locataire Microsoft 365. Une fois la réinitialisation de mot de passe en libre-service (SSPR) activée, vous adopterez le rôle d’un utilisateur, vous vous inscrirez à SSPR et vous réinitialiserez votre mot de passe.  Enfin, en tant qu’administrateur, vous serez en mesure de voir les journaux d’audit et les insighs d’utilisation pour SSPR.

**Durée estimée** : 15 à 20 minutes

### Tâche 1

Dans cette tâche, en tant qu’administrateur, vous allez parcourir certains des paramètres de configuration disponibles pour SSPR.

1. Ouvrez le navigateur Microsoft Edge. Dans la barre d’adresses, saisissez **https://entra.microsoft.com** et connectez-vous avec les informations d’identification d’admin Microsoft 365 fournies par votre hôte de labo autorisé (ALH).
    1. Dans la fenêtre de connexion, entrez **admin@WWLxZZZZZZ.onmicrosoft.com** (où ZZZZZZ est votre ID de locataire unique communiqué par votre ALH), puis sélectionnez **Suivant**.
    1. Entrez le mot de passe d’administrateur qui vous a été communiqué par votre fournisseur d’hébergement de labo. Cliquez sur **Connexion**.
    1. Lorsque vous êtes invité à rester connecté, sélectionnez **Oui**.

1. Dans le volet de navigation gauche, développez l’option de **Protection**, puis sélectionnez **Réinitialisation de mot de passe**.  

1. Les propriétés de la réinitialisation du mot de passe en libre-service sont affichées. Sélectionnez l’icône d’information à côté de **Activer la réinitialisation de mot de passe en libre-service** pour voir la description. Vérifiez que **Sélectionné** est surligné en bleu. Passez maintenant le curseur de la souris sur l’icône d’information à côté de l’indication **Sélectionner un groupe** et notez la description : « Définit le groupe d’utilisateurs qui sont autorisés à réinitialiser leurs propres mots de passe ». Vous devez inclure des utilisateurs dans le groupe, vous ne pouvez pas les sélectionner individuellement. Notez qu’un groupe est déjà répertorié : SSPRSecurityGroupUsers. (Ce groupe a été préconfiguré dans le cadre de votre locataire Microsoft 365). Enfin, remarquez l’encadré bleu : « Ces paramètres ne s’appliquent qu’aux utilisateurs finaux de votre organisation. Les administrateurs bénéficient toujours du libre-service pour la réinitialisation de leur mot de passe, et doivent utiliser deux méthodes d’authentification pour réinitialiser leur mot de passe. »

1. Dans le volet de navigation gauche de la page Réinitialisation du mot de passe, sélectionnez **Méthodes d’authentification**.

1. Dans l’option Nombre de méthodes requises pour réinitialiser, sélectionnez **1**. Remarquez l’encadré informatif à l’écran.

1. Remarquez les différentes méthodes disponibles pour les utilisateurs.  Les cases **E-mail** et **Téléphone (SMS uniquement)** devraient déjà être cochées, si ce n’est pas le cas, sélectionnez-les.

1. Dans le volet de navigation gauche de la page Réinitialisation du mot de passe, sélectionnez **Inscription**.  

1. Assurez-vous que le paramètre Obliger les utilisateurs à s’inscrire durant la connexion est défini sur **Oui**.  Laissez le paramètre « Nombre de jours avant que les utilisateurs ne soient invités à reconfirmer leurs informations d’authentification » sur la valeur par défaut de 180.   Remarquez l’encadré informatif sur la page.

1. Dans le volet de navigation de gauche, sélectionnez **Notifications**.  

1. Assurez-vous que le paramètre Notifier les utilisateurs en cas de réinitialisation de mot de passe est défini sur **Oui**.  Laissez le paramètre Notifier tous les administrateurs quand d’autres administrateurs réinitialisent leur mot de passe sur Non.

1. Notez que le volet de navigation Réinitialisation du mot de passe comprend également des options permettant d’afficher les journaux d’audit et les informations sur l’utilisation et les insights.

1. Fermez la fenêtre de réinitialisation de mot de passe en sélectionnant le **X** en haut à droite de l’écran. Vous êtes alors renvoyé au centre d’administration Microsoft Entra.

1. Ne fermez pas la fenêtre Microsoft Entra.

### Tâche 2

Dans cette tâche, en tant qu’administrateur, vous allez ajouter l’utilisateur que vous avez créé dans l’exercice de labo précédent au groupe de sécurité SSPR.

1. Ouvrez l’onglet du navigateur pour la page d’accueil du centre d’administration Microsoft Entra **[entra.microsoft.com](https://entra.microsoft.com)**. Si nécessaire, développez **Identité**.

1. Dans le volet de navigation de gauche, sous « Identité », développez **Groupes** puis sélectionnez **Tous les groupes**.

1. Une liste des groupes existants s’affiche. Dans le champ Rechercher des groupes, saisissez **SSPR**, puis sélectionnez **SSPRSecurityGroupUsers** dans les résultats de recherche.  Vous accédez à l’option de configuration de ce groupe.

1. Dans le volet de navigation de gauche, sélectionnez **Membres**.

1. En haut de la page, sélectionnez **+ Ajouter des membres**.  

1. Dans la zone de recherche, saisissez **Sara Perez**.  Une fois que l’utilisateur **Sara Perez** apparaît sous la zone de recherche, sélectionnez-le, puis appuyez sur **Sélectionner** en bas de la page.  Vous revenez à la page des membres.  Sélectionnez **Actualiser** dans la partie supérieure de la page. Vous devriez maintenant voir Sara Perez dans la liste des membres du groupe de sécurité SSPR.

1. Déconnectez-vous de tous les onglets du navigateur en cliquant sur l’icône de l’utilisateur à côté de l’adresse e-mail dans le coin supérieur droit de l’écran. Ensuite, fermez toutes les fenêtres du navigateur.

### Tâche 3

Dans cette tâche, en tant qu’utilisateur Sara Perez, vous allez suivre le processus d’inscription pour réinitialiser votre mot de passe en libre-service.  Cette tâche nécessite un appareil mobile sur lequel vous pouvez recevoir des SMS.

1. Ouvrez Microsoft Edge et saisissez **https://login.microsoft.com** dans la barre d’adresses.

1. Connectez-vous en tant que Sara Perez.

1. Une fenêtre contextuelle s’affiche indiquant que d’autres informations sont requises.  La configuration demande que les membres du groupe SSPRSecurityGroupUsers s’inscrivent lorsqu’ils se connectent.  Sélectionnez le bouton **Suivant**.  Remarque : au lieu de demander aux utilisateurs de procéder eux-mêmes à l’inscription, les administrateurs peuvent configurer directement les méthodes d’authentification lors de l’ajout d’un utilisateur. Pour ce faire, les administrateurs doivent connaître et définir les numéros de téléphone et les adresses e-mail dont se servent les utilisateurs pour effectuer la réinitialisation de mot de passe en libre-service, et réinitialiser le mot de passe d’un utilisateur.

1. La page « Sécuriser votre compte » s’ouvre.  La fenêtre qui s’affiche concerne la méthode Microsoft Authenticator qui nécessite l’application Authenticator.  Pour ce labo, nous allons utiliser une autre méthode pour éviter d’avoir à télécharger l’application.  Sélectionnez **Je veux configurer une autre méthode**.
    1. Dans la fenêtre contextuelle qui s’affiche, sélectionnez la flèche déroulante, **Téléphone**, puis **Confirmer**.
    1. Vous êtes invité à entrer un numéro de téléphone. Assurez-vous que l’option **Recevoir un code** est activée.   Saisissez le numéro de téléphone sur lequel vous pouvez recevoir le code et sélectionnez **Suivant**.  
    1. Une nouvelle fenêtre s’ouvre, indiquant qu’un code a été envoyé au numéro de téléphone que vous avez entré.  Entrez le code que vous avez reçu, puis sélectionnez **Suivant**. Une fenêtre s’ouvre, indiquant que le code a été vérifié. Sélectionnez **Suivant**, puis **Terminé**.  

1. Vous pouvez maintenant terminer votre connexion. Si vous constatez que le délai de connexion a expiré, entrez à nouveau le mot de passe.

1. Déconnectez-vous de tous les onglets du navigateur en cliquant sur l’icône de l’utilisateur à côté de l’adresse e-mail dans le coin supérieur droit de l’écran. Ensuite, fermez toutes les fenêtres du navigateur.

### Tâche 4 (facultative)

Dans cette tâche, vous adopterez le rôle de l’utilisateur, Sara Perez, et vous réinitialiserez votre mot de passe.

1. Ouvrez Microsoft Edge.

1. Dans la barre d’adresse, entrez **https://login.microsoftonline.com** .

1. Connectez-vous en tant que Sara Perez en saisissant votre adresse e-mail **sara@WWLxZZZZ.onmicrosoft.com** (où ZZZZZZ est votre ID de locataire unique fourni par le fournisseur d’hébergement de labo) et sélectionnez le bouton **Suivant**. Il se peut que la fenêtre Choisir un compte s’ouvre. Si c’est le cas, sélectionnez le compte de Sara Perez.

1. Sur la page Saisie du mot de passe, sélectionnez **Mot de passe oublié**.

1. La fenêtre Revenir à votre compte s’ouvre.   Vérifiez que l’e-mail pour Sara Perez, sara@WWLxZZZZ.onmicrosoft.com, s’affiche dans la zone E-mail ou Nom d’utilisateur.  Si ce n’est pas le cas, saisissez-le.  

1. Dans la zone vide, saisissez les caractères affichés dans l’image ou les mots de l’audio. Une fois que vous les avez saisis, sélectionnez **Suivant**.

1. L’écran affiche Revenir à votre compte et indique Étape de vérification 1 > choisir un nouveau mot de passe. Laissez le paramètre par défaut **Envoyer un SMS sur mon téléphone mobile**.  Vous êtes invité à entrer votre numéro de téléphone mobile.  Une fois que vous l’avez entré, sélectionnez le bouton **Suivant**. 

1. Saisissez le code de vérification et appuyez sur **Suivant**.

1. Dans l’écran suivant, vous êtes invité à entrer un nouveau mot de passe et à le confirmer.  Saisissez-les maintenant et sélectionnez le bouton **Terminer**.

1. Un message indiquant que votre mot de passe a été réinitialisé s’affiche à l’écran.  Sélectionnez **Cliquer ici** pour vous connecter avec votre nouveau mot de passe.

1. Dans la zone d’informations Choisir un compte, sélectionnez **sara@WWLxZZZZZZ.onmicrosoft.com**, saisissez votre nouveau mot de passe, puis appuyez sur le bouton **Se connecter**.  Si vous êtes invité à rester connecté, sélectionnez **Non**.

1. Vous devriez maintenant être connecté au compte Microsoft de Sara.

1. Déconnectez-vous en sélectionnant l’icône d’utilisateur à côté de l’adresse e-mail, dans le coin supérieur droit de l’écran, et en sélectionnant **Se déconnecter**. Ensuite, fermez toutes les fenêtres de navigation.

### Tâche 5 (facultative)

Dans cette tâche, en tant qu’administrateur, vous allez brièvement consulter les journaux d’audit, ainsi que les informations et données d’utilisation associées à la réinitialisation du mot de passe.

1. Ouvrez Microsoft Edge.

1. Dans la barre d’adresses, saisissez **https://entra.microsoft.com** et connectez-vous avec les informations d’identification d’admin Microsoft 365 fournies par votre hôte de labo autorisé (ALH).

1. Vous êtes dans le centre d’administration Microsoft Entra.  Dans le volet de navigation gauche, développez l’option de **Protection**, puis sélectionnez **Réinitialisation de mot de passe**.

1. Dans le volet de navigation de gauche, sélectionnez **Journaux d’audit**.  Remarquez les informations et les filtres disponibles.  Remarquez également que vous pouvez télécharger les journaux.  

1. Sélectionnez **Télécharger**.  Remarquez que vous pouvez les télécharger au format CSV ou JSON.  Fermez la fenêtre en sélectionnant le **X** en haut à droite.

1. Dans le volet de navigation de gauche, sélectionnez **Utilisation et insights**.

1. Remarquez les informations disponibles concernant l’inscription.  Remarquez que l’actualisation de ces données peut prendre du temps, même après une actualisation, de sorte qu’elles peuvent ne pas encore refléter les données d’inscription ou d’utilisation de la tâche précédente.

1. En haut de la page, sélectionnez **Utilisation** pour afficher le nombre de réinitialisations de mot de passe en libre-service et le nombre de déverrouillages de comptes par méthode.  Remarquez que l’actualisation de ces données peut prendre du temps, même après une actualisation, de sorte qu’elles peuvent ne pas encore refléter les données d’utilisation de la tâche précédente.

1. Fermez les onglets de navigateur.

### Révision

Dans ce labo, en tant qu’administrateur, vous avez suivi le processus d’activation de la réinitialisation du mot de passe en libre-service. Une fois la réinitialisation de mot de passe en libre-service (SSPR) activée, vous adopterez le rôle d’un utilisateur pour vous inscrire à SSPR et vous réinitialiserez votre mot de passe.  Enfin, en tant qu’administrateur, vous avez appris où accéder aux journaux d’audit et aux données d’utilisation et d’insights pour SSPR.
