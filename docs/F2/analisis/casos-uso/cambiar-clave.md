# **Caso de Uso: Cambiar Clave**

## **ID**
- **CU-004**

## **Descripción**
Permite al usuario cambiar su PIN (clave de acceso) en el cajero automático.

## **Actores**
- **Actor Primario:** Usuario (cliente del banco).
- **Actores Secundarios:** Sistema del cajero, Sistema bancario.

## **Precondiciones**
- El usuario debe tener una tarjeta válida.
- El usuario debe conocer su PIN actual.

## **Flujo Principal**
1. El usuario inserta la tarjeta en el cajero.
2. El sistema solicita el ingreso del PIN.
3. El usuario ingresa su PIN actual.
4. El sistema verifica el PIN.
5. El usuario selecciona la opción "Cambiar clave".
6. El sistema solicita el nuevo PIN.
7. El usuario ingresa el nuevo PIN.
8. El sistema solicita la confirmación del nuevo PIN.
9. El usuario confirma el nuevo PIN.
10. El sistema actualiza el PIN en la base de datos.
11. El sistema muestra un mensaje de confirmación.
12. El usuario retira la tarjeta.

## **Flujos Alternativos**
- **Flujo Alternativo 1:** Si el PIN actual es incorrecto:
  1. El sistema muestra un mensaje de error.
  2. El sistema solicita reintroducir el PIN (hasta 3 intentos).
  3. Si el usuario supera los intentos, la tarjeta se bloquea.
- **Flujo Alternativo 2:** Si el nuevo PIN no cumple con los requisitos:
  1. El sistema muestra un mensaje de error.
  2. El sistema solicita ingresar un nuevo PIN válido.

## **Excepciones**
- La tarjeta está bloqueada o es inválida.
- El usuario cancela la operación antes de confirmar el nuevo PIN.

## **Postcondiciones**
- El PIN de la tarjeta se actualiza en el sistema.
- El usuario recibe un mensaje de confirmación.

## **Requisitos Asociados**
- [RF-001](../requerimientos.md#rf001)
- [RF-026](../requerimientos.md#rf026)
