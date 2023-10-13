<!---
---
Démonstration : Titre : « Réinitialisation de mot de passe en libre-service Microsoft Entra (SSPR) » Parcours d’apprentissage/Module/Unité : « Parcours d’apprentissage : Décrire les fonctionnalités de Microsoft Entra ; Module 2 : Décrire les fonctionnalités d’authentification de Microsoft Entra ID ; Unité 4 : Décrire la réinitialisation de mot de passe en libre-service (SSPR) »
---
--->

# Démonstration : réinitialisation de mot de passe en libre-service (SSPR) Microsoft Entra

Cette démonstration correspond au contenu Learn suivant :

- Parcours d’apprentissage : décrire les fonctionnalités de Microsoft Entra
- Module : décrire les fonctionnalités d’authentification de Microsoft Entra ID
- Unité : décrire la réinitialisation du mot de passe en libre-service

## Scénario de la démonstration

Cette démonstration vous permettra de découvrir les divers paramètres associés à l’activation de la réinitialisation de mot de passe en libre-service (SSPR).

1. Revenez à l’onglet ouvert du navigateur intitulé « Centre d’administration accueil Microsoft Entra ».  Si vous avez précédemment fermé cet onglet de navigateur, ouvrez Microsoft Edge et connectez-vous à **[entra.microsoft.com](https://entra.microsoft.com)** avec vos informations d’identification d’administrateur Microsoft 365.

1. Dans le volet de navigation gauche, développez **Protection**, puis sélectionnez **Réinitialisation de mot de passe**.

1. L’onglet des propriétés apparaît en surbrillance.  Dans la fenêtre Propriétés, vous remarquerez que SSPR peut être activé pour Aucun, Sélectionné ou Tous.
    1. Survolez l’icône d’information près de l’intitulé « Réinitialisation de mot de passe activée » avec votre curseur. Expliquez que vous pouvez choisir « Sélectionné » pour limiter la réinitialisation de mot de passe à un groupe limité d’utilisateurs, ou encore choisir Aucun ou Tous.
    1. Survolez l’icône d’information près de l’intitulé « Sélectionner un groupe » avec votre curseur et expliquez que c’est ici que vous identifiez le groupe d’utilisateurs autorisés à réinitialiser leurs propres mots de passe.   Vous devez inclure des utilisateurs dans le groupe : vous ne pouvez pas sélectionner des utilisateurs de manière individuelle.  En outre, si vous changez de groupe, celui que vous sélectionnez remplace alors le groupe actuellement répertorié.  C’est pourquoi il est conseillé d’ajouter des utilisateurs au groupe SSPR.
    1. Vous remarquerez qu’une zone d’informations bleu clair s’affiche. Expliquez la raison de sa présence aux participants : elle précise que ces paramètres s’appliquent uniquement aux utilisateurs finaux dans l’organisation. Les administrateurs bénéficient toujours du libre-service pour la réinitialisation de leur mot de passe, et doivent utiliser deux méthodes d’authentification pour réinitialiser leur mot de passe.

1. Dans le volet de navigation de gauche de la réinitialisation de mot de passe, sélectionnez Méthodes d’authentification.
    1. Survolez l’icône d’information près de l’intitulé « Nombre de méthodes nécessaires à la réinitialisation » avec votre curseur.  Expliquez que cette option permet de définir le nombre de méthodes d’identification alternatives qu’un utilisateur dans ce répertoire doit disposer pour réinitialiser son mot de passe.   Ne modifiez pas ce paramètre.
    1. Expliquez les différentes « méthodes à la disposition des utilisateurs » et précisez notamment que SSPR prend en charge les questions de sécurité. Sélectionnez Questions de sécurité pour afficher les options d’utilisation des questions de sécurité. Quand vous avez fini la présentation des options, revenez en arrière et sélectionnez Questions de sécurité afin de décocher ce sujet.

1. Dans le volet de navigation gauche de la réinitialisation de mot de passe, sélectionnez Enregistrement.
    1. Survolez l’icône d’information près de l’intitulé « Exiger l’enregistrement des utilisateurs lors de leur connexion » avec votre curseur.   Expliquez cela aux utilisateurs.  
    1. Passez le curseur de la souris sur l’icône d’information à côté de l’indication « Nombre de jours avant que les utilisateurs ne soient invités à reconfirmer leurs informations d’authentification ».   Expliquez cela aux utilisateurs.  

1. Dans le volet de navigation gauche de la réinitialisation de mot de passe, sélectionnez Notifications.  Survolez l’icône d’information avec votre curseur pour obtenir une description et expliquez les deux paramètres.

1. Prenez note de la manière dont le volet de navigation de la réinitialisation de mot de passe inclut également des options servant à afficher les journaux d’audit ainsi que les informations et données d’utilisation.

1. Cliquez sur le X en haut à droite de la page. Cela vous ramène à la page principale du locataire Contoso.

1. Gardez cette page du navigateur ouverte pour la démonstration suivante.

### Révision

Dans cette démonstration, vous avez montré les paramètres associés à la réinitialisation de mot de passe en libre-service.
