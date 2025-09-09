---
lab:
  title: Explorer Privileged Identity Management
  module: Describe the identity protection and governance capabilities of Microsoft Entra
---

# Labo : Explorer Privileged Identity Management

Ce labo correspond au contenu Learn suivant :

- Parcours d’apprentissage : Décrire les fonctionnalités de Microsoft Entra
- Module : décrire les fonctionnalités de gouvernance et de protection des identités de Microsoft Entra
- Unité : Décrire les fonctionnalités de Privileged Identity Management

## Scénario du labo

Dans ce labo, vous allez découvrir certaines fonctionnalités de base de Privileged Identity Management (PIM). PIM nécessite une licence Microsoft Entra ID P2.  Dans ce labo, en tant qu’administrateur, vous allez configurer l’un de vos utilisateurs, Dominic Saucier, avec un rôle Administrateur d’utilisateurs Microsoft Entra, à l’aide de Privileged Identity Management (PIM).   Avec les privilèges Administrateur utilisateur, Diego pourra créer des utilisateurs et des groupes, gérer des licences, et bien plus encore.  À la fois administrateur et utilisateur, Dominic doit avoir accès aux licences Microsoft Entra ID P2.

**Durée estimée :** 60 minutes

### Tâche 1

Dans cette tâche, en tant qu’administrateur, vous réinitialiserez le mot de passe de l’utilisateur Diego Siciliani. Cette étape est nécessaire pour que vous puissiez vous connecter initialement en tant qu’utilisateur dans les tâches suivantes.

1. Ouvrez Microsoft Edge.  Dans la barre d’adresse, entrez **https://entra.microsoft.com** .

1. Connectez-vous avec les informations d’identification d’administrateur Microsoft 365 fournies par votre ALH.
    1. Dans la fenêtre de connexion, entrez **admin@WWLxZZZZZZ.onmicrosoft.com** (où ZZZZZZ est votre ID de locataire unique communiqué par votre ALH), puis sélectionnez **Suivant**.
    1. Entrez le mot de passe d’administrateur qui vous a été communiqué par votre fournisseur d’hébergement de labo. Cliquez sur **Connexion**.
    1. Selon votre hébergeur de labo et si c’est la première fois que vous vous connectez au locataire, vous serez peut-être invité à terminer le processus d’inscription MFA. Si c’est le cas, suivez les invites à l’écran pour configurer la MFA.
    1. Une fois connecté, vous êtes redirigé vers la page Centre d’administration Microsoft 365.

1. Dans le volet de navigation gauche, développez **Identités**, développez **Utilisateurs**, puis sélectionnez **Tous les utilisateurs**.

1. Sélectionnez **Diego Siciliani** dans la liste des utilisateurs.

1. Sélectionnez **Réinitialiser le mot de passe** en haut de la page. Comme vous ne vous êtes jamais connecté en tant que Dominic Saucier, vous ne connaissez pas le mot de passe de cet utilisateur et vous devez le réinitialiser.

1. Lorsque la fenêtre de réinitialisation du mot de passe s’ouvre, sélectionnez **Réinitialiser le mot de passe**.  IMPORTANT : Notez le nouveau mot de passe. Vous en aurez besoin pour vous connecter en tant qu’utilisateur lors d’une tâche ultérieure.

1. Dans le volet de navigation à gauche, sélectionnez **Accueil** pour retourner à la page d’accueil du centre d’administration Microsoft Entra.

1. Gardez cette page du navigateur ouverte, car vous en aurez besoin dans la tâche suivante.

### Tâche 2

Dans cette tâche, en tant qu’administrateur, vous affectez un rôle Microsoft Entra ID à Dominic dans Privileged Identity Management.

1. Ouvrez l’onglet du navigateur pour la page d’accueil du centre d’administration Microsoft Entra.

1. Dans le panneau de navigation de gauche, développez **Gouvernance des identités**, puis sélectionnez **Gestion des identités privilégiées**.

1. Vous vous trouvez maintenant sur la page de démarrage rapide de Privileged Identity Management. Passez en revue les informations de la page Démarrage. Dans la fenêtre principale, sous l’emplacement intitulé Gérer l’accès, sélectionnez **Gérer**.

1. Vous êtes maintenant dans la page Rôles Contoso.  Dans la barre de recherche, en haut de la page, saisissez **utilisateur**.  Dans les résultats de la recherche, sélectionnez **Administrateur d’utilisateurs**.

1. En haut de la page, sélectionnez **+ Ajouter des affectations**.

1. Sur la page Ajouter des affectations, assurez-vous que l’option **Adhésion** est soulignée.  Ici, vous configurez les paramètres d’appartenance pour le rôle Administrateur d’utilisateurs dans PIM.

1. Laissez la valeur par défaut du type d’étendue : Annuaire.  

