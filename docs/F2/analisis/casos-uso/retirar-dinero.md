# **Caso de Uso: Retirar Dinero**

## **ID**
- **CU-001**

## **Descripción**
Permite al usuario retirar una cantidad específica de dinero de su cuenta bancaria a través de un cajero automático.

## **Actores**
- **Actor Primario:** Usuario (cliente del banco).
- **Actores Secundarios:** Sistema del cajero, Sistema bancario.

## **Precondiciones**
- El usuario debe tener una tarjeta válida.
- El usuario debe tener saldo suficiente en su cuenta.
- El cajero debe tener suficiente efectivo.

## **Flujo Principal**
| **Acción del Usuario**               | **Acción del Sistema**                     |
|--------------------------------------|--------------------------------------------|
| Inserta la tarjeta en el cajero.     | Solicita el ingreso del PIN.               |
| Ingresa el PIN.                      | Verifica el PIN.                           |
| Selecciona "Retirar dinero".         | Muestra las opciones de monto disponibles. |
| Selecciona el monto a retirar.       | Verifica el saldo en la cuenta.            |
| Confirma la transacción.             | Entrega el dinero y la tarjeta.            |
| Retira el dinero y la tarjeta.       | Muestra un comprobante de la transacción.  |

## **Flujos Alternativos**
- **Flujo Alternativo 1:** Si el PIN es incorrecto, el sistema solicita reintroducir el PIN (hasta 3 intentos).
- **Flujo Alternativo 2:** Si el saldo es insuficiente, el sistema muestra un mensaje de error.

## **Excepciones**
- El cajero no tiene suficiente efectivo.
- La tarjeta está bloqueada o es inválida.

## **Postcondiciones**
- El saldo de la cuenta se reduce según el monto retirado.
- El usuario recibe el dinero y un comprobante.