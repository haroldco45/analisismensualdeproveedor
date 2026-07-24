# 📊 Financial Analyzer Mensual
## Análisis Operacional Mes a Mes por Proveedor

Una **web app instalable (PWA)** para analizar la salud operacional de cada proveedor MES A MES.

---

## 🎯 ¿Para qué sirve?

Cada mes metes datos **reales y operacionales** y la app te dice:

✅ **¿Me alcanza el inventario para fin de mes?**  
✅ **¿Voy a poder pagar al proveedor?** (margen CxC vs CxP + Inventario como respaldo)  
✅ **¿Qué tan rápido se vende este proveedor?** (rotación mensual)  
✅ **¿En cuántos días se me agota el stock?**  
✅ **¿Qué pasa proyectado a fin de mes?**  
✅ **¿Cuál es mi posición REAL considerando el inventario que tengo?**

**USO REAL**: Cada jueves (o día de corte) ingresas datos del mes y sabes exacto si hay problema o no. **Incluye tu inventario como respaldo operacional.**

---

## 📊 Datos que Necesitas (Operacionales)

| Campo | Significado | Ejemplo |
|-------|-------------|---------|
| **Nombre Proveedor** | Código o nombre | BRINSA |
| **Días Hábiles TOTALES** | Días que se trabaja en todo julio (sin domingos/festivos) | 22 |
| **Días Hábiles TRABAJADOS** | Del 1 hasta hoy (24 julio = 15 días hábiles) | 15 |
| **Ventas Mes Actual** | Lo que VENDISTE de este proveedor este mes | 45,000,000 COP |
| **Inventario Actual** | Lo que TIENES HOY en bodega de este proveedor | 186,250,515 COP |
| **CxC Proveedor** | Lo que TE DEBEN los clientes por compras de este proveedor | 65,000,000 COP |
| **CxP Proveedor** | Lo que LE DEBES al proveedor (lo que le compraste) | 120,000,000 COP |

### 📌 Nota Importante
La app **calcula automáticamente** los días que faltan:
```
Días que Faltan = Días Hábiles Totales - Días Hábiles Trabajados
                = 22 - 15 = 7 días
```

No necesitas ingresar manualmente, la app te lo muestra en tiempo real.

---

## 🛡️ **IMPORTANTE: Margen CON Respaldo**

La app ahora calcula **DOS márgenes diferentes**:

### **1. Margen Simple (CxC - CxP)**
```
Lo que me deben - Lo que debo
346,358,973 - 284,671,374 = +$61,687,599 ✓ Positivo
```

### **2. Margen CON Respaldo (Inventario + CxC - CxP)**
```
Inventario + Lo que me deben - Lo que debo
186,250,515 + 346,358,973 - 284,671,374 = +$247,938,114 ✓ MUCHO MÁS POSITIVO
```

**¿La diferencia?**  
Tu inventario es tu **respaldo más importante**. Puedes venderlo HOY y convertirlo en efectivo para pagar al proveedor.

**En la app:**
- 🔴 Margen Simple negativo = "Parece que debo"
- 🟢 Margen CON Respaldo positivo = "Pero tengo inventario para cubrir"

---

## 🔍 Ejemplo: BRINSA - Julio 2026

### Datos Ingresados:
```
Días hábiles totales del mes: 22
Días hábiles trabajados: 15
👉 APP CALCULA: Días que faltan = 7

Ventas mes: COP 45,000,000
Inventario: COP 186,250,515
CxC (me deben): COP 65,000,000
CxP (le debo): COP 120,000,000
```

### Análisis Inmediato:
```
💵 Venta Diaria:        COP 3,000,000
📦 Rotación Mensual:    0.24x (bajo, inventario lento)

💰 Margen Simple:       -COP 61,687,599 (SIN inventario)
🛡️  Margen CON Respaldo: +COP 124,562,916 (CON inventario como backup)

⏱️  Cobertura Inv:       62 días (alcanza hasta mes que viene)
```

**¿Lo ves?** Sin el inventario parece que debes. Pero CON el inventario tienes $124M+ de respaldo para pagar sin problema.

### Proyecciones a Fin de Mes (31 julio):
```
Ventas proyectadas:     COP 63,000,000 (45M + 3M diaria × 6 días)
CxC proyectada:         COP 77,600,000 (cobros lentos)
Inventario proyectado:  COP 123,250,515 (consumo moderado)
CxP:                    COP 120,000,000 (igual)
Margen proyectado:      -COP 42,400,000 (SIGUE NEGATIVO)
```

### Recomendaciones:
```
🔴 CRÍTICO: Debes MUCHO más de lo que te deben. 
   → Acelera cobro a clientes ASAP
   → Riesgo: No puedas pagar a BRINSA fin de mes

✓ Inventario: Sobra para los 6 días que faltan (62 días de cobertura)
   → No necesitas reorder urgente

⚠️ Rotación lenta: Considera bajar precio/promoción si es viable
```

---

## 🚀 Cómo Usar

### Opción 1: Web en navegador
1. Abre `financial-analyzer.html` en Chrome/Safari
2. Llena los 7 datos operacionales
3. Click en **"🔍 Analizar Mes"**
4. Lee recomendaciones inmediatas

