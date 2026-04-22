# Reporte Gerencial Grapes Market

Sistema de reportería gerencial automatizada en Python que consolida múltiples fuentes exportadas del ERP (GlobalBluePoint) para generar análisis de ventas, stock y rentabilidad en USD — información que el sistema no provee de forma nativa.

## Problema

El ERP utilizado no permite cruzar datos entre módulos ni visualizar métricas en USD. Los reportes de ventas, costos, stock y movimientos viven en exportaciones separadas sin forma de consolidarlos desde el sistema.

## Solución

Pipeline en Python/pandas que integra 5+ fuentes de datos y genera automáticamente:
- Presentación PPT con indicadores gerenciales
- Planilla Excel con análisis detallado por SKU

## Análisis incluidos

- Ventas y rentabilidad en USD (profit por SKU, por marca, por canal)
- Clasificación ABC por profit
- Rotación de inventario y cobertura en meses
- Aging de stock (productos sin movimiento, en riesgo)
- Quiebres de stock
- Seguimiento de órdenes por proveedor (QNAP, 10GTeK)
- Análisis canal MercadoLibre vs venta directa
- Plan de reposición con lead time y nivel de servicio

## Stack

- Python · pandas · NumPy
- python-pptx · openpyxl
- fuzzywuzzy · Google Colab

## Estructura

Los datos de entrada se leen desde `./data/` (exportaciones del ERP en `.xlsx`). El notebook está pensado para correr en Google Colab con Google Drive montado.

## Nota

Los datos utilizados son propietarios. El notebook se publica sin outputs ni datos reales.
