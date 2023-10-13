<!---
---
Labo : Titre : « Explorer Privileged Identity Management. » Parcours d’apprentissage/Module/Unité : « Parcours d’apprentissage : Décrire les fonctionnalités de Microsoft Entra ; Module 4 : Module : Décrire les fonctionnalités de protection et de gouvernance des identités de Microsoft Entra ; Unité 4 : Décrire les fonctionnalités de Privileged Identity Management »
---
--->

# Labo : Explorer Privileged Identity Management

Ce labo correspond au contenu Learn suivant :

- Parcours d’apprentissage : Décrire les fonctionnalités de Microsoft Entra
- Module : décrire les fonctionnalités de gouvernance et de protection des identités de Microsoft Entra
- Unité : Décrire les fonctionnalités de Privileged Identity Management

## Scénario du labo

Dans ce labo, vous allez découvrir certaines fonctionnalités de base de Privileged Identity Management (PIM). PIM nécessite une licence Microsoft Entra ID P2.  Dans ce labo, en tant qu’administrateur, vous allez configurer l’un de vos utilisateurs, Dominic Saucier, avec un rôle Administrateur d’utilisateurs Microsoft Entra, à l’aide de Privileged Identity Management (PIM).   Les privilèges d’administrateur d’utilisateurs permettront à Dominic de créer des utilisateurs et des groupes, de gérer les licences, etc.  À la fois administrateur et utilisateur, Dominic doit avoir accès aux licences Microsoft Entra ID P2.

**Durée estimée** : 45-60 minutes

### Tâche 1

Dans cette tâche, en tant qu’administrateur, vous réinitialiserez le mot de passe de l’utilisateur Dominic Saucier. Cette étape est nécessaire pour pouvoir se connecter initialement en tant qu’utilisateur dans les tâches ultérieures.

1. Ouvrez Microsoft Edge.  Dans la barre d’adresse, entrez **https://entra.microsoft.com** .

1. Connectez-vous avec les informations d’identification d’administrateur Microsoft 365 fournies par votre ALH.
    1. Dans la fenêtre de connexion, entrez **admin@WWLxZZZZZZ.onmicrosoft.com** (où ZZZZZZ est votre ID de locataire unique communiqué par votre ALH), puis sélectionnez **Suivant**.
    1. Entrez le mot de passe d’administrateur qui vous a été communiqué par votre fournisseur d’hébergement de labo. Sélectionnez **Connexion**.
    1. Lorsque vous êtes invité à rester connecté, sélectionnez **Oui**.

1. Dans le volet de navigation gauche, développez **Identités**, développez **Utilisateurs**, puis sélectionnez **Tous les utilisateurs**.

1. Sélectionnez **Dominic Saucier** dans la liste des utilisateurs.

1. Sélectionnez **Réinitialiser le mot de passe**  en haut de la page. Comme vous ne vous êtes jamais connecté en tant que Dominic Saucier, vous ne connaissez pas le mot de passe de cet utilisateur et vous devez le réinitialiser.

1. À l’ouverture de la fenêtre de réinitialisation du mot de passe, sélectionnez **Réinitialiser le mot de passe**.  IMPORTANT : Notez le nouveau mot de passe. Vous en aurez besoin pour vous connecter en tant qu’utilisateur lors d’une tâche ultérieure.

1. Dans le volet de navigation à gauche, sélectionnez **Accueil** pour retourner à la page d’accueil du centre d’administration Microsoft Entra.

1. Gardez cette page du navigateur ouverte, car vous en aurez besoin dans la tâche suivante.

### Tâche 2

Dans cette tâche, en tant qu’administrateur, vous allez affecter un rôle Azure AD à Dominic dans Privileged Identity Management.

1. Ouvrez l’onglet du navigateur pour la page d’accueil du centre d’administration Microsoft Entra.

1. Dans le volet de navigation gauche, sous « Identité », développez **Gouvernance des identités**, puis sélectionnez **Privileged Identity Management**.

1. Vous vous trouvez maintenant sur la page de démarrage rapide de Privileged Identity Management. Passez en revue les informations de la page Démarrage. Sélectionnez **Gérer**.

1. Vous êtes maintenant dans la page Rôles Contoso.  Dans la barre de recherche en haut de la page, saisissez **Utilisateur**.  Dans les résultats de la recherche, sélectionnez **Administrateur d’utilisateurs**.

1. En haut de la page, sélectionnez **+ Ajouter des affectations**.

1. Sur la page Ajouter des affectations, assurez-vous que l’option **Appartenance** est soulignée.  Ici, vous configurez les paramètres d’appartenance pour le rôle Administrateur d’utilisateurs dans PIM.

1. Conservez la valeur par défaut du type d’étendue, à savoir Répertoire.  