### Opción 2: Instalar como App
**Android/iOS**: Abre → "Instalar" o "Añadir a pantalla de inicio"  
**Escritorio**: Click en ícono de instalación  
✅ Funciona offline una vez instalada

---

## 📈 Qué Hace Diferente Este Análisis

| Métrica | Significado | Acción |
|---------|-------------|--------|
| **Rotación Mensual** | ¿Qué % del inventario se vendió? | Si < 0.2x: inventario congelado |
| **Cobertura Inventario** | ¿Cuántos días de venta tienes? | Si < días que faltan: reorder urgente |
| **Margen Simple** | CxC - CxP (sin contar activos) | Indicador de liquidez inmediata |
| **Margen CON Respaldo** | Inventario + CxC - CxP | Tu posición REAL operacional |
| **Venta Diaria** | Promedio real de ventas/día | Base para proyecciones confiables |
| **Proyecciones Fin Mes** | ¿Cómo termina julio? | Planeación real para agosto |

### ⭐ La Clave: Margen CON Respaldo

Este es **el número más importante** para Harold:
- Si es **POSITIVO** = Posición sólida, tienes cómo pagar
- Si es **NEGATIVO** = Incluso vendiendo todo, hay problema
- Considera tu inventario como **activo líquido** que puedes convertir en efectivo

---

## 🎯 Cuándo Usar Cada Margen

### **Margen Simple (CxC - CxP): Liquidez Inmediata**
Úsalo cuando:
- Necesitas efectivo HOY para pagar al proveedor
- El dinero de clientes aún no ha llegado
- Tienes compromisos de pago próximos

💭 "¿Tengo dinero ahorita para pagar?"

### **Margen CON Respaldo: Posición Operacional Real**
Úsalo cuando:
- Analizas tu salud financiera de proveedor mes a mes
- Tomas decisiones estratégicas (reorder, precio, promociones)
- Presentas reporte a junta directiva/socio

💭 "¿Estoy en buena posición financiera considerando TODO?"

---

## 💾 Datos Guardados

✅ Se guardan **localmente** en tu dispositivo  
✅ NO se envían a internet  
✅ Histórico de análisis anterior  
✅ Puedes borrar cuando quieras  

---

## 📋 Cómo Usar Mes a Mes

### Inicio de Mes (1 de julio)
1. Averigua: ¿Cuántos días hábiles tiene julio?
   - Típicamente: 22 días (6 días/semana)
   - O 20 días (5 días/semana)
   - Ingresa ese número en "Días Hábiles TOTALES"

### Cada Día o Corte
1. Ingresa "Días Hábiles Trabajados" hasta HOY
2. La app **automáticamente** calcula cuántos faltan
3. Completa los otros datos (ventas, inventario, CxC, CxP)
4. Lee análisis y toma decisiones

### Fin de Mes
- Haz un análisis final con todos los datos de julio cerrado
- Prepárate para agosto con el mismo proceso

---

## 🔐 Uso en Distrileco - Flujo Operacional

### Al Inicio de Mes (1 de julio)
- Determina: ¿Cuántos días hábiles tiene julio? (generalmente 22)
- Guarda ese número en la app

### Cada Jueves o Día de Corte
1. Actualiza: ¿Cuántos días hábiles hemos trabajado hasta hoy?
   - App calcula automáticamente cuántos faltan
2. Ingresa datos frescos: ventas mes, inventario HOY, CxC/CxP actualizado
3. Lee análisis: ¿Hay problema de liquidez? ¿Falta inventario?
4. Toma decisión: Reorder urgente? Acelerar cobro? Bajar precio?

### Ejemplo - Viernes 24 de julio (hoy)
```
Entrada:
- Días hábiles totales: 22
- Días trabajados hoy: 15
- App calcula: Faltan 7 días ✓

Otros datos:
- Ventas: COP 45M
- Inventario: COP 186M
- CxC: COP 65M
- CxP: COP 120M

App dice: "Debes COP 55M más de lo que te deben. 
          Acelera cobro AHORA."

Acción: Llamas al gerente de cartera en el acto.
```

**Beneficio**: De "no sé si tengo problema" a "sé exacto qué hacer"

---

## 📅 Guía Rápida: Cómo Calcular Días Hábiles

### Julio 2026 (Ejemplo)
```
Si trabajas 6 días/semana (L-Sa):
- Total julio: 22 días hábiles ← DISTRILECO

Si trabajas 5 días/semana (L-V):
- Total julio: 20 días hábiles  

Si trabajas 24/7:
- Total julio: 31 días
```

### Pasos para Calcular
1. Abre calendario de julio 2026
2. Cuenta: Lunes a sábado (o L-V según tu caso)
3. Excluye: Domingos + festivos si cierras
4. Resultado = Ingresa en "Días Hábiles TOTALES"

### Cada Día
- Mete "Días Hábiles TRABAJADOS" hasta HOY
- App calcula automáticamente cuántos faltan ✓

---

**Desarrollada por Vibras Positivas HM — Derechos de Autor Reservados**
