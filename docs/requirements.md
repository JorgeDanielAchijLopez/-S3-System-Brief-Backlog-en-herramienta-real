
```markdown
# Requirements – InvControl Pro

## Link al Backlog

Tablero del proyecto:
https://trello.com/invite/b/69a13d69fc56024f57f95125/ATTIfdd25a428ed3c6fcf224fff46a57acd0C0F953F1/invcontrol-pro-product-backlog 

---

## Historias de Usuario

1. Registrar productos con código único — **Must**
2. Registrar venta diaria — **Must**
3. Conciliación de inventario — **Must**
4. Registrar facturas contables — **Must**
5. Ver reporte de ganancias y pérdidas — **Should**
6. Historial de movimientos por producto — **Should**
7. Gestión básica de usuarios — **Could**
8. Exportar reporte a PDF — **Won’t (por ahora)**

---

## Historias Must con criterios Given/When/Then

### 1 Registrar productos con código único (Must)

**Given** que el usuario está en el módulo de productos  
**When** ingresa un código nuevo válido  
**Then** el sistema debe permitir guardar el producto correctamente  

**Given** que ya existe un producto con el mismo código  
**When** intenta registrarlo nuevamente  
**Then** el sistema debe mostrar un mensaje de error  

---

### 2 Registrar venta diaria (Must)

**Given** que el producto tiene stock disponible  
**When** el usuario registra una venta  
**Then** el sistema debe descontar la cantidad vendida del inventario  

**Given** que el stock es menor a la cantidad solicitada  
**When** el usuario intenta registrar la venta  
**Then** el sistema debe impedir la operación y mostrar una alerta  

---

## MVP Rationale

El MVP está compuesto por las cuatro historias con prioridad Must: registro de productos, registro de ventas, conciliación de inventario y registro de facturas contables. 
Estas funcionalidades permiten cubrir el problema principal del sistema: controlar inventario y reflejar correctamente las ganancias del negocio. Sin estas historias, el sistema no cumpliría su propósito central.
Las historias Should, Could y Won’t se consideran mejoras posteriores para ampliar funcionalidad sin afectar el núcleo del producto.
