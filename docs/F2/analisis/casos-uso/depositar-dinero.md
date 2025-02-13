# **Depositar Dinero**

## **ID**
- **CU-003**

## **Descripción**
Permite al usuario depositar dinero en su cuenta bancaria a través de un cajero automático.

## **Actores**
- **Actor Primario:** Usuario (cliente del banco).
- **Actores Secundarios:** Sistema del cajero, Sistema bancario.

## **Precondiciones**
- El usuario debe tener una tarjeta válida.
- El usuario debe tener dinero en efectivo para depositar.

## **Flujo Principal**
| **Acción del Usuario**               | **Acción del Sistema**                     |
|--------------------------------------|--------------------------------------------|
| Inserta la tarjeta en el cajero.     | Solicita el ingreso del PIN.               |
| Ingresa el PIN.                      | Verifica el PIN.                           |
| Selecciona "Depositar dinero".       | Solicita el monto a depositar.             |
| Ingresa el monto.                    | Solicita el efectivo.                      |
| Inserta el efectivo en el cajero.    | Verifica el monto y lo deposita en la cuenta. |
| Confirma la transacción.             | Muestra un comprobante de la transacción.  |

## **Flujos Alternativos**
- **Flujo Alternativo 1:** Si el PIN es incorrecto, el sistema solicita reintroducir el PIN (hasta 3 intentos).
- **Flujo Alternativo 2:** Si el efectivo no es válido, el sistema lo rechaza.

## **Excepciones**
- El cajero no puede procesar el efectivo.
- La tarjeta está bloqueada o es inválida.

## **Postcondiciones**
- El saldo de la cuenta aumenta según el monto depositado.
- El usuario recibe un comprobante.