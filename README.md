# Formulario de contacto

Práctica de formularios HTML con envío mediante [FormSubmit](https://formsubmit.co/). El sitio permite introducir los datos de contacto y un mensaje, y muestra una página de confirmación después de enviar el formulario.

## Funcionalidades

- Campos obligatorios para nombre, apellido, correo electrónico y mensaje.
- Validación básica del navegador mediante los atributos `required` y `type="email"`.
- Casilla de aceptación de términos y condiciones.
- Envío del formulario mediante una petición `POST` a FormSubmit.
- Redirección a una página de confirmación tras el envío.
- Diseño adaptable para pantallas pequeñas y grandes.

## Estructura del proyecto

```text
.
├── index.html       # Formulario de contacto
├── gracias.html     # Página mostrada después del envío
├── css/
│   └── estilos.css  # Estilos y diseño responsive
└── notas.txt        # Notas de la práctica
```

## Uso local

No se necesita un proceso de compilación ni instalar dependencias. Para probarlo:

1. Abre `index.html` en un navegador, o sirve la carpeta con cualquier servidor estático.
2. Completa todos los campos del formulario.
3. Acepta los términos y condiciones y pulsa **Enviar**.

También se puede iniciar un servidor local con Python:

```bash
python -m http.server 8000
```

Después, visita <http://localhost:8000>.

## Configuración de FormSubmit

La configuración del envío está en el formulario de `index.html`:

- `action`: dirección de correo que recibe los mensajes a través de FormSubmit.
- `_subject`: asunto del correo recibido.
- `_template`: plantilla utilizada por FormSubmit.
- `_next`: URL de `gracias.html` que se carga después de un envío correcto.

Antes de publicar el proyecto, revisa la dirección de correo del atributo `action` y adapta la URL de `_next` al dominio donde se aloje el sitio. FormSubmit puede solicitar una confirmación inicial de la dirección receptora.

## Tecnologías

- HTML5
- CSS3
- FormSubmit
- Google Fonts (Poppins)
