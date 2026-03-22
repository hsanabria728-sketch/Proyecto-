# 🔧 Análisis de Fallas en Robots de Ensamblaje Industrial
### Proyecto Final — Módulo 3: Visualización Inteligente | EAN Universidad 2024

![Excel + IA](https://img.shields.io/badge/Excel-IA--Powered-217346?style=flat&logo=microsoft-excel&logoColor=white)
![Módulo 3](https://img.shields.io/badge/EAN-M%C3%B3dulo%203-1F3864?style=flat)
![Área](https://img.shields.io/badge/%C3%81rea-Ingenier%C3%ADa%20Mecatr%C3%B3nica-00B0F0?style=flat)
![Estado](https://img.shields.io/badge/Estado-Completo-00B050?style=flat)

---

## 📋 Descripción del Proyecto

Este proyecto aplica **Excel con Inteligencia Artificial** para analizar **60 eventos de falla** registrados en robots de ensamblaje industrial durante el año 2024 en la Planta Mecatrónica EAN.

### Problema Resuelto
> ¿Cómo identificar patrones de falla, priorizar mantenimiento y reducir costos operativos en una planta con 8 robots industriales usando Excel + IA?

### Resultado
Dashboard interactivo con KPIs de mantenimiento predictivo que permite tomar decisiones basadas en datos, identificando el 15-20% de fallas que generan el 60-70% del impacto económico.

---

## 📂 Estructura del Repositorio

```
📦 proyecto-fallas-robots-ean/
├── 📊 Dashboard_Fallas_Robots.xlsx    # Archivo principal con dashboard interactivo
├── 📄 Informe_Proyecto_Final.docx     # Bitácora y análisis completo
├── 📋 README.md                       # Este archivo
└── 🎬 [enlace-video]                  # Video de presentación (ver sección Videos)
```

---

## 🗂️ Contenido del Archivo Excel

| Hoja | Descripción |
|------|-------------|
| `Datos_Crudos` | 60 registros originales de fallas con 10 variables |
| `Datos_Limpios` | Datos enriquecidos con fórmulas IA: Mes, Semestre, Índice de Criticidad |
| `Análisis` | Estadísticas por tipo de falla, KPIs globales, análisis por robot + gráficos |
| `DASHBOARD` | Dashboard interactivo con KPIs, gráficos y tabla de estado por robot |
| `Instrucciones_IA` | Guía de prompts para usar con Excel Ideas y Copilot |

---

## 🤖 Herramientas de IA Utilizadas

### Excel Ideas
- Análisis automático de patrones en el dataset
- Sugerencias de visualizaciones relevantes
- Detección de outliers en costos y tiempos de paro

**Cómo activarlo:**
```
Seleccionar rango Datos_Limpios!A2:L62 → Insertar → Ideas
```

### Microsoft Copilot en Excel
Prompts utilizados en el proyecto:

```
"Analiza las fallas más frecuentes por tipo y robot en 2024"
"¿Cuál es el tipo de falla con mayor costo acumulado?"
"Genera una fórmula para calcular el MTBF por robot"
"Crea un gráfico de barras de fallas por mes del año 2024"
"Resume los robots con mayor costo de mantenimiento"
```

### Power Query
- Limpieza y estandarización de fechas
- Creación de columnas calculadas (Mes, Semestre)
- Transformación de tipos de dato

---

## 📊 KPIs del Dashboard

| KPI | Descripción | Fórmula Excel |
|-----|-------------|---------------|
| **Total Fallas** | Eventos registrados en 2024 | `=COUNTA(Datos_Limpios!A3:A62)` |
| **Costo Total** | Inversión total en reparaciones | `=SUM(Datos_Limpios!G3:G62)` |
| **Horas de Paro** | Tiempo productivo perdido | `=SUM(Datos_Limpios!F3:F62)` |
| **Fallas Críticas** | Eventos con alta prioridad | `=COUNTIF(Datos_Limpios!L3:L62,"CRÍTICA")` |
| **Costo Promedio** | Costo por evento de falla | `=AVERAGE(Datos_Limpios!G3:G62)` |
| **Paro Promedio** | Duración media por falla | `=AVERAGE(Datos_Limpios!F3:F62)` |

---

## 🏭 Caso de Aplicación

**Contexto:** Planta de manufactura de componentes electrónicos con 8 robots industriales (ROB-001 a ROB-008) operando en 3 turnos.

**Variables analizadas:**
- 🔴 **Tipos de Falla:** Eléctrica, Mecánica, Neumática, Software, Sensor, Hidráulica
- ⚙️ **Componentes:** Motor principal, Actuador lineal, PLC, Sensor posición, Válvula solenoide, Encoder rotativo, Cilindro hidráulico, Servo drive, Panel HMI, Reductor planetario
- 📅 **Período:** Enero — Diciembre 2024
- 👷 **Turnos:** Mañana, Tarde, Noche

**Índice de Criticidad (fórmula IA-asistida):**
```excel
=IF(AND(Tiempo_Paro>20, Costo>2000), "CRÍTICA",
  IF(AND(Tiempo_Paro>10, Costo>1000), "ALTA",
    IF(Tiempo_Paro>5, "MEDIA", "BAJA")))
```

---

## 🚀 Cómo Usar este Proyecto

### Requisitos
- Microsoft Excel 365 (para funciones de IA completas)
- Acceso a Microsoft Copilot (opcional, para funciones avanzadas)

### Pasos
1. **Abrir** `Dashboard_Fallas_Robots.xlsx`
2. **Ir a la hoja** `DASHBOARD` para ver el resumen ejecutivo
3. **Explorar** `Datos_Limpios` para ver los datos enriquecidos
4. **Revisar** `Análisis` para ver los gráficos estadísticos
5. **Consultar** `Instrucciones_IA` para replicar el análisis con Copilot/Ideas
6. **Activar interactividad:** Insertar → Segmentador de datos → Turno / Robot / Criticidad

---

## 💡 Hallazgos Principales

- 🔴 Los tipos **Eléctrica** y **Mecánica** concentran el mayor número de fallas
- 🌙 El **turno nocturno** presenta mayor incidencia en robots de alta antigüedad
- 💰 El **15-20% de fallas críticas** genera el **60-70% del costo total**
- ⏱️ La IA reduce el tiempo de análisis exploratorio aproximadamente un **70%**

---

## ⚖️ Reflexión Ética

Este proyecto incorpora IA de manera responsable:

- ✅ **Datos simulados** — No se usan datos reales de empleados
- ✅ **Fórmulas documentadas** — Toda lógica es transparente y auditable
- ✅ **Validación humana** — La IA apoya pero no reemplaza el juicio del ingeniero
- ✅ **Privacidad considerada** — Guía de manejo de datos en `Instrucciones_IA`
- ✅ **Reproducibilidad** — Instrucciones completas para replicar el análisis

---

## 📚 Competencias Desarrolladas (EAN Módulo 3)

| Competencia | Nivel |
|-------------|-------|
| Comprensión de conceptos IA en Excel | ⭐⭐⭐⭐⭐ |
| Aplicación técnica (Copilot, Ideas, Power Query) | ⭐⭐⭐⭐⭐ |
| Limpieza y análisis con IA | ⭐⭐⭐⭐⭐ |
| Visualización y comunicación (Dashboard) | ⭐⭐⭐⭐⭐ |
| Documentación y ética | ⭐⭐⭐⭐⭐ |

---

## 📖 Referencias

- Microsoft. (2024). *Excel Ideas — Análisis inteligente de datos*. Microsoft Support.
- Microsoft. (2024). *Microsoft Copilot en Excel*. Microsoft 365.
- EAN Universidad. (2024). *Módulo 3: Visualización Inteligente y Proyecto Aplicado*.
- Moubray, J. (1997). *Reliability-Centered Maintenance (RCM II)*. Industrial Press.
- Nakajima, S. (1988). *Introduction to TPM: Total Productive Maintenance*. Productivity Press.

---

## 👤 Autor

**Estudiante de Ingeniería Mecatrónica**
Universidad EAN — Proyecto Final Módulo 3
2024

---

*Proyecto desarrollado con fines académicos para la certificación del Módulo 3 de Excel con IA — EAN Universidad.*
