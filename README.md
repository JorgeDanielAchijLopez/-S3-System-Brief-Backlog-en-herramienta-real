# -S3-System-Brief-Backlog-en-herramienta-real
# 1 Nombre del Sistema
InvControl Pro
(Sistema de Gestión de Inventarios, Ventas Diarias y Conciliación Contable)
# 2 Problema que resuelve 
Muchos pequeños y medianos negocios gestionan su inventario y ventas diarias de forma manual (Excel o papel), lo que genera errores en conteo, diferencias entre inventario físico y sistema, y poca claridad sobre ganancias reales.
Además, la conciliación entre ventas, facturas contables y existencias suele hacerse de forma separada, causando inconsistencias.
No existe una vista integrada que permita conocer en tiempo real:
--ventas por día
--estado actual del inventario por código de producto
--diferencias por conciliación
--estado de ganancias y pérdidas
--Esto impacta la toma de decisiones financieras y operativas.
# 3 Usuarios / Stakeholders 
--Administrador del negocio – necesita control financiero y reportes.
--Encargado de inventario – registra productos y realiza conciliaciones.
--Contador – registra facturas manuales y revisa ganancias/pérdidas.
--Dueño/Propietario – interesado en indicadores de rentabilidad.
# 4 Objetivos de éxito 
--Reducir en al menos 80% los errores de conciliación manual.
--Permitir visualizar ganancias/pérdidas en menos de 5 segundos.
--Registrar ventas diarias en menos de 1 minuto por operación.
--Detectar diferencias de inventario el mismo día que ocurren.
# 5 Alcance 
--Registro de productos con código único.
--Registro de ventas diarias por producto.
--Actualización automática del inventario al vender.
--Módulo de conciliación de inventario (físico vs sistema).
--Registro manual de facturas contables.
--Panel de ganancias y pérdidas.
--Reporte básico por día.
--Gestión básica de usuarios (admin / inventario).
# 6 Fuera de Alcance (No incluye) 
--Integración con sistemas bancarios.
--Facturación electrónica automática ante la SAT.
--Aplicación móvil nativa.
--Inteligencia artificial predictiva.
--Integración con e-commerce externo.
# 7 Supuestos 
--El negocio trabaja con productos identificados por código único.
--Las ventas se registran el mismo día que ocurren.
--El usuario tiene conocimientos básicos de computación.
--El inventario inicial será cargado manualmente.
--No se requiere conexión con sistemas fiscales gubernamentales en v1.
# 8 Riesgos + Mitigaciones 
--Riesgo: Usuarios no registran ventas correctamente.
Mitigación: Interfaz simple + validaciones obligatorias.

--Riesgo: Datos inconsistentes en conciliación.
Mitigación: Registro histórico de movimientos + auditoría básica.

--Riesgo: Resistencia al cambio (uso de Excel previo).
Mitigación: Capacitación breve y sistema intuitivo.
# 9 Requerimientos v1
Functional Requirements (FR) 
--FR1. El sistema debe permitir registrar productos con código único, nombre, costo y precio de venta.
--FR2. El sistema debe permitir registrar ventas diarias asociadas a un producto.
--FR3. El sistema debe descontar automáticamente el inventario al registrar una venta.
--FR4. El sistema debe permitir realizar conciliación ingresando cantidad física y mostrar diferencias.
--FR5. El sistema debe permitir registrar facturas contables manualmente (gasto o ingreso).
--FR6. El sistema debe mostrar un reporte de ganancias y pérdidas por rango de fecha.
--FR7. El sistema debe generar un historial de movimientos por producto.
# 10 Non-Functional Requirements (NFR) 
flowchart LR
    Admin[Administrador]
    Inventario[Encargado de Inventario]
    Contador[Contador]
    Sistema[InvControl Pro]
    Reportes[Reportes Financieros]

    Admin -->|Consulta Reportes| Sistema
    Inventario -->|Registra productos y conciliaciones| Sistema
    Contador -->|Registra facturas| Sistema
    Sistema -->|Genera| Reportes
    Sistema -->|Muestra estado de| Admin 
    

