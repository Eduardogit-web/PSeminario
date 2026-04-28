```markdown
#  Ficha del Dataset: Amazon Fine Food Reviews

## 1. Información General
* **Nombre:** Amazon Fine Food Reviews
* **Fuente:** Kaggle / Stanford Network Analysis Project (SNAP)
* **Tamaño Original:** 568,454 registros.
* **Número de Columnas:** 10.
* **Licencia:** Dominio Público (CC0).

## 2. Diccionario de Datos

| Columna | Tipo | Descripción |
| :--- | :--- | :--- |
| `ProductId` | String | Identificador único del producto (ASIN). |
| `UserId` | String | Identificador único del usuario. |
| `HelpfulnessNumerator` | Int | Usuarios que votaron "Es útil". |
| `HelpfulnessDenominator`| Int | Total de usuarios que votaron. |
| `Score` | Int | Calificación (1 a 5 estrellas). |
| `Time` | Timestamp | Fecha en formato Unix. |
| `Summary` | String | Resumen corto de la reseña. |
| `Text` | String | Cuerpo completo de la reseña. |

## 3. Diagnóstico de Calidad
* **Duplicados:** Se detectaron múltiples entradas para el mismo `UserId`, `ProductId` y `Time`. Estos serán eliminados.
* **Sesgo de Votos:** Gran cantidad de registros tienen 0 votos, lo que impide calcular una tasa de utilidad representativa. Se aplicará un filtro de confianza de $\ge 5$ votos totales.
* **Variable Objetivo:** Se define como útil una reseña con un ratio $\ge 0.7$ (70% de votos positivos).

## 4. Limitaciones
* **Fecha:** Datos actualizados solo hasta 2012.
* **Idioma:** Dataset limitado exclusivamente al idioma inglés.
* **Subjetividad:** La utilidad es un concepto subjetivo que varía según el tipo de producto.