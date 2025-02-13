# **Transferir Dinero**

## **ID**
- **CU-002**

## **Descripción**
Permite al usuario transferir dinero desde su cuenta a otra cuenta bancaria.

## **Actores**
- **Actor Primario:** Usuario (cliente del banco).
- **Actores Secundarios:** Sistema del cajero, Sistema bancario.

## **Precondiciones**
- El usuario debe tener una tarjeta válida.
- El usuario debe tener saldo suficiente en su cuenta.
- La cuenta de destino debe ser válida.

## **Flujo Principal**
| **Acción del Usuario**               | **Acción del Sistema**                     |
|--------------------------------------|--------------------------------------------|
| Inserta la tarjeta en el cajero.     | Solicita el ingreso del PIN.               |
| Ingresa el PIN.                      | Verifica el PIN.                           |
| Selecciona "Transferir dinero".      | Solicita el número de cuenta de destino.   |
| Ingresa el número de cuenta destino. | Verifica la cuenta de destino.             |
| Ingresa el monto a transferir.       | Verifica el saldo en la cuenta.            |
| Confirma la transacción.             | Realiza la transferencia y muestra un comprobante. |

## **Flujos Alternativos**
- **Flujo Alternativo 1:** Si el PIN es incorrecto, el sistema solicita reintroducir el PIN (hasta 3 intentos).
- **Flujo Alternativo 2:** Si el saldo es insuficiente, el sistema muestra un mensaje de error.

## **Excepciones**
- La cuenta de destino no existe o es inválida.
- La tarjeta está bloqueada o es inválida.

## **Postcondiciones**
- El saldo de la cuenta se reduce según el monto transferido.
- El saldo de la cuenta de destino aumenta según el monto transferido.
- El usuario recibe un comprobante.