# metaltura/angular

Le vocabulaire Angular, qui hérite de la partie « page unique » du métamodèle d'application. Le dépôt `spring-angular` le relie à Spring.

## Ce qu'il contient

- `models/Angular.yaml` — le vocabulaire Angular (PLAT-308), de la même forme que celui de React : une interface Angular (Frontend) et son service (Service). Un client d'API React y est signalé (`angularServicesOnly`). Les composants sont ceux de spa : le générateur tire du nom le sélecteur et les fichiers d'un composant Angular autonome.

## Ce dont il dépend

| Dépôt | Ce qu'il en emploie | Ligne `depends` |
| --- | --- | --- |
| `metaltura/application` | `Application`, que `Angular` désigne ou spécialise | `metaltura/application/Application@v2.0.0` |

`Diagram` et `Uml` sont des modèles système de Metaltura : leur nom seul suffit.

## L'utiliser depuis un autre dépôt

Écrire dans la liste `depends` du modèle :

```yaml
depends:
  - metaltura/angular/Angular@v2.0.0
```

Metaltura clone ce dépôt à l'étiquette `v2.0.0`, puis `metaltura/application` dont il dépend, et `metaltura/domain` que ce dernier nomme. Toute la librairie est à `v2.0.0` : Metaltura refuse qu'un même dépôt soit demandé à deux versions.

## D'où il vient

Ce dépôt vient du dépôt privé `Kogitec/simple-mda`, `main` à `96a1a75` (PLAT-1461), rangé par sujet par PLAT-1498 en un seul commit : son modèle était sous `models/applications/spring-angular/`. L'historique de ses fichiers reste dans `simple-mda`, archivé.
