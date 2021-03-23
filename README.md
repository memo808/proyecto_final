# proyecto_final

Guillermo Arturo García Ramírez

A partir de información pública de la Encuesta Nacional sobre Disponibilidad y Uso de Tecnologías de Información y Comunicaciones en los Hogares - ENDUTIH (https://www.inegi.org.mx/programas/dutih/2019/) del Instituto Nacional de Estadística Geografía e Informática (INEGI) se hace un análisis de clasificación de aprendizaje supervisado para las variables de TV de paga, Internet, telefonía fija y telefonía móvil. Esto con el objetivo de saber qué variables determinan el consumo de los hogares mexicanos de estas 4 variables. Asimismo, se analiza si existen indicios de sustitución entre los servicios de TV de paga-Internet y telefonía fija-telefonía móvil.

Se aplican 3 modelos de aprendizaje supervisado de clasificación (logístico, de árboles de decisión y de random forest) para cada una de las 4 variables de interés (TV de paga, Internet, telefonía fija y telefonía móvil). Las variables “target” (que toman valores de 0 y 1) son las 4 variables de interés y las variable explicativas (X) son las diferentes preguntas de la Encuesta Nacional sobre Disponibilidad y Uso de Tecnologías de la Información en los Hogares (ENDUTIH) del INEGI. Dentro de los resultados sobresalen las siguientes variables significativas para determinar o explicar los 4 servicios de interés:
-TV de paga
  * El hogar tiene Internet (logístico, árboles y RandomForest)
  * El hogar utiliza su computadora para ver contenidos por internet (logístico)
  * El hogar utiliza internet para ver OTT gratis (logístico y árboles) 
  * El hogar utiliza smart tv para navegar por internet (logístico y Random Forest)
- Internet
  * El hogar tiene TV de paga (logístico y RandomForest)
  * El hogar utiliza internet para ver OTT de pago (logístico, árboles y RandomForest)
  * El hogar utiliza internet para ver OTT gratis (logístico y árboles)
  * El hogar utiliza smart tv para navegar por internet (logístico, árboles y RandomForest)
- Telefonía fija
  * El hogar cuenta con teléfono celular (logístico y RandomForest)
  * El hogar cuenta con conexión a Internet (logístico, árboles y RandomForest)
  * El hogar utiliza Facebook (logístico y RandomForest)
  * El hogar utiliza internet para realizar llamadas telefónicas y enviar mensajes (Random Forest)
-Telefonía móvil
  * El hogar cuenta con telefonía fija (logístico)
  * El hogar cuenta con conexión a Internet (logístico, árboles y RandomForest)
  * En el hogar tienen instaladas en el celular apps de comunicación (logístico, árboles y RandomForest)
  * En el hogar utilizan Whatsapp (logístico y RandomForest)

¿Qué modelo arrojo los mejores resultados de acuerdo a las métricas de evaluación de accuracy score y AUC?
-TV de paga
  * Accuracy score -> árboles de decisión (0.6392)
  * AUC -> árboles de decisión (0.6456)
- Internet
  * Accuracy score -> random forest (0.85)
  * AUC -> árboles de decisión (0.8557)
- Telefonía fija
  * Accuracy score -> random forest (0.72)
  * AUC -> árboles de decisión (0.7716)
-Telefonía móvil
  * Accuracy score -> random forest (0.80)
  * AUC -> random forest (0.7993)

Los archivos de la ENDUTIH 2019 y los del BIT estaban en formato "CSV" desde su descarga en las fuentes originales. Los archivos de ENDUTIH 2015 a 2018 en las fuentes de descarga están en formato "DBF", por lo que primero se abrieron en Excel para convertirlos a un archivo "CSV" y ya poder abrirlos en Jupyter Notebook y trabajar con ellos.

