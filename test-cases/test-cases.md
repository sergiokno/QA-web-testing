# Test Cases — QA Web Testing

## Módulo: Sign Up

---

### TC-SIGNUP-001 — Registro con usuario existente

**Tipo:** Funcional / Negativa  
**Prioridad:** Alta  
**Estado:** PASS

**Precondición:**  
El usuario utilizado ya se encuentra registrado en la aplicación.

**Pasos:**
1. Ingresar a Product Store.
2. Seleccionar **Sign up**.
3. Ingresar un nombre de usuario previamente registrado.
4. Ingresar una contraseña.
5. Seleccionar **Sign up**.

**Resultado esperado:**  
El sistema debe impedir la creación de una cuenta con un nombre de usuario existente.

**Resultado actual:**  
El sistema impide el registro y muestra el mensaje `This user already exist.`

**Evidencia:**  
`test-evidence/TC-SIGNUP-001-existing-user.png`

---

### TC-SIGNUP-002 — Registro con campos vacíos

**Tipo:** Funcional / Negativa  
**Prioridad:** Alta  
**Estado:** PASS

**Precondición:**  
La ventana de registro se encuentra disponible.

**Pasos:**
1. Seleccionar **Sign up**.
2. Dejar Username vacío.
3. Dejar Password vacío.
4. Seleccionar **Sign up**.

**Resultado esperado:**  
El sistema debe impedir el registro cuando los campos obligatorios están vacíos.

**Resultado actual:**  
El sistema impide el registro y muestra el mensaje `Please fill out Username and Password.`

**Evidencia:**  
`test-evidence/TC-SIGNUP-002-empty-fields.png`

---

### TC-SIGNUP-003 — Registro con contraseña corta

**Tipo:** Funcional / Exploratoria  
**Prioridad:** Media  
**Estado:** PASS con observación

**Datos de prueba:**  
Username: `qa_prueba_2026`  
Password: contraseña de 3 caracteres.

**Pasos:**
1. Seleccionar **Sign up**.
2. Ingresar un usuario nuevo.
3. Ingresar una contraseña de 3 caracteres.
4. Seleccionar **Sign up**.

**Resultado esperado:**  
El sistema debe aplicar las reglas de validación definidas para la contraseña.

**Resultado actual:**  
El sistema permite crear la cuenta y muestra `Sign up successful.`

**Observación:**  
La aplicación permite contraseñas de 3 caracteres. No se reporta como defecto debido a que no se dispone de un requisito que establezca una longitud mínima.

**Evidencia:**  
`test-evidence/TC-SIGNUP-003-short-password.png`

---

### TC-SIGNUP-004 — Registro con caracteres especiales en el usuario

**Tipo:** Funcional / Exploratoria  
**Prioridad:** Media  
**Estado:** PASS

**Datos de prueba:**  
Username: `qa@prueba`

**Pasos:**
1. Seleccionar **Sign up**.
2. Ingresar `qa@prueba` como Username.
3. Ingresar una contraseña.
4. Seleccionar **Sign up**.

**Resultado esperado:**  
El sistema debe procesar el registro de acuerdo con las reglas establecidas para el nombre de usuario.

**Resultado actual:**  
El sistema registra correctamente al usuario y muestra `Sign up successful.`

**Evidencia:**  
`test-evidence/TC-SIGNUP-004-special-characters.png`

---

### TC-SIGNUP-005 — Registro con espacios en el nombre de usuario

**Tipo:** Funcional / Exploratoria  
**Prioridad:** Media  
**Estado:** PASS con observación

**Datos de prueba:**  
Username: `qa prueba`

**Pasos:**
1. Seleccionar **Sign up**.
2. Ingresar un Username que contenga un espacio.
3. Ingresar una contraseña.
4. Seleccionar **Sign up**.

**Resultado esperado:**  
El sistema debe aplicar las reglas definidas para el formato del nombre de usuario.

**Resultado actual:**  
El sistema permite registrar el usuario y muestra `Sign up successful.`

**Observación:**  
Se acepta un nombre de usuario que contiene espacios. No se reporta como defecto al no disponer de un requisito que prohíba este formato.

**Evidencia:**  
`test-evidence/TC-SIGNUP-005-username-with-spaces.png`

---

## Módulo: Login

### TC-LOGIN-001 — Inicio de sesión con campos vacíos

**Tipo:** Funcional / Negativa  
**Prioridad:** Alta  
**Estado:** PASS

**Precondición:**  
La ventana de inicio de sesión se encuentra disponible.

**Pasos:**
1. Seleccionar **Log in**.
2. Dejar Username vacío.
3. Dejar Password vacío.
4. Seleccionar **Log in**.

**Resultado esperado:**  
El sistema debe impedir el inicio de sesión cuando los campos obligatorios están vacíos.

**Resultado actual:**  
El sistema impide el inicio de sesión y muestra el mensaje `Please fill out Username and Password.`

**Evidencia:**  
`test-evidence/TC-LOGIN-001-empty-fields.png`

---

### TC-LOGIN-002 — Inicio de sesión con usuario inexistente

**Tipo:** Funcional / Negativa  
**Prioridad:** Alta  
**Estado:** PASS

**Datos de prueba:**  
Username: `usuarioincorrecto`  
Password: contraseña de prueba incorrecta.

**Pasos:**
1. Seleccionar **Log in**.
2. Ingresar un nombre de usuario que no se encuentre registrado.
3. Ingresar una contraseña.
4. Seleccionar **Log in**.

**Resultado esperado:**  
El sistema debe impedir el inicio de sesión con un usuario inexistente.

**Resultado actual:**  
El sistema impide el inicio de sesión y muestra el mensaje `User does not exist.`

**Evidencia:**  
`test-evidence/TC-LOGIN-002-invalid-user.png`

---

### TC-LOGIN-003 — Inicio de sesión con contraseña incorrecta

**Tipo:** Funcional / Negativa  
**Prioridad:** Alta  
**Estado:** PASS

**Precondición:**  
El usuario utilizado se encuentra registrado en la aplicación.

**Datos de prueba:**  
Username: `sergio1234`  
Password: contraseña incorrecta.

**Pasos:**
1. Seleccionar **Log in**.
2. Ingresar un usuario registrado.
3. Ingresar una contraseña incorrecta.
4. Seleccionar **Log in**.

**Resultado esperado:**  
El sistema debe impedir el inicio de sesión cuando la contraseña es incorrecta.

**Resultado actual:**  
El sistema impide el inicio de sesión y muestra el mensaje `Wrong password.`

**Evidencia:**  
`test-evidence/TC-LOGIN-003-wrong-password.png`
