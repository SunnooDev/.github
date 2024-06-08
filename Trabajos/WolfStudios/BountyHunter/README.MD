# Descripción

Plugin encargado de dar precio por la cabeza de un jugador, tanto por
el uso de comandos como automáticamente al matar a un jugador.

Al matar a un jugador con recompensa se le dará una cabeza con la que
podrás reclamar la recompenza

- **Version:** 0.0.1
- **Minecraft version:** 1.19.2

## Dependencias
|   |                         |
|---|-------------------------|
| ✅ | Dependencias requeridas |
| ⬛ | Dependencia opcional    |

- ✅ LuckPerms
- ⬛ PlaceHolderApi

## Comandos

### Alias:

- **/bountyhunter**
- **/bounty**
- **/bh**

### Colocar recompensa sobre un jugador
### `/bounty set <<Player>> <<Nivel>> <<Razón>>`

Permite colocar una recompensa sobre un **jugador**, los **niveles** 
son los que se establezcan en el archivo [Config](#config) y la 
**Razón** por la cual se pone la recompensa

### Eliminar recompensa de un jugador
### `/bounty remove <<player>>`

Elimina la recompensa de un jugador

## Permisos

### Permisos de comandos
- **bountyhunty.bounty.set: Permite usar el comando [/Bounty set](#colocar-recompensa-sobre-un-jugador)**
- **bountyhunty.bounty.remove: Permite usar el comando [/Bounty remove](#eliminar-recompensa-de-un-jugador)**

## Placeholders

- **`%bountyhunter_nivel%`:** Placeholder del nivel de recompenza del jugador
- **`%bountyhunter_razon%`:** Placeholder del último de motivo de recompeza
- **`%bountyhunter_recompenza%`:** Placeholder de la recompenza que tiene el jugador

## Config

La configuración de este plugin consta de 3 secciones:

### HunterLevel
Esta sección corresponde al nivel requerido para que salga la recompensa en
el chat y a su vez los permisos de trabajo requeridos para llevar a cabo
la caceria.

*En caso de no tener el nivel requerido se le dará la cabeza pero también
una recompenza por el*

La sección se compone de secciones con **números** en formato
**String** como **key's** y **listas** de **Strings** como **values**:

```yaml
hunterLevel:
  '1':
    - jobsinmotals.job.police
  '2':
    - jobsinmotals.job.bountyhunter
    - jobsinmotals.job.police
```

### Levels
Esta sección corresponde al valor de la recompensa por cada
nivel de busqueda.

La sección se corresponde de secciones con **números** en formato 
**String** como **key's** y **números** como **values**:

```yaml
levels:
  '1': 2500
  '2': 5000
  '3': 7500
  '4': 10000
  '5': 12500
```

----

## Creditos
**[FunkyoEnma](https://github.com/FunkyoEnma) [[Redes](linktr.ee/FunkyoEnma)]**