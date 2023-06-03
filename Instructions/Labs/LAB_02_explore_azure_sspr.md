<a name="---"></a><!---
---
Labo : Titre : « Découvrir Azure AD Authentication avec réinitialisation de mot de passe en libre-service » Parcours d’apprentissage/Module/Unité : « Parcours d’apprentissage : Décrire les fonctionnalités d’Azure Active Directory (Azure AD) - Solution Microsoft Entra ; Module 2 : Décrire les fonctionnalités d’authentification d’Azure AD ; Unité 4 : Décrire la réinitialisation de mot de passe en libre-service (SSPR) dans Azure AD »
---
--->

# <a name="lab-explore-azure-ad-authentication-with-self-service-password-reset"></a>Labo : Découvrir l’authentification Azure AD avec réinitialisation de mot de passe en libre-service

Ce labo correspond au contenu Learn suivant :

- Parcours d’apprentissage : Décrire les fonctionnalités d’Azure Active Directory (Azure AD) - Solution Microsoft Entra
- Module : Décrire les fonctionnalités d’authentification d’Azure AD
- Unité : Décrire la réinitialisation de mot de passe en libre-service (SSPR) dans Azure AD

## <a name="lab-scenario"></a>Scénario du labo

Dans ce labo, vous allez suivre le processus d’activation de la réinitialisation du mot de passe en libre-service en tant qu’administrateur. Une fois la réinitialisation de mot de passe en libre-service (SSPR) activée, vous adopterez le rôle d’un utilisateur, vous vous inscrirez à SSPR et vous réinitialiserez votre mot de passe.  Enfin, en tant qu’administrateur, vous serez en mesure de consulter les journaux d’audit, ainsi que les informations et données d’utilisation de SSPR.

**Durée estimée** : 15-20 minutes

### <a name="task-1"></a>Tâche 1

Dans cette tâche, en tant qu’administrateur, vous allez ajouter un utilisateur existant, Annette Varieur, au groupe SSPRSecurityUsers.  Vous devrez également réinitialiser le mot de passe de l’utilisateur afin de pouvoir vous connecter pour la première fois, en tant qu’utilisateur, et vous inscrire à SSPR.

1. Ouvrez Microsoft Edge.

2. Dans la barre d’adresse, entrez **portal.azure.com** et connectez-vous avec vos informations d’identification.
    1. Dans la fenêtre de connexion, entrez **admin@WWLxZZZZZZ.onmicrosoft.com** (où ZZZZZZ représente votre ID de locataire unique communiqué par votre fournisseur d’hébergement de labo), puis sélectionnez **Suivant**.
    1. Entrez le mot de passe d’administrateur qui vous a été communiqué par votre fournisseur d’hébergement de labo. Sélectionnez **Connexion**.
    1. Lorsque vous êtes invité à rester connecté, sélectionnez **Oui**.

3. Sélectionnez **Azure Active Directory**.  

4. Dans le volet de navigation gauche, sélectionnez **Groupes**.

5. Une liste de groupes existants s’affiche. Dans le champ Rechercher des groupes, saisissez **SSPR**, puis sélectionnez **SSPRSecurityGroupUsers** dans les résultats de la recherche.  Vous accédez ainsi à l’option de configuration de ce groupe.

6. Dans le volet de navigation de gauche, sélectionnez **Membres**.

7. En haut de la page, sélectionnez **+ Ajouter des membres**.  

8. Dans la zone de recherche, saisissez **Annette**.  Une fois que l’utilisateur, **Annette Varieur**, apparaît sous la zone de recherche, sélectionnez-le, puis appuyez sur **Sélectionner** en bas de la page.

9. Fermez la fenêtre SSPRSecurityUsers en sélectionnant le **X** dans le coin supérieur droit de l’écran.

10. Revenez à la page Active Directory, en sélectionnant **Contoso** dans le coin supérieur gauche de l’écran, juste au-dessus de la mention Groupes, pour revenir à la page Contoso Azure Active Directory.

11. Dans le volet de navigation de gauche, sélectionnez **Utilisateurs**.

12. Sélectionnez **Annette Varieur** dans la liste des utilisateurs.

13. Sélectionnez **Réinitialiser le mot de passe**  en haut de la page. Comme vous ne vous êtes encore jamais connecté en tant qu’Annette Varieur, vous devez réinitialiser le mot de passe.

14. À l’ouverture de la fenêtre de réinitialisation du mot de passe, sélectionnez **Réinitialiser le mot de passe**.  IMPORTANT : Notez le nouveau mot de passe. Vous en aurez besoin pour vous connecter en tant qu’utilisateur lors d’une tâche ultérieure.

15. Fermez la fenêtre de réinitialisation du mot de passe en sélectionnant le **X** dans le coin supérieur droit de la page.

