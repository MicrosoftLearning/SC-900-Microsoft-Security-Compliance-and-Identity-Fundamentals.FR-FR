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

## Scénario de démonstration

Cette démonstration vous permettra de découvrir les divers paramètres associés à l’activation de la réinitialisation de mot de passe en libre-service (SSPR).

1. Revenez à l’onglet ouvert du navigateur intitulé « Centre d’administration accueil Microsoft Entra ».  Si vous avez précédemment fermé cet onglet de navigateur, ouvrez Microsoft Edge et connectez-vous à **[entra.microsoft.com](https://entra.microsoft.com)** avec vos informations d’identification d’administrateur Microsoft 365.

1. Dans le volet de navigation gauche, développez **Protection**, puis sélectionnez **Réinitialisation de mot de passe**.

1. L’onglet Propriétés est en surbrillance.  Dans la fenêtre Propriétés, vous remarquerez que SSPR peut être activé pour Aucun, Sélectionner ou Tous.
    1. Placez votre curseur sur l’icône d’information à côté de la mention « Réinitialisation du mot de passe en libre-service activée » et signalez que vous pouvez choisir « Sélectionné » pour restreindre la réinitialisation du mot de passe à un groupe limité d’utilisateurs, par opposition à « Aucun » ou « Tous ».
    1. Placez votre curseur sur l’icône d’information à côté de la mention « Sélectionner un groupe » et précisez qu’il s’agit de l’endroit où vous identifiez le groupe d’utilisateurs autorisés à réinitialiser eux-mêmes leur mot de passe.   Vous devez inclure des utilisateurs dans le groupe, vous ne pouvez pas les sélectionner individuellement.  De plus, si vous modifiez le groupe, le groupe que vous sélectionnez remplace le groupe actuellement répertorié.  C’est pourquoi il est conseillé d’ajouter des utilisateurs au groupe SSPR.
    1. Remarquez le cadre d’information bleu clair et attirez l’attention des participants sur le fait que ces paramètres ne s’appliquent qu’aux utilisateurs finaux de votre organisation. Les administrateurs bénéficient toujours du libre-service pour la réinitialisation de leur mot de passe, et doivent utiliser deux méthodes d’authentification pour réinitialiser leur mot de passe.

1. Dans le volet de navigation gauche, développez Protection, puis sélectionnez Méthodes d’authentification.
    1. Placez votre curseur sur l’icône d’information à côté de la mention « Nombre de méthodes nécessaires à la réinitialisation ».  Précisez que ce paramètre définit le nombre de méthodes d’identification alternatives dont un utilisateur de ce répertoire doit disposer pour réinitialiser son mot de passe.   Ne modifiez pas le paramètre.
    1. Expliquez les différentes « méthodes disponibles pour les utilisateurs », y compris la prise en charge des questions de sécurité par le SSPR. Sélectionnez Questions de sécurité pour afficher les options d’utilisation des questions de sécurité. Quand vous avez fini la présentation des options, revenez en arrière et sélectionnez Questions de sécurité afin de décocher ce sujet.

1. Dans le volet de navigation de gauche, sélectionnez Inscription.
    1. Passez votre souris sur l’icône d’information située à côté de la mention « Obliger les utilisateurs à s’inscrire durant la connexion ».   Faites-le remarquer aux utilisateurs.  
    1. Passez le curseur de la souris sur l’icône d’information à côté de l’indication « Nombre de jours avant que les utilisateurs ne soient invités à reconfirmer leurs informations d’authentification ».   Faites-le remarquer aux utilisateurs.  

1. Dans le volet de navigation de gauche, sélectionnez Notifications.  Expliquez les deux paramètres. Passez votre souris sur l’icône d’information pour obtenir la description.

1. Notez que le volet de navigation Réinitialisation du mot de passe comprend également des options permettant d’afficher les journaux d’audit et les informations sur l’utilisation et les insights.

1. Sélectionnez le X en haut à droite pour fermer la page. Cette opération vous renvoie à la page principale du locataire Contoso.

1. Gardez cette page du navigateur ouverte pour la prochaine démo.

### Révision

Dans cette démo, vous avez montré les paramètres associés à la réinitialisation du mot de passe en libre-service.
