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

1) Garantizar el crecimiento de la cantidad de usuarios
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

# Consultar saldo 
# Realizar pago






