# Cotización de Comercialización — RBL Automation

Generación de cotizaciones PDF con marca para clientes de RBL Automation, principalmente Caterpillar México.

## Workflow
- Editar script Python → Ejecutar → Sobrescribir el mismo archivo PDF (no crear archivos nuevos en cada iteración)
- Plantilla: esquema de colores azul marino y dorado, banner redondeado "RBL Automation", tablas de línea de artículos en español
- Bloque de términos: tipo de cambio usado, exclusión de IVA, términos de pago (CRÉDITO), validez de 30 días
- Nombres de archivo: `Cotizacion_RBL_Automation_DDMMYY-HHMM.pdf`; números de cotización con formato DDMMYY-HHMM
- Reglas de negocio por defecto: TC 20 MXN/USD y margen de utilidad del 8%

## Stack técnico
- Python con ReportLab y pypdf
- pdftoppm para renderizar previews y calibración de coordenadas

## Contexto de negocio
- Cliente principal: Caterpillar México (Dpto. Compras) — contacto Bryan Brizuela (Bryan.Brizuela@cat.com)
- Se pega un bloque de configuración completo al inicio de cada sesión
- Se suben PDFs originales como referencia visual cuando se necesitan correcciones

## Ejemplo completado
- Cotización formal en MXN para Caterpillar México cubriendo retrofit y calibración de un Leitz PMM-C CMM, basada en cotización de proveedor de ITS Metrology Solutions (TC 20, margen 8%, precios en MXN sin IVA)
