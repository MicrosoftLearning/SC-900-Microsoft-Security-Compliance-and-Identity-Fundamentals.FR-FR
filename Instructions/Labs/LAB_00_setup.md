---
lab:
  title: Configuration du laboratoire
  module: Setup your Microsoft 365 lab tenant (not associated with a Learn module)
---

# Labo : configuration du locataire Microsoft 365

## Locataires WWL - Conditions d’utilisation
Si un locataire vous est fourni dans le cadre d’une formation dispensée par un instructeur, notez qu’il est mis à votre disposition dans le seul but de prendre en charge les labos pratiques de la formation.

Vous ne devez ni partager ni utiliser les locataires en dehors des labos pratiques. Le locataire utilisé dans ce cours est un locataire d’essai. Au terme de la classe, le locataire ne pourra pas faire l’objet d’une prolongation et vous ne pourrez plus l’utiliser ni y accéder.

Vous n’êtes pas autorisé à convertir un locataire en abonnement payant. Les locataires obtenus dans le cadre de ce cours sont la propriété de Microsoft Corporation. Nous nous réservons le droit d’y accéder et d’en reprendre possession à tout moment.

## Scénario du labo

Ce labo de configuration consiste à activer les fonctionnalités Microsoft de journal d’audit et de surveillance des fichiers dans le locataire Microsoft 365.

**Durée estimée** : 5 à 10 minutes

### Configuration - Activer le journal d’audit et la surveillance des fichiers dans Microsoft 365

Lors de cette tâche de configuration, vous allez activer les fonctionnalités de journal d’audit et de surveillance des fichiers dans Microsoft 365.  

1. Ouvrez Microsoft Edge. Dans la barre d’adresse, entrez **`https://admin.microsoft.com`** .

1. Connectez-vous avec les informations d’identification d’administrateur du locataire Microsoft 365 fournis par votre hôte de labo autorisé (ALH).

1. Sélectionnez **Tout afficher** dans le volet de navigation gauche du centre d’administration Microsoft 365.

1. Sous Centres d’administration, sélectionnez **Sécurité**.  Une nouvelle page de navigateur s’ouvre sur la page d’accueil de Microsoft Defender.

1. Dans le volet de navigation de gauche, faites défiler vers le bas et développez **Système**.  Dans la liste développée, sélectionnez **Audit**.  Remarque : la fonctionnalité d’audit est également accessible via le portail Microsoft Purview.

1. Lorsque vous accédez à la page Audit, patientez 1 à 2 minutes.  Si l’audit n’est PAS activé, vous voyez une barre bleue en haut de la page indiquant de commencer à enregistrer les activités des utilisateurs et des administrateurs.  Sélectionnez **Commencer à enregistrer les activités de l’utilisateur et de l’administrateur**.  Une fois l’audit activé, la barre bleue disparaît.  S’il n’y a pas de barre bleue, alors l’audit est déjà activé et aucune autre action n’est requise.  Si vous voyez un message : « Désolé, nous avons des difficultés à déterminer si l’activité est enregistrée. Essayez d’actualiser la page », et que rien ne change après l’actualisation de la page, vous devez activer l’audit via PowerShell.
    1. Cliquez avec le bouton droit sur l’icône Windows PowerShell dans la barre des tâches et sélectionnez **Exécuter en tant qu’administrateur**.
    1. Pour confirmer que le module Exchange Online PowerShell est installé sur l’ordinateur, entrez **`Get-InstalledModule ExchangeOnlineManagement | Format-List Name,Version,InstalledLocation`**.  Vous verrez le nom, la version et l’emplacement de l’installation d’Exchange OnlineManagement.
    1. Chargez maintenant le module en entrant **`Import-Module ExchangeOnlineManagement`**.
    1. Pour vous connecter, entrez **`Connect-ExchangeOnline -UserPrincipalName admin@WWLxZZZZZZ.onmicrosoft.com`**.  Pour l’UPN, entrez le nom d’utilisateur de l’administrateur trouvé dans l’onglet Ressources de votre labo.
    1. Vous êtes invité à vous connecter.  Entrez le nom d’utilisateur administratif et le mot de passe trouvés dans l’onglet Ressources de votre labo.
    1. Pour activer l’audit, entrez **`Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $true`**. Un message s’affiche indiquant que la modification peut prendre jusqu’à 60 minutes pour prendre effet.
    1. Bien qu’elle puisse prendre jusqu’à 60 minutes, vous pouvez vérifier que la commande a été reçue en entrant **`Get-AdminAuditLogConfig | FL UnifiedAuditLogIngestionEnabled`**.  Si l’audit est activé, la propriété UnifiedAuditLogIngestionEnabled affiche la valeur true.

1. Dans le volet de navigation de gauche, dans Système, sélectionnez **Paramètres**.

1. Dans la page des paramètres, sélectionnez **Applications cloud**.   Faites défiler vers le bas, puis, dans **Protection des données**, sélectionnez **Fichiers**.

1. Si celle-ci n’est pas déjà cochée, cochez la case située à côté de l’option **Activer la surveillance des fichiers**, puis cliquez sur **Enregistrer**.  

1. Cela conclut le labo de configuration du locataire Microsoft 365.

### Révision

Avec cette configuration, vous avez activé les fonctionnalités de journal d’audit et de surveillance des fichiers dans Microsoft 365.
