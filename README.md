# Ensayo de Compresión de Hormigón

## Propósito
Este proyecto organiza y documenta el procesamiento de datos obtenidos de un ensayo de compresión en probetas de hormigón. El objetivo es calcular el esfuerzo a partir de la carga aplicada y generar la curva de esfuerzo-desplazamiento, garantizando la reproducibilidad del análisis.

## Entradas
Los datos experimentales provienen de los ensayos de laboratorio y se encuentran en la carpeta `datos_origen`.
*   **Archivo de datos:** `ensayo_hormigon.xlsx` (contiene la tabla original de tiempo, carga y desplazamiento).
*   **Parámetros de la probeta:** Diámetro (D) = 150 mm, Altura (H) = 300 mm.
*   **Área transversal calculada:** A = (π * D²) / 4 = 17671.46 mm²

## Procedimiento
1.  Se extraen los datos crudos (tiempo, carga, desplazamiento) de la tabla original, ignorando los metadatos y notas sueltas.
2.  Se calcula el esfuerzo (σ) utilizando la fórmula σ = P / A, donde P es la carga en kN (convertida a Newtons multiplicando por 1000) y A es el área transversal en mm². El resultado se expresa en Megapascales (MPa).
3.  Se genera el gráfico de Esfuerzo (MPa) vs. Desplazamiento (mm).

## Salidas
Los resultados del análisis se encuentran en la carpeta `resultados`.
*   **Tabla procesada:** Los datos limpios con el cálculo del esfuerzo se consolidaron para análisis.
*   **Gráfico final:** `grafico_final.png` - Curva esfuerzo-desplazamiento con unidades explícitas.

## Herramientas Utilizadas
*   Microsoft Excel: Para revisión inicial de la estructura tabular.
*   Python (Pandas, Matplotlib): Recomendado para la automatización del cálculo de esfuerzo y generación del gráfico reproducible.
*   Git/GitHub: Para el control de versiones y trazabilidad de los cambios.

## Unidades y Supuestos
*   **Tiempo:** [s] (segundos) o minutos (según registro del equipo).
*   **Carga (P):** [kN] (kiloNewtons).
*   **Desplazamiento:** [mm] (milímetros).
*   **Dimensiones (D, H):** [mm].
*   **Esfuerzo (σ):** [MPa] (Megapascales, equivalentes a N/mm²).
*   **Supuesto:** Se asume que la carga en los datos originales está en kN, un estándar común para prensas de ensayo de hormigón.

## Limitaciones
*   Los datos provienen de un integrante anterior; no se cuenta con el registro fotográfico de la falla ni la calibración del equipo.
*   El informe heredado indica que parte de la redacción se apoyó con IA sin especificar los *prompts*, por lo que el análisis de contexto debe auditarse cuidadosamente.
