# Schéma des circuits touristiques
Ce schéma permet de modéliser les différents attributs des circuits touristiques 

## Contexte

Il existe un besoin d'harmonisation de la publication en open data de données essentielles produites par les administrations publiques wallones. En octobre 2022, plus de 660 jeux de données sont publiés sur le portail [Open Data Wallonie Bruxelles (ODWB)](https://www.odwb.be/explore/?sort=modified), qui sont très hétérogènes. 

Constatant la production de jeux de données disparates à l'échelle de la fédération Wallonie-Bruxelles, Futuro Cité a réuni, dans le cadre d'un groupe de travail sollicité depuis mai 2021, une vingtaine de collectivités. La concertation de celles-ci a permis 1) d'identifier collectivitement des jeux de données jugés prioritaires et 2) de s'accorder sur des spécifications des modèles de données. 
La standardisation de ces données prioritaires est en effet essentielles pour s'assurer de leur publication homogène et de faciliter leur exploitation (notamment leur agrégation) par les réutilisateurs. Elle faciliten l'exploitation des données publiées par les réutilisateurs (agrégation, consolidation et traitements automatiques).

## Construction du schéma de données 

Les membres du groupe de travail ont défini un schéma de données qui décrit le format des fichiers, les différents champs, les valeurs possibles… Ils se sont appuyés sur un état des lieux du patrimoine de données des collectivités wallones et sur une étude des modèles utilisés par des collectivités déjà productrices de ces données (notamment Liège et Namur), en prenant en compte les retours faits par les réutilisateurs de données. 

## Description du schéma

La documentation des champs du schéma est accessible sur .... *(le site de futurocité)*

