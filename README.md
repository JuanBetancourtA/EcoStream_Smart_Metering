# EcoStream Smart Metering - Detección de Anomalías e Hidro-Fugas

## 📊 Vista General del Dashboard
Aquí puedes ver el resultado visual de la solución desarrollada:
![Dashboard de Control](Deteccióndeanomalíasyfugasocultas.png)

## 🏢 Contexto del Proyecto
Este proyecto simula un escenario real en una empresa de gestión hidráulica (**EcoStream**). El objetivo principal consiste en analizar las lecturas por telemedida de los contadores inteligentes (smart meters) distribuidos en tres barrios principales de Madrid (Centro, Retiro y Salamanca) para identificar ineficiencias de consumo, pérdidas de agua no contabilizadas y posibles fugas en la red.

## 🛠️ Tecnologías Utilizadas
* **Base de Datos:** Arquitectura de datos relacional modelada inicialmente en SQLite.
* **Modelo de Datos:** Implementación de un modelo en estrella (Star Schema) en Power BI con tablas de dimensiones (`Dim_Contadores`, `Dim_Geografia`) y una tabla de hechos (`Fact_Lecturas_Horarias`).
* **Lenguaje DAX:** Creación de medidas explícitas y optimizadas para calcular el consumo total y segmentar el comportamiento nocturno.
* **Visualización:** Power BI Desktop aplicando un diseño de interfaz ejecutivo de alto contraste orientado a salas de control.

## 🔍 Principales Hallazgos y Lógica de Negocio
* **Detección de la Anomalía:** Al cruzar los consumos por tramos horarios, se identificó un comportamiento crítico en el barrio de **Salamanca**. Mientras que los perfiles residenciales normales (Centro y Retiro) reducen su consumo a prácticamente cero durante la madrugada (00:00 a 06:00), Salamanca mantiene un flujo constante de **108 m³**.
* **Impacto Operativo:** Este patrón técnico confirma la existencia de una **fuga oculta o una pérdida de agua estructural** de gran volumen en la red de distribución de esa zona, permitiendo a los equipos de ingeniería priorizar el mantenimiento correctivo y evitar el desperdicio de recursos.
