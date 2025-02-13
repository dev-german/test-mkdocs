# **Requerimientos Funcionales: Cajero Automático**

Este documento describe los requerimientos funcionales del sistema del cajero automático, sin agruparlos por casos de uso. Estos requerimientos cubren las funcionalidades necesarias para operaciones como retirar dinero, transferir dinero, depositar dinero y cambiar clave.

---

## **Requerimientos Funcionales**

### **Autenticación y Seguridad**
1. **RF-001:** El sistema debe permitir al usuario insertar una tarjeta válida. <a id="rf001"></a>
2. **RF-002:** El sistema debe solicitar al usuario que ingrese su PIN. <a id="rf002"></a>
3. **RF-003:** El sistema debe validar el PIN ingresado con el sistema bancario.
4. **RF-004:** El sistema debe bloquear la tarjeta después de 3 intentos fallidos de ingreso de PIN.
5. **RF-005:** El sistema debe garantizar la seguridad de las transacciones mediante el uso de cifrado.

### **Retiro de Dinero**
6. **RF-006:** El sistema debe mostrar un menú con la opción "Retirar dinero".
7. **RF-007:** El sistema debe permitir al usuario seleccionar un monto de retiro de una lista predefinida o ingresar un monto manualmente.
8. **RF-008:** El sistema debe verificar que el saldo de la cuenta sea suficiente para el retiro.
9. **RF-009:** El sistema debe verificar que el cajero tenga suficiente efectivo para dispensar.
10. **RF-010:** El sistema debe dispensar el monto solicitado en efectivo.
11. **RF-011:** El sistema debe actualizar el saldo de la cuenta en el sistema bancario.
12. **RF-012:** El sistema debe imprimir un comprobante de la transacción.

### **Transferencia de Dinero**
13. **RF-013:** El sistema debe mostrar un menú con la opción "Transferir dinero".
14. **RF-014:** El sistema debe solicitar al usuario que ingrese el número de cuenta de destino.
15. **RF-015:** El sistema debe validar que la cuenta de destino exista y sea válida.
16. **RF-016:** El sistema debe solicitar al usuario que ingrese el monto a transferir.
17. **RF-017:** El sistema debe verificar que el saldo de la cuenta sea suficiente para la transferencia.
18. **RF-018:** El sistema debe ejecutar la transferencia y actualizar los saldos de ambas cuentas.
19. **RF-019:** El sistema debe imprimir un comprobante de la transacción.

### **Depósito de Dinero**
20. **RF-020:** El sistema debe mostrar un menú con la opción "Depositar dinero".
21. **RF-021:** El sistema debe solicitar al usuario que ingrese el monto a depositar.
22. **RF-022:** El sistema debe aceptar el efectivo depositado por el usuario.
23. **RF-023:** El sistema debe verificar el monto depositado.
24. **RF-024:** El sistema debe actualizar el saldo de la cuenta en el sistema bancario.
25. **RF-025:** El sistema debe imprimir un comprobante de la transacción.

### **Cambio de Clave**
26. **RF-026:** El sistema debe mostrar un menú con la opción "Cambiar clave". <a id="rf026"></a>
27. **RF-027:** El sistema debe solicitar al usuario que ingrese un nuevo