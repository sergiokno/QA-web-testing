# Test Results — QA Web Testing

## Resumen de ejecución

Se realizaron pruebas funcionales sobre las principales funcionalidades de la aplicación Product Store.

| Métrica | Resultado |
|---|---:|
| Casos de prueba ejecutados | 15 |
| Casos PASS | 15 |
| Casos FAIL | 0 |
| Defectos reportados | 1 |

## Resultados por módulo

| Módulo | Ejecutados | PASS | FAIL |
|---|---:|---:|---:|
| Sign Up | 5 | 5 | 0 |
| Login | 3 | 3 | 0 |
| Carrito de compras | 4 | 4 | 0 |
| Proceso de compra | 3 | 3 | 0 |
| **Total** | **15** | **15** | **0** |

## Defectos encontrados

### BUG-001 — Samsung Galaxy S7 muestra imagen incorrecta

**Módulo:** Catálogo de productos  
**Severidad:** Medium  
**Prioridad:** Medium  
**Estado:** Open

Durante las pruebas exploratorias del catálogo se identificó que Samsung Galaxy S7 muestra la misma imagen utilizada para Samsung Galaxy S6.

El defecto se encuentra documentado en:

`bug-reports/BUG-001.md`

La evidencia correspondiente se encuentra en:

`test-evidence/BUG-001-samsung-s7-image.png`

## Observaciones

Durante las pruebas de registro se observó que la aplicación permite:

- Contraseñas de 3 caracteres.
- Nombres de usuario con caracteres especiales.
- Nombres de usuario con espacios.

Estos comportamientos no fueron registrados como defectos debido a que no se dispone de requisitos que establezcan restricciones específicas para estos campos.

## Conclusión

Las funcionalidades evaluadas de registro, inicio de sesión, carrito y proceso de compra presentaron el comportamiento esperado durante la ejecución de las pruebas.

Se identificó un defecto visual en el catálogo de productos relacionado con la imagen mostrada para Samsung Galaxy S7.
