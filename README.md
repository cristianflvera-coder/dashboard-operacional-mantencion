# 📊 Dashboard Operacional — Área de Mantención

> **Proyecto personal implementado en entorno real de trabajo**  
> Empresa de logística y distribución nacional | Área de Mantención Industrial  
> **Actualmente instalado en pantalla de la oficina, visible para todo el equipo**

---

## 🧩 Problema que resolvía

El sistema de bitácora digital (proyecto anterior) generaba más de 2.200 registros de actividad técnica, pero la visualización disponible tenía limitaciones críticas:

- El dashboard nativo de Google Forms **solo era accesible por el jefe del área**, quien debería compartir su cuenta para que otros lo vieran
- Contenía **demasiada información irrelevante**, lo que dificultaba la toma de decisiones rápida
- Para obtener datos clave, la jefatura debía **abrir Excel o el computador** y buscar manualmente
- No existía una vista unificada y simple que permitiera **de un solo vistazo** identificar quién estaba por debajo de las estadísticas aprobadas

---

## 💡 Solución implementada

Diseñé un dashboard operacional en **Google Looker Studio**, conectado en tiempo real a la base de datos de la bitácora en Google Sheets, con acceso público por link para todo el equipo y visualización permanente en una pantalla de la oficina.

### Flujo del sistema

```
Google Sheets (Bitácora)
       │
       │  Conexión en tiempo real
       ▼
  Google Looker Studio
       │
       ├── Dashboard visible en pantalla de oficina (acceso público)
       ├── Filtro de período configurable (día / semana / mes / año)
       └── Link compartido al equipo vía WhatsApp
```

---

## 📈 Gráficos implementados

| Gráfico | Tipo | Información que entrega |
|---|---|---|
| Actividad por técnico | Barras horizontales | Quién ha enviado más y menos registros en el período |
| Evolución en el tiempo | Líneas | Comportamiento de la actividad durante el año |
| Actividad por tipo de trabajo | Circular | Qué clase de trabajos se realizan y en qué proporción |
| Actividad por turno | Circular | Distribución de trabajos por turno (mañana/tarde/noche/intermedio) |
| Actividad por ubicación | Barras | Qué áreas y máquinas concentran más intervenciones |
| Filtro de período | Control interactivo | Permite filtrar todos los gráficos por rango de fechas simultáneamente |

---

## 🎯 Valor generado

**Para la jefatura:**
- Visibilidad inmediata al llegar a la oficina, sin abrir Excel ni el computador
- Identificación instantánea de técnicos por debajo de las estadísticas aprobadas
- Análisis del comportamiento del equipo por día, semana, mes o el período que estime conveniente
- Comprensión clara de qué áreas concentran más trabajo y qué tipo de intervenciones se realizan

**Para el equipo:**
- Dashboard visible para todos en la pantalla de la oficina, sin necesidad de compartir cuentas
- Transparencia sobre el rendimiento colectivo e individual
- Acceso al link desde cualquier celular vía WhatsApp

---

## 🔄 Comparativa antes / después

| Aspecto | Antes | Después |
|---|---|---|
| Acceso | Solo el jefe (cuenta privada) | Todo el equipo (link público) |
| Visualización | Dashboard nativo de Forms con exceso de datos | Vista limpia con solo los datos relevantes |
| Disponibilidad | Requería abrir computador o Excel | Pantalla permanente en la oficina |
| Filtro de período | No disponible de forma simple | Control interactivo configurable |
| Actualización | Manual | Tiempo real automático |
| Toma de decisiones | Lenta, requería búsqueda manual | Inmediata, de un solo vistazo |

---

## 🔒 Consideraciones de seguridad

Como parte de mi formación en ciberseguridad, identifiqué los siguientes puntos relevantes:

### ✅ Controles existentes
- El dashboard es de **solo lectura**, nadie puede modificar los datos desde él
- Los datos originales en Google Sheets mantienen acceso restringido al propietario
- El link público solo permite visualizar, no editar ni exportar los datos subyacentes

### ⚠️ Consideraciones identificadas
1. **Acceso no autenticado** — Cualquier persona con el link puede ver el dashboard, incluyendo datos de productividad individual del personal
2. **Sin control de acceso por roles** — No es posible mostrar distintas vistas según quién accede (jefatura vs técnico vs externo)
3. **Datos personales visibles** — Los nombres completos de los técnicos son visibles públicamente para quien tenga el link
4. **Sin registro de quién accede** — Looker Studio no registra quién visualiza el dashboard ni desde dónde

### 🔧 Mejoras propuestas
- Implementar acceso por dominio de Google Workspace corporativo en lugar de link público
- Crear vistas diferenciadas por rol mediante filtros de identidad
- Evaluar si los nombres completos deben reemplazarse por identificadores internos

> *Análisis desarrollado como parte de mi formación en Técnico en Ciberseguridad (Instituto Profesional San Sebastián, en curso desde marzo 2026).*

---

## 🛠️ Tecnologías utilizadas

- **Google Looker Studio** — Visualización de datos y dashboard interactivo
- **Google Sheets** — Fuente de datos en tiempo real
- **Google Forms** — Captura de datos origen (ver proyecto anterior)
- **WhatsApp** — Distribución del link al equipo

---

## 📸 Capturas

![Dashboard Operacional](dashboard_preview.png)

---

## 🔗 Proyecto relacionado

Este dashboard es una extensión del proyecto **Sistema de Bitácora Digital**, disponible en:  
[github.com/cristianfloresvera/sistema-bitacora-operacional](https://github.com/cristianfloresvera/sistema-bitacora-operacional)

---

## 👤 Autor

**Cristian Flores Vera**  
Técnico Eléctrico de Mantención → Técnico en Ciberseguridad (en formación)  
📍 Santiago, Chile  
🔗 [linkedin.com/in/cristianfloresvera](https://linkedin.com/in/cristianfloresvera)  
🎓 CISCO Networking Academy | Instituto Profesional San Sebastián

---

*Dashboard diseñado e implementado íntegramente por el autor, conectado a datos reales de operación. Actualmente en uso activo en pantalla de la oficina del área de mantención.*
