# ESTRATEXIA DE VERSIONADO

A continuación veras unha breve descrición da estratexía de ramificación e de etiquetaxe das versións operativas do software.

## Ramas

Decidín ramificar o proxecto do seguinte xeito:

| RAMA              | PROPÓSITO
|:-                 |:-
| master            | Integrar as versións listas para produción das outras ramas
| documentacion     | Desenvolvemento da documentación do proxecto
| api               | Desenvolvemento do código da `API`
| frontal           | Desenvolvemento do código do `FRONTAL`
| persistencia      | Desenvolvemento do código do `Sistema de persitencia de datos`
| test_api          | Test da `API`
| test_frontal      | Test do `FRONTAL`
| test_persistencia | Test do `Sistema de persitencia de datos`

## Etiquetas

O modelo da etiquetas para o proxecto describirase na seguinte táboa:

| BLOQUE    | PROPÓSITO
|:-         |:-
| prefixo   | Indicará o tipo de estabilidade e madurez da compilación do módulo
| x         | Incrementos que incorporen un cambio no modelo de datos ou que supoñan cambios importantes. Pode supoñer que sexa preciso unha migración de datos ou que cambien as dependencias do módulo
| y         | Incrementos con novas funcionalidades estables. Pode supoñer unha actualización do módulo
| z         | Incrementos que solucionen erros (bugs)
| sufixo    | Indicará o módulo que está sendo versionado
Información sobre os `prefixos` e os `sufixos`:

| PREFIXOS  | PROPÓSITO
|:-         |:-
| a         | Versión en probas `alfa` aínda sen test completo
| b         | Versión en probas `beta` aínda sen test completo
| rc        | Versión na última fase de probas antes de ser promovida como versión en produción `release candidate`
| v         | Versión estable `release branch` para implementar en produción

| SUFIXOS       | PROPÓSITO
|:-             |:-
| api           | Indicará que o versionado corresponde ó módulo da `API`
| frontal       | Indicará que o versionado corresponde ó módulo do `FRONTAL`
| persistencia  | Indicará que o versionado corresponde ó módulo do `persistencia de datos`

Estas etiquetas serán idénticas á versión do package.json a excepción dos prefixos e sufixos que serán suprimidos.

## Exemplos

``` bash
a0.9.0-api
b0.9.3-api
rc0.9.5-frontal
v1.0.0-frontal
```