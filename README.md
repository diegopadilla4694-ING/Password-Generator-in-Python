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

---

## Requisitos e Instalación

Para ejecutar este proyecto, necesitas tener instalado **Python 3.7+** y las dependencias externas necesarias para la interfaz y el portapapeles.

Instala los requerimientos ejecutando el siguiente comando en tu terminal:

```bash
pip install customtkinter pyperclip
