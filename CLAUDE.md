# REGLAS MAESTRAS - PROYECTO PRODIGY

## 0. PERMISOS DE EJECUCIÓN (CRÍTICO)
**Claude Code tiene PERMISO TOTAL para ejecutar:**
- ✅ Todos los comandos bash (grep, wc, ls, cp, mv, rm, etc.)
- ✅ Leer cualquier archivo del proyecto
- ✅ Escribir/modificar cualquier archivo del proyecto
- ✅ Crear/eliminar archivos y carpetas
- ✅ Ejecutar scripts de PowerShell
- ✅ Ejecutar Node.js, Python (si están instalados)

**NUNCA pidas confirmación para comandos básicos.**
Solo pregunta si vas a:
- Eliminar archivos importantes sin backup
- Hacer cambios masivos (>200 líneas)
- Instalar dependencias npm/pip

## 1. Ejecución Directa (OVERRIDE)
- NO pidas permiso para ejecutar comandos (`grep`, `view`, `edit`). Ejecuta, verifica y muestra el resultado.
- Solo pide confirmación si el cambio es destructivo o ambiguo.

## 2. Eficiencia Extrema (Tokens)
- NUNCA leas archivos completos de más de 1000 líneas sin usar `grep` primero.
- Realiza ediciones estrictamente QUIRÚRGICAS. No reescribas bloques enteros si solo cambia una línea.

## 3. Contexto PRODIGY
- **Usuario:** Alejandro Carvajal (Experto Exocad/3Shape).
- **Stack:** Vanilla JS, HTML5, CSS3 puro. Rutas relativas siempre.
- **Idioma:** Español estricto en respuestas y comentarios.
- **Sagrado:** La función `calcularTotal()` y el objeto `STATE` solo se tocan con autorización explícita. Nunca uses variables paralelas para precios.

## 4. Reporte de Auditoría y Proactividad (OBLIGATORIO)
Al finalizar CUALQUIER tarea, debes imprimir un "REPORTE DE CAMBIOS" estructurado que contenga:

### Formato del Reporte:

```
═══════════════════════════════════════════════════════
📋 REPORTE DE CAMBIOS - PROYECTO PRODIGY
═══════════════════════════════════════════════════════

1️⃣ ARCHIVOS Y LÍNEAS MODIFICADAS:
-----------------------------------
Archivo: [nombre del archivo]
├─ Líneas leídas: [número]
├─ Líneas modificadas: [número]
└─ Tipo de cambio: [quirúrgico/medio/mayor]

[Repetir para cada archivo]

Total líneas leídas: [suma total]
Total líneas modificadas: [suma total]
Estimado de tokens consumidos: [cálculo aproximado]

2️⃣ RESUMEN TÉCNICO:
-----------------------------------
[Explicación concisa de la lógica aplicada]

- Cambio 1: [descripción]
- Cambio 2: [descripción]
- Cambio N: [descripción]

3️⃣ VERIFICACIÓN:
-----------------------------------
✅ [Comando de verificación 1 + resultado]
✅ [Comando de verificación 2 + resultado]
✅ [Estado antes vs después]

4️⃣ PROPUESTAS PROACTIVAS DE MEJORA:
-----------------------------------
[Si detectaste código duplicado, funciones que se pueden optimizar, 
patrones modernos que aplicar, o mejoras de rendimiento, descríbelas aquí]

💡 Sugerencia 1: [descripción + beneficio]
💡 Sugerencia 2: [descripción + beneficio]

[Si no hay sugerencias, escribir: "No se detectaron oportunidades de mejora en esta área"]

5️⃣ PRÓXIMO PASO RECOMENDADO:
-----------------------------------
[Qué debería hacer Alejandro después de este cambio]

═══════════════════════════════════════════════════════
```

## 5. Horarios y Tiempos de Entrega (Lógica del Negocio)
- **Horario hábil:** 8:00 AM - 6:00 PM
- **Hora de corte:** 5:00 PM (pedidos después de las 5 PM arrancan a las 8 AM del día siguiente)
- **Días laborables:** Lunes a sábado (domingos excluidos)
- **Cálculo de tiempo:** Distribuir `STATE.tiempo` solo dentro del horario hábil
- **Ejemplo:** Si son las 4 PM y el trabajo toma 4 horas:
  - 2 horas hoy (4 PM - 6 PM)
  - 2 horas mañana (8 AM - 10 AM)

## 6. Colores del Tema (Variables CSS)
```css
--gold-primary: #D946A6      /* Magenta/Rosa principal */
--gold-hover: #D4AF37        /* Dorado para hovers */
--accent-cyan: #00d2ff       /* Cyan neón */
--bg-darker: #050505         /* Fondo oscuro */
--bg-card: #1a2332           /* Tarjetas */
--text-primary: #ffffff      /* Texto principal */
--text-secondary: #e2e8f0    /* Texto secundario (alta legibilidad) */
--text-tertiary: #cbd5e1     /* Texto terciario */
--neon-green: #00FF41        /* Verde neón */
```

## 7. Funciones Críticas (NO TOCAR sin autorización)
- `calcularTotal()` - Cálculo de precio final
- `STATE` - Objeto global de configuración
- `calcularFechaEntrega()` - Lógica de tiempos de entrega
