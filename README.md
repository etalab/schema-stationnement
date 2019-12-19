# Schéma des lieux de stationnement

Ce schéma permet de modéliser les stationnements en parcs publics et privés à usage public.

## Contexte

Dans le cadre des travaux de l’équipe du Point d’accès national et de la mise en oeuvre de l’ouverture des données pour améliorer l’information dont disposent les voyageurs, l’équipe de transport.data.gouv.fr propose une solution simple et structurée pour l’ouverture des données de parcs de stationnement en France : la Base Consolidée des Données de Stationnement (BCS).

Il s’adresse à toute nouvelle agglomération qui souhaiterait se lancer dans l’ouverture d’une base décrivant les stationnements hors-voirie de son ressort territorial.

L’équipe de [transport.data.gouv.fr](https://transport.data.gouv) mettra à disposition des acteurs un générateur CSV conforme au schéma de données, ainsi qu’un validateur pour les collectivités qui voudraient créer le fichier par leurs soins.

## Cadre juridique

L'ouverture des données de stationnement nécessaires à l'information voyageur est une obligation légale, définie par le [règlement délégué (UE) 2017/1926](https://eur-lex.europa.eu/legal-content/FR/TXT/PDF/?uri=CELEX:32017R1926) concernant la mise à disposition de services d'informations sur les déplacements multimodaux. Ces obligations sont précisées en droit français par la loi d'orientation des mobilités (LOM), qui désigne les collectivités territoriales comme étant responsables de la mise à disposition des données sur la plateforme [transport.data.gouv.fr](https://transport.data.gouv.fr], qui constitue le Point d'Accès National des données de mobilité.

>Lorsqu’elles confient la gestion du stationnement en ouvrage ou sur voirie à un prestataire, les collectivités territoriales et leurs groupements sont responsables de la fourniture des données mentionnées au 3°. Elles peuvent en confier la charge à ce prestataire" (Article 9, alinéa 5)

Les collectivités, et par extension leurs prestataires, ont la responsabilité de transmettre les données existantes les plus complètes possibles.

Afin de faciliter la réutilisation de ces données, et réduire le coût d'intégration de ces données dans des services tiers, un schéma a été défini afin d'assurer une harmonisation de ces données sur l'ensemble du territoire. Le schéma définit des informations **nécessaires** et des données **additionnelles**. Cette distinction a été mise en place pour ne pas pénaliser les petits producteurs de données, et définit un standard minimal de complétude des données. Il est cependant demandé aux producteurs de données de compléter le schéma avec le plus grand niveau de détail possible, afin de transmettre une information plus riche à l'usager final.

## Finalité

La base des stationnements permet de regrouper en un unique fichier consolidé l'ensemble de l'offre de stationnement en France, dans un format standard et unifié. Cette standardisation des données facilite grandement le travail d'intégration de ces données par des services réutilisateurs.

La base présente plusieurs cas d'usage :
- Elle permet de mettre en avant l'offre de stationnement d'une collectivité en permettant à des services de calcul d'itinéraire d'intégrer ces données. Cela permet notamment à ces services de proposer des itinéraires multimodaux à leurs usagers, combinant voiture et transports en commun par exemple ;
- Elle peut servir également à apporter une plus grande transparence sur l'offre de stationnement existante dans une ville, les tarifs qui y sont pratiqués.

### Transmission des données

Dans le but de constituer un répertoire consolidé des parcs de stationnement en France, les collectivités peuvent transmettre systématiquement, sous forme de tableau mis à jour, les données relatives aux parcs de stationnement publics, ou privés à usage public.

### Format de fichier

Le fichier doit être encodé en UTF-8 et utiliser le point-virgule comme séparateur de colonnes. Aucune valeur ne peut contenir le caractère « point-virgule » choisi comme séparateur, sauf dans le cas des “listes ouvertes” ou on peut séparer les différentes attributs par des points virgules. L'en-tête de colonne sur la première ligne est obligatoire. Tous les champs sont obligatoires ; si la donnée n'est pas disponible, la colonne doit être présente et vide.

Nom du fichier : `Parking_nom_AAAAMMJJ.csv` avec nom étant le nom de la collectivité productrice des données, par exemple `Parking_Ain_20191013.csv`.

### Fichiers d'exemples

### Mises à jour

Les mises à jour sont effectuées à partir du fichier communiqué précédemment et en reprennent, en les modifiant le cas échéant, les données qui y figurent déjà.

## Consolidation
Le Point d'accès national aux données de transport ([transport.data.gouv.fr](https://transport.data.gouv.fr)) réalise une consolidation régulière des fichiers déposés sur [data.gouv.fr](https://data.gouv.fr) avec le mot-clé `stationnement` respectant le format de référence décrit ici.