1. Sous Sélectionner des membres, sélectionnez **Aucun membre sélectionné**. Cela ouvre la fenêtre Sélectionner un membre.

1. Dans la barre de recherche, saisissez **Dominic**.  Dans les résultats de la recherche, sélectionnez **Dominic Saucier**, puis appuyez sur **Sélectionner** au bas de la page.  

1. Sous Sélectionner des membres, vous voyez 1 membre(s) sélectionné(s), ainsi que le nom et l’adresse e-mail du membre sélectionné, à savoir Dominic Saucier dans notre exemple. Au bas de la page Ajouter des affectations, sélectionnez **Suivant**.  

1. Vous êtes maintenant dans la page Paramètres.  Conservez le paramètre par défaut du type d’affectation, à savoir Éligible.

1. Si la case Éligible en permanence est cochée, sélectionnez **Éligible en permanence**, pour désactiver le champ.

1. Dans les champs Début d’affectation, conservez la date et l’heure par défaut, à savoir aujourd’hui et l’heure actuelle.

1. Dans les champs Fin d’affectation, remplacez la date par la date d’aujourd’hui (notez que le paramètre par défaut correspond à la date actuelle dans un an, vous devez donc modifier l’année). Réglez l’heure en ajoutant deux heures à l’heure actuelle. Après avoir défini l’heure à laquelle l’affectation se termine, appuyez sur la touche Tab du clavier et sélectionnez **Affecter** au bas de la page.  

1. Cela vous renvoie à la fenêtre Affectations.  Après quelques secondes, Dominic Saucier devrait apparaître dans le tableau Administrateur d’utilisateurs, avec les détails de l’affectation. Si rien ne se passe au bout de quelques secondes, sélectionnez **Actualiser** en haut de la page.

1. En haut de la page, sélectionnez **Paramètres**.

1. Différentes options sont disponibles dans les détails relatifs à l’Administrateur d’utilisateurs du paramètre Rôle.  Notez que le paramètre « Exiger une justification lors de l’activation » est défini sur oui, tout comme le paramètre « Exiger Azure MFA lors de l’activation ».  Ces deux paramètres apparaîtront dans la tâche suivante, lorsque Dominic activera le rôle.  Notez également que l’autorisation « Exiger une approbation pour l’activation » est définie sur Non.  Réinitialise les paramètres à leurs valeurs par défaut.  Fermez la page en sélectionnant le **X** dans le coin supérieur droit de l’écran.

1. Déconnectez-vous en cliquant sur l’icône d’utilisateur à côté de l’adresse e-mail, dans le coin supérieur droit de l’écran, et en sélectionnant **Se déconnecter**. Ensuite, fermez toutes les fenêtres de navigation.

### Tâche 3

Dans cette tâche, vous adopterez le rôle de Dominic Saucier et vous vous connecterez au centre d’administration Microsoft Entra. Ensuite, vous accéderez à la fonctionnalité Privileged Identity Management de Microsoft Entra afin d’activer le rôle Administrateur d’utilisateurs qui vous a été attribué.  Une fois le rôle activé, vous apporterez quelques modifications à la configuration d’un utilisateur existant. Remarque : Pour cette tâche, vous devrez avoir un accès immédiat à un appareil mobile qui vous permettra de recevoir des SMS.

1. Ouvrez Microsoft Edge.  Dans la barre d’adresse du navigateur, entrez **Entra.microsoft.com**.

1. Connectez-vous en tant que Dominic Saucier.
    1. Dans la fenêtre de connexion, entrez **DiegoS@WWLxZZZZZZ.onmicrosoft.com** (où ZZZZZZ représente votre ID de locataire unique fourni par votre fournisseur d’hébergement de labo), puis sélectionnez **Suivant**.
    1. Entrez le mot de passe temporaire que vous avez noté lors de la tâche précédente et sélectionnez **Se connecter**.  Sélectionnez **Connexion**.
    1. Le mot de passe que vous avez entré étant un mot de passe temporaire, vous devez le changer maintenant. Entrez le mot de passe actuel, entrez un nouveau mot de passe, puis confirmez le nouveau mot de passe.  Notez ce nouveau mot de passe, car vous en aurez besoin pour accomplir la tâche.
    1. Lorsque vous êtes invité à rester connecté, sélectionnez **Oui**.

