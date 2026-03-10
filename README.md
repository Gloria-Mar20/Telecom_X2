<div align="center">
<h1>  CHALLENGE - TelecomX2_LATAM  </h1>
<h2> Análisis de deserción de Clientes </h2>
</div>



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
  <img width="1595" height="1178" alt="graf1" src="https://github.com/user-attachments/assets/0b797130-6c1b-42b8-8332-1e97ad6a7c36" />
  <img width="1648" height="1176" alt="graf2" src="https://github.com/user-attachments/assets/f4a6475c-3343-45e3-881e-b15db9a1cb66" />
</p>

<p align="center">
<img width="2578" height="1176" alt="graf3" src="https://github.com/user-attachments/assets/fa5d8337-ceec-47bc-9b43-9b7217a98aea" />
</p>

De los gráficos podemos indicar que:
* Los clientes que cancelan tienden a tener pocos meses de contrato.
* Existe una relación directa entre: Mayor tiempo de contrato -> Mayor gasto total -> Menor probabilidad de churn.
<h1></h1>

<h3> Correlación </h3>
<img width="4732" height="3954" alt="graf4" src="https://github.com/user-attachments/assets/efaa37a2-32e5-414f-9647-d550d4b3d356" />
</p>

La matriz de correlación indica que cada variable tiene una correlación perfecta consigo misma, es decir 1.0.

* Bloques morado fuerte - correlación positiva fuerte.
* Bloques morado claro - correlación negativa fuerte.
* Bloques blancos - casi sin relación.
<h1></h1>
<h3> Modelos de comparación </h3>

<p align="center">
<img width="321" height="115" alt="tabla " src="https://github.com/user-attachments/assets/4ab44255-bfe4-4c5d-bccb-e75bc124e285" />
</p>

<p align="center">
<img width="6544" height="2366" alt="graf-final" src="https://github.com/user-attachments/assets/04af8b22-1af1-4696-93cb-c67ce33d9e11" />
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





