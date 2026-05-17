# Password-Generator-in-Python

Una aplicación de escritorio moderna, ligera y segura diseñada en Python para generar contraseñas de alta entropía de forma instantánea. Su interfaz gráfica permite crear credenciales robustas con un solo clic, automatizando el proceso de copiado para mejorar la seguridad y la experiencia del usuario.

---

## Propósito del Proyecto

El objetivo principal de este software es mitigar el uso de contraseñas débiles o reutilizadas. La aplicación resuelve este problema ofreciendo una herramienta utilitaria que genera cadenas alfanuméricas aleatorias que cumplen con los estándares modernos de ciberseguridad.

### Características Clave:
*   **Seguridad Criptográfica:** Utiliza el módulo `secrets` de Python, el cual accede a las fuentes de aleatoriedad del sistema operativo, garantizando que las contraseñas sean inmunes a la ingeniería inversa probabilística.
*   **Complejidad Forzada:** El algoritmo garantiza la inclusión obligatoria de al menos una letra, un número y un carácter especial (`!@#$%^&*()-_=+`).
*   **Ventana Persistente (`Topmost`):** La interfaz se mantiene siempre en primer plano por encima de otras ventanas, ideal para interactuar con ella mientras te registras en un sitio web.
*   **Control Antiedición:** El campo de texto está bloqueado como "Solo Lectura" (`readonly`) para evitar que el usuario altere accidentalmente la contraseña generada.



# Codigo
-`Import`-> `customtkinter`, `secrets`, `string` `pyperclip`

Cada import fue utlizada para generar una cadena de strings aleaoria y segura.

**customtkinter**: Genera una interfaz mas pulida y visualmente mas atractriva.

**secrets**: Genera strings o variables de manera mas segura y robusta.

**string**: Lo use para convertir digitos y ascii_letter de manera aletoria.

**pyperclip**: Me permite copiar la contraseña de a mi portapapeles con Automatización.


**class password_suggesgtion():**
-> Contiene constructores para crear la interfaz grafica ya sea un `self` -> title, geometry, attributes, label, configure, btn, pack.

**self.password = self.secret_password():**
-> Esto llama a una funcion interna dentro del codigo que es `secret_password()` que contiene parte de la logica del codigo.

**self.entry.insert(0, self.password):** Escribe la contraseña generada dentro de la caja.

**self.entry.configure(state="readonly"):*Pone la caja en modo sólo lectura. Así el usuario puede ver y copiar la contraseña, pero no puede borrarla ni modificarla por accidente usando el teclado.

---

## Requisitos e Instalación

Para ejecutar este proyecto, necesitas tener instalado **Python 3.7+** y las dependencias externas necesarias para la interfaz y el portapapeles.

Instala los requerimientos ejecutando el siguiente comando en tu terminal:

```bash
pip install customtkinter pyperclip
