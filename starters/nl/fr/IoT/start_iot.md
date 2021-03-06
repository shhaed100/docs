---

copyright:
  2016

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}


# Initiation au module de démarrage de {{site.data.keyword.iot_short_notm}}
{: #gettingstartedtemplate}
<!-- Provide and appropriate ID above -->
*Dernière mise à jour : 27 juin 2016*
{: .last-updated}

Commencez à utiliser {{site.data.keyword.iot_full}} à l'aide du conteneur boilerplate du module de démarrage de {{site.data.keyword.iot_short_notm}}. Avec le module de démarrage, vous pouvez rapidement simuler un terminal, créer des cartes, générer des données et commencer à analyser et à afficher des données dans le tableau de bord de {{site.data.keyword.iot_short_notm}}.
{: shortdesc}

Le module de démarrage déploie et connecte automatiquement ces services :

{{site.data.keyword.iot_short_notm}} - la plateforme fournit un kit d'outils IoT polyvalent comportant des terminaux de passerelle, la gestion des terminaux et un accès puissant aux applications. {{site.data.keyword.iot_short_notm}} vous permet de collecter des données relatives à des terminaux connectés et d'effectuer des analyses sur des données temps réel à partir de votre organisation.

{{site.data.keyword.sdk4nodefull}} - crée un environnement d'exécution dans lequel Node-RED s'exécute.

{{site.data.keyword.cloudantfull}} - base de données dans laquelle Node-RED stocke des métadonnées.

## A propos de {{site.data.keyword.iot_short_notm}}
{: #about_iotplatform}
{{site.data.keyword.iot_short_notm}} fournit aux applications un accès puissant aux terminaux et aux données IoT afin de vous aider à composer rapidement des applications d'analyse, des tableaux de bord de visualisation et des applications IoT mobiles.
{{site.data.keyword.iot_short_notm}} vous permet d'effectuer des opérations de gestion de terminaux puissantes, de stocker des données de terminal et d'y accéder, et de connecter une grande diversité de terminaux et de terminaux de passerelle. {{site.data.keyword.iot_short_notm}} fournit une communication sécurisée vers et depuis vos terminaux à l'aide de MQTT et de TLS.

## A propos de Node-RED
{: #about_nodered}
Node-RED est un outil qui permet de relier des terminaux matériels, des API et des services en ligne selon des méthodes inédites et intéressantes.  Vous pouvez utiliser Node-RED pour créer un thermostat simulé qui envoie des données simulées à votre service {{site.data.keyword.iot_short_notm}}. Vous pouvez créer des cartes pour afficher des données temps réel dans le tableau de bord de {{site.data.keyword.iot_short_notm}}. Pour plus d'informations, voir la [documentation Node-RED](https://console.ng.bluemix.net/docs/starters/Node-RED/nodered.html#nodered).

## Navigation dans l'application
{: #gettingaround}
A mesure que vous exécuterez les étapes suivantes, vous serez amené à utiliser trois onglets différents dans votre navigateur :
  1. Tableaux de bord de *{{site.data.keyword.Bluemix_notm}}* - Le tableau de bord de {{site.data.keyword.Bluemix_notm}} vous permet de voir l'état de votre déploiement, de lire la documentation et de lancer les tableaux de bord.
  2. Tableau de bord de *{{site.data.keyword.iot_short_notm}}* - Ce tableau de bord vous permet de gérer ce service. Vous pourrez ainsi définir des types de terminal, enregistrer des terminaux, surveiller les données de capteur entrantes, créer des cartes de visualisation de données et afficher des visualisations de données réelles.
  3. *Node-RED* - En exécutant Node-RED comme une application Web node.js, vous pourrez configurer et exécuter le flux de simulateur de terminaux et gérer d'autres flux pour traiter les données à partir de {{site.data.keyword.iot_short_notm}}.

## Définition d'un terminal simulé dans {{site.data.keyword.iot_short_notm}}
{: #definingsimdev}
Enregistrez votre terminal auprès de {{site.data.keyword.iot_short_notm}} :
  1.	Dans {{site.data.keyword.Bluemix_notm}}, accédez à l'onglet de présentation de votre application déployée.
  2.	Cliquez sur la zone {{site.data.keyword.iot_short_notm}} box dans la section ou l'onglet Connexions.
  3.	Cliquez sur Lancer le tableau de bord pour ouvrir le tableau de bord de {{site.data.keyword.iot_short_notm}} dans une nouvelle fenêtre du navigateur.
  4.	Sélectionnez Terminaux.
  5.	Cliquez sur Ajouter un terminal.
  6.	Cliquez sur Créer un type de terminal dans la boîte de dialogue Ajouter un terminal.
  7.	Cliquez sur Créer un type de terminal dans la boîte de dialogue Création d'un type de terminal.
  8. Entrez un nom descriptif et une description pour le type de terminal, par exemple, thermostat.
  9.	Ignorez Définir un modèle.
  10.	Ignorez Métadonnées.
  11.	Cliquez sur Créer pour ajouter le nouveau type de terminal.
  12.	Cliquez sur Suivant pour ajouter votre terminal (l'option Sélectionner un type de terminal est présélectionnée).
  13.	Entrez un ID de terminal, par exemple, LivingRoomThermo1.
  14.	Ignorer : Entrez des métadonnées de terminal.
  15.	Cliquez sur Suivant pour ajouter une connexion de terminal à l'aide d'un jeton d'authentification généré automatiquement.
  16.	Vérifiez que les informations récapitulatives sont correctes, puis cliquez sur Ajouter pour ajouter la connexion.
  17.	Sur la page Informations sur le terminal qui s'affiche, copiez et sauvegardez les informations sur le terminal :
      -	ID organisation
      -	Type de terminal
      -	ID terminal
      - Méthode d'authentification
      - Jeton d'authentification

**Conseil** : Vous aurez besoin des informations ID organisation, Type de terminal et ID terminal au cours des quelques étapes suivantes pour finaliser la configuration de l'application Node-RED et établir la connexion.

## Configuration et exécution du simulateur de terminal Node-RED
{: #confignodered}
Configurez le simulateur de terminal Node-RED. Utilisez le simulateur de terminal pour envoyer des messages de terminal MQTT à {{site.data.keyword.iot_short_notm}}. Le simulateur de terminal envoie des informations de température et d'humidité à {{site.data.keyword.iot_short_notm}}.

1. Dans votre tableau de bord de Bluemix, ouvrez Node-RED en sélectionnant **Afficher l'application** ou en cliquant sur le lien (par exemple, http:// myIoTApp.mybluemix.net).
2.	Cliquez sur **Accédez à votre éditeur de flux Node-RED** pour ouvrir l'éditeur.
3.	Cliquez deux fois sur le noeud **Envoyer** vers {{site.data.keyword.iot_short_notm}} de couleur bleue dans le flux de simulateur de terminal.
  1.	Vérifiez que l'option Authentication = Service Bluemix
  2.	Collez le type de terminal à partir du terminal que vous avez enregistré.
  3.	Collez l'ID terminal à partir du terminal que vous avez enregistré.
  4.	Cliquez sur OK.
4.	Dans l'angle supérieur droit de l'éditeur de flux Node-RED, cliquez sur **Déployer**.
5.	Configurez le flux de contrôle de température Node-RED.
  1.	Cliquez deux fois sur le noeud IBM IoT App de couleur bleue dans le flux de simulateur de terminal.
  2.	Remplacez la valeur de l'option Authentification par Service Bluemix.
  3.	Sélectionnez Tout pour Type de terminal, ID terminal, Evénement et Format.
  4.	Cliquez sur OK.
6.	Dans l'angle supérieur droit de l'éditeur de flux Node-RED, cliquez sur **Déployer**.
7.	Validez la connexion de terminal.
  1.	Dans l'autre onglet ou fenêtre de navigateur, revenez dans le tableau de bord de {{site.data.keyword.iot_short_notm}}.
  2.	Sélectionnez Terminaux et cliquez sur LivingRoomThermo1 ou sur le nom du terminal que vous avez ajouté, si celui-ci est différent.  
  La page Informations sur le terminal s'ouvre. Cette vue vous permet d'afficher l'état de connexion pour votre terminal. Le terminal est à l'état Déconnecté.
  3.	De retour dans votre éditeur de flux Node-RED, cliquez sur le bouton correspondant au noeud d'envoi de données de couleur grise afin de générer un contenu d'actif.
  Le contenu comporte les points de données suivants :
  ```
  {"d":{"temp":15,"humidity":50,"location":{"longitude":-98.49,"latitude":29.42}}}
  ```
  4.	Dans l'onglet de débogage du panneau de droite, vérifiez que des messages sont créés.
  5.	Sur la page Informations sur le terminal {{site.data.keyword.iot_short_notm}}, assurez-vous que vous voyez les mêmes points de données que ceux reçus du terminal dans la section Informations sur les capteurs.

8.	Connectez votre exemple de terminal IoT à {{site.data.keyword.iot_short_notm}} pour visualiser les données de terminal.

## Création de cartes dans {{site.data.keyword.iot_short_notm}} pour afficher des données réelles
{: #createcards}
Pour créer des cartes, procédez comme suit :

### Génération automatique de données toutes les 3 secondes
1. Dans l'onglet Node-RED, cliquez deux fois sur le noeud Envoyer des données.
2.	Définissez un intervalle de répétition de 3 secondes.
3.	Procédez au déploiement.

### Création de nouvelles cartes dans le tableau de bord
1. Accédez à l'onglet de navigateur du tableau de bord de {{site.data.keyword.iot_short_notm}}.
2. Sélectionnez TABLEAUX.
3. Cliquez sur Créer un nouveau tableau.
4. Donnez-lui un nom, par exemple, Home Environment.
5. Procédez à la création.
6. Cliquez sur Ajouter une nouvelle carte (pour la température).
   1.	Sous Terminaux, sélectionnez Graphique en temps réel.
   2.	Sous Données source de carte, cochez votre terminal "LivingRoomThermo1", puis cliquez sur Suivant.
   3. Cliquez sur Connecter un nouveau fichier.
       - Nom : Température
       - Événement : Mise à jour
       - Propriété : temp
       - Type : Variable flottante
       - Unité : °C
       - Précision : 2
       - Min : 0
       - Max : 50
       - Suivant
  4. Cliquez sur Aperçu de la carte.
       - Sélectionnez L
       - Suivant
  5. Cliquez sur Informations sur la carte.
       - Titre : Température
  6.	Cliquez sur Soumettre.
  7.	La carte de température apparaît sur le tableau de bord et comporte un graphique des données de température réelles.
7.	Cliquez sur Ajouter une nouvelle carte (pour l'humidité).
  1.	Sous Terminaux, sélectionnez Plus de détails.
  2.	Sélectionnez Jauge.
  3.	Sous Données source de carte, cochez votre terminal, puis cliquez sur Suivant.
  4.	Cliquez sur Connecter un nouveau fichier.
       -	Nom : Humidité
       -	Événement : Mise à jour
       -	Propriété : humidity
       -	Type : Variable flottante
       -	Unité : "% d'humidité relative"
       -	Précision : 1
       -	Min : 10
       -	Max : 95
       -	Suivant
  5.	Cliquez sur Aperçu de la carte.
       -	Paramètres
          -	Seuil inférieur : 40 et correct
          -	Milieu : satisfaisant
          -	Seuil supérieur : 50 et correct
       -	Sélectionnez M
       -	Suivant
  6.	Cliquez sur Informations sur la carte.
       -	Titre : Humidité
  7.	Cliquez sur Soumettre.
  8.	La carte d'humidité apparaît sur le tableau de bord et comporte une jauge illustrant les données d'humidité réelles.
8.	Cliquez sur Ajouter une nouvelle carte (pour l'emplacement).
  1.	Sous Terminaux, sélectionnez Plus de détails.
  2.	Sélectionnez Valeur.
  3.	Sous Données source de carte, cochez votre terminal "LivingRoomThermo1", puis cliquez sur Suivant.
  4.	Cliquez sur Connecter un nouveau fichier.
       -	Nom : Latitude
       -	Événement : Mise à jour
       -	Propriété : location.latitude
       -	Type : Variable flottante
       -	Unité : "°N"
       -	Précision : 2
       -	Min : -180
       -	Max : 180
  5. Cliquez sur Connecter un nouveau fichier.
       -	Nom : Longitude
       -	Événement : Mise à jour
       -	Propriété : location.longitude
       -	Type : Variable flottante
       -	Unité : "°E"
       -	Précision : 2
       -	Min : -180
       -	Max : 180
       -  Suivant
  6.	Cliquez sur Aperçu de la carte.
       -	Sélectionnez L
       -	Suivant
  7.	Cliquez sur Informations sur la carte.
       -	Titre : Emplacement
  8.	Cliquez sur Soumettre.
9.	Surveillez la mise à jour de vos nouvelles cartes en temps réel à l'aide des données de simulateur générées par le flux Node-RED.
**Remarque** : Node-RED continue d'envoyer des données tant que vous ne l'arrêtez pas.
10.	Dans l'éditeur de flux Node-RED, mettez à jour le noeud Envoyer des données en affectant la valeur Aucun à l'intervalle de répétition.
11.	Procédez au déploiement.

## Etape suivante ?
{: #whatsnext}
A présent que votre terminal simulé envoie des données à {{site.data.keyword.iot_short_notm}}, vous pouvez continuer d'effectuer des itérations sur votre projet IoT.

1. [Effectuez des recherches dans nos recettes IoT](https://developer.ibm.com/recipes/?post_type=tutorials&s=watson+iot) pour connecter un terminal physique, tel que Raspberry Pi, et envoyer des données à {{site.data.keyword.iot_short_notm}}.
2. [Déployez un exemple d'application node.js pour visualiser des données de terminal.](https://www.bluemix.net/docs/services/IoT/visualizingdata_sample.html)
3.	Protégez l'éditeur de flux Node-RED par un mot de passe. Par défaut, l'éditeur est ouvert et tout utilisateur peut accéder et modifier des flux. Pour protéger l'éditeur par un mot de passe, procédez comme suit :
  1.	Dans le tableau de bord Bluemix, sélectionnez la page 'Variables d'environnement' pour votre application.
  2.	Ajoutez les variables définies par l'utilisateur suivantes :
       -	NODE_RED_USERNAME - nom d'utilisateur pour la sécurisation de l'éditeur
       -	NODE_RED_PASSWORD - mot de passe pour la sécurisation de l'éditeur
  3.	Cliquez sur Sauvegarder.


# Liens connexes
{: #rellinks}

## Exemples et tutoriels
{: #samples}
* [Recettes relatives à la connexion de vos terminaux](https://developer.ibm.com/recipes/?post_type=tutorials&s=iot){:new_window}
* [Organisation {{site.data.keyword.iot_short}} Play](https://play.internetofthings.ibmcloud.com/){:new_window}
* [Connexion d'un Intel Galileo à {{site.data.keyword.iot_short}}](https://developer.ibm.com/recipes/tutorials/connect-an-intel-galileo-to-the-internet-of-things-foundation-connect/){:new_window}
* [Connexion d'un kit de démarrage ARM&reg; mbed&trade; IoT Starter Kit](https://developer.ibm.com/recipes/tutorials/arm-mbed-iot-starter-kit-part-1/){:new_window}
* [Connexion d'un terminal Raspberry Pi à {{site.data.keyword.iot_short}}](https://developer.ibm.com/recipes/tutorials/raspberry-pi-4/){:new_window}

## Référence d'API
{: #api}
* [Documentation de l'API {{site.data.keyword.iot_short}}](https://docs.internetofthings.ibmcloud.com/swagger/v0002.html#/){:new_window}


## Liens connexes
{: #general}
* [Documentation de l'API {{site.data.keyword.iot_short_notm}}](https://www.bluemix.net/docs/services/IoT/iotplatform_overview.html){:new_window}
* [Documentation du module de démarrage {{site.data.keyword.sdk4nodefull}}](https://console.ng.bluemix.net/docs/starters/Node-RED/nodered.html){:new_window}