1. Sous Sélectionner des membres, sélectionnez **Aucun membre sélectionné**. La fenêtre Sélectionner un membre s’ouvre.

1. Dans la barre de recherche, saisissez **Diego**.  Dans les résultats de la recherche, sélectionnez **Diego Siciliani**, puis appuyez sur **Sélectionner** en bas de la page.  

1. Sous Sélectionner des membres, vous voyez 1 membre(s) sélectionné(s), ainsi que le nom et l’adresse e-mail du membre sélectionné, à savoir Dominic Saucier dans notre exemple. En bas de la page Ajouter des affectations, sélectionnez **Suivant**.  

1. Vous êtes maintenant dans la page Paramètres.  Laissez la valeur par défaut du paramètre Type d’affectation : Éligible.

1. Si la case Éligible en permanence est cochée, sélectionnez **Éligible en permanence** pour supprimer la coche.

1. Dans les champs Début de l’affectation, conservez la date et l’heure par défaut, à savoir aujourd’hui et l’heure actuelle.

1. Dans les champs Fin de l’affectation, modifiez la date pour qu’elle corresponde à la date d’aujourd’hui. (Notez que la valeur par défaut est d’un an à partir d’aujourd’hui, vous devez donc modifier l’année). Pour l’heure, définissez deux heures à partir de l’heure actuelle. Après avoir défini le champ de l’heure de fin de l’affectation, appuyez sur la touche de tabulation de votre clavier et sélectionnez **Affecter** en bas de la page.  

1. Vous revenez ainsi à la fenêtre Affectations.  Après quelques secondes, vous devriez voir Diego Siciliani listé dans la table de l’Administrateur d’utilisateurs, avec les informations de l’affectation. Si, après quelques secondes, vous ne voyez toujours pas la mise à jour, sélectionnez **Actualiser** en haut de la page.

1. En haut de la page, sélectionnez **Paramètres**.

1. Dans les informations relatives au rôle de l’Administrateur d’utilisateurs, remarquez les différentes options.  Notez que le paramètre « Exiger une justification lors de l’activation » est défini sur « Oui », et « Lors de l’activation, exiger la MFA Azure » est également défini sur « Oui ».  Ces deux paramètres apparaîtront dans la tâche suivante, lorsque Dominic activera le rôle.  Notez également que l’autorisation « Exiger une approbation pour l’activation » est définie sur Non.  Réinitialise les paramètres à leurs valeurs par défaut.  Fermez la page en sélectionnant le **X** en haut à droite de l’écran.

1. Déconnectez-vous en sélectionnant l’icône d’utilisateur à côté de l’adresse e-mail, dans le coin supérieur droit de l’écran, et en sélectionnant **Se déconnecter**. Ensuite, fermez toutes les fenêtres de navigation.

### Tâche 3

Dans cette tâche, vous adopterez le rôle de Dominic Saucier et vous vous connecterez au centre d’administration Microsoft Entra. Ensuite, vous accéderez à la fonctionnalité Privileged Identity Management de Microsoft Entra afin d’activer le rôle Administrateur d’utilisateurs qui vous a été attribué.  Une fois le rôle activé, vous apporterez quelques modifications à la configuration d’un utilisateur existant. Remarque : pour cette tâche, vous devez avoir accès à un appareil mobile à utiliser avec l’application Microsoft Authenticator.

1. Ouvrez Microsoft Edge.  Dans la barre d’adresse du navigateur, entrez **Entra.microsoft.com**.

1. Connectez-vous en tant que Diego Siciliani.
    1. Dans la fenêtre de connexion, entrez **DiegoS@WWLxZZZZZZ.onmicrosoft.com** (où ZZZZZZ représente votre ID de locataire unique communiqué par votre fournisseur d’hébergement de labo), puis sélectionnez **Suivant**.
    1. Entrez le mot de passe temporaire que vous avez noté lors de la tâche précédente et sélectionnez **Se connecter**.  Cliquez sur **Connexion**.
    1. Le mot de passe que vous avez entré étant un mot de passe temporaire, vous devez le changer maintenant. Entrez le mot de passe actuel, entrez un nouveau mot de passe, puis confirmez le nouveau mot de passe.  Notez ce nouveau mot de passe, car vous en aurez besoin pour accomplir la tâche.
    1. Comme c’est votre première connexion en tant que Diego, il peut vous être demandé d'installer l’authentification multifacteur. Suivez les invites à l’écran pour installer l’authentification multifacteur.
    1. Lorsque vous êtes invité à rester connecté, sélectionnez **Oui**.

