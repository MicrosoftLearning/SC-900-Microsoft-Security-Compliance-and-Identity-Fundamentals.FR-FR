---
lab:
  title: 'Explorer la gouvernance des identités dans Azure AD avec Privileged Identity Management'
  module: 'Module 4 : Décrire les fonctionnalités de protection et de gouvernance des identités d’Azure AD'
---


# <a name="lab-explore-identity-governance-in-azure-ad-with-privileged-identity-management"></a>Labo : Découvrir la gouvernance des identités dans Azure AD avec Privileged Identity Management

Ce labo correspond au contenu Learn suivant :

- Parcours d’apprentissage : Décrire les fonctionnalités d’Azure Active Directory (Azure AD) - Solution Microsoft Entra
- Module : Décrire les fonctionnalités de gouvernance et de protection des identités d’Azure AD
- Unité : Décrire les fonctionnalités de Privileged Identity Management

## <a name="lab-scenario"></a>Scénario du labo

Dans ce labo, vous allez découvrir certaines fonctionnalités de base de Privileged Identity Management (PIM). PIM nécessite Azure AD Premium P2.  Dans ce labo, en tant qu’administrateur, vous allez configurer l’un de vos utilisateurs, Dominic Saucier, avec un rôle Administrateur d’utilisateurs Azure AD, à l’aide de Privileged Identity Management (PIM).   Les privilèges d’administrateur d’utilisateurs permettront à Dominic de créer des utilisateurs et des groupes, de gérer les licences, etc.  À la fois administrateur et utilisateur, Dominic doit avoir accès aux licences Azure AD Premium P2.

**Durée estimée** : 45-60 minutes

### <a name="task-1"></a>Tâche 1

Dans cette tâche, en tant qu’administrateur, vous réinitialiserez le mot de passe de l’utilisateur Dominic Saucier. Cette étape est nécessaire pour pouvoir se connecter initialement en tant qu’utilisateur dans les tâches ultérieures.

1. Ouvrez Microsoft Edge.  Dans la barre d’adresse, entrez **portal.azure.com**.

2. Connectez-vous avec vos informations d’identification d’administrateur.
    1. Dans la fenêtre de connexion, entrez **admin@WWLxZZZZZZ.onmicrosoft.com** (où ZZZZZZ représente votre ID de locataire unique fourni par votre fournisseur d’hébergement de labo), puis sélectionnez **Suivant**.
    1. Entrez le mot de passe d’administrateur qui vous a été communiqué par votre fournisseur d’hébergement de labo. Sélectionnez **Connexion**.
    1. Lorsque vous êtes invité à rester connecté, sélectionnez **Oui**.

3. Sélectionnez **Azure Active Directory**.  

4. Dans le volet de navigation de gauche, sélectionnez **Utilisateurs**.

5. Sélectionnez **Dominic Saucier** dans la liste des utilisateurs.

6. Sélectionnez **Réinitialiser le mot de passe**  en haut de la page. Comme vous ne vous êtes jamais connecté en tant que Dominic Saucier, vous ne connaissez pas le mot de passe de cet utilisateur et vous devez le réinitialiser.

7. À l’ouverture de la fenêtre de réinitialisation du mot de passe, sélectionnez **Réinitialiser le mot de passe**.  IMPORTANT : Notez le nouveau mot de passe. Vous en aurez besoin pour vous connecter en tant qu’utilisateur lors d’une tâche ultérieure.

8. Fermez la fenêtre de réinitialisation du mot de passe en sélectionnant le **X** dans le coin supérieur droit de la page.

9. Fermez la fenêtre de profil de Dominic en sélectionnant le **X** dans le coin supérieur droit de la page.

10. Fermez la fenêtre Tous les utilisateurs en sélectionnant le **X** dans le coin supérieur droit de la page. Vous devez maintenant être dans la page Contoso Azure Active Directory.

11. Gardez cette page du navigateur ouverte, car vous en aurez besoin dans la tâche suivante.

### <a name="task-2"></a>Tâche 2

Dans cette tâche, en tant qu’administrateur, vous allez affecter un rôle Azure AD à Dominic dans Privileged Identity Management.

1. Accédez à l’onglet du navigateur ouvert intitulé Contoso - Microsoft Azure.   Si vous avez fermé l’onglet du navigateur, ouvrez Microsoft Edge. Dans la barre d’adresse, saisissez portal.azure.com, connectez-vous avec vos informations d’identification d’administrateur, puis sélectionnez Azure Active Directory.  

2. Dans le volet de navigation de gauche, sélectionnez **Identity Governance**.

3. Dans le volet de navigation de gauche, sous Privileged Identity Management, sélectionnez **Rôles Azure AD**.

4. Vous vous trouvez maintenant dans la fenêtre de démarrage rapide de Privileged Identity Management.  Sélectionnez **Gérer**.

5. Vous êtes maintenant dans la page Rôles Contoso.  Dans la barre de recherche en haut de la page, saisissez **Utilisateur**.  Dans les résultats de la recherche, sélectionnez **Administrateur d’utilisateurs**.

