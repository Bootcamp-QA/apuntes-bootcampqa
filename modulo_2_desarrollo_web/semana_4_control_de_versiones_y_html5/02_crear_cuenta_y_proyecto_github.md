# Crear cuenta y proyecto en Github

# Video de la clase


[Ver clase: Crear Cuenta Github - 20 min](https://bootcampqa.com/videos/crearCuentaGithub.mp4)

[Ver clase: Crear Proyecto Github usando Plantilla - 10 min](https://bootcampqa.com/videosauto/auto-crear-proyecto-usando-plantilla.mp4)

[Ver clase: Crear Proyecto Github de cero - 10 min](https://bootcampqa.com/videos/crearproyectogithub.mp4)

[Ver clase: Publicar web con github pages - 5 min](https://bootcampqa.com/videosauto/auto-publicarpagina-editar-readme.mp4)

# Apuntes

# GitHub – Apuntes

## Crear cuenta en GitHub y configurar GitHub Settings

### Crear una cuenta en GitHub

1. Vaya a https://github.com/
2. Haga clic en **Sign up (Registrarse)**.
3. Siga las indicaciones para crear su cuenta personal.
4. Elija **GitHub Free** (cuenta gratuita).
5. Verifique su correo electrónico.

---

## Acceder a GitHub Settings

1. Inicie sesión (login) en su cuenta de GitHub.
2. Haga clic en el icono lateral de su usuario.
3. Elija la opción **Settings (Configuración)**.
4. Una vez dentro, verá todas las opciones de configuración de su cuenta y proyectos.

---

### Settings: Public Profile

Aquí puede agregar la información que otros usuarios verán al visitar su perfil de GitHub.

1. En **Settings**, haga clic en **Public profile**.
2. Puede modificar:
   - **Nombre**
   - **Email**: correo con el que las empresas pueden contactarlo.
   - **Bio**: breve presentación personal.
   - **URL**: enlace a su sitio web (si tiene).
   - **Social accounts**: recomendable agregar su perfil de LinkedIn.
   - **Foto de perfil** (opcional).

---

### Settings: Password & Authentication

Aquí puede cambiar su contraseña y activar la autenticación en dos pasos.

1. En **Settings**, haga clic en **Password and authentication**.
2. Vaya a la sección **Two-factor authentication**.
3. Elija el método de autenticación adicional que prefiera (SMS es el más sencillo).
4. Seleccione **Add** en **SMS/Text**.
5. Resuelva el puzzle de seguridad.
6. Introduzca su número de teléfono.
7. Agregue el código de verificación recibido.
8. A partir de ese momento, cada vez que inicie sesión deberá introducir también el código SMS enviado a su móvil.

---

## Crear y abrir un proyecto en GitHub

### Crear un nuevo proyecto (repositorio)

1. Haga clic en la pestaña **Repositories**.
2. Presione el botón **New repository**.

### Completar la información del proyecto

- **Owner**: puede seleccionar su usuario o una organización si tiene una creada.
- **Repository name**: debe tener el mismo nombre que su proyecto en JIRA.
- **Public**: recomendado para proyectos gratuitos y de código abierto.
  - **Private**: usado principalmente por empresas con planes de pago.
- **Add README**: agrega un archivo con información básica del proyecto.
- **.gitignore**: permite ignorar archivos, no es necesario para este proyecto.
- **License**: no es necesaria.

Haga clic en **Create repository** para finalizar.

---

### Crear proyecto en GitHub desde una plantilla (Template)

Esta opción permite crear un repositorio ya configurado a partir de una plantilla existente, sin necesidad de configurarlo todo manualmente.

### Crear repositorio desde plantilla

1. Abre la **URL de la plantilla** de github.
2. En la página del repositorio plantilla, haz clic en el botón **Use this template**.
3. Selecciona **Create a new repository**.
4. Completa la información:
   - **Owner**: tu usuario de GitHub.
   - **Repository name**: nombre de tu proyecto.
   - **Visibility**: selecciona **Public** (recomendado).
5. Haz clic en **Create repository**.

## Abrir un proyecto en GitHub

1. Haga clic en **Repositories**.
2. Seleccione el nombre de su repositorio.
3. Una vez abierto, copie la **URL del repositorio**.
4. Para volver a abrirlo en el futuro, solo debe pegar la URL en el navegador.

---

## Publicar página de tu proyecto – GitHub Pages

### Publicar página en GitHub Pages

1. Abra su repositorio introduciendo su URL en el navegador.
2. Haga clic en **Settings**.
3. Dentro de Settings, seleccione **Pages**.
4. En **Source**, elija **Deploy from a branch**.
5. Seleccione:
   - **Branch**: `main`
   - **Folder**: `/root`
   - Haga clic en **Save**.
6. En la parte superior aparecerá un mensaje con la **URL de su sitio web** y el botón **Visit site**.
7. **Importante**: el mensaje puede tardar entre **10 y 15 minutos** en aparecer. Recargue la página hasta verlo.
8. Guarde la URL de su sitio web.
9. Cada vez que suba cambios al repositorio, el sitio web se actualizará automáticamente.
   - Los cambios pueden tardar **10 a 15 minutos** en reflejarse.
10. Puede ver el progreso de la publicación en la pestaña **Actions**.