1. Vous devez être connecté au centre d’administration Microsoft Entra.
1. Dans le volet de navigation gauche, développez **Gouvernance ID**, puis sélectionnez **Privileged Identity Management**.
1. Dans le volet de navigation de gauche, sélectionnez **Mes rôles**.  Vous voyez maintenant des informations sur vos affectations éligibles.  Vous constatez que vous, Dominic, avez le rôle Administrateur d’utilisateurs.  
1. Dans la dernière colonne de la table, Action étiquetée, sélectionnez **Activer**.
1. Vous voyez une icône d’avertissement indiquant qu’une vérification supplémentaire est requise.  Sélectionnez **Cliquez pour continuer**.  Rappelez-vous que les paramètres PIM pour le rôle Administrateur d’utilisateurs exigent une authentification multifacteur.  De plus, comme les informations de contact de Diego à utiliser pour la MFA (méthode d’authentification) n’ont pas été configurées auparavant, il doit enregistrer ses informations, pour pouvoir utiliser la MFA.  Bien qu’il doive utiliser la MFA à chaque fois qu’il se connecte en tant qu’Administrateur d’utilisateurs, le processus d’enregistrement de la MFA n’est nécessaire qu’une seule fois au cours de la période d’affectation.
1. La fenêtre qui s’affiche et les étapes qui suivent concernent la méthode de l’application Microsoft Authenticator. .
    1. Si vous avez déjà installé l’application Microsoft Authenticator sur votre appareil mobile, sélectionnez **Suivant**. Sinon, sélectionnez **Télécharger maintenant** et suivez les étapes.
    1. Vous commencerez à configurer votre compte.  Cliquez sur **Suivant**.
    1. À l’aide de l’application Microsoft Authenticator sur votre appareil mobile, sélectionnez **+** pour ajouter un compte, puis sélectionnez **Compte professionnel ou scolaire**.
    1. Sélectionnez l’option pour **Numériser le code QR** puis, sur votre appareil mobile, numérisez le code QR sur l’écran de votre PC.
    1. À l’aide de l’application Microsoft Authenticator sur votre appareil mobile, numérisez le code QR.
    1. Suivez les étapes sur votre PC et votre appareil mobile, puis sélectionnez **Suivant**.
    1. Une fois que vous avez configuré vos informations de sécurité, une fenêtre de réussite s’affiche.  Cliquez sur **Terminé**.

1. Une fois le processus d’inscription MFA terminé, vous êtes ramené vers la page Administrateur d’utilisateurs actifs PIM.
1. La fenêtre Activer l’Administrateur d’utilisateurs s’affiche.  Vous devez entrer la raison de l’activation.  Dans la boîte qui s’affiche, saisissez le motif de votre choix (500 caractères maximum), puis sélectionnez **Activer**.
1. L’état (3 étapes de progression) s’affiche au fil du processus d’activation.
1. Une fois l’activation terminée, vous revenez dans la page Mes rôles | Rôles Microsoft Entra ID, où vous voyez une notification vous informant que vous avez activé un rôle.  Sélectionnez **Cliquez ici** pour afficher vos rôles actifs.  Si vous remarquez que l’heure de fin est différente de celle qui a été configurée à l’origine, sélectionnez le bouton Actualiser en haut de la page (l’actualisation peut prendre quelques minutes).
1. Retournez à la page d’accueil du centre d’administration Microsoft Entra en sélectionnant **Accueil** depuis le volet de navigation à gauche. 
1. En tant qu’administrateur d’utilisateurs Microsoft Entra ID, vous pouvez créer des utilisateurs et des groupes, gérer les licences, et davantage. Dans le volet de navigation de gauche, développez **Identités**, puis sélectionnez **Utilisateurs**.
1. Dans la liste des utilisateurs, sélectionnez **Bianca Pisani**.
1. Dans le volet de navigation de gauche, sélectionnez **Groupes**.
1. Notez les groupes auxquels Bianca est déjà affectée. En haut de la page, sélectionnez **+ Appartenances**.
1. Dans la liste des groupes, sélectionnez **Équipe du projet Mark 8**.
1. En bas de la page, cliquez sur **Sélectionner**.
1. Dans la page Groupes, notez que le groupe de l’équipe du projet Mark 8 a été ajouté à la liste (si vous ne le voyez pas immédiatement, sélectionnez le bouton **Actualiser**).
1. Déconnectez-vous en sélectionnant l’icône d’utilisateur à côté de l’adresse e-mail, dans le coin supérieur droit de l’écran, et en sélectionnant **Se déconnecter**. Ensuite, fermez toutes les fenêtres de navigation.
1. La durée du rôle Administrateur d’utilisateurs est limitée à la durée qui a été configurée.

### Révision

Dans ce labo, vous avez découvert PIM.  En tant qu’administrateur, vous avez configuré Diego avec des privilèges d’administrateur d’utilisateurs pour une durée déterminée.  Ensuite, en tant que Diego, vous avez suivi le processus d’activation des privilèges Administrateur d’utilisateurs et d’un utilisateur d’un groupe.  Rappelez-vous que PIM nécessite une licence Microsoft Entra ID Premium P2.
