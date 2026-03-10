<div align="center">
<h1> ✨✨✨ CHALLENGE - TelecomX2_LATAM ✨✨✨ </h1>
<h2> Análisis de deserción de Clientes </h2>
</div>

![Badge en Desarollo](https://img.shields.io/badge/ENTREGA-%2018/02/2026-pink)

<h3> Introducción </h3>

Desarrollar modelos predictivos capaces de prever qué clientes tienen mayor probabilidad de cancelar sus servicios.
<h1></h1>

<h3> Tratamiento de Datos </h3>

* Se descargo la información modificada de Telecom X.
* Se importó la información desde un archivo csv.
* Se realizó la eliminación de la columna ID.
* Se identifico y separo las variables explicativas y respuesta.
* Se realizó correlación de los datos.
* Se realizó la normalización de los datos.
* Se realizó el balanceo de los datos.
* Se creó el dummy.
* Se verificaron 4 modelos de comparación.
  * Regresión Logística.
  * Random Forest.
  * Decision Tree.
  * XGBoost.
 * Se realizó la comparación de los modelos.
 * Se realizó un análisis de importancia de las variables.
 * Conclusión.
<h1></h1>

<h3> Análisis dirigido </h3>

<p align="center">
  <img width="500" height="547" alt="image" src="https://github.com/user-attachments/assets/0b89572e-efc9-4065-b13d-836e2b7383bb" />
  <img width="500" height="547" alt="image" src="https://github.com/user-attachments/assets/f7d0ab28-cbbd-4d7b-b20f-5757edf63ff5" />
</p>

<p align="center">
  <img width="699" height="315" alt="image" src="https://github.com/user-attachments/assets/07a60cde-d5c9-4f40-953b-29b2b4b24e15" />
</p>

De los gráficos podemos indicar que:
* Los clientes que cancelan tienden a tener pocos meses de contrato.
* Existe una relación directa entre: Mayor tiempo de contrato -> Mayor gasto total -> Menor probabilidad de churn.
<h1></h1>

<h3> Correlación </h3>
<img width="1886" height="1059" alt="image" src="https://github.com/user-attachments/assets/820a56b5-763c-4d3e-ac92-a064063ffa86" />

<p align="center">
  <img width="500" height="323" alt="image" src="https://github.com/user-attachments/assets/1a11c19d-a85b-42b9-a9f2-62ca7217ce92" />
</p>

La matriz de correlación indica que cada variable tiene una correlación perfecta consigo misma, es decir 1.0.

* Bloques morado fuerte - correlación positiva fuerte.
* Bloques morado claro - correlación negativa fuerte.
* Bloques blancos - casi sin relación.
<h1></h1>

<h3> Modelos de comparación </h3>

<p align="center">
  <img width="500" height="265" alt="image" src="https://github.com/user-attachments/assets/5997e2ee-3a6b-437f-8578-7e712cdf6043" />
</p>

<p align="center">
  <img width="1662" height="606" alt="image" src="https://github.com/user-attachments/assets/b664b772-60e9-43d2-a298-df6a822c38ca" />
</p>

Las métricas más importantes para **Churn** son:
* Recall - El porcentaje de clientes que sí abandonan.

* F1_score - El balance entre:
  - precision - qué tan confiable es cuando predice "churn".
  - Recall - qué tanto detecta churn real.
  
* AUC - Área bajo la curva ROC, qué tan bien el modelo separa a los clientes que abandonan de los que no.
  - 0.50 - modelo aleatorio
  - 0.70 - 0.80 → aceptable
  - 0.80 - 0.90 → muy bueno
  - 0.90 + → excepcional

**Se determina que el modelo de Regresión Logística es el mejor modelo.**
<h1></h1>

<h3> Importacia de las variables </h3>

<p align="center">
  <strong>Importancia de las variables en regresión logística</strong>
</p>
<p align="center">
  <img width="500" height="181" alt="image" src="https://github.com/user-attachments/assets/10ae8fdd-52b7-48c1-aa22-36b925613c70" />
</p>

<p align="center">
  <strong>Importancia de las variables en Random Forest</strong>
<p align="center">
  <img width="500" height="179" alt="image" src="https://github.com/user-attachments/assets/dbc235d9-d276-44cf-801a-bd85cea57791" />
</p>

<p align="center">
  <strong>Importancia de las variables en XGBoost</strong>
<p align="center">
  <img width="500" height="176" alt="image" src="https://github.com/user-attachments/assets/7a85f334-1c73-4ea9-a033-58b00a41fccc" />
</p>

<h3> Conclusión </h3>

* El tipo de contrato es determinante para churn.
  - Mes a mes - alto riesgo.
  - Dos años - bajo riesgo.

* La antigüedad del cliente con la empresa es clave.

* Los cargos mensuales y totales influyen en el churn.
  - Cargos altos - mayor churn.

* El servicio de Internet tipo Fibra es un riesgo. Podría deberse a:
  - Costos altos.
  - Problemas del servicio.
  - Tiempo de instalación.

Los modelos coinciden en que los contratos mensuales generan poca antigüedad y si el cargo es alto generará un churn.
Los clientes con servicio de fibra óptica, son mayormente propensos a cancelar el servicio.

Se debe enforcar la retención en nuevos clientes, contratos flexibles (mes a mes) y costos altos mensules o totales.
<h1></h1>