1. Vous devez être connecté au centre d’administration Microsoft Entra.
1. Dans le volet de navigation gauche, développez **Gouvernance des identités**, puis sélectionnez **Privileged Identity Management**.
1. Dans le volet de navigation de gauche, sélectionnez **Mes rôles**.  Vous voyez maintenant des informations sur vos affectations éligibles.  Vous constatez que vous, Dominic, avez le rôle Administrateur d’utilisateurs.  
1. Dans la dernière colonne du tableau, intitulée Action, sélectionnez **Activer**.
1. Vous voyez une icône d’avertissement indiquant qu’une vérification supplémentaire est requise.  Sélectionnez **Cliquer pour continuer**.  Rappelez-vous que les paramètres PIM pour le rôle Administrateur d’utilisateurs exigent une authentification multifacteur.  De plus, comme les coordonnées de Dominic n’ont pas été configurées au préalable pour l’utilisation de la MFA (méthodes d’authentification), il doit enregistrer ses informations afin de pouvoir l’utiliser.  Même s’il doit procéder à une MFA chaque fois qu’il se connecte en tant qu’administrateur d’utilisateurs, pendant la période d’affectation, le processus d’inscription MFA n’est requis qu’une seule fois.
1. Une notification vous indique que des informations supplémentaires sont requises. Sélectionnez **Suivant**.
1. Saisissez votre mot de passe.
1. Dans le coin inférieur gauche de la fenêtre de Microsoft Authenticator, sélectionnez **Je veux configurer une autre méthode.** .
1. Vous êtes invité à choisir une autre méthode.  À côté de la mention Application d’authentification, sélectionnez la flèche vers le bas.   Sélectionnez **Téléphone**, puis **Confirmer**.
1. Vous êtes invité à entrer un numéro de téléphone de votre choix. Assurez-vous que l’indicatif du pays de votre numéro de téléphone est exact.  Saisissez votre numéro de téléphone, assurez-vous que l’option **Envoyez-moi un code par SMS** est sélectionnée, puis sélectionnez **Suivant**.
1. Saisissez le code à 6 chiffres que vous avez reçu sur votre téléphone et sélectionnez **Suivant**.
1. Une notification vous indique que votre téléphone a été inscrit. Sélectionnez **Suivant**, puis **Terminé**.
1. Un message vous demande si vous souhaitez rester connecté.  Sélectionnez **Oui**.
1. La fenêtre Activer Administrateur d’utilisateurs apparaît.  Vous devez entrer la raison de l’activation.  Dans la zone qui s’affiche, saisissez la raison de votre choix (500 caractères maximum), puis sélectionnez **Activer**.
1. L’état (3 étapes de progression) s’affiche au fil du processus d’activation.
1. Une fois l’activation terminée, vous revenez dans la page Mes rôles | Rôles Azure AD, où vous voyez une notification vous informant que vous avez activé un rôle.  Sélectionnez **Cliquer ici** pour consulter vos rôles actifs.  Si vous remarquez que l’heure de fin est différente de celle qui a été configurée à l’origine, sélectionnez la touche d’actualisation en haut de la page (l’actualisation peut prendre quelques minutes).
1. Retournez à la page d’accueil du centre d’administration Microsoft Entra en sélectionnant **Accueil** depuis le volet de navigation à gauche. 
1. En tant qu’administrateur d’utilisateurs Azure AD, vous pouvez créer des utilisateurs et des groupes, de gérer les licences, etc. Dans le volet de navigation gauche, développez **Identités**, sélectionnez **Utilisateurs**, puis sélectionnez **Tous les utilisateurs**.
1. Dans la liste des utilisateurs, sélectionnez **Bernadette Plourde**.
1. Dans le volet de navigation de gauche, sélectionnez **Licences**.
1. Notez qu’aucune licence n’est affectée à Bernadette.  En haut de la page, sélectionnez **+ Affectations**.
1. Dans la liste des licences sélectionnées, sélectionnez **Office 365 E3** et **Windows 10 Enterprise E3**.
1. Au bas de la page, sélectionnez **Enregistrer**.  Une brève notification s’affiche dans le coin supérieur droit de la page, indiquant que les licences ont été attribuées.
1. Fermez la page des affectations de licence mises à jour, en sélectionnant le **X** dans le coin supérieur droit de la page.
1. Déconnectez-vous en cliquant sur l’icône d’utilisateur à côté de l’adresse e-mail, dans le coin supérieur droit de l’écran, et en sélectionnant **Se déconnecter**. Ensuite, fermez toutes les fenêtres de navigation.
1. La durée du rôle Administrateur d’utilisateurs est limitée à la durée qui a été configurée.

### Révision

Dans ce labo, vous avez découvert PIM.  En tant qu’administrateur, vous avez configuré les privilèges d’administrateur d’utilisateurs de Dominic pour une durée déterminée.  Ensuite, vous avez adopté le rôle de Dominic et avez suivi le processus d’activation des privilèges d’administrateur d’utilisateurs et de configuration des paramètres utilisateur.  Rappelez-vous que PIM nécessite des licences Azure AD Premium P2.