16. Fermez la fenêtre Annette Varieur en sélectionnant le **X** dans le coin supérieur droit de la page.

17. Fermez la fenêtre Utilisateurs en sélectionnant le **X** dans le coin supérieur droit de la page.

18. Laissez la fenêtre de présentation de Contoso ouverte. Vous l’utiliserez dans la tâche suivante.

### <a name="task-2"></a>Tâche 2

Dans cette tâche, vous apprendrez, en tant qu’administrateur, à configurer la réinitialisation du mot de passe pour les utilisateurs, y compris les types de méthodes d’authentification à utiliser.

1. Accédez à l’onglet Contoso - Microsoft Azure ouvert dans votre navigateur. Si vous avez fermé l’onglet, ouvrez une page du navigateur et saisissez portal.azure.com dans la barre d’adresse. Ensuite, sélectionnez Azure Active Directory.  Vous devriez être connecté en tant qu’administrateur dans le portail Azure : si ce n’est pas le cas, reconnectez-vous.

1. Dans le volet de navigation de gauche, sélectionnez **Réinitialisation du mot de passe**.  

1. Les propriétés de la réinitialisation de mot de passe en libre-service sont affichées.  Assurez-vous que l’option **Réinitialisation en libre-service** est **sélectionnée** pour le groupe listé, **SSPRSecurityGroupUsers**.  Passez le curseur de la souris sur l’icône d’information à côté de l’indication « sélectionner un groupe » et notez la description : « Définit le groupe d’utilisateurs qui sont autorisés à réinitialiser leurs propres mots de passe ». Vous devez inclure des utilisateurs dans le groupe : vous ne pouvez pas sélectionner des utilisateurs de manière individuelle.  En outre, si vous changez de groupe, celui que vous sélectionnez remplace alors le groupe actuellement répertorié.  C’est pourquoi il est conseillé d’ajouter des utilisateurs au groupe SSPR.  Enfin, prenez note de la zone d’informations bleue indiquant « Ces paramètres ne s’appliquent qu’aux utilisateurs finaux de votre organisation. Les administrateurs bénéficient toujours du libre-service pour la réinitialisation de leur mot de passe et doivent utiliser deux méthodes d’authentification pour réinitialiser leur mot de passe. »

1. Dans le volet de navigation gauche de Réinitialisation du mot de passe, sélectionnez **Méthodes d’authentification**.

1. Dans l’option Nombre de méthodes requises pour réinitialiser, sélectionnez **1**. Notez la zone d’informations à l’écran.

1. Notez les différentes méthodes dont disposent les utilisateurs.  Les cases **E-mail** et **Téléphone mobile (SMS uniquement)** doivent déjà être cochées. Si ce n’est pas le cas, sélectionnez-les.

1. Dans le volet de navigation gauche de Réinitialisation du mot de passe, sélectionnez **Inscription**.  

1. Assurez-vous que le paramètre Exiger que les utilisateurs s’inscrivent quand ils se connectent ? est défini sur **Oui**.  Laissez le paramètre « Nombre de jours avant que les utilisateurs ne soient invités à reconfirmer leurs informations d’authentification » sur la valeur par défaut de 180.   Notez la zone d’informations sur la page.

1. Dans le volet de navigation gauche de Réinitialisation du mot de passe, sélectionnez **Notifications**.  

1. Assurez-vous que le paramètre Notifier les utilisateurs lors des réinitialisations de mot de passe ? est défini sur **Oui**.  Laissez le paramètre Notifier tous les administrateurs quand d’autres administrateurs réinitialisent leur mot de passe ? défini sur non.

1. Prenez note de la manière dont le volet de navigation de la réinitialisation de mot de passe inclut également des options servant à afficher les journaux d’audit ainsi que les informations et données d’utilisation.

1. **Déconnectez-vous** de tous les onglets de navigation en cliquant sur l’icône d’utilisateur à côté de l’adresse e-mail en haut à droite de l’écran. Ensuite, fermez toutes les fenêtres de navigation.

### <a name="task-3"></a>Tâche 3

Dans cette tâche, vous adopterez le rôle de l’utilisateur, Annette Varieur, et vous vous inscrirez à la réinitialisation de mot de passe en libre-service.  Cette tâche nécessite un appareil mobile sur lequel vous pouvez recevoir des SMS ou un compte e-mail personnel auquel vous avez accès.

1. Ouvrez Microsoft Edge.

2. Dans la barre d’adresse, entrez **login.microsoftonline.com**.

3. Connectez-vous en tant qu’Annette Varieur.
    1. Dans la fenêtre de connexion, entrez **AdeleV@WWLxZZZZZZ.onmicrosoft.com** (où ZZZZZZ représente votre ID de locataire unique fourni par votre fournisseur d’hébergement de labo), puis sélectionnez **Suivant**.
    1. Saisissez le mot de passe que vous avez noté lors de la tâche précédente. Sélectionnez **Connexion**.
    1. Lorsque vous êtes invité à rester connecté, sélectionnez **Oui**.


4. Comme il s’agit de votre première connexion en tant qu’Annette Varieur, un message vous demandera de réinitialiser votre mot de passe.  Saisissez votre ancien mot de passe.  Pour votre nouveau mot de passe, entrez **SC900-Lab**. Saisissez **SC900-Lab** dans le champ de confirmation du mot de passe.  Sélectionnez **Connexion**.  Remarque : Nous utilisons ce mot de passe uniquement pour les besoins du labo. La meilleure pratique consiste à saisir un mot de passe plus sûr.

5. Une fenêtre contextuelle s’affiche pour indiquer que d’autres informations sont nécessaires.  La configuration demande que les membres du groupe SSPRSecurityGroupUsers s’inscrivent lorsqu’ils se connectent.  Sélectionnez le bouton **Suivant**.  Remarque :  Les administrateurs peuvent directement configurer les méthodes d’authentification lorsqu’ils ajoutent un utilisateur, plutôt que de demander aux utilisateurs de s’inscrire eux-mêmes. Pour ce faire, les administrateurs doivent connaître et définir les numéros de téléphone et les adresses e-mail dont se servent les utilisateurs pour effectuer la réinitialisation de mot de passe en libre-service, et réinitialiser le mot de passe d’un utilisateur.

6. La page « Sécuriser votre compte » s’ouvre.  La fenêtre qui s’affiche concerne la méthode d’authentification par téléphone. Si vous ne disposez pas d’un appareil mobile permettant de recevoir des SMS, passez à l’étape suivante.  Vous êtes invité à entrer un numéro de téléphone. Assurez-vous que l’option **Envoyez-moi un code par SMS** est activée.   Saisissez le numéro de téléphone sur lequel vous pouvez recevoir un code par SMS et appuyez sur le **bouton Suivant**.  Une nouvelle fenêtre s’ouvre, indiquant qu’un code a été envoyé au numéro de téléphone que vous avez entré.  Saisissez le code reçu et sélectionnez **Suivant**. Une fenêtre s’ouvre indiquant Opération réussie et votre méthode de connexion par défaut.  Sélectionnez **Terminé**.  

7. Ignorez cette étape si vous avez pu configurer SSPR avec votre numéro de téléphone mobile.  Vous pouvez également définir une autre méthode, comme indiqué dans le coin inférieur gauche de la fenêtre.  Si vous choisissez de définir une méthode différente, sélectionnez **Je veux définir une méthode différente**. Ensuite, une fenêtre contextuelle s’affiche et vous demande : Quelle méthode souhaitez-vous utiliser ?  Dans la liste déroulante, sélectionnez votre méthode par défaut, **E-mail**, puis sélectionnez le bouton **Confirmer**.  Saisissez l’adresse e-mail que vous souhaitez utiliser, puis sélectionnez **Suivant**.  Une nouvelle fenêtre s’ouvre, indiquant qu’un code a été envoyé à l’adresse e-mail que vous avez entrée.  Accédez à l’adresse e-mail que vous avez saisie pour obtenir le code.  Saisissez le code reçu et sélectionnez **Suivant**. Une fenêtre s’ouvre indiquant Opération réussie et votre méthode de connexion par défaut.  Sélectionnez **Terminé**.

8. Vous pouvez maintenant terminer votre connexion.  Vous devez être dans la page d’accueil du portail Azure.  Si vous constatez que le délai de connexion a expiré, entrez à nouveau le mot de passe, SC900-Lab.

9. Déconnectez-vous du portail Azure et fermez la fenêtre du navigateur.

### <a name="task-4-optional"></a>Tâche 4 (facultative)

Dans cette tâche, vous adopterez le rôle de l’utilisateur, Annette Varieur, et vous réinitialiserez votre mot de passe.

1. Ouvrez Microsoft Edge.

2. Dans la barre d’adresse, entrez **login.microsoftonline.com**.

3. Connectez-vous en tant qu’Annette Varieur en saisissant votre adresse e-mail **AdeleV@WWLxZZZZ.onmicrosoft.com** (où ZZZZZZ est votre ID de locataire unique fourni par le fournisseur d’hébergement de labo) et appuyez sur le bouton **Suivant**. Il se peut qu’une fenêtre Choisir un compte s’ouvre à la place. Dans ce cas, sélectionnez le compte d’Annette Varieur.

4. Dans la fenêtre Saisir le mot de passe, sélectionnez **J’ai oublié mon mot de passe**.

5. La fenêtre Réaccéder à votre compte s’ouvre.   Vérifiez que l’e-mail pour Adele Vance, AdeleV@WWLxZZZZ.onmicrosoft.com, s’affiche dans la zone E-mail ou Nom d’utilisateur.  Si ce n’est pas le cas, saisissez-la.  

