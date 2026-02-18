# Alcance del Proyecto - Bankify

## 1. Sistema
**Bankify**: Plataforma de gestión bancaria digital diseñada para la administración de usuarios, cuentas, transacciones financieras y generación de reportes tributarios.

## 2. Problema a resolver
La necesidad de centralizar y automatizar las operaciones bancarias básicas (depósitos, consultas y gestión de cuentas) garantizando la seguridad mediante roles (clientes, asesores, supervisores y gerentes) y facilitando el cumplimiento de obligaciones tributarias ante entidades externas como la DIAN.

## 3. Diagrama de contexto

![Diagrama de Contexto de Bankify](C:\Laboratorios DOSW\lab3DOSW\DOSW_LAB03_Bootcamp_Daniel_Sebastian_Jeimmy\Docs\uml\Bankify_Context_Diagram.drawio.png)

[Ver diagrama en pantalla completa](C:\Laboratorios DOSW\lab3DOSW\DOSW_LAB03_Bootcamp_Daniel_Sebastian_Jeimmy\Docs\uml\Bankify_Context_Diagram.drawio.png)

## 4. Alcance del sistema
El sistema Bankify permitirá realizar las siguientes funciones:

### Gestión de Accesos y Seguridad
* **Autenticación:** Validación mediante usuario y contraseña para operadores y clientes.

### Gestión de Usuarios y Clientes
* **Administración de Clientes:** Los supervisores podrán crear, activar, inactivar y actualizar información de los clientes.
* **Eliminación:** Capacidad de eliminar registros de clientes y sus cuentas asociadas.

### Gestión de Cuentas Bancarias
* **Control de Cuentas:** * El **Asesor** tiene permisos totales (crear, activar, inactivar y actualizar).
    * El **Cliente** tiene permiso limitado para inactivar sus propias cuentas.
* **Servicios Financieros:**
    * Consulta de saldo en tiempo real por parte del cliente.
    * Realización de depósitos (tanto por el propietario como por terceros).

### Módulo de Reportes
* **Reporte de Rentas (Cliente):** Generación automática del certificado tributario para declaración de renta personal.
* **Reporte DIAN (Gerente Financiero):** Generación consolidada de reportes de todas las cuentas del sistema para fines legales.