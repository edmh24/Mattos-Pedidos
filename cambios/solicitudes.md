<!-- Autor: Mattos -->

# Solicitudes de cambio de NovaTech-Pedidos

## INC-014 — Subtotal incorrecto

- **Descripción:** El sistema devuelve el precio unitario como subtotal.
- **Tipo de cambio:** Correctivo.
- **Justificación:** El subtotal debe considerar todas las unidades solicitadas.
- **Requisito afectado:** RN-01.
- **Archivo afectado:** `codigo/pedidos.py`.
- **Riesgo:** Una fórmula incorrecta puede generar importes equivocados.
- **Criterio de aceptación:** Con precio S/ 80 y cantidad 3, el subtotal es S/ 240.
- **Decisión simulada:** Aprobada. Corrige el incumplimiento de RN-01.

## CR-015 — Cálculo de envío y total

- **Descripción:** Incorporar el cálculo automático del envío y del total del pedido.
- **Tipo de cambio:** Perfectivo. Agrega una funcionalidad.
- **Justificación:** La gerencia solicita conocer el importe final con el envío incluido.
- **Requisitos afectados:** RN-02, RN-03 y RN-04.
- **Archivos afectados:** `codigo/pedidos.py` y `documentos/requisitos.md`.
- **Riesgo:** Cobrar envío cuando el subtotal es exactamente S/ 300.
- **Criterio de aceptación:** Para subtotales de S/ 240, S/ 300 y S/ 450,
  los costos de envío son S/ 20, S/ 0 y S/ 0. Los totales son S/ 260,
  S/ 300 y S/ 450, respectivamente.
- **Decisión simulada:** Aprobada. Se verificará el límite de S/ 300.