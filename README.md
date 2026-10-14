# TrueFoam GUI Multi-Core

Interface Windows de calcul aérodynamique (traînée, portance, écoulement) sur un objet fourni en STL fermé,
avec le choix de la version d'OpenFOAM® : openfoam.com (v2412, v2512, v2506, v2406) et openfoam.org (11 à 14).

## Télécharger

Page **Releases** de ce dépôt : `TrueFOAM-MC-Windows.zip`. Le dézipper en gardant le dossier entier, puis lancer
`TrueFOAM-MC.exe` (logiciel non signé : « Informations complémentaires », puis « Exécuter quand même »).

Il faut Windows 10 ou 11 (64 bits, 16 Go de RAM conseillés) et Docker Desktop lancé. Le moteur de chaque version
d'OpenFOAM est construit sur votre PC au premier calcul (bouton « Construire le moteur »).

## Écart mesuré entre versions d'OpenFOAM

Chaque version est comparée à v2412 sur une série fixe (cube, plaque, cylindre, sphère, drone V2V Speeder 3″) :

| Versions | Écart sur la traînée |
|---|---|
| openfoam.com v2512, v2506, v2406 | sous 1 % |
| openfoam.org 11 à 14, sans couches limites | sous 1 % |
| openfoam.org 11 à 14, avec couches limites | 2,5 % au plus (k-ε réalisable non proposé) |

Une version ou une fonction qui ne tient pas sa tolérance n'est pas proposée : elle est grisée, avec la raison.
La thermique (refroidissement par l'air) est « en essai » et proposée avec les versions openfoam.com seulement.

Cet écart mesure la cohérence entre versions, pas la justesse face à la soufflerie.

OpenFOAM® est une marque déposée d'OpenCFD Ltd. Ce logiciel n'est ni approuvé ni produit par OpenCFD Ltd ni par la
Fondation OpenFOAM. OpenFOAM n'est pas inclus : il est téléchargé dans Docker sur votre PC.
