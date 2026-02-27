# System Brief – InvControl Pro

## Problema

Muchos pequeños y medianos negocios gestionan su inventario y ventas manualmente, lo que genera errores en el control de existencias y diferencias entre inventario físico y sistema. Además, las facturas contables y ventas no siempre están integradas, dificultando conocer las ganancias reales.

InvControl Pro centraliza inventario, ventas y registro contable en un solo sistema.

---

## Stakeholders

- Administrador del negocio
- Encargado de inventario
- Contador
- Propietario

---

## Scope (Incluye)

- Registro de productos con código único
- Registro de ventas diarias
- Descuento automático de inventario
- Conciliación de inventario
- Registro manual de facturas
- Reporte de ganancias y pérdidas

---

## No-Scope (No incluye)

- Integración bancaria
- Facturación electrónica SAT
- Aplicación móvil
- Integración con e-commerce
- Multi-sucursal

---

## Diagrama de Contexto

```mermaid
flowchart LR
    Admin[Administrador]
    Inventario[Encargado Inventario]
    Contador[Contador]
    Sistema[InvControl Pro]
    Reportes[Reportes Financieros]

    Admin -->|Consulta reportes| Sistema
    Inventario -->|Registra productos y conciliia| Sistema
    Contador -->|Registra facturas| Sistema
    Sistema -->|Genera| Reportes
