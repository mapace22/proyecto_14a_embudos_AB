# proyecto_14a_embudos_AB
Análisis de la prueba A/B para embudo en sistema de recomendaciones | Hipótesis, Tasa de Conversión y Sesgo | Python | Pandas | NumPy | Statsmodels | Prueba Z | Jupyter Notebook | Plotly (Sankey) | Matplotlib | Seaborn

# Análisis de Prueba A/B: Sistema de Recomendaciones

Este proyecto analiza una prueba A/B para evaluar un nuevo sistema de recomendaciones en una plataforma de e-commerce y su impacto en la conversión de ventas.

## 🔍 Visión General

**Objetivo principal:**  
Determinar si el nuevo sistema de recomendaciones (Grupo B) incrementa las conversiones comparado con el sistema actual (Grupo A).

## ⚙️ Metodología de Análisis

### 📊 Análisis Exploratorio (EDA)
- **Validación de la prueba**:
  - Desequilibrio en asignación (Grupo A > Grupo B)
  - Grupos comparables en comportamiento y tipo de dispositivo
- **Anomalías detectadas**:
  - Número de compras > adiciones al carrito (posible issue de tracking)
  - Inconsistencias en el embudo de conversión

### 📈 Análisis de Conversiones
**Resultados clave:**
| Métrica               | Grupo A | Grupo B | Diferencia |
|-----------------------|---------|---------|------------|
| Conversión a carrito  | 48.04%  | 51.72%  | +7.66% ↑   |
| Conversión a compra   | 52.05%  | 50.82%  | -2.36% ↓   |

**Visualizaciones:**
- Gráfico de Sankey (flujo del embudo de conversión)
- Diagrama de embudo comparativo

### 📉 Pruebas Estadísticas
| Métrica               | Valor p | Significancia |
|-----------------------|---------|---------------|
| Conversión a carrito  | 0.0012  | ✅ Sí          |
| Conversión a compra   | 0.2808  | ❌ No          |

*Prueba Z aplicada con α=0.05*

## ✅ Conclusiones

1. **Interés inicial ↑ pero ventas ↓**  
   - +7.66% en carritos (significativo)
   - -2.36% en compras (no significativo)

2. **Problemas identificados**:
   - Cuello de botella en etapas finales
   - Posibles errores en tracking

## 🎯 Recomendaciones

1. **Acciones inmediatas**:
   - 🛑 No implementar el nuevo sistema
   - 🔍 Auditoría del sistema de tracking

2. **Próximos pasos**:
   - 🔄 Nueva prueba A/B enfocada en carrito/pago
   - ⚙️ Optimizar flujo de compra post-recomendación

## 💻 Tecnologías Utilizadas

| Categoría           | Herramientas                          |
|---------------------|---------------------------------------|
| Análisis de datos   | Python, Pandas, NumPy                 |
| Estadística         | statsmodels                           |
| Visualización       | Plotly (Sankey), Matplotlib, Seaborn  |
