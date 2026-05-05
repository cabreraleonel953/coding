---
marp: true
theme: default
paginate: true
header: 'Sistema de Inventario y E-commerce - Ferretería'
footer: 'Presentación de Proyecto Final - Victor Leonel Cabrera Garduño'
style: |
  section { background-color: #ffffff; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; }
  h1 { color: #2c3e50; border-bottom: 2px solid #3498db; }
  h2 { color: #2980b9; }
  .columns { display: grid; grid-template-columns: repeat(2, minmax(0, 1fr)); gap: 1rem; }
---

# Desarrollo de Sistema de Control de Inventario y E-commerce

**Presenta:** Victor Leonel Cabrera Garduño
**Fecha:** 11 de Mayo del 2026
<!-- _paginate: Hide -->

---

## 1. Introducción y Contexto
*   **El Negocio:** Ferretería familiar con más de 1,000 productos en stock.
*   **Operación Actual:** Gestión basada 100% en la memoria del dueño y hojas de papel.
*   **El Reto:** Evolucionar un negocio tradicional hacia la era digital sin interrumpir la operación diaria.

---

## 2. Justificación del Proyecto 
¿Por qué se realiza  este sistema?
*   **Pérdida Económica:** Ventas no concretadas por desconocimiento de existencias.
*   **Ineficiencia en Compras:** Actualmente se compra por "intuición", lo que genera sobrestock de productos de baja rotación.

---

## 3. Análisis de Procesos
<div class="columns">
<div>

### Proceso Actual
1. Cliente pregunta.
2. Hace uso de su memoria para saber si cuenta con stock.
3. Venta manual (sin registro de stock).
4. El dueño estima cuándo volver a comprar.
</div>
<div>

### Proceso Propuesto 
1. Consulta rápida en tablet/PC.
2. Venta registra salida automática.
3. El sistema alerta: "Stock bajo".
4. El cliente compra desde su casa vía web.
</div>
</div>

---

## 4. Definición del Alcance 
Para asegurar el éxito en 6 semanas, hemos delimitado el proyecto:

*   **Prioridad 1:** Control de inventario (Altas, Bajas, Modificaciones).
*   **Prioridad 2:** E-commerce con carrito de compras para público general.
*   **Prioridad 3:** Panel de cotizaciones para clientes mayoristas.


---

## 5. Arquitectura Técnica del Sistema
*Inserta aquí tu imagen de Arquitectura de Capas*
![w:700](URL_IMAGEN_ARQUITECTURA)

*   **Frontend:** Interfaz web para administradores y clientes.
*   **Backend/DB:** Repositorio centralizado para productos, pedidos y usuarios.

---

## 6. Modelo de Datos y Entidades
*Inserta aquí tu imagen de Entidades de Negocio*
![w:800](URL_IMAGEN_ENTIDADES)

*   Estructura relacional de 6 tablas principales para garantizar la integridad de la información.

---

## 7. Plan de Trabajo: Metodología Scrum
*Inserta aquí tu imagen del Diagrama de Gantt*
![w:900](URL_IMAGEN_GANTT)

*   **Ciclos Cortos:** 3 Sprints para entregar valor incremental cada 2 semanas[cite: 1].

---

## 8. Gestión de Datos: Calidad e Históricos
*   **Migración Inicial:** Se realizará un conteo físico de 500 productos para asegurar un 90% de precisión inicial[cite: 1].
*   **Frecuencia:** Actualización en tiempo real (Real-time update) en cada transacción[cite: 1].
*   **Seguridad:** Roles diferenciados para que los empleados no puedan borrar el catálogo[cite: 1].

---

## 9. Análisis de Negocio (Modelos Descriptivos)
El sistema no solo guarda datos, ayuda a pensar:
*   **Modelo de Rotación:** ¿Qué herramientas se venden cada 15 días y cuáles cada 3 meses?[cite: 1]
*   **Antigüedad de Stock:** Identificación de "productos estancados" para aplicar promociones[cite: 1].
*   **Dashboard de Decisiones:** Vista rápida de qué comprar hoy basándose en el stock mínimo[cite: 1].

---

## 10. Soporte y Capacitación
Para que el sistema sea adoptado con éxito[cite: 1]:
*   **Manual de Usuario:** Guía paso a paso para el dueño y empleados[cite: 1].
*   **Sesiones Prácticas:** Capacitación en entorno de pruebas antes de salir a producción[cite: 1].
*   **Documentación Técnica:** Código comentado para futuros mantenimientos[cite: 1].

---

## 11. Conclusiones y Futuro
*   **Resultados Esperados:** Reducción de faltantes, ahorro de tiempo y presencia digital profesional[cite: 1].
*   **Próximos Pasos:** Integración con facturación y expansión a un sistema multisucursal[cite: 1].

---

# ¿Dudas o Comentarios?
### ¡Muchas gracias por su atención!