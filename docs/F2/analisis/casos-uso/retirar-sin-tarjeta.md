# **Retirar Dinero sin Tarjeta**

## **ID**
- **CU-005**

## 1. Información General
- **Nombre del Caso de Uso**: Retirar Dinero sin Tarjeta
- **Actor Principal**: Cliente del banco
- **Actores Secundarios**: Sistema bancario, Cajero automático
- **Descripción**: Permite a un cliente retirar dinero de su cuenta bancaria sin necesidad de usar una tarjeta física, utilizando un código generado por la aplicación móvil del banco.

---

## 2. Flujo Básico (Flujo Principal)

1. **Iniciar retiro sin tarjeta**:
   - El cliente abre la aplicación móvil del banco.
   - Selecciona la opción "Retirar sin tarjeta".

2. **Ingresar monto y cuenta**:
   - El cliente ingresa el monto que desea retirar.
   - Selecciona la cuenta desde la cual se debitará el dinero.

3. **Generar código de retiro**:
   - El sistema bancario valida la disponibilidad de fondos.
   - Si hay fondos suficientes, el sistema genera un código de retiro único y lo muestra en la aplicación.

4. **Acudir al cajero automático**:
   - El cliente se dirige a un cajero automático.
   - Selecciona la opción "Retirar sin tarjeta" en el cajero.

5. **Ingresar código de retiro**:
   - El cliente ingresa el código generado en la aplicación.
   - El sistema valida el código.

6. **Confirmar y retirar dinero**:
   - El cajero muestra el monto a retirar.
   - El cliente confirma la operación.
   - El cajero entrega el dinero.

7. **Finalizar operación**:
   - El sistema actualiza el saldo de la cuenta.
   - El cajero imprime un comprobante (opcional).
   - La operación finaliza.

---

## 3. Flujos Alternativos

### 3.1. Fondos insuficientes
- **Paso**: 3 (Generar código de retiro).
- **Condición**: El cliente no tiene fondos suficientes en la cuenta.
- **Acción**:
  - El sistema muestra un mensaje de error: "Fondos insuficientes".
  - El caso de uso termina.

### 3.2. Código inválido o expirado
- **Paso**: 5 (Ingresar código de retiro).
- **Condición**: El código ingresado es inválido o ha expirado.
- **Acción**:
  - El cajero muestra un mensaje de error: "Código inválido o expirado".
  - El cliente debe generar un nuevo código en la aplicación.

### 3.3. Cajero sin efectivo
- **Paso**: 6 (Confirmar y retirar dinero).
- **Condición**: El cajero no tiene suficiente efectivo.
- **Acción**:
  - El cajero muestra un mensaje: "No hay efectivo disponible".
  - El cliente puede intentar en otro cajero.

---

## 4. Requisitos Especiales
- **Seguridad**: El código de retiro debe ser único y tener un tiempo de expiración (por ejemplo, 10 minutos).
- **Disponibilidad**: La opción de retirar sin tarjeta debe estar disponible las 24 horas del día.
- **Notificaciones**: El cliente debe recibir una notificación en la aplicación móvil cuando el retiro sea exitoso.

---

## 5. Precondiciones
- El cliente debe tener una cuenta bancaria activa.
- El cliente debe tener la aplicación móvil del banco instalada y configurada.
- El cajero automático debe soportar la funcionalidad de retiro sin tarjeta.

---

## 6. Postcondiciones
- El monto retirado se debita de la cuenta del cliente.
- El cliente recibe el dinero en efectivo.
- Se registra la transacción en el historial de la cuenta.

---

## 7. Reglas de Negocio
- **Límite de retiro**: El monto máximo que se puede retirar sin tarjeta es de $500 por transacción.
- **Tiempo de expiración**: El código de retiro expira después de 10 minutos.
- **Número de intentos**: El cliente tiene un máximo de 3 intentos para ingresar el código correctamente.

---

## 8. Notas
- Este caso de uso puede variar dependiendo de las políticas del banco y la tecnología utilizada.
- La funcionalidad de retiro sin tarjeta puede no estar disponible en todos los cajeros automáticos.