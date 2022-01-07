---
lab:
    title: 'Explorer Microsoft Defender pour le cloud'
    module : 'Module 3, leçon 2 : Décrire les fonctionnalités des solutions de sécurité Microsoft : Décrire les fonctionnalités de gestion de la sécurité d’Azure'
---

# Labo : Explorer Microsoft Defender pour le cloud

## Scénario du labo
Dans ce labo, nous allons découvrir Microsoft Defender pour le cloud et apprendre à utiliser le Niveau de sécurité Azure pour améliorer la posture de sécurité de votre organisation.

**Durée estimée** : 30 minutes

#### Tâche 1 : Dans cette tâche, vous découvrirez brièvement Microsoft Defender pour le cloud.
1.	Ouvrez Microsoft Edge. Dans la barre d’adresse, saisissez **portal.azure.com**.

1. Connectez-vous avec vos informations d’identification d’administrateur.
    1. Dans la fenêtre de connexion, saisissez **admin@WWLxZZZZZZ.onmicrosoft.com** (ZZZZZZ représente votre ID de locataire unique fourni par votre fournisseur d’hébergement de labo), puis sélectionnez **Suivant**.
    1. Saisissez le mot de passe d’administrateur fourni par votre fournisseur d’hébergement de labo. Sélectionnez **Se connecter**.
    1. Lorsque vous êtes invité à rester connecté, sélectionnez **Oui**.

1. Dans le coin supérieur gauche de l’écran, en regard de la mention Microsoft Azure, sélectionnez l’icône de menu Afficher le portail (les trois lignes horizontales également appelées icône Hamburger), puis, dans le volet de navigation de gauche, sous l’option Favoris, sélectionnez **Microsoft Defender pour le cloud**.  Si la sélection n’apparaît pas dans la liste Favoris, entrez **Microsoft Defender pour le cloud** dans la zone de recherche, puis sélectionnez **Microsoft Defender pour le cloud** dans la liste des résultats.

1. Prenez note des informations disponibles sur la page de présentation de Microsoft Defender pour le cloud.  

1. Il est possible qu’une zone d’informations bleue s’affiche en haut de la page. Cela signifie que vous consultez des informations limitées.  Sélectionnez **Cliquer ici**.
    1. Attribuez-vous le rôle nécessaire pour assurer la visibilité au niveau du locataire.  Sélectionnez **Administrateur de sécurité**, puis **Obtenir l’accès** au bas de la page.
    1. Le message suivant s’affichera probablement : Le groupe d’administration racine n’existe pas.  Conformément à la description, le système créera le groupe pour vous.  La création du groupe peut prendre jusqu’à 15 minutes (mais généralement moins).  Une fois l’accès accordé, sélectionnez **Microsoft Defender pour le cloud** dans le coin supérieur gauche de la page, au-dessus de la mention Obtenir des autorisations, puis actualisez la page de présentation de Microsoft Defender pour le cloud.

1. Les informations affichées en haut de la page incluent le nombre d’abonnements Azure, le nombre de ressources évaluées, le nombre de recommandations actives et les éventuelles alertes de sécurité.  Sur le corps de la page s’affichent des cartes qui représentent le niveau de sécurité, la conformité réglementaire, Insights, Azure Defender, etc.  

1. Sélectionnez **Ressources évaluées** en haut de la page.  (Remarque : cela équivaut sélectionner Inventaire dans le volet de navigation gauche de la page d’accueil de Microsoft Defender pour le cloud.)
    1. Cela vous permet d’accéder à la page **Inventaire** qui affiche le pass Azure correspondant à votre abonnement Azure.  Sélectionnez **Pass Azure - Parrainage**.
    1. La page Resource Health vous fournit une liste de recommandations.  Dans cette liste, sélectionnez **Plusieurs propriétaires doivent être attribués à votre abonnement**.
    1. Cliquez sur la flèche de déroulement près des étapes de correction. Prenez note de la présence d’étapes de correction détaillées ainsi que de la possibilité de prendre des mesures.  
    1. Sélectionnez **Microsoft Defender pour le cloud** en haut à gauche de l’écran pour revenir à la page de présentation de Microsoft Defender pour le cloud.

1. Sélectionnez **Recommandations actives** en haut de la page.  (Remarque : cela équivaut à sélectionner Recommandations dans le volet de navigation gauche de la page d’accueil de Microsoft Defender pour le cloud.)
    1. La page des recommandations affiche votre tableau de bord de niveau de sécurité.
    1. Sous ce tableau de bord, vous trouvez une liste de contrôles. Chaque contrôle de sécurité représente un risque de sécurité devant être atténué et inclut également des informations sur le niveau maximal associé à ce contrôle, le niveau actuel, l’augmentation potentielle du niveau et l’état d’intégrité de la ressource.  
    1. Sélectionnez l’un des contrôles, par exemple **Activer la MFA**.  Sélectionnez l’un des sous-éléments, par exemple **La MFA doit être activée sur les comptes disposant de droits de propriétaire sur votre abonnement**.  Une page s’ouvre : elle contient une description, les étapes de correction et les ressources concernées. Quittez cette page en cliquant sur le **X** en haut à droite de l’écran.
    1. Quittez la page des recommandations en cliquant sur le **X** en haut à droite de l’écran. Cela vous ramènera à la page de présentation.

