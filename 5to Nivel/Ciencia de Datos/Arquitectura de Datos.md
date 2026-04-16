La **arquitectura de datos** es el diseño de sistemas para soportar las necesidades de datos de una empresa. Hay varios patrones de diseño arquitectural tradicionales que evolucionan del [[Data Warehouse]], y un nuevo enfoque moderno denominado [[Data Mesh]].

## Data Fabric

Una data fabric es una capa integrada de datos conectados. Se asume que por debajo de la capa se puede tener variedad de OLTPs, BIs, data lakes, repositorios, etc.

La data fabrics tiene mecanismos para encontrar entidades/tablas/datos. Es la arquitectura de Microsoft Fabric.

## Data Lake

En un data lake se pasa de un [[ETL]] a un ELT. Es la época del big data, donde se utilizaba Hadoop con MapReduce para distribuir horizontalmente la carga durante el procesamiento en paralelo. Spark es similar pero guarda los datos en memoria y permite crear grafos dirigidos acíclicos. Databricks está basado en Spark.

La flexibilidad de los data lakes los puede convertir en data *swamps* a la larga. Hoy en día ya no se usan ya que es muy difícil mantenerlos.

## Data Hub

Es similar a un data lake pero enfocado en servir la información volviendo a los orígenes (las fuentes). Solo una parte de la información se almacena en el "data lake", mientras que el resto se buscan en tiempo real al sistema OLTP.

## Medallion

Bronze (datos crudos) $\longrightarrow$ Silver (datos limpios) $\longrightarrow$ Gold (datos listos para su consumo).

Cada uno de los tres niveles encapsula ciertas transformaciones.

## Lakehouse

Sources $\longrightarrow$ landing zone $\longrightarrow$ bronze $\longrightarrow$ silver $\longrightarrow$ gold.