6. En haut de la page, sélectionnez **+ Affectations**.

7. Sur la page Ajouter des affectations, assurez-vous que l’option **Appartenance** est soulignée.  Ici, vous configurez les paramètres d’appartenance pour le rôle Administrateur d’utilisateurs dans PIM.

8. Conservez la valeur par défaut du type d’étendue, à savoir Répertoire.  

9. Sous Sélectionner des membres, sélectionnez **Aucun membre sélectionné**. Cela ouvre la fenêtre Sélectionner un membre.

10. Dans la barre de recherche, saisissez **Dominic**.  Dans les résultats de la recherche, sélectionnez **Dominic Saucier**, puis appuyez sur **Sélectionner** au bas de la page.  

11. Sous Sélectionner des membres, vous voyez 1 membre(s) sélectionné(s), ainsi que le nom et l’adresse e-mail du membre sélectionné, à savoir Dominic Saucier dans notre exemple. Au bas de la page Ajouter des affectations, sélectionnez **Suivant**.  

12. Vous êtes maintenant dans la page Paramètres.  Conservez le paramètre par défaut du type d’affectation, à savoir Éligible.

13. Si la case Éligible en permanence est cochée, sélectionnez **Éligible en permanence**, pour désactiver le champ.

14. Dans les champs Début d’affectation, conservez la date et l’heure par défaut, à savoir aujourd’hui et l’heure actuelle.

15. Dans les champs Fin d’affectation, remplacez la date par la date d’aujourd’hui (notez que le paramètre par défaut correspond à la date actuelle dans un an, vous devez donc modifier l’année). Réglez l’heure en ajoutant deux heures à l’heure actuelle. Après avoir défini l’heure à laquelle l’affectation se termine, appuyez sur la touche Tab du clavier et sélectionnez **Affecter** au bas de la page.  

16. Cela vous renvoie à la fenêtre Affectations.  Après quelques secondes, Dominic Saucier devrait apparaître dans le tableau Administrateur d’utilisateurs, avec les détails de l’affectation. Si rien ne se passe au bout de quelques secondes, sélectionnez **Actualiser** en haut de la page.

17. En haut de la page, sélectionnez **Paramètres**.

18. Différentes options sont disponibles dans les détails relatifs à l’Administrateur d’utilisateurs du paramètre Rôle.  Notez que le paramètre « Exiger une justification lors de l’activation » est défini sur oui, tout comme le paramètre « Exiger Azure MFA lors de l’activation ».  Ces deux paramètres apparaîtront dans la tâche suivante, lorsque Dominic activera le rôle.  Notez également que l’autorisation « Exiger une approbation pour l’activation » est définie sur Non.  Réinitialise les paramètres à leurs valeurs par défaut.  Fermez la page en sélectionnant le **X** dans le coin supérieur droit de l’écran.

19. Déconnectez-vous en cliquant sur l’icône d’utilisateur à côté de l’adresse e-mail, dans le coin supérieur droit de l’écran, et en sélectionnant **Se déconnecter**. Ensuite, fermez toutes les fenêtres de navigation.

### <a name="task-3"></a>Tâche 3

Dans cette tâche, vous adopterez le rôle de Dominic Saucier et vous vous connecterez au portail Azure. Ensuite, vous accéderez à la fonctionnalité Privileged Identity Management d’Azure Active Directory afin d’activer le rôle Administrateur d’utilisateurs qui vous a été attribué.  Une fois le rôle activé, vous apporterez quelques modifications à la configuration d’un utilisateur existant. Remarque : Pour cette tâche, vous devrez avoir un accès immédiat à un appareil mobile qui vous permettra de recevoir des SMS.

1. Ouvrez Microsoft Edge.  Dans la barre d’adresse du navigateur, saisissez **portal.azure.com**.

1. Connectez-vous en tant que Dominic Saucier.
    1. Dans la fenêtre de connexion, entrez **DiegoS@WWLxZZZZZZ.onmicrosoft.com** (où ZZZZZZ représente votre ID de locataire unique fourni par votre fournisseur d’hébergement de labo), puis sélectionnez **Suivant**.
    1. Entrez le mot de passe temporaire que vous avez noté lors de la tâche précédente et sélectionnez **Se connecter**.  Sélectionnez **Connexion**.
    1. Le mot de passe que vous avez entré étant un mot de passe temporaire, vous devez le changer maintenant. Saisissez le mot de passe actuel.  Pour les champs du nouveau mot de passe et de confirmation du mot de passe, entrez **SC900-Lab**.
    1. Lorsque vous êtes invité à rester connecté, sélectionnez **Oui**.

1. Vous devez maintenant être connecté au portail Azure.
1. Sur la page d’accueil principale, sous les services Azure, sélectionnez **Azure Active Directory**.
1. Dans le volet de navigation de gauche, sélectionnez **Identity Governance**.
1. Dans le volet de navigation de gauche, sous Privileged Identity Management, sélectionnez **Rôles Azure AD**.
1. Dans le volet de navigation de gauche, sélectionnez **Mes rôles**.  Des informations sur vos rôles Azure AD apparaissent maintenant.  Vous constatez que vous, Dominic, avez le rôle Administrateur d’utilisateurs.  
1. Dans la dernière colonne du tableau, intitulée Action, sélectionnez **Activer**.
1. Vous voyez une icône d’avertissement indiquant qu’une vérification supplémentaire est requise.  Sélectionnez **Cliquer pour continuer**.  Rappelez-vous que les paramètres PIM pour le rôle Administrateur d’utilisateurs exigent une authentification multifacteur.  De plus, comme les coordonnées de Dominic n’ont pas été configurées au préalable pour l’utilisation de la MFA (méthodes d’authentification), il doit enregistrer ses informations afin de pouvoir l’utiliser.  Même s’il doit procéder à une MFA chaque fois qu’il se connecte en tant qu’administrateur d’utilisateurs, pendant la période d’affectation, le processus d’inscription MFA n’est requis qu’une seule fois.
1. Une notification vous indique que des informations supplémentaires sont requises. Sélectionnez **Suivant**.
1. Saisissez votre mot de passe, **SC900-Lab**.
1. Dans le coin inférieur gauche de la fenêtre de Microsoft Authenticator, sélectionnez **Je veux configurer une autre méthode.** .
1. Vous êtes invité à choisir une autre méthode.  À côté de la mention Application d’authentification, sélectionnez la flèche vers le bas.   Sélectionnez **Téléphone**, puis **Confirmer**.
1. Vous êtes invité à entrer un numéro de téléphone de votre choix. Assurez-vous que l’indicatif du pays de votre numéro de téléphone est exact.  Saisissez votre numéro de téléphone, assurez-vous que l’option **Envoyez-moi un code par SMS** est sélectionnée, puis sélectionnez **Suivant**.
1. Saisissez le code à 6 chiffres que vous avez reçu sur votre téléphone et sélectionnez **Suivant**.
1. Une notification vous indique que votre téléphone a été inscrit. Sélectionnez **Suivant**, puis **Terminé**.
1. Un message vous demande si vous souhaitez rester connecté.  Sélectionnez **Oui**.
1. La fenêtre Activer Administrateur d’utilisateurs apparaît.  Vous devez entrer la raison de l’activation.  Dans la zone qui s’affiche, saisissez la raison de votre choix (500 caractères maximum), puis sélectionnez **Activer**.
1. L’état (3 étapes de progression) s’affiche au fil du processus d’activation.
1. Une fois l’activation terminée, vous revenez dans la page Mes rôles | Rôles Azure AD, où vous voyez une notification vous informant que vous avez activé un rôle.  Sélectionnez **Cliquer ici** pour consulter vos rôles actifs.  Si vous remarquez que l’heure de fin est différente de celle qui a été configurée à l’origine, sélectionnez la touche d’actualisation en haut de la page (l’actualisation peut prendre quelques minutes).
1. Fermez la fenêtre en sélectionnant le **X** dans le coin supérieur droit de l’écran.
1. Fermez la fenêtre Privileged Identity Management | Démarrage rapide en sélectionnant le **X** dans le coin supérieur droit de l’écran.
1. Fermez la fenêtre Identity Governance en sélectionnant le **X** dans le coin supérieur droit de l’écran.
1. Vous vous trouvez maintenant dans la page Contoso Azure Active Directory.  En tant qu’administrateur d’utilisateurs Azure AD, vous pouvez créer des utilisateurs et des groupes, de gérer les licences, etc.   Dans le volet de navigation de gauche, sélectionnez **Utilisateurs**.
1. Dans la liste des utilisateurs, sélectionnez **Bernadette Plourde**.
1. Dans le volet de navigation de gauche, sélectionnez **Licences**.
1. Notez qu’aucune licence n’est affectée à Bernadette.  En haut de la page, sélectionnez **+ Affectations**.
1. Dans la liste des licences sélectionnées, sélectionnez **Office 365 E3** et **Windows 10 Enterprise E3**.
1. Au bas de la page, sélectionnez **Enregistrer**.  Une brève notification s’affiche dans le coin supérieur droit de la page, indiquant que les licences ont été attribuées.
1. Fermez la page des affectations de licence mises à jour, en sélectionnant le **X** dans le coin supérieur droit de la page.
1. Déconnectez-vous en cliquant sur l’icône d’utilisateur à côté de l’adresse e-mail, dans le coin supérieur droit de l’écran, et en sélectionnant **Se déconnecter**. Ensuite, fermez toutes les fenêtres de navigation.
1. La durée du rôle Administrateur d’utilisateurs est limitée à la durée qui a été configurée.

### <a name="review"></a>Révision

Dans ce labo, vous avez découvert PIM.  En tant qu’administrateur, vous avez configuré les privilèges d’administrateur d’utilisateurs de Dominic pour une durée déterminée.  Ensuite, vous avez adopté le rôle de Dominic et avez suivi le processus d’activation des privilèges d’administrateur d’utilisateurs et de configuration des paramètres utilisateur.  Rappelez-vous que PIM nécessite des licences Azure AD Premium P2.