6. Dans la case vide, saisissez les caractères affichés dans l’image ou les mots que vous entendez. Une fois que vous les avez saisis, sélectionnez **Suivant**.

7. L’écran affiche Réaccéder à votre compte et indique Vérification étape 1 > choisir un nouveau mot de passe. Conservez le paramètre par défaut **Envoyer un SMS à mon téléphone mobile**.  Vous êtes invité à entrer votre numéro de téléphone mobile.  Une fois que vous l’avez entré, sélectionnez le bouton **Suivant**.  Si vous avez sélectionné la méthode par e-mail au moment de l’inscription, la fenêtre Réaccéder à votre compte indique ceci : Vous allez recevoir sur votre adresse de messagerie secondaire un e-mail contenant un code de vérification.  Sélectionnez **E-mail**.

8. Saisissez le code de vérification, puis appuyez sur **Suivant**.

9. Dans l’écran suivant, vous êtes invité à entrer un nouveau mot de passe et à le confirmer.  Saisissez-le et appuyez sur le bouton **Terminer**.

10. Un message indiquant que votre mot de passe a été réinitialisé s’affiche à l’écran.  Sélectionnez **cliquer ici** pour vous connecter avec votre nouveau mot de passe.

11. Dans la zone d’informations Choisir un compte, sélectionnez **AdeleV@WWLxZZZZZZ.onmicrosoft.com** , saisissez votre nouveau mot de passe, puis appuyez sur le bouton **Se connecter**.  Si vous êtes invité à rester connecté, Sélectionnez **Non**.

12. Vous devez maintenant vous trouver dans le portail Office.

13. Déconnectez-vous en cliquant sur l’icône d’utilisateur à côté de l’adresse e-mail, dans le coin supérieur droit de l’écran, et en sélectionnant **Se déconnecter**. Ensuite, fermez toutes les fenêtres du navigateur.

### <a name="task-5-optional"></a>Tâche 5 (facultative)

Dans cette tâche, en tant qu’administrateur, vous allez brièvement consulter les journaux d’audit, ainsi que les informations et données d’utilisation associées à la réinitialisation du mot de passe.

1. Ouvrez Microsoft Edge.

2. Dans la barre d’adresse, entrez **portal.azure.com**

3. Connectez-vous avec vos informations d’identification d’administrateur.
    1. Dans la fenêtre de connexion, entrez **admin@WWLxZZZZZZ.onmicrosoft.com** (où ZZZZZZ représente votre ID de locataire unique communiqué par votre fournisseur d’hébergement de labo), puis sélectionnez **Suivant**.
    1. Entrez le mot de passe d’administrateur qui vous a été communiqué par votre fournisseur d’hébergement de labo. Sélectionnez **Connexion**.
    1. Lorsque vous êtes invité à rester connecté, sélectionnez **Oui**.

4. Sélectionnez **Azure Active Directory**.  

5. Dans le volet de navigation de gauche, sélectionnez **Réinitialisation du mot de passe**.

6. Dans le volet de navigation de gauche, sélectionnez **Journaux d’audit**.  Notez les informations et les filtres disponibles.  Notez également que vous pouvez télécharger les journaux.  

7. Sélectionnez **Télécharger**.  Notez que vous pouvez formater le fichier téléchargé au format CSV ou JSON.  Fermez la fenêtre en sélectionnant le **X** dans le coin supérieur droit de l’écran.

8. Dans le volet de navigation de gauche, sélectionnez **Utilisation et informations**.

9. Notez les informations disponibles relatives à l’inscription.  Notez que l’actualisation de ces données peut prendre un certain temps, même après avoir effectué une actualisation. Il se peut donc qu’elles ne reflètent pas encore les données d’inscription ou d’utilisation de la tâche précédente.

10. En haut de la page, sélectionnez **Utilisation** pour consulter le nombre de réinitialisations de mot de passe en libre-service et de déverrouillages de comptes par méthode.  Notez que l’actualisation de ces données peut prendre un certain temps, même après avoir effectué une actualisation. Il se peut donc qu’elles ne reflètent pas encore les données d’utilisation de la tâche précédente.

11. Fermez les onglets de votre navigateur.

### <a name="review"></a>Révision

Dans ce labo, vous avez suivi le processus d’activation de la réinitialisation du mot de passe en libre-service en tant qu’administrateur. Une fois la réinitialisation de mot de passe en libre-service (SSPR) activée, vous adopterez le rôle d’un utilisateur pour vous inscrire à SSPR et vous réinitialiserez votre mot de passe.  Enfin, en tant qu’administrateur, vous découvrez où accéder aux journaux d’audit, ainsi qu’aux informations et données d’utilisation de SSPR.