Un [gabarit au format tableur](https://github.com/FuturoCite/standard-circuits-touristiques/blob/main/Schema_circuits_touristiques_gabarit.xlsx) est également prévu pour faciliter la publication d'un jeu de données conforme au format du schéma.
Un exemple valide au format CSV est consultable [ici](https://github.com/FuturoCite/standard-circuits-touristiques/blob/main/exemple-valide.csv).  

Le tableau ci-dessous donne un aperçu des champs du schéma. 

<table>
  <tr>
   <td><strong>Nom</strong>
   </td>
   <td><strong>Description</strong>
   </td>
  </tr>
  <tr>
   <td>identifiant
   </td>
   <td>Ce champ contient un identifiant unique local. Le producteur de données le génère en associant le code INS de la commune dans laquelle se situe le départ du circuit à un nombre. Ce champ permet d'éviter localement les doublons. Le code INS de la commune est accessible ici :<a href="https://statbel.fgov.be/fr/open-data/code-refnis"> https://statbel.fgov.be/fr/open-data/code-refnis</a>
   </td>
  </tr>
  <tr>
   <td>Nom
   </td>
   <td>Ce champ contient le nom du circuit touristique.
   </td>
  </tr>
  <tr>
   <td>GPX
   </td>
   <td>Ce champ contient un lien URL renvoyant vers la trace gpx du circuit.
   </td>
  </tr>
  <tr>
   <td>Description
   </td>
   <td>Ce champ est recommandé. Il contient une description du circuit.
   </td>
  </tr>
  <tr>
   <td>Moyen de locomotion
   </td>
   <td>Ce champ précise le moyen de locomotion du circuit. Une valeur est possible parmi la liste suivante : Marche ; Trail ; Vélo/VTC ; VTT ; Cheval ; Voiture
   </td>
  </tr>
  <tr>
   <td>Difficulté du circuit
   </td>
   <td>Ce champ est recommandé. Il indique la difficulté du circuit réalisé avec le moyen de locomotion identifié dans le champ Type de locomotion. 1=Très facile, 2=Facile, 3=Moyen, 4=Difficile
   </td>
  </tr>
  <tr>
   <td>Photos
   </td>
   <td>Ce champ est recommandé. Il renseigne une url renvoyant vers une ou plusieurs photos du circuit. En cas de plusieurs url : elles doivent être séparées par un point virgule.
   </td>
  </tr>
  <tr>
   <td>Adresse du point de départ
   </td>
   <td>Ce champ contient l'adresse du point de départ la plus précise possible du circuit.
   </td>
  </tr>
  <tr>
   <td>Latitude du point de départ
   </td>
   <td>Ce champ indique la latitude du point de départ. Les coordonnées d'un lieu peuvent être générées ici :<a href="https://www.coordonnees-gps.fr/carte/pays/BE"> https://www.coordonnees-gps.fr/carte/pays/BE</a>
   </td>
  </tr>
  <tr>
   <td>Longitude du point de départ
   </td>
   <td>Ce champ indique la longitude du point de départ. Les coordonnées d'un lieu peuvent être générées ici :<a href="https://www.coordonnees-gps.fr/carte/pays/BE"> https://www.coordonnees-gps.fr/carte/pays/BE</a>
   </td>
  </tr>
  <tr>
   <td>Balisage
   </td>
   <td>Ce champ décrit le balisage du circuit.
   </td>
  </tr>
  <tr>
   <td>Balisage bi-directionnel
   </td>
   <td>Ce champ indique si le balisage permet la réalisation du circuit dans les deux sens ou pas. La valeur "true" signifie un balisage bi-directionnel, "false" signifie un balisage uni-directionnel.
   </td>
  </tr>
  <tr>
   <td>Geométrie
   </td>
   <td>Ce champ indique la géométrie du circuit. La liste des coordonnées est générée à partir d'un fichier GPX.
   </td>
  </tr>
  <tr>
   <td>Longueur
   </td>
   <td>Ce champ contient la longueur du circuit exprimée en km.
   </td>
  </tr>
  <tr>
   <td>Dénivelé
   </td>
   <td>Ce champ indique le dénivelé moyen du circuit en mètres.
   </td>
  </tr>
  <tr>
   <td>Temps estimé
   </td>
   <td>Ce champ indique le temps moyen estimé pour la réalisation du circuit. Il respecte le format hh:mm.
   </td>
  </tr>
  <tr>
   <td>Profil altimétrique
   </td>
   <td>Ce champ contient une url renvoyant au profil altimétrique du circuit.
   </td>
  </tr>
  <tr>
   <td>Accessibilité PMR
   </td>
   <td>Ce champ est recommandé. Il indique si le circuit est accessible aux personnes à mobilités réduites.
   </td>
  </tr>
  <tr>
   <td>Accessibilité Poussette
   </td>
   <td>Ce champ est recommandé. Il indique si le circuit est accessible aux poussettes.
   </td>
  </tr>
  <tr>
   <td>En boucle
   </td>
   <td>Ce champ indique si le circuit est en boucle (true) ou linéaire (false).
   </td>
  </tr>
  <tr>
   <td>Informations complémentaires
   </td>
   <td>Ce champ donne toute information jugée utile au promeneur. Il indique par exemple si le circuit comporte des revêtements particuliers, des difficultés notables, des passages nécessitant d'emprunter des échelles...
   </td>
  </tr>
  <tr>
   <td>Thème
   </td>
   <td>Ce champ précise le ou les thèmes éventuels du circuit.
   </td>
  </tr>
  <tr>
   <td>Gestionnaire
   </td>
   <td>Ce champ est recommandé. Il indique le nom du gestionnaire du circuit. Il peut s'agir d'une commune, d'un office du tourisme, d'un groupe d'action locale…
   </td>
  </tr>
  <tr>
   <td>Contact
   </td>
   <td>Ce champ contient l'url du site web du gestionnaire du circuit.
   </td>
  </tr>
  <tr>
   <td>Date de création de la donnée
   </td>
   <td>Ce champ indique la date de création de la donnée dans le jeu. Il respecte le format ISO 8601 : année-mois-jour (YYYY-MM-DD)
   </td>
  </tr>
  <tr>
   <td>Date de dernière modification de la donnée
   </td>
   <td>Ce champ indique la date de la dernière modification de la donnée dans le jeu. Il respecte le format ISO 8601 : année-mois-jour (YYYY-MM-DD).
   </td>
  </tr>
</table>

## Format de fichier 

Le format de fichier retenu pour la publication des données est le CSV (Comma Separated Values, valeurs séparées par des virgules).

Les fichiers doivent, sauf exception et autant que possible, respecter les règles de formatage suivantes :

* l’encodage des caractères est UTF-8,
* le séparateur des colonnes est la virgule,
* le séparateur des nombres décimaux est le point,
* le séparateur de valeurs multiples dans un champ est le point-virgule,
* si un champ contient une virgule, il doit être entouré de guillemets doubles,
* chaque ligne doit avoir le même nombre de champs,
* le type MIME ou Content-Type est text/csv.

### Recommandation pour le nommage des fichiers 

Les fichiers doivent, sauf exception et autant que possible, respecter les règles de nommage suivantes :

* YYYY-MM-DD : Date de création du fichier
* idProducteur : code ISN unique de la commune pour identifier le producteur
* circuits-touristiques : nom du fichier, en minuscules non accentuées
* territoire : Nom du territoire concerné, non accentué (exemple : Liege)
* extension : Si les règles de formatage sont respectées, l'extension est .csv

Exemple : 2022-10-25_62063_circuits-touristiques_Liege.csv

### Recommandation pour la mise en conformité 

Ces conseils reprennent ceux du [Socle commun des données locales publié par Open Data france](https://scdl.opendatafrance.net/docs/recommandations-relatives-aux-jeux-de-donnees.html)

Les fichiers doivent comporter :

* Toutes les colonnes, y compris celles dont les cellules ne sont pas renseignées, dans le bon ordre, et avec des en-têtes correctement nommées sur la première ligne (nom correspondant strictement au schéma)
* Autant de lignes que nécessaire comprenant des cellules dont les valeurs peuvent être obligatoires (elles doivent être impérativement renseignées) ou optionnelles (elles sont seulement recommandées ou soumises à condition de disponibilité / pertinence)
