# Tema 5.1: Page Object Model con Playwright (Python)

## ¿Qué es Page Object Model?

El **Page Object Model (POM)** es una forma de organizar las pruebas automatizadas para que sean más claras, mantenibles y fáciles de modificar.  
La idea principal es **separar la lógica de la página de la lógica de los tests**. Cada página de la web tiene su propia clase que contiene los selectores y las acciones que se pueden realizar.

---

## ¿Por qué usar Page Object Model?

- Hace los tests más fáciles de leer y entender.
- Evita repetir código.
- Si cambia un selector, solo se modifica en un sitio.
- Facilita el mantenimiento del proyecto.

---

## Estructura básica del proyecto

project/
│
├── pages/
│   ├── components/          # Elementos reutilizables como el menú, header o footer
│   ├── home_page.py         # Clase para la página Home
│   ├── contact_page.py      # Clase para la página Contact
│   └── about_page.py        # Clase para la página About
│
├── tests/
│   ├── test_home.py         # Tests relacionados con Home
│   ├── test_contact.py      # Tests del formulario de contacto
│   └── test_about.py        # Tests de About
│
└── requirements.txt

## Carpeta `pages`

- Contiene **una clase por cada página** de la web.
- Cada clase de página tiene:
  - **Selectores** definidos como variables dentro de la clase.
  - **Funciones**, una por cada acción que se puede realizar en la página.
- Si hay elementos que se repiten en varias páginas, como un menú, header o footer, se crean **clases aparte** dentro de `pages/components`.

---

## Carpeta `tests`

- Contiene **un archivo por cada funcionalidad o conjunto de pruebas**.
- Los tests:
  - No usan selectores directamente.
  - Llaman a las funciones definidas en las páginas y componentes.
  - Se enfocan en **qué se prueba**, no en cómo se hace la interacción.

---

## Buenas prácticas

- **Una función por acción:** cada función representa una acción concreta que el usuario puede realizar en la página o componente.
- **Selectores como variables:** definir los selectores como variables dentro de la clase permite actualizar los selectores en un solo sitio si cambian.
- **Componentes reutilizables:** cualquier elemento que se repita en varias páginas (menú, footer, header) debe tener su propia clase en `components`.
- **Tests limpios:** los tests solo llaman a las funciones de las páginas y componentes; no deben contener lógica de interacción con elementos ni selectores.
- **Organización clara:**
  - `pages/`: clases por página o componentes.
  - `tests/`: archivos por funcionalidad o conjunto de tests.

---

## Resumen

- Cada **página** → una clase en `pages`.
- **Elementos repetidos** → clase aparte en `pages/components`.
- **Una función por acción** dentro de la clase.
- **Selectores como variables** en la clase.
- **Tests** → un archivo por funcionalidad, llaman a las funciones de páginas/componentes.
- Beneficio: código **limpio, reutilizable y fácil de mantener**.


## Ejemplo

project/
│
├── pages/
│   └── home_page.py        # Clase para la página Home
│
├── tests/
│   └── test_home.py        # Tests relacionados con home
│
└── requirements.txt

home_page.py
---

from playwright.sync_api import Page

class HomePage:
    def __init__(self, page: Page):
        self.page = page
        self.url = "https://bootcampqa.com"

    def open_home_page(self):
        print("Given user visits homepage")
        self.page.goto(self.url)

    def verify_home_page_url(self):
        print("Then user should see home page")
        expect(page).to_have_url(self.url)


---
test_home.py

---
from playwright.sync_api import Page, expect
from pages.home_page import HomePage

def test_visit(page: Page):
    home_page = HomePage(page)
    home_page.open_home_page()
    home_page.verify_home_page_url()
    