1. Sur la page principale, sélectionnez **Conformité réglementaire**. La page de conformité réglementaire fournit une liste de contrôles de conformité.  Sous chaque contrôle apparaît une liste d’évaluations fondées sur l’Azure Security Benchmark qui fournit des recommandations quant à la manière de sécuriser vos solutions cloud dans Azure.
    1. Cliquez sur **IM. Identity Management** puis sélectionnez **IM-6 Use strong authentication controls (Utiliser des contrôles d’authentification puissants)**.  La liste indique les mesures concernant la responsabilité assumée par le client pouvant être prises pour améliorer la situation de conformité.
    1. Sélectionnez le **X** dans le coin supérieur droit pour fermer la page et revenir à la page de présentation du Microsoft Defender pour le cloud. 
    1. Laissez la page de présentation de Microsoft Defender pour le cloud ouverte. Elle vous sera utile pour la tâche suivante.


#### Tâche 2 : Dans cette tâche, vous accéderez au Niveau de sécurité Azure et découvrirez les recommandations permettant d’améliorer votre niveau de sécurité. 

1. Sur la page de présentation de Microsoft Defender pour le cloud, sélectionnez la carte **Niveau de sécurité**.
1. Sélectionnez **Pass Azure - Parrainage**.  Notez votre niveau de sécurité.
1. Sur la page Recommandations, sélectionnez **Mettre en œuvre les meilleures pratiques de sécurité** pour développer la liste. Vous remarquerez que l’état d’intégrité de ses ressources est affiché en rouge.
1. Sélectionnez l’élément **Plusieurs propriétaires doivent être affectés à votre abonnement**, dont l’état d’intégrité des ressources est affiché en rouge. 
1. Sous la mention **Ressources affectées**, vérifiez si l’option Ressources défectueuses est activée ou soulignée, puis sélectionnez l’abonnement Azure dans la liste.
1. En haut de la page Contrôle d’accès (IAM), sélectionnez **+ Ajouter**. Ensuite, dans la liste déroulante, sélectionnez **Ajouter une attribution de rôle**.
    1. Dans le volet de gauche de la page, sélectionnez **Propriétaire** (le premier élément de la liste) pour que la ligne soit affichée en gris, puis sélectionnez **Suivant** au bas de la page.
    1. En regard de la mention Membres, sélectionnez **+ Sélectionner des membres**. 
    1. Dans la fenêtre Sélectionner des membres qui s’affiche dans le volet de droite, sélectionnez **Alex Wilber**, puis cliquez sur **Sélectionner** au bas de la page.  
    1. Sur la page Ajout de l’attribution de rôle, vérifiez si Alex Wilber est répertorié dans la liste des membres, puis sélectionnez **Suivant** et ensuite **Examiner + Attribuer**.
    1. La mise à jour du statut peut prendre jusqu’à 24 heures. Ensuite, votre niveau de sécurité sera également mis à jour dans la mesure où tous les éléments du groupe Gérer les accès et les autorisations sont respectés.
    1. Dans le coin supérieur gauche de la page, au-dessus de la mention Pass Azure, sélectionnez **Microsoft Defender pour le cloud** pour revenir à la page de présentation de Microsoft Defender pour le cloud.
1. Gardez cette page ouverte pour la prochaine tâche.


#### Tâche 3 :  Gardez à l’esprit que Microsoft Defender pour le cloud existe en deux modes : sans fonctions avancées de sécurité (version gratuite) et avec fonctions avancées de sécurité, disponibles dans les plans de Microsoft Defender pour le cloud. Dans cette tâche, vous découvrirez la marche à suivre pour activer ou désactiver les plans de Microsoft Defender pour le cloud.

1.	Sur la page de présentation de Microsoft Defender pour le cloud, sélectionnez **Paramètres d’environnement** dans le volet de navigation de gauche.
1. Sélectionnez le signe « plus grand que **>** » affiché en regard de la liste Tenant Root Group afin de la développer (ne sélectionnez pas directement la liste Tenant Root Group car vous seriez dirigé vers une autre page), puis sélectionnez **Pass Azure - Parrainage**
1.	Sur la page Plans Defender, vous remarquerez que vous pouvez choisir de les activer tous ou sélectionner des plans Defender individuels. Si tous les plans sont désactivés, laissez les paramètres tels quels.
1.	Vous pouvez maintenant fermer l’onglet du navigateur pour quitter le portail Azure.


#### Révision
Dans ce labo, vous avez découvert Microsoft Defender pour le cloud et vous avez appris à utiliser le Niveau de sécurité Azure pour améliorer la posture de sécurité de votre organisation.
