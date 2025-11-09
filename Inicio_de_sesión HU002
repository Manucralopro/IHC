Feature: HU002 - Inicio de sesión
  Como usuario registrado,
  Quiero iniciar sesión en TrashTracker,
  Para acceder a mi cuenta y ver mis reportes.

  Scenario Outline: Inicio de sesión correcto
    Given que el <usuario> tiene una cuenta activa
    When ingresa el <correo> y la <contraseña> correctos
    And presiona "Iniciar sesión"
    Then el sistema valida las credenciales
    And redirige al mapa principal

    Examples:
      | usuario | correo               | contraseña |
      | u1      | ana.perez@gmail.com  | Trash123   |

  Scenario Outline: Error al ingresar contraseña incorrecta
    Given que el <usuario> tiene una cuenta activa
    When ingresa el <correo> correcto pero <contraseña> errónea
    Then el sistema muestra "Credenciales inválidas"
    And permanece en la pantalla de inicio

    Examples:
      | usuario | correo               | contraseña   |
      | u2      | ana.perez@gmail.com  | ClaveErrada  |
