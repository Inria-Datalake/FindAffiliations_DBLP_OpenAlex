# FindAffiliations_DBLP_OpenAlex
A script to find affiliations from a list of conference papers found in DBLP

## Installation
Copier le script dans un environnement Jupyter Notebook
Modifier les variables
Lancer le script

## Variables à modifier
annee_min = année début (par ex: 2021)
annee_max = année fin (par ex: 2025)
cible_dblp = url du congrès sur dblp, avec ".xml" au lieu de ".html" à la fin (ex: "https://dblp.org/db/conf/uss/index.xml")
nom_fichier = un nom se terminant par ".xlsx", par exemple "uss_affiliations.xlsx"
email_contact = saisir une adresse mail, pour identifier le demandeur auprès des api.

## Ce que fait le script
- d'après l'url spécifiée de DBLP (base bibliographique en sciences du numérique), il récupère, pour les volumes de chaque année spécifiée, le doi, le titre et les auteurs de chaque pubiblication.
- exclus : les contribtions aux workshops.

## Résultat
Tableau .xlsx enregistré dans le même dossier que le script et portant le nom spécifié dans la variable.
Ce tableau contient une ligne par auteur pour chaque publication, et l'affiliation trouvée dans OpenAlex, ainsi que la méthode qui a permis de trouver l'affiliation.
Il comporte également le doi arXiv si celui-ci existe dans DBLP.
Il contient les colonnes suivantes : annee	/ titre	/ auteur_dblp	/ auteur_openalex	/ affiliations	/ arxiv_url	/ arxiv_id	/ doi	source_openalex
