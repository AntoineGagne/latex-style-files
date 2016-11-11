# `uldesign`

Ce package contient des feuilles de style `LaTeX` utiles pour les cours de *Design* à l'Université Laval. Cette documentation assume que vous avez le logiciel `make` installé.

## Installation

Pour installer le package, vous pouvez tout simplement faire la commande suivante:

```shell
make install
```

Ensuite, vous devez ajouter le package à la base de données de `LaTeX`. Voir [ici](https://en.wikibooks.org/wiki/LaTeX/Installing_Extra_Packages#Manual_installation) pour plus d'informations.

## Désinstallation

Pour désinstaller le package, vous pouvez faire la commande suivante:

```shell
make uninstall
```

## Démonstration

Un fichier de démonstration se trouve dans `demo/demo.tex`. Pour le compiler (en assumant que vous avez auparavant installé le package), vous pouvez faire une des commandes suivantes:

```shell
make
```

ou

```shell
make install
```

## Nouvelles commandes

Les feuilles de style du package `uldesign` définissent de nouvelles commandes qui sont utilisées dans un environnement spécifique ou bien qui est utilisable dans tous les environnements.

### Maison de la qualité

#### `\criteria`

#### `\globalobjective`

#### `\objective`

#### `\constraint`

### Cahier des charges

#### `\newsection`

#### `\newsectionheader`

### Plan d'étude

#### `\studyplansection`

#### `\studyplancriteria`

#### `\studyplanprocedure`

#### `\studyplanhypothesis`

### Autres

#### `\emptycell`

#### `\lborder`

#### `\dline`

## Nouveaux environnements

### `houseofqualities`

### `requirements`

### `studyplan`
