# Requerimientos 

## Requerimientos funcionales 

1)	Permitir autenticación de usuarios, utilizando usuario y contraseña  
2)	Poder consultar el saldo de una cuenta 
3)	Poder realizar depósito de dinero de una forma controlada
4)	Verificar que el número de cuenta tenga exactamente 10 dígitos que sean números
5)	Los dos primeros dígitos de la cuenta corresponden a un banco 
6)	Poder generar reportes tributarios para los clientes en formato PDF
7)	Generar un reporte para la DIAN en formato JSON

## Requerimientos no funcionales

1)    Garantizar el crecimiento de la cantidad de usuarios
2)	Tener un buen tiempo de respuesta, cargar cada parte de la pagina en menos de 4 segundos
3)	Capacidad para recuperación de la información por algún fallo 
4)	Que la interfaz sea intuitiva para el fácil manejo del usuario
5)	Que tenga diseño responsive para poder verla desde cualquier dispositivo

---

# Detalle de requerimientos funcionales

## Autenticacion del usuario

Codigo: RF-01

Nombre: Autenticacion del usuario

Descripcion: El sistema debe permitir que clientes y operadores accedan mediante credenciales validas como usuario y contraseña

Como se ejecutara: El usuario ingresa sus credenciales en la parte de login y el sistema valida la informacion y si es correcta o incorrecta

Actor Principal: Cliente u operador

Precondiciones: 

      1) El usuario debe estar registrado en el sistema
      2) La cuenta del usuario debe estar activa

Datos de entrada: Usuario y contraseña

Datos de salida: Acceso al sistema en caso de ser valido y en caso contrario un mensaje indicando el por que no se pudo acceder

Flujo Basico:

      1) Usuario ingresa a login
      2) Usuario ingresa credenciales
      3) Sistema las reconoce como validas
      4) Acceso de usuario a sistema

Flujo alterno:

      1) Usuario ingresa a login
      2) Usuario ingresa credenciales
      3) Sistema NO las reconoce como validas
      4) Mensaje de error indicando por que no se pudo acceder

## Consultar saldo

Codigo: RF-02

Nombre: Consulta saldo

Descripcion: El sistema debe permitir al cliente visualizar el saldo disponible de su cuenta

Como se ejecutara: El cliente autenticado selecciona la opcion de consultar saldo, y el sistema le muestra su saldo actualizado segun la informacion de la base de datos

Actor Principal: Cliente

Precondiciones: 

      1) El cliente debe estar autenticado
      2) La cuenta del cliente debe estar activa

Datos de entrada: La solicitud del cliente por ver su saldo

Datos de salida: Saldo actual del cliente con fecha de ultima actualizacion

Flujo Basico:

      1) Cliente selecciona la opcion de consultar saldo
      2) El sistema revisa la informacion con la base de datos
      3) Sistema retorna el saldo actual del cliente con ultima fecha de modificacion

Flujo alterno:

      1) Si hay un error en la cuenta o un fallo de conectividad con el acceso a la informacion se muestra un mensaje a el usuario indicando el error

## Realizar pago

Codigo: RF-03

Nombre: Realizar pago

Descripcion: El sistema debe permitir al cliente realizar pagos desde su cuenta hacia terceros

Como se ejecutara: El cliente autenticado ingresa los datos requeridos del destinatario, el sitema revisa el saldo del cliente para verificar saldo suficiente y registra la transaccion

Actor Principal: Cliente

Precondiciones: 

      1) El cliente debe estar autenticado
      2) La cuenta del cliente debe estar activa
      3) La cuenta debe tener saldo suficiente

Datos de entrada: Numero de cuenta del destinatario y monto a enviar

Datos de salida: Confirmacion del pago

Flujo Basico:

      1) Cliente ingresa los datos del pago
      2) El sistema revisa la informacion del destinatario y del saldo, para que sean correctas y veridicas
      3) Sistema registra la transaccion y se la confoirma a el usuario

Flujo alterno:

      1) Si hay saldo insuficiente se da un mensaje de error a el usuario explicando el motivo
      2) Si la cuenta del destinatario es invalida, se le da un mensaje a el usuario notificando el error

---
# Preguntas

a. ¿Identifica algún requerimiento que deba detallarse más? ¿cuál(es)?

R/ Poder realizar depósito de dinero de una forma controlada

b. ¿Existen requerimientos que se contradigan entre sí? ¿cuál(es)?

R/ No, cada requerimiento habla de una opcion diferente y no contradice lo mencionado en algun otro

c. Si tuviera que dar una prioridad a los requerimientos, ¿cuáles deberían ser los 2 más importantes que deberían implementarse en una primera iteración del proyecto?

R/ 
1) Permitir autenticación de usuarios, utilizando usuario y contraseña
2) Poder consultar el saldo de una cuenta

Estas 2, ya que la autenticacion de la cuenta es de suma importancia para la seguridad tanto del banco mo la de los usuarios y ademas la consulta del saldo es mas importante que la realizacion de un pago, ya que sin saber tu saldo nop puedes estar seguro de si tienes el dinero suficiente.

d. ¿Existe algún requerimiento que no debería realizarse?
     
R/Tener un buen tiempo de respuesta, cargar cada parte de la pagina en menos de 4 segundos, no se puede asegurar ese tiempo de respuesta, ya que no solo depende de lo que se desarrolle sino tambien de factores externos incontrolables.

---
# Mockup

## URL

    https://www.figma.com/design/4KF2meLkxB0JbxuDfCXLje/Bankify?node-id=0-1&t=naiDW17e8Wm1ueUq-1

## Breve explicacion

En la pagina 1 al darle al boton de realizar pago, se dirige a la pagina 2.
En la pagina 2 al llenar las casillas y darle continuar se dirige a la pagina 3.
En la pagina 3 al darle confirmar pago se dirige a la pagina 4.
En la pagina 4 se finaliza el mockup de la funcionalidad seleccionada en el caso de que el pago si fue exitoso.










