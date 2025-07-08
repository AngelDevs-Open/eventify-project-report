# Capítulo V: Product Implementation, Validation & Deployment

## 5.1. Software Configuration Management

Con el fin de garantizar la consistencia, trazabilidad y calidad a lo largo del ciclo de vida de Eventify, el equipo ha definido un conjunto de decisiones y convenciones orientadas a la gestión de configuraciones. Esta sección describe los mecanismos adoptados para controlar el código fuente, configurar los entornos de desarrollo y definir el proceso de despliegue de la aplicación web.

Estas prácticas permiten asegurar que las versiones del software se mantengan estables, que el trabajo colaborativo sea eficiente y que las implementaciones sean controladas y reproducibles.

### 5.1.1. Software Development Environment Configuration
Para asegurar una colaboración eficiente y mantener la calidad en el desarrollo de Eventify, se ha definido un entorno de desarrollo común para todos los miembros del equipo. A continuación, se listan los productos de software utilizados en las distintas etapas del ciclo de vida del producto digital, indicando su propósito y su enlace de referencia o descarga correspondiente.

**Product UX/UI Design**

Para el diseño de la experiencia de usuario y la interfaz de la Landing page de Eventify, se utilizaron las siguientes herramientas:

- Figma: Se empleó para la creación de wireframes, mock-ups y prototipos de la aplicación web.[https://www.figma.com/es-es/](https://www.figma.com/es-es/)
- UXPressia: Utilizada para elaborar User Personas, Empathy Maps, Journey Maps e Impact Maps. [https://uxpressia.com/](https://uxpressia.com/)
- Miro: Se utilizó para la creación de los mapas de escenarios As-Is y To-Be. [https://miro.com/es/](https://miro.com/es/)

**Software Development**

Para el desarrollo del software de l Landing Page, se adoptaron los siguientes productos:

- WebStorm (Instalación local): Utilizado como entorno de desarrollo para trabajar con HTML, CSS y JavaScript. [https://www.jetbrains.com/es-es/webstorm/](https://www.jetbrains.com/es-es/webstorm/)
- Git (Instalación local): Empleado para gestionar los cambios de código de manera local mediante commits y ramas. [https://git-scm.com/](https://git-scm.com/)
- GitHub: Plataforma de repositorio remoto para la gestión de versiones del código, implementando el flujo GitFlow para garantizar un desarrollo organizado. [https://github.com/](https://github.com/)

**Project Management and Collaboration**

En la gestión de proyectos y colaboración del equipo se utilizaron:

- Trello: Utilizado para la planificación y seguimiento de tareas, distribuidas en listas de "por hacer", "en progreso" y "hecho".
- WhatsApp: Medio de comunicación instantánea para coordinar avances, resolver dudas rápidas y hacer recordatorios. [https://web.whatsapp.com/](https://web.whatsapp.com/)
- Discord: Utilizado como plataforma de comunicación por voz y chat, facilitando reuniones rápidas y discusiones técnicas en equipo. [https://discord.com/](https://discord.com/)
- Zoom: Herramienta utilizada para realizar reuniones virtuales más formales, presentaciones de avances y coordinación general del equipo. [https://www.zoom.com/es](https://www.zoom.com/es)

**Software Documentation**

Para la documentación del proyecto se emplearon las siguientes herramientas:

- Vertabelo: Herramienta utilizada para el diseño, creación y documentación colaborativa de bases de datos. [https://vertabelo.com/](https://vertabelo.com/)
- PlantUML Editor: Utilizada para la creación del diagrama de clases que ayuda en la planificación y visualización del sistema. [https://plantuml.com/](https://plantuml.com/)
- Structurizr: Herramienta usada para modelar la arquitectura de software mediante diagramas C4. [https://structurizr.com/](https://structurizr.com/)


**Software Testing**

En cuanto a la validación del software:

- WebStorm Preview: Se utilizó la función de vista previa integrada en WebStorm para revisar manualmente archivos .md y otros componentes antes de ser integrados en el repositorio de GitHub. [https://www.jetbrains.com/es-es/webstorm/](https://www.jetbrains.com/es-es/webstorm/)


### 5.1.2. Source Code Management
La gestión del código fuente es una parte fundamental en el desarrollo colaborativo de software, ya que permite un control eficiente sobre las modificaciones realizadas en el proyecto a lo largo de su ciclo de vida. En este apartado, se describe el sistema de control de versiones implementado en el proyecto Eventify, utilizando GitHub como plataforma principal. Además, se detallan las convenciones de trabajo adoptadas por el equipo, como el modelo GitFlow, el versionado semántico (Semantic Versioning) y las convenciones de commit mediante Conventional Commits. Estas prácticas aseguran un desarrollo ordenado y una integración continua efectiva entre los miembros del equipo.

**URL de los Repositorios:**
- Organización: [https://github.com/AngelDevs-Web](https://github.com/AngelDevs-Web)
- Reporte: [https://github.com/AngelDevs-Web/eventify-project-report](https://github.com/AngelDevs-Web/eventify-project-report)
- Landing Page: [https://github.com/AngelDevs-Open/eventify-landing-page](https://github.com/AngelDevs-Open/eventify-landing-page)

**Estructura de Ramas:**

Para mantener un flujo organizado en el desarrollo y facilitar la colaboración, se ha implementado el modelo GitFlow, creando las siguientes ramas:

- Master Branch: Rama principal (main) que contiene las versiones estables del proyecto. Todas las demás ramas derivan de esta.
- Develop: Rama secundaria donde se integran todas las características nuevas antes de fusionarse a la rama main.
- Feature Branches (Chapter I,II,III,IV,V): Para esta primera entrega son ramas dedicadas a cada capítulo del informe, permitiendo que cada miembro trabaje de manera independiente sin afectar el desarrollo principal.
- Release Branche: Rama creada cuando el equipo decide que la rama develop está lista para ser convertida en una nueva versión estable.
- Cover: Rama destinada a los elementos de la portada del informe.
- Student-outcome: Rama dedicada a los resultados de cada uno de los integrantes en relación con el proyecto.
- Bibliography: Rama cuya funcionalidad es realizar la bibliografía del informe del proyecto.
- Annexes: Rama destinada a enumerar los anexos de cada entrega del informe.

**Convenciones de commits:**

Para la escritura de commits en el proyecto Eventify, se sigue la convención 'Conventional Commits', el cual cuenta con un formato estándar para facilitar la lectura y entendimiento del historial de cambios dentro del proyecto.
```
    <type>[optional scope]: <description>
    
    [optional body]
    
    [optional footer(s)]
```
- Type:
    - feat: Añadir una nueva característica.
    - fix: Correción de errores.
    - docs: Modificaciones en la documentación.
    - style: Cambios que no afectan la lógica del código.
    - refactor: Modificaciones que no añaden características y/o errores.
    - test: Adición/Modificación de pruebas.


- Scope: Brinda información extra acerca del área del código afectado.
```
   feat(auth): add register functionality.
```
**Ejemplos básicos de commits:**
```
   feat(login): add organizer authentication module.
```
```
   fix(payment): resolve payment security issue.
```
```
   docs(README): update index instructions.
```

#### 5.1.3. Source Code Style Guide & Conventions

En el proyecto Eventify, hemos implementado una serie de guías de estilo y convenciones para asegurar que todo el equipo de desarrollo siga una estructura consistente y clara en todo el ciclo de vida del proyecto. Esto facilita la legibilidad del código, mejora la colaboración entre los desarrolladores y asegura que el código sea mantenible a largo plazo.

#### Nomenclatura General

Para asegurar la coherencia en todo el código, se seguirán las siguientes directrices:

- Los nombres de variables, funciones y métodos deben utilizar **camelCase**.
- Los nombres de clases y componentes seguirán la convención **PascalCase**.
- Para los archivos y carpetas, se empleará la convención **kebab-case**.

El uso de **inglés** para todos los nombres es obligatorio, con el fin de asegurar la comprensión entre los miembros del equipo y facilitar la colaboración internacional.

**Ejemplos**:

- Variables: `eventDetails`, `userProfile`
- Clases: `EventManager`, `User`
- Archivos: `event-manager.service.ts`, `user.controller.js`

#### Espacios y Sangría

La **sangría** de código en Eventify seguirá las siguientes reglas para asegurar la claridad y el orden del código:

- Se utilizarán **2 espacios** para la sangría en archivos HTML, CSS, JavaScript, y TypeScript.
- En archivos **Java**, se utilizarán **4 espacios** para la sangría.

Esta convención ayuda a mantener la consistencia en todos los lenguajes empleados en el proyecto y facilita la colaboración entre diferentes desarrolladores.

**Ejemplo de HTML con sangría**:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Eventify</title>
  </head>
  <body>
    <h1>Eventos Disponibles</h1>
    <p>Encuentra y reserva eventos fácilmente</p>
  </body>
</html>
```

#### Convenciones por Lenguaje

1. **HTML/CSS/JavaScript**:

    - Se utilizará la [Google HTML/CSS Style Guide](https://google.github.io/styleguide/htmlcssguide.html) para asegurar la consistencia en la estructura y la presentación de los archivos HTML y CSS.
    - Para JavaScript, adoptamos la [Airbnb JavaScript Style Guide](https://github.com/airbnb/javascript), ampliamente conocida y utilizada en la industria.
2. **TypeScript**:

    - **Angular** es el framework elegido para el frontend de Eventify, por lo que seguimos la [Angular Style Guide](https://angular.io/guide/styleguide), que dicta cómo deben estructurarse los módulos, servicios y componentes.
    - También seguimos la [Google TypeScript Style Guide](https://google.github.io/styleguide/tsguide.html) para garantizar la correcta tipificación y legibilidad del código.
3. **Java**:

    - En el backend, utilizamos **Spring Boot** para crear APIs y servicios web. Seguimos la [Google Java Style Guide](https://google.github.io/styleguide/javaguide.html) para mantener consistencia en la estructura de las clases y los métodos.
    - Los nombres de clases serán descriptivos, utilizando sustantivos para clases y verbos para métodos.

**Ejemplo de una clase Java**:

```java
public class EventManager {
    private int availableTickets;

    public EventManager(int tickets) {
        this.availableTickets = tickets;
    }

    public void reserveTicket() {
        if (availableTickets > 0) {
            availableTickets--;
        }
    }
}
```

4. **Gherkin**:
    - Para escribir los tests automatizados, seguimos la convención de [Gherkin Syntax](https://cucumber.io/docs/gherkin/). Esto permite una descripción clara y precisa de los escenarios de prueba en los archivos `.feature`.
    - Utilizamos **Given-When-Then** para describir el comportamiento esperado en cada escenario.

**Ejemplo de Gherkin**:

```gherkin

Feature: Event ticket booking

  Scenario: Successful ticket reservation
    Given the user is logged in
    When they select an available event
    Then the system should confirm the ticket reservation
```

#### Espaciado y Comillas

- **Espacios**: Siempre se debe colocar un espacio alrededor de los operadores y entre los parámetros en las funciones.

  **Ejemplo**:

  ```javascript
  let totalTickets = 200;
  let bookedTickets = 45;
  let availableTickets = totalTickets - bookedTickets;
  ```
- **Comillas**: En **JavaScript** y **TypeScript**, se utilizan comillas simples (`'`) para cadenas, mientras que en **HTML** se prefieren las comillas dobles (`"`).

#### Límite de Longitud de Línea

El código no debe exceder las **80 columnas** por línea. En caso de necesitar más espacio, se recomienda dividir la línea de código para mejorar la legibilidad.

#### 5.1.4. Software Deployment Configuration

## 5.2. Landing Page, Services & Applications Implementation

### 5.2.1. Sprint 1

En el Sprint 1, nos enfocamos en diseñar y desarrollar la Landing Page de Eventify, con el objetivo de presentar de forma clara y atractiva los beneficios de la plataforma para organizadores y anfitriones de eventos. Durante este sprint, trabajamos en una estructura de navegación intuitiva y una disposición visual que permitiera resaltar las características principales del servicio. Nos organizamos como equipo para dividir las tareas y lograr un diseño completamente responsivo, asegurando que la página se visualice correctamente en distintos tamaños de pantalla.

#### 5.2.1.1. Sprint Planning 1

|             Sprint #             |                                                                                                                                                                                                                                                                                                                                                                                                                                                 Sprint 1                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|:--------------------------------:|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|
|  **Sprint Planning Background**  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|               Date               |                                                                                                                                                                                                                                                                                                                                                                                                                                                 25/04/25                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|               Time               |                                                                                                                                                                                                                                                                                                                                                                                                                                               23:40 horas                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|             Location             |                                                                                                                                                                                                                                                                                                                                                                                                                                      Reunión virtual - Zoom/Discord                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|           Prepared By            |                                                                                                                                                                                                                                                                                                                                                                                                                                     Fabrizio Alexander Cutiri Agüero                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|            Attendees             |                                                                                                                                                                                                                                                                                                                                                          - Aldave Aldave Jean Pierr <br> - Omar Christian Berrocal Ramirez  <br> - Deybbi Anderson Crisanto Calle  <br> - Fabrizio Alexander Cutiri Agüero  <br> - July Zelmira Paico Calderon                                                                                                                                                                                                                                                                                                                                                           |
|    Sprint n-1 Review Summary     |                                                                                                                                                                                                                                                                                                                                                                                                                            Este es el primer sprint a realizar por el equipo                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Sprint n-1 Retrospective Summary |                                                                                                                                                                                                                                                                                                                                Durante este srpint se acordó implementar reuniones frecuentes para hacer un seguimiento del avance y cumplir las metas establecidas. Además destacó el compromiso de los miembros del equipo por cumplir con los objetivos establecidos.                                                                                                                                                                                                                                                                                                                                 |
|  **Sprint Goal & User Stories**  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|          Sprint 1 Goal           | Nuestro enfoque en este sprint estuvo en desarrollar la Landing Page de Eventify, ofreciendo a los nuevos usuarios una interfaz visualmente atractiva y fácil de navegar que les permitiera conocer a fondo nuestra propuesta. Nos centramos en construir secciones clave como Inicio, Beneficios, Funcionalidades, Planes, Quiénes Somos y About the Product, con el fin de comunicar de forma clara el valor que Eventify aporta a organizadores y anfitriones de eventos. <br/>Creemos que esto ayuda a los usuarios a comprender rápidamente cómo funciona la plataforma, generando una experiencia inicial positiva y confiable. <br/>Validaremos este trabajo cuando la Landing Page esté completamente operativa, con una navegación fluida, contenido informativo en cada sección y una experiencia responsiva que permita a los usuarios interactuar correctamente desde cualquier dispositivo. |
|        Sprint 1 Velocity         |                                                                                                                                                                                                                                                                                                                                                                                                                                     Velocidad de 18 - Primer Sprint                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|       Sum of Story Points        |                                                                                                                                                                                                                                                                                                                                                                                                                                        Sprint 1 - 20 Story Points                                                                                                                                                                                                                                                                                                                                                                                                                                        |

#### 5.2.1.2. Aspect Leaders and Collaborators


|            Team Member            | GitHub Username | Header | Footer | Inicio | Beneficios | Funcionalidades | Planes | About Us | About the product |
|:---------------------------------:|:---------------:|:------:|:------:|:------:|:----------:|:---------------:|:------:|:--------:|:-----------------:|
|     Aldave Aldave, Jean Pierr     |   Jean Pierr    |   C    |   L    |   C    |     C      |        C        |   C    |    C     |         L         |
| Berrocal Ramirez, Omar Christian  |      OmBRz      |   C    |   C    |   C    |     C      |        L        |   C    |    L     |         C         |
|  Crisanto Calle, Deybbi Anderson  |     Dacc03      |   L    |   C    |   C    |     C      |        C        |   C    |    C     |         C         |
| Cutiri Agüero, Fabrizio Alexander |    Fabrizio     |   C    |   C    |   C    |     L      |        C        |   L    |    C     |         C         |
|   Paico Calderon, July Zelmira    |      JulyP      |   C    |   C    |   L    |     C      |        C        |   C    |    C     |         C         |

#### 5.2.1.3. Sprint Backlog 1

Para el sprint 1 usamos la herramienta trello para organizar las tareas del equipo.

Enlance: https://trello.com/b/iDs1MVOZ/eventify-sprint-backlog-1 

![trello_sprint_1](/assets/chapter-V/TRELLO.png) 

<table>
  <tr>
    <td> <strong>Sprint #</strong></td>
    <td align="center" colspan="7"> <strong>Sprint 1</strong> </td>
  </tr>

   <tr>
    <td align="center" colspan="2"> <strong>User Story</strong></td>
    <td align="center" colspan="6"> <strong>Work-item/Task</strong></td>
  </tr>
  <tr>
    <td align="center"> <strong>ID</strong> </td>
    <td align="center"> <strong>Title</strong> </td>
    <td align="center"> <strong>ID</strong> </td>
    <td align="center"> <strong>Title</strong> </td>
    <td align="center"> <strong>Description</strong> </td>
    <td align="center"> <strong>Estimation (Hours)</strong> </td>
    <td align="center"> <strong>Assigned To</strong></td>
    <td align="center"> <strong> Status (To-do/In-Process/To-Review/Done)  </strong></td>
  </tr>
  <!---------------------------------------------------------------------- -->
  <tr>
    <td rowspan="1" align="center"> ID </td>
    <td rowspan="1" align="center"> US01 Navegación sencilla</td>
    <td align="center"> TA01 </td>
     <td align="center"> Menú con hipervínculos</td>
    <td align="center">Cada Hipervínculo debe de redirigirte a una sección específica de la landing page </td>
    <td align="center"> 2</td>
    <td align="center"> Aldave Aldave, Jean Pierr</td>
    <td align="center">Done</td>
  </tr>

<!----------------------------------------------->
  <tr>
    <td rowspan="1" align="center"> ID </td>
    <td rowspan="1" align="center"> US02 Propuesta de valor clara</td>
    <td align="center"> TA01 </td>
    <td align="center"> Hero</td>
    <td align="center"> Se debe desarrollar un banner con una frase que represente a la aplicación web.</td>
    <td align="center"> 2</td>
    <td align="center"> Cutiri Agüero, Fabrizio Alexander</td>
    <td align="center">Done</td>
  </tr>

  <!----------------------------------------------->
  <tr>
    <td rowspan="1" align="center"> ID </td>
    <td rowspan="1" align="center"> US05 Llamada a la acción</td>
    <td align="center"> TA01 </td>
    <td align="center"> Call to action</td>
    <td align="center"> Se debe desarrollar un botón call to action que redirija a la aplicación web.</td>
    <td align="center"> 1</td>
    <td align="center"> Berrocal Ramirez, Omar Christian </td>
    <td align="center">Done</td>
  </tr>


<!-------------------------------------------------->
  <tr>
    <td rowspan="1" align="center"> ID </td>
    <td rowspan="1" align="center"> US03 Información segmentada</td>
    <td align="center"> TA01 </td>
    <td align="center"> Benefits</td>
    <td align="center"> crea la seccion de beneficios de la plataforma web, que muestra los atractivos de la apliación.</td>
    <td align="center"> 2</td>
    <td align="center"> Paico Calderon, July Zelmira </td>
    <td align="center"> Done</td>
  </tr>

  <!----------------------------------------------->
  <tr>
    <td rowspan="1" align="center"> ID </td>
    <td rowspan="1" align="center"> US04 Funcionalidades de la aplicación</td>
    <td align="center"> TA01 </td>
    <td align="center"> Functionalities</td>
    <td align="center"> Se debe desarrollar una sección que liste las funcionalidades que obtiene cada segmento objetivo en al plataforma web.</td>
    <td align="center"> 2</td>
    <td align="center"> Berrocal Ramirez, Omar Christian </td>
    <td align="center">Done</td>
  </tr>
  <!------------------------------------------------>
   <tr>
    <td rowspan="1" align="center"> ID </td>
    <td rowspan="1" align="center"> US06 Visualización de tutorial de la aplicación</td>
    <td align="center"> TA01 </td>
    <td align="center"> About the product</td>
    <td align="center"> Se desarrolla secion donde figura un video que explica el funcionamiento de la plataforma web.</td>
    <td align="center"> 1</td>
    <td align="center"> Paico Calderon, July Zelmira </td>
    <td align="center"> Done</td>
  </tr>
  <!------------------------------------------------>
   <tr>
    <td rowspan="1" align="center"> ID </td>
    <td rowspan="1" align="center"> US07 Confianza y seguridad.</td>
    <td align="center"> TA01 </td>
    <td align="center"> About us</td>
    <td align="center"> Debe presentar una sección con la información del equipo de trabajo.</td>
    <td align="center"> 2 </td>
    <td align="center"> Crisanto Calle, Deybbi Anderson </td>
    <td align="center"> Done</td>
  </tr>
  <!------------------------------------------------>
   <tr>
    <td rowspan="1" align="center"> ID </td>
    <td rowspan="1" align="center"> US08 Velocidad de carga.</td>
    <td align="center"> TA01 </td>
    <td align="center"> Loading</td>
    <td align="center"> Se debe implementar funciones que permitan lazy loading o carga diferida.</td>
    <td align="center"> 2</td>
    <td align="center">  Cutiri Agüero, Fabrizio Alexander </td>
    <td align="center"> Done</td>
  </tr>
  <!------------------------------------------------>
   <tr>
    <td rowspan="1" align="center"> ID </td>
    <td rowspan="1" align="center"> US09 Visualización de precios.</td>
    <td align="center"> TA01 </td>
    <td align="center"> Subscriptions</td>
    <td align="center"> Debe presentar la información de los precios de cada plan de suscripción.</td>
    <td align="center"> 2</td>
    <td align="center"> Aldave Aldave, Jean Pierr </td>
    <td align="center"> Done</td>
  </tr>
  <!------------------------------------------------>
   <tr>
    <td rowspan="1" align="center"> ID </td>
    <td rowspan="1" align="center"> US10 Diseño responsive</td>
    <td align="center"> TA01 </td>
    <td align="center"> Responsive</td>
    <td align="center"> Se desarrolla implementa configuraciones de ajustes para diferentes tamaños de pantallas.</td>
    <td align="center"> 2</td>
    <td align="center"> Crisanto Calle, Deybbi Anderson </td>
    <td align="center"> Done</td>
  </tr>

</table>

#### 5.2.1.4. Development Evidence for Sprint Review

<table>
  <tr>
    <td align ="center" > <strong>Repository</strong></td>
    <td  align ="center" > <strong>Branch</strong></td>
    <td  align ="center" > <strong>Commit ID</strong></td>
    <td  align ="center" > <strong>Commit message</strong></td>
    <td  align ="center" > <strong>Commit Masagge body</strong></td>
    <td  align ="center" > <strong>Commit on (date)</strong></td>
  </tr>

  <tr>
    <td rowspan="27" align="center">https://github.com/AngelDevs-Web/eventify-landing-page </td>
    <td align="center"> main</td>
    <td align="center"> 7d73095c182e4d75e94b25b7ac954d082912f412</td>
    <td align="center"> chore: initial commit</td>
    <td align="center"> ---</td>
    <td align="center"> 27/04/2025</td>
  </tr>

  <tr>
    <td align="center">feature/funcionalities</td>
    <td align="center" > 1d9b985bd179a7e02f3896845bae43695099d7dd</td>
    <td align="center"> style(functionalities): add styles for functionalities section.</td>
    <td align="center"> ---</td>
    <td align="center"> 27/04/2025</td>
  </tr>

  <tr>
    <td align="center"> feature/header</td>
    <td align="center">97bec8773ba0df16b23986bbd048f088d4884962</td>
    <td align="center"> style(header): style header section for landing page.</td>
    <td align="center"> ---</td>
    <td align="center"> 27/04/2025</td>
  </tr>

  <tr>
    <td align="center"> feature/about-us</td>
    <td align="center"> e4f70d8e829878a40fae3e1e0070d6bdb19a5796</td>
    <td align="center"> style(about-us): add styles for about us section.</td>
    <td align="center"> ---</td>
    <td align="center">27/04/2025</td>
  </tr>

  <tr>
    <td align="center"> feature/about-the-product</td>
    <td align="center"> 9d2397cb6fc1cf0e6225641a0494edd6d24a573f</td>
    <td align="center"> style(about-the-product): add styles for about the product section for landing page.</td>
    <td align="center"> ---</td>
    <td align="center">27/04/2025</td>
  </tr>

  <tr>
    <td align="center"> feature/hero</td>
    <td align="center"> 11e233f5c5f2dfd3ec65485fec398599298e2c43</td>
    <td align="center">style(hero): add styles for hero section</td>
    <td align="center"> ---</td>
    <td align="center"> 27/04/2025</td>
  </tr>

  <tr>
    <td align="center"> feature/plans</td>
    <td align="center"> fc083a88e837c5a88562754667e8304158e2a64a</td>
    <td align="center"> style(plans-section): style plans section for landing page.</td>
    <td align="center"> ---</td>
    <td align="center"> 27/04/2025</td>
  </tr>

  <tr>
    <td align="center"> feature/footer</td>
    <td align="center"> 49582dc112638bbf70854593e64bff2e19a8d9fd</td>
    <td align="center"> style(footer): add styles for footer section.</td>
    <td align="center"> ---</td>
    <td align="center"> 27/04/2025</td>
  </tr>

  <tr>
    <td align="center"> feature/benefits</td>
    <td align="center">eb1a05507dc9affc037e5e06747b84cc72334901</td>
    <td align="center"> style(benefits): add styles for benefits section for landing page.</td>
    <td align="center"> ---</td>
    <td align="center">27/04/2025</td>
  </tr>


  <tr>
    <td align="center"> develop</td>
    <td align="center">7d73095c182e4d75e94b25b7ac954d082912f412</td>
    <td align="center">chore: initial commit.</td>
    <td align="center"> ---</td>
    <td align="center">27/04/2025</td>
  </tr>
</table>


#### 5.2.1.5. Execution Evidence for Sprint Review 

Despues de finalizar el sprint 1, hemos logrado implementar todas las funcionalidades de nuestra landing page, con excepción de la sección about the product, que todavía no contiene un video que muestre el funcionamiento de nuestra plataforma web, puesto que la plataforma web aún no existe en este sprint. A continuación, te invitamos a explorar nuestros avances a través de imágenes que muestran el resultado obtenido.

***header:*** La barra de navegación que nos ayudará a redirigirnos por las diferentes secciones de la landing page.

![Header](/assets/chapter-V/navbar.png)

***Hero:*** Banner que contiene un botón que te llevará a registrarte a nuestra apliación web.

![Hero](/assets/chapter-V/Hero.png)

***Benefits:*** Sección donde los visitantes de la landing page podrán ver los beneficios principales que les ofrece nuestra aplicación.

![Benefits](/assets/chapter-V/Benefits.png)

***Functionality:*** Seccion donde los visitantes de la lading page podrán ver como es que funciona nuestra aplicacion y que les ofrece.

![Functionalities](/assets/chapter-V/functionalities.png)

***Plans***: Sección donde los visitantes podrán ver los planes con los que contamos para suscribirse a la aplicación web, podiendo ver los precios y una descripción de dicho plan.

![Plans](/assets/chapter-V/plans.png)

***About-us:*** Sección que muestra los miembros del equipo de trabajo y descripción del startup.

![About_us](/assets/chapter-V/about_us.png)

***About-the-product:*** Sección con un video que muestra el funcionamiento de la plataforma web.

![About_the_product](/assets/chapter-V/about_the_product.png)

***Footer:*** Contenido extra con información de contacto como correo, teléfono y redes sociales.

![footer](/assets/chapter-V/footer.png)

#### 5.2.1.6. Services Documentation Evidence for Sprint Review

En el primer sprint, hemos realizado el diseño, la programación y el despligue de la Landing Page que presentará nuesta apliación web "Eventify"

<table> 
  <tr>
    <td> <strong>End Point </strong></td>
    <td align="center"> <strong>Funciones</strong> </td>
  </tr>

  <tr>
    <td> https://angeldevs-open.github.io/eventify-landing-page/ </td>
    <td> Desplegar Landing Page de Eventify</td>
  </tr>
</table>


#### 5.2.1.7. Software Deployment Evidence for Sprint Review

Para el despliegue de nuestra Landing Page hemos utilizado GitHub Pages. Para hacer esto, hemos trabajado en un repositorio de GitHub donde divimos el trabajo en ramas. En la sección de configuración y Pages, seleccionamos la rama main para desplegar nuestra web. 


**Link de la landing page desplegada:**  https://angeldevs-open.github.io/eventify-landing-page/

![GitHub-Pages](/assets/chapter-V/github-pages.png)



#### 5.2.1.8. Team Collaboration Insights during Sprint

La meta de este sprint fue la implementación de la Landing Page. Para llevar a cabo este objetivo, hicimos uso de diversas herramientas como GitHub, WebStorm, HTML, CSS y JavaScript. Como evidencias del trabajo realizado tenemos los diagramas de flujo que representan los commits realizados por cada miembro del equipo AngelDevs.

![Commits-landing](/assets/chapter-V/commits-landing.png)
La imagen muestra un gráfico de barras donde se refleja la cantidad de commits hechos por cada miembro del equipo en la Landing Page.

![Contribuitors-landing](/assets/chapter-V/contribuitors-landing.png)
En esta imagen se refleja la el nivel de modificaciones realizadas por los commits de cada integrante en el repositorio de la Landing Page.

![Network-landing](/assets/chapter-V/network-landing.png)
En la imagen se puede apreciar las ramas feature creadas para el repositorio y las fechas en que se unieron, así como se aplicó gitflow para su desarrollo.


### 5.2.2. Sprint 2
En el presente Sprint nos enfocamos en desarrollar la primera versión del frontend de nuestra aplicación web Eventify. Para ello definimos en el sprint backlog, tareas relacionadas a las principales funcionalidades que presenta nuestro proyecto como la creación de cotizaciones para los eventos, la creación de tareas que se realizarán durante la planeación del evento, entre otros.

#### 5.2.2.1. Sprint Planning 2

A continuación, el cuadro correspondiente al sprint planning 2, donde se rescatan aspectos importantes del sprint planning meeting.

| Sprint #                           | Sprint 2                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Sprint Planning Background**     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Fecha**                          | 06/05/25                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Hora**                           | 23:40 horas                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **Lugar**                          | Reunión virtual - Zoom/Discord                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Preparado por**                  | Omar Christian Berrocal Ramirez                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Asistentes**                     | - Aldave Aldave Jean Pierr  <br> - Deybbi Anderson Crisanto Calle  <br> - Fabrizio Alexander Cutiri Agüero  <br> - July Zelmira Paico Calderon                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Sprint 1 Review Summary**        | Se logró implementar la versión inicial del Frontend, exponiendo las vistas core del negocio. Se establecieron las tecnologías base del proyecto: Angular y Typecript. Además se corrigieron errores del sprint anterior.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Sprint 1 Retrospective Summary** | Durante el Sprint 2 se acordó implementar en el Frontend las principales vistas de nuestro negocio con la finalidad de generar espectativas a los clientes desde la primera versión del producto. También se identificó la necesidad de establecer estándares de componentes reutilizables y convenciones claras de código desde el inicio del desarrollo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **Sprint Goal & User Stories**     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Sprint 2 Goal**                  | Nuestro enfoque en este sprint es construir la primera versión funcional del Frontend de Eventify con con Angular, incorporando componentes reutilizables, diseño responsive y navegación fluida. Nos centraremos en desarrollar las secciones previamente definidas (Inicio, Quote, Settings, Calendar) utilizando código limpio y modular, aplicando Angular Material para los componentes visuales. Buscamos entregar una versión navegable que los usuarios puedan ver y usar desde diferentes dispositivos. Esto nos permitirá realizar pruebas tempranas de usabilidad y validar si la interfaz cumple con los objetivos de claridad, atractivo visual y navegación intuitiva. Este trabajo será validado mediante una demo funcional desplegada localmente y/o en hosting temporal (como Netlify o Vercel), que permita recibir feedback interno antes de pasar a etapas más avanzadas de integración o backend. |
| **Sprint 2 Velocity**              | Velocidad de 26 - Primer Sprint                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Story Points Totales**           | Sprint 2 - 32 Story Points                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |

#### 5.2.2.2. Aspect Leaders and Collaborators

En esta sección, elaboraremos el artefacto Leadership-and-Collaboration Matrix (LACX) para asignar claramente quién asumirá el rol de líder y quiénes serán los colaboradores durante el Sprint 3.

|            Team Member            | GitHub Username | TaskManagement | ProfileManagement | QuoteManagement | Event Management | Calendar | 
|:---------------------------------:|:---------------:|:--------------:|:-----------------:|:---------------:|:----------------:|:--------:| 
|     Aldave Aldave, Jean Pierr     |   Jean Pierr    |       L        |         C         |        C        |        C         |    C     |  
| Berrocal Ramirez, Omar Christian  |      OmBRz      |       C        |         C         |        C        |        C         |    L     |   
|  Crisanto Calle, Deybbi Anderson  |     Dacc03      |       C        |         L         |        C        |        C         |    C     |   
| Cutiri Agüero, Fabrizio Alexander |    Fabrizio     |       C        |         C         |        L        |        C         |    C     |    
|   Paico Calderon, July Zelmira    |      JulyP      |       C        |         C         |        C        |        C         |    L     |  

#### 5.2.2.3. Sprint Backlog 2


Para el sprint 2 usamos la herramienta trello para organizar las tareas del equipo.

Enlance: https://trello.com/b/rzR3S25M/eventify-sprint-backlog-2

<table>
  <tr>
    <td> <strong>Sprint #</strong></td>
    <td align="center" colspan="7"> <strong>Sprint 2</strong> </td>
  </tr>

   <tr>
    <td align="center" colspan="2"> <strong>User Story</strong></td>
    <td align="center" colspan="6"> <strong>Work-item/Task</strong></td>
  </tr>
  <tr>
    <td align="center"> <strong>ID</strong> </td>
    <td align="center"> <strong>Title</strong></td>
    <td align="center"> <strong>ID</strong> </td>
    <td align="center"> <strong>Title</strong></td>
    <td align="center"> <strong>Description</strong></td>
    <td align="center"> <strong>Estimation (Hours)</strong></td>
    <td align="center"> <strong>Assigned To</strong></td>
    <td align="center"> <strong> Status (To-do/In-Process/To-Review/Done)  </strong></td>
  </tr>
  <!---------------------------------------------------------------------- -->
  <tr>
    <td rowspan="3" align="center"> ID </td>
    <td rowspan="3" align="center"> US24 Solicitar cotización a un organizador</td>
    <td align="center"> TA01 </td>
     <td align="center"> Create a qoute management</td>
    <td align="center">Crear un formulario para generar una cotización </td>
    <td align="center"> 3</td>
    <td align="center"> Cutiri Agüero, Fabrizio Alexander</td>
    <td align="center">Done</td>
  </tr>
  <tr>
    <td align="center"> TA02 </td>
     <td align="center"> Add component to create and edit services into a quote</td>
    <td align="center"> Crea componentes para crear y editar cotizaciones en una tabla</td>
    <td align="center"> 3</td>
    <td align="center"> Cutiri Agüero, Fabrizio Alexander</td>
    <td align="center">Done</td>
  </tr>
  <tr>
    <td align="center"> TA03 </td>
     <td align="center">Add external service for CRUD operations of quotes</td>
    <td align="center"> Crea un servicio para acceder al fake api y hacer operaciones de CRUD</td>
    <td align="center"> 2</td>
    <td align="center"> Cutiri Agüero, Fabrizio Alexander</td>
    <td align="center">Done</td>
  </tr>

<!----------------------------------------------->
  <tr>
    <td rowspan="1" align="center"> ID </td>
    <td rowspan="1" align="center"> US21 Vista de cronograma del evento</td>
    <td align="center"> TA01 </td>
    <td align="center"> Create a calendar to view events registered</td>
    <td align="center"> Se crea un calendario donde figurarán los eventos en los días correspondientes.</td>
    <td align="center"> 2</td>
    <td align="center"> Berrocal Ramirez, Omar Christian</td>
    <td align="center">Done</td>
  </tr>

  <!----------------------------------------------->
  <tr>
    <td rowspan="1" align="center"> ID </td>
    <td rowspan="1" align="center"> US19 Gestión de presupuesto del evento</td>
    <td align="center"> TA01 </td>
    <td align="center"> Add external service for CRUD operations of services into a quote</td>
    <td align="center"> Se crea un servicio para acceder al apifake y hacer operaciones de crud.</td>
    <td align="center"> 2</td>
    <td align="center"> Cutiri Agüero, Fabrizio Alexander</td>
    <td align="center">Done</td>
  </tr>


<!-------------------------------------------------->
  <tr>
    <td rowspan="3" align="center"> ID </td>
    <td rowspan="3" align="center"> US18 Lista de tareas del evento</td>
    <td align="center"> TA01 </td>
    <td align="center"> Create a task management board</td>
    <td align="center"> crea un board de gestión de tareas.</td>
    <td align="center"> 2</td>
    <td align="center"> Aldave Aldave, Jean Pierr </td>
    <td align="center"> Done</td>
  </tr>
  <tr>
    <td align="center"> TA02 </td>
     <td align="center">Add a component to create and edit tasks</td>
    <td align="center"> Crea componentes para crear y editar tareas en el task board</td>
    <td align="center"> 3</td>
    <td align="center"> Aldave Aldave, Jean Pierr</td>
    <td align="center">Done</td>
  </tr>
   <tr>
    <td align="center"> TA03 </td>
     <td align="center">Add external service for CRUD operations of tasks</td>
    <td align="center"> Crea un servicio para acceder al fake api y obtener, editar o elimnar datos de las tareas.</td>
    <td align="center"> 2</td>
    <td align="center"> Aldave Aldave, Jean Pierr</td>
    <td align="center">Done</td>
  </tr>

  <!----------------------------------------------->
  <tr>
    <td rowspan="1" align="center"> ID </td>
    <td rowspan="1" align="center"> US22 Visualización de resumen del evento</td>
    <td align="center"> TA01 </td>
    <td align="center"> Create event summary</td>
    <td align="center"> Se debe desarrollar un card que muestre el resumen del evento</td>
    <td align="center"> 2</td>
    <td align="center"> Paico Calderon, July Zelmira </td>
    <td align="center">In Progress</td>
  </tr>
  <!------------------------------------------------>
   <tr>
    <td rowspan="2" align="center"> ID </td>
    <td rowspan="2" align="center"> US23 Visualizar perfiles de organizadores	</td>
    <td align="center"> TA01 </td>
    <td align="center"> Organizer profile</td>
    <td align="center"> Se desarrolla secion de perfil del organizador.</td>
    <td align="center"> 3</td>
    <td align="center"> Crisanto Calle, Deybbi Anderson </td>
    <td align="center"> Done</td>
  </tr>
  <tr>
    <td align="center"> TA02 </td>
     <td align="center">Add Reviews and rating</td>
    <td align="center"> Crea una vista con las reseñas y calificaciones que tiene el organizador.</td>
    <td align="center"> 2</td>
    <td align="center">Crisanto Calle, Deybbi Anderson</td>
    <td align="center">In Progress</td>
  </tr>
  <!------------------------------------------------>
   <tr>
    <td rowspan="1" align="center"> ID </td>
    <td rowspan="1" align="center"> US17 Registro de nuevo evento.</td>
    <td align="center"> TA01 </td>
    <td align="center"> Create a new event</td>
    <td align="center"> Crea un componente que genere un evento cuando se apruebe la cotización.</td>
    <td align="center"> 2 </td>
    <td align="center"> Paico Calderon, July Zelmira </td>
    <td align="center"> In Progress</td>
  </tr>


</table>

#### 5.2.2.4. Development Evidence for Sprint Review

Se mostrarán los commits realizados en el desarrollo de este sprint para los productos solicitados.

<table>
  <tr>
    <td align ="center" > <strong>Repository</strong></td>
    <td  align ="center" > <strong>Branch</strong></td>
    <td  align ="center" > <strong>Commit ID</strong></td>
    <td  align ="center" > <strong>Commit message</strong></td>
    <td  align ="center" > <strong>Commit Masagge body</strong></td>
    <td  align ="center" > <strong>Commit on (date)</strong></td>
  </tr>

  <tr>
    <td rowspan="27" align="center"> https://github.com/AngelDevs-Open/eventify-front-end </td>
    <td align="center"> feature/task-management</td>
    <td align="center">f3b0fe13e560b1e1bb511930e59199ec478cba07 </td>
    <td align="center"> feat(task): add task management component page.</td>
    <td align="center"> ---</td>
    <td align="center"> 16/05/2025</td>
  </tr>

  <tr>
      <td align="center"> feature/task-management</td>
      <td align="center">4431b8d3813c931938917855a7ce4f101adb07b1</td>
      <td align="center"> feat(task): create task entity..</td>
      <td align="center"> ---</td>
      <td align="center">16/05/2025</td>
  </tr>
  <tr>
      <td align="center"> feature/task-management</td>
      <td align="center">5caaf73d68baba681bce650b0638181fdd41a289</td>
      <td align="center"> feat(task): add task item component.</td>
      <td align="center"> ---</td>
      <td align="center">16/05/2025</td>
  </tr>
  <tr>
      <td align="center"> feature/task-management</td>
      <td align="center">4c946b7ef9fcdba8ddd12088f7336a4432fd35b8</td>
      <td align="center"> feat(task): add task column component.</td>
      <td align="center"> ---</td>
      <td align="center">16/05/2025</td>
  </tr>
  <tr>
      <td align="center"> feature/task-management</td>
      <td align="center">78a3f28589f7fc21f2b26d085f9899680c42f58f</td>
      <td align="center"> feat(task): add task column entity.</td>
      <td align="center"> ---</td>
      <td align="center">16/05/2025</td>
  </tr>
  <tr>
      <td align="center"> feature/task-management</td>
      <td align="center">c34e9f5f504768eb39d8652e1a07d3c55e004781</td>
      <td align="center"> feat(task): add task entity.</td>
      <td align="center"> ---</td>
      <td align="center">16/05/2025</td>
  </tr>
  <tr>
      <td align="center"> feature/task-management</td>
      <td align="center">2d20ccb6f44c643f770ab37ec9ccadd7898c512f</td>
      <td align="center"> feat(task): add task board component.</td>
      <td align="center"> ---</td>
      <td align="center">16/05/2025</td>
  </tr>
  <tr>
      <td align="center"> feature/quote-management</td>
      <td align="center">15bc0d46ec5178b533eabe43f6ca595114c5a45b</td>
      <td align="center"> feat(quote): add quote order entity</td>
      <td align="center"> ---</td>
      <td align="center">16/05/2025</td>
  </tr>
 <tr>
      <td align="center"> feature/quote-management</td>
      <td align="center">633026fdce3a52a124d079be18512a049c5bb48e</td>
      <td align="center"> feat(quote): add service item entity</td>
      <td align="center"> ---</td>
      <td align="center">16/05/2025</td>
  </tr>
<tr>
      <td align="center"> feature/quote-management</td>
      <td align="center">40d9280bc960c81b832104c1e15272d38aec4366</td>
      <td align="center"> feat(quote): add services to quote order and service item</td>
      <td align="center"> ---</td>
      <td align="center">16/05/2025</td>
  </tr>
<tr>
      <td align="center"> feature/quote-management</td>
      <td align="center">5052d27a5a6e89db9231bd830e121aa42f73e100</td>
      <td align="center"> feat(quote): add service item create and edit component</td>
      <td align="center"> ---</td>
      <td align="center">16/05/2025</td>
  </tr>
<tr>
      <td align="center"> feature/quote-management</td>
      <td align="center">359cc0ca698eca6b332d6f35daeb82c8343b61e7</td>
      <td align="center"> feat(quote): add quote management component with data maintenance functionality</td>
      <td align="center"> ---</td>
      <td align="center">16/05/2025</td>
  </tr>
</table>


#### 5.2.2.5. Execution Evidence for Sprint Review

Se muestra lo logrado en la ejecución del segundo sprint. Usando Gitflow y trabajando en ramas para ejecutar pruebas y realizar actualizaciones sin comprometer la rama principal.

**Bounded Context Quote Management**

**Quote Management**

Esta es la página donde se gestionan todas las cotizaciones. Se puede crear cotizaciones nuevas, asi como actualizar los datos de cotizaciones anteriormente registradas, si en caso el organizador necesite definir cambios de último momento.

![quote-management](../assets/chapter-V/quote-management.png)

**Quote Order Form Component | Service Item Form Component**

![quote-and-service-component](../assets/chapter-V/quote-service-edit-create.png)
![quote-and-service-edit-action-component](../assets/chapter-V/quote-service-edit-action.png)

Este es el formulario donde se define información relevante respecto al posible evento que se vaya a realizar. El organizador podrá definir el tipo de evento que se planeará, la cantidad de invitados, asi como la fecha que se celebraria. Además se podrá agregar los servicios que incluirá en la planeación.
Estos formularios, a su vez tienen la opción de editar cotizaciones y servicios que ya han sido registrados.

**Bounded Context - Event Management**

**Calendar Component**

![calendar-component](../assets/chapter-V/calendar-event.png)

El siguiente calendario permitirá mostrar los eventos que el organizador este gestionando. Además se ira actualizando conforme se registren nuevos eventos. 

#### 5.2.2.6. Services Documentation Evidence for Sprint Review

Para este segundo Sprint, hemos realizado la implementación y el despliegue del FrontEnd de nuestra aplicación Web "Eventify".
Para ello hemos utilizado Firebase como servicio de hosting y Firebase CLI para el despliegue.
<table> 
  <tr>
    <td> <strong>End Point </strong></td>
    <td align="center"> <strong>Funciones</strong> </td>
  </tr>

  <tr>
    <td> https://angeldevs-open.github.io/eventify-landing-page/</td>
    <td> Desplegar Landing Page de Eventify</td>
  </tr>
  <tr>
    <td> https://eventify-open-frontend.web.app</td>
    <td> Desplegar Front End</td>
  </tr>
  <tr>
    <td> https://eventify-frontend.free.beeceptor.com</td>
    <td> Desplegar Fake API</td>
  </tr>
</table>

#### 5.2.2.7. Software Deployment Evidence for Sprint Review

Para el despliegue del FrontEnd utilizamos el servicio de hosting que ofrece Firebase. Para ello, hemos utilizado Firebase CLI para vincular nuestro proyecto con Firebase y mediante lineas de comandos realizar el despliegue.

![firebase-service](../assets/chapter-V/firebase-open.png)

![firebase-json](../assets/chapter-V/firebase-open-json.png)

### 5.2.2.8. Team Collaboration Insights during Sprint.

La meta para este Sprint fue la implementación y despliegue de la primera versión del FrontEnd de nuestro proyecto. Para ello, utilizamos diversas herramientas como GitHub, Webstorm, Angular, Angular material, ngx-translate-core, entre otros. Como evidencia de que se trabajo de forma colaborativa se presentan los insights del repositorio en Github donde se desarrollo el proyecto.

![collaboration-insights](../assets/chapter-V/pulse-open.png)
En esta imagen se muestran el total de commits que hizo cada integrante durante el desarrollo del Frontend

![contributors-frontend](../assets/chapter-V/contributors%20-%20open.png)
En esta imagen se refleja el nivel de modificaciones realizadas por los commits de cada integrante en el repositorio del FrontEnd.

![gitflow-1](../assets/chapter-V/network-open.png)

![gitflow-2](../assets/chapter-V/network-2-open.png)

Finalmente en estas imagenes se pueden apreciar las ramas con las que se ha trabajado durante el desarrollo del FrontEnd

### 5.2.3. Sprint 3

Durante el Sprint actual nos enfocamos en desarrollar la versión inicial del backend de nuestra aplicación web Eventify. Además, se realizaron mejoras y correcciones tanto en la landing page como en el frontend. Para lograrlo, definimos en el sprint backlog diversas tareas relacionadas con las funcionalidades principales del negocio, como las cotizaciones para eventos y la creación de tareas que se llevarán a cabo durante su planificación.

#### 5.2.3.1.Spring Planning 3.


|            Sprint #            |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    Sprint 3                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|:------------------------------:|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|
| **Sprint Planning Background** |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|              Date              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    07/06/25                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|              Time              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  11:40 horas                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|            Location            |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      Reunión presencial - Aula UPC VH107                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|          Prepared By           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        Omar Christian Berrocal Ramirez                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|           Attendees            |                                                                                                                                                                                                                                                                                                                                                                                                                                                                - Aldave Aldave Jean Pierr   <br> - Deybbi Anderson Crisanto Calle  <br> - Fabrizio Alexander Cutiri Agüero  <br> - July Zelmira Paico Calderon                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|    Sprint 2 Review Summary     |                                                                                                                                                                                                                                                                                                                                                                                Se logró documentar y diseñar la una estructura del Landing Page y el FrontEnd de la apliación web, definiendo secciones clave e identificando los componentes necesarios para una muestra del funcionamiento de la aplicación. Se establecieron las tecnologías base del proyecto: Angular, Angular Materials.                                                                                                                                                                                                                                                                                                                                                                                 |
| Sprint 2 Retrospective Summary |                                                                                                                                                                                                                                                                                                                                                                                                   Durante el Sprint 2 se acordó que el enfoque visual y estructural era fundamental para atraer a nuevos usuarios. También se identificó la necesidad de establecer estándares de componentes reutilizables y convenciones claras de código desde el inicio del desarrollo.                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Sprint Goal & User Stories** |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|         Sprint 3 Goal          | Nuestro enfoque está en brindar información detallada respecto a nuestra aplicación y el equipo de desarrollo, así como cerrar la conversión de los visitantes a través del sitio web del negocio, además de implementar nuevas características, como la búsqueda de organizadores de eventos, planes de suscripción, comunicación directa entre organizadores y anfitriones, notificaciones, autenticación de usuarios y la gestión de eventos, tareas y cotizaciones a través de una API. Creemos que esto nos ayudará a captar la atención de diferentes tipos de visitantes (recurrentes, racionales y emocionales) y brindará una experiencia de usuario más completa y escalable tanto para los organizadores como para los anfitriones. Esto se confirmará cuando los usuarios puedan buscar organizadores de eventos, comprar un plan de suscripción mensual, comunicarse a través del chat, recibir notificaciones relevantes y los organizadores puedan crear, actualizar o cancelar eventos, tareas y cotizaciones utilizando los puntos finales API implementados. |
|       Sprint 3 Velocity        |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        Velocidad de 26 - Primer Sprint                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|      Sum of Story Points       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           Sprint 3 - 22 Story Points                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |

#### 5.2.3.2. Aspect Leaders and Collaborators.
|            Team Member            | GitHub Username | Task Management | Profile Management | Quote Management | Event Management | Review Management | 
|:---------------------------------:|:---------------:|:--------------:|:-----------------:|:---------------:|:----------------:|:--------:| 
|     Aldave Aldave, Jean Pierr     |   Jean Pierr    |       L        |         C         |        C        |        C         |    C     |     
|  Crisanto Calle, Deybbi Anderson  |     Dacc03      |       C        |         L         |        C        |        C         |    C     |   
| Cutiri Agüero, Fabrizio Alexander |    Fabrizio     |       C        |         C         |        L        |        C         |    C     |    
|   Paico Calderon, July Zelmira    |      JulyP      |       C        |         C         |        C        |        L         |    C     |
| Berrocal Ramirez, Omar Christian  |      OmBRz      |       C        |         C         |        C        |        C         |    L     |  

#### 5.2.3.3.Sprint Backlog 3.


Para el sprint 3 usamos la herramienta trello para organizar las tareas del equipo.

![sprint-backlog 3](../assets/chapter-V/sprint-backlog-3.png)

Enlance: https://trello.com/b/2zjBMbhf/eventify-sprint-backlog-3

<table>
  <tr>
    <td> <strong>Sprint #</strong></td>
    <td align="center" colspan="7"> <strong>Sprint 3</strong> </td>
  </tr>

   <tr>
    <td align="center" colspan="2"> <strong>User Story</strong></td>
    <td align="center" colspan="6"> <strong>Work-item/Task</strong></td>
  </tr>
  <tr>
    <td align="center"> <strong>ID</strong> </td>
    <td align="center"> <strong>Title</strong></td>
    <td align="center"> <strong>ID</strong> </td>
    <td align="center"> <strong>Title</strong></td>
    <td align="center"> <strong>Description</strong></td>
    <td align="center"> <strong>Estimation (Hours)</strong></td>
    <td align="center"> <strong>Assigned To</strong></td>
    <td align="center"> <strong> Status (To-do/In-Process/To-Review/Done)  </strong></td>
  </tr>
  <!---------------------------------------------------------------------- -->
  <tr>
    <td rowspan="2" align="center"> US26 </td>
    <td rowspan="2" align="center">  Calificar organizador tras evento</td>
    <td align="center"> TA09 </td>
     <td align="center"> Create a review for profile and social event</td>
    <td align="center">Crear un registro de una reseña para el peril y el evento</td>
    <td align="center"> 2</td>
    <td align="center"> Berrocal Ramirez, Omar Christian</td>
    <td align="center">Done</td>
  </tr>
  <tr>
    <td align="center"> TA05 </td>
     <td align="center"> Implement reviews business rules</td>
    <td align="center"> Implementar las reglas de negocio para las reseñas</td>
    <td align="center"> 2</td>
    <td align="center"> Berrocal Ramirez, Omar Christian</td>
    <td align="center">Done</td>
  </tr>

<!----------------------------------------------->
  <tr>
    <td rowspan="2" align="center"> US18 </td>
    <td rowspan="2" align="center">  Lista de tareas del evento</td>
    <td align="center"> TA01 </td>
    <td align="center"> Change status of the task</td>
    <td align="center"> habilitar el cambio de estado de las tareas en el dashboard.</td>
    <td align="center"> 2</td>
    <td align="center"> Aldave Aldave, Jean Pierr</td>
    <td align="center">In Progress</td>
  </tr>
<tr>
    <td align="center"> TA14 </td>
     <td align="center"> Create Task for organizer dashboard</td>
    <td align="center"> Crear lista de tareas para el organizador</td>
    <td align="center"> 2</td>
    <td align="center"> Aldave Aldave, Jean Pierr</td>
    <td align="center">In Progress</td>
  </tr>

  <!----------------------------------------------->
  <tr>
    <td rowspan="1" align="center"> US28 </td>
    <td rowspan="1" align="center">  Filtro de evento social</td>
    <td align="center"> TA02 </td>
    <td align="center"> Implement event filters</td>
    <td align="center"> Agregar operaciones de filtro para encontrar eventos.</td>
    <td align="center"> 3</td>
    <td align="center"> Paico Calderon, July Zelmira</td>
    <td align="center">Done</td>
  </tr>


<!-------------------------------------------------->
  <tr>
    <td rowspan="2" align="center"> US19 </td>
    <td rowspan="2" align="center">  Gestión de presupuesto del evento</td>
    <td align="center"> TA07 </td>
    <td align="center"> Create a quote for the organizer</td>
    <td align="center"> crea un cotización para el organizador de eventos.</td>
    <td align="center"> 2</td>
    <td align="center"> Cutiri Agüero, Fabrizio Alexander </td>
    <td align="center"> Done</td>
  </tr>
  <tr>
    <td align="center"> TA06 </td>
     <td align="center">Implement quote business rules.</td>
    <td align="center"> Implementa las reglas de negocio para la generación de cotizaciones.</td>
    <td align="center"> 3</td>
    <td align="center"> Cutiri Agüero, Fabrizio Alexander</td>
    <td align="center">Done</td>
  </tr>

  <!----------------------------------------------->
  <tr>
    <td rowspan="1" align="center"> US29 </td>
    <td rowspan="1" align="center">  Visualización de los evento</td>
    <td align="center"> TA11 </td>
    <td align="center"> Create and delete a social event register</td>
    <td align="center"> Implementa operaciones para gestionar la sección de eventos.</td>
    <td align="center"> 4</td>
    <td align="center"> Paico Calderon, July Zelmira </td>
    <td align="center">Done</td>
  </tr>
  <!------------------------------------------------>
   <tr>
    <td rowspan="2" align="center"> US31 </td>
    <td rowspan="2" align="center">  Visualizar perfiles de organizadores	</td>
    <td align="center"> TA08 </td>
    <td align="center"> Create a profile</td>
    <td align="center"> Crea un registro de un perfil.</td>
    <td align="center"> 2</td>
    <td align="center"> Crisanto Calle, Deybbi Anderson </td>
    <td align="center"> Done</td>
  </tr>
  <tr>
    <td align="center"> TA10 </td>
     <td align="center">Implemnt profile business rules</td>
    <td align="center"> Implementa las reglas del negocio para los perfiles.</td>
    <td align="center"> 2</td>
    <td align="center">Crisanto Calle, Deybbi Anderson</td>
    <td align="center">Done</td>
  </tr>
  <!------------------------------------------------>
   <tr>
    <td rowspan="2" align="center"> US07 </td>
    <td rowspan="2" align="center">  Confianza y seguridad.</td>
    <td align="center"> TA03 </td>
    <td align="center"> Implement about us section.</td>
    <td align="center"> Crea una seeción about us en el landing page.</td>
    <td align="center"> 1 </td>
    <td align="center"> Cutiri Agüero, Fabrizio Alexander </td>
    <td align="center"> Done</td>
  </tr>
   <tr>
    <td align="center"> TA04 </td>
     <td align="center">Create About the product Section</td>
    <td align="center"> Crea una sección para el video about the product.</td>
    <td align="center"> 1</td>
    <td align="center">Cutiri Agüero, Fabrizio Alexander</td>
    <td align="center">In Progress</td>
  </tr>


</table>

#### 5.2.3.4. Development Evidence for Sprint Review

A continuación, se mostrarán los commits registrados en el repositorio correspondiente al backend para el desarrollo del sprint 3.

<table>
  <tr>
    <td align ="center" > <strong>Repository</strong></td>
    <td  align ="center" > <strong>Branch</strong></td>
    <td  align ="center" > <strong>Commit ID</strong></td>
    <td  align ="center" > <strong>Commit message</strong></td>
    <td  align ="center" > <strong>Commit Masagge body</strong></td>
    <td  align ="center" > <strong>Commit on (date)</strong></td>
  </tr>

  <tr>
    <td rowspan="27" align="center"> https://github.com/AngelDevs-Open/eventify-platfom </td>
    <td align="center"> feature/quote-management</td>
    <td align="center"> 7a0818d304df438dbd82258b650c13ca61912a2e</td>
    <td align="center"> chore: specify type of date columns for service item</td>
    <td align="center"> ---</td>
    <td align="center"> 21/06/2025</td>
  </tr>

  <tr>
    <td align="center">feature/profile-management</td>
    <td align="center" > 6b1d27b0ce336255dbd3a171a2bf78ef30eae65e</td>
    <td align="center"> feat: add @operation annotations to ProfileController endpoints</td>
    <td align="center"> ---</td>
    <td align="center"> 20/06/2025</td>
  </tr>

  <tr>
    <td align="center"> feature/reviews-management</td>
    <td align="center">e0ee6a9f679a46df2f638830f10a0de953170703</td>
    <td align="center"> fix: bean creation failure.</td>
    <td align="center"> ---</td>
    <td align="center"> 21/06/2025</td>
  </tr>

  <tr>
    <td align="center"> feature/event-management</td>
    <td align="center"> c08586c4b3f3719d0c38e66fb63914536ba81026</td>
    <td align="center"> feat(value-object): Add StatusType value object.</td>
    <td align="center"> ---</td>
    <td align="center">22/06/2025</td>
  </tr>

  <tr>
    <td align="center"> feature/develop</td>
    <td align="center"> e0ee6a9f679a46df2f638830f10a0de953170703</td>
    <td align="center"> fix: bean creation failure.</td>
    <td align="center"> ---</td>
    <td align="center">21/06/2025</td>
  </tr>
</table>


<table>
  <tr>
    <td align ="center" > <strong>Repository</strong></td>
    <td  align ="center" > <strong>Branch</strong></td>
    <td  align ="center" > <strong>Commit ID</strong></td>
    <td  align ="center" > <strong>Commit message</strong></td>
    <td  align ="center" > <strong>Commit Masagge body</strong></td>
    <td  align ="center" > <strong>Commit on (date)</strong></td>
  </tr>

  <tr>
    <td rowspan="27" align="center"> https://github.com/AngelDevs-Web/eventify-landing-page </td>
    <td align="center"> feature/develop</td>
    <td align="center"> 0963aedef8bb20d59df2d13aa055eb85a93a427b</td>
    <td align="center"> feat(quote): https://github.com/AngelDevs-Web/eventify-landing-page</td>
    <td align="center"> ---</td>
    <td align="center"> 14/06/2025</td>
  </tr>

  <tr>
    <td align="center">feature/header</td>
    <td align="center" > ccbd9bd848ce8ed3b55375c366a333cb54d499d2</td>
    <td align="center"> feat(header): add call to action button for recurrent visitor</td>
    <td align="center"> ---</td>
    <td align="center"> 21/06/2025</td>
  </tr>

  <tr>
    <td align="center"> feature/header</td>
    <td align="center">256f0b9f00475606d77ea8ed89ba35699aebafe1</td>
    <td align="center"> feat(header): update spanish content</td>
    <td align="center"> ---</td>
    <td align="center"> 21/06/2025</td>
  </tr>

  <tr>
    <td align="center"> feature/about-the-product</td>
    <td align="center"> 2aaac34b379b09cf34072e2e85a2b1914054c504</td>
    <td align="center"> feat(about-the-product): update spanish and english content</td>
    <td align="center"> ---</td>
    <td align="center">21/06/2025</td>
  </tr>

  <tr>
    <td align="center"> feature/quotes-management</td>
    <td align="center"> b49a8805c6d67bafa46fca58befdf725cb947ecc</td>
    <td align="center"> feat(quote): add organizer id value object</td>
    <td align="center"> ---</td>
    <td align="center">20/06/2025</td>
  </tr>

  <tr>
    <td align="center"> feature/functionalities</td>
    <td align="center"> acf90db98ac3f2506059571064dbd17716c99d17</td>
    <td align="center">chore: update position of functionalities section</td>
    <td align="center"> ---</td>
    <td align="center"> 21/06/2025</td>
  </tr>

  <tr>
    <td align="center"> feature/plans</td>
    <td align="center"> 9771385ffabfcb08508348278b1afeae547b4a5c</td>
    <td align="center"> style: update style of plans section</td>
    <td align="center"> ---</td>
    <td align="center"> 21/06/2025</td>
  </tr>

  <tr>
    <td align="center"> feature/about-us</td>
    <td align="center"> 669bee4d5894851a4912cea3225f7913513fc4cc</td>
    <td align="center"> style(about-us): update styles for about us section</td>
    <td align="center"> ---</td>
    <td align="center"> 21/06/2025</td>
  </tr>

  <tr>
    <td align="center"> feature/about-the-team</td>
    <td align="center">b6afb677df8658ab31530dc37b2863ba4c2cbf7b</td>
    <td align="center"> feat(about-the-team): add about the team section in both languages</td>
    <td align="center"> ---</td>
    <td align="center">21/06/2025</td>
  </tr>

  <tr>
    <td align="center"> feature/header</td>
    <td align="center">34b801d0904799f58217f671debdcb87fa77d293</td>
    <td align="center"> chore: change order of language switcher buttons</td>
    <td align="center"> ---</td>
    <td align="center">21/06/2025</td>
  </tr>
</table>


#### 5.2.3.5.Execution Evidence for Sprint Review.

Para el Sprint 3, se alcanzó el objetivo de desplegar la segunda versión de la aplicación web. Adicionalmente, se logró la implementación de la primera versión del backend.

**Backend**

![execution-backend-1](../assets/chapter-V/execution-backend-1.png)

![execution-backend-2](../assets/chapter-V/execution-backend-2.png)

![execution-backend-3.png](../assets/chapter-V/execution-backend-3.png)

#### 5.2.3.6.Services Documentation Evidence for Sprint Review.

A continuación, se muestran los endpoints documentados

<table> 
  <tr>
    <td> <strong>Action </strong></td>
    <td> <strong>End Point </strong></td>
    <td align="center"> <strong>Funciones</strong> </td>
  </tr>

  <tr>
    <td> GET</td>
    <td> /api/v1/organizers/{organizerId}/quotes</td>
    <td> Obtiene todas las cotizaciones de un organizador</td>
  </tr>
  <tr>
    <td> GET</td>
    <td> /api/v1/quotes/{quoteId}</td>
    <td> Obtiene una cotización por ID</td>
  </tr>
  <tr>
    <td> PUT</td>
    <td> /api/v1/quotes/{quoteId}</td>
    <td> Actualiza una cotización por ID</td>
  </tr>
  <tr>
    <td> DELETE</td>
    <td> /api/v1/quotes/{quoteId}</td>
    <td> Elimina una cotización por ID</td>
  </tr>
  <tr>
    <td> POST</td>
    <td> /api/v1/quotes</td>
    <td> Crea una nueva cotización</td>
  </tr>
  <tr>
    <td> POST</td>
    <td> /api/v1/quotes/{quoteId}/confirmations</td>
    <td> Actualiza el estado de una cotización a "Accepted"</td>
  </tr>
  <tr>
    <td> POST</td>
    <td> /api/v1/quotes/{quoteId}/rejections</td>
    <td> Actualiza el estado de una cotización a "Rejected"</td>
  </tr>
  <tr>
    <td> GET</td>
    <td> /api/v1/quotes/{quoteId}/service-items/{serviceItemId}</td>
    <td> Obtiene un servicio de una cotización por ID</td>
  </tr>
  <tr>
    <td> PUT</td>
    <td> /api/v1/quotes/{quoteId}/service-items/{serviceItemId}</td>
    <td> Actualiza un servicio de una cotización</td>
  </tr>
  <tr>
    <td> DELETE</td>
    <td> /api/v1/quotes/{quoteId}/service-items/{serviceItemId}</td>
    <td> Elimina un servicio de una cotización</td>
  </tr>
  <tr>
    <td> POST</td>
    <td> /api/v1/quotes/{quoteId}/service-items</td>
    <td> Crea un nuevo servicio para una cotización</td>
  </tr>
  <tr>
    <td> GET</td>
    <td> /api/v1/quotes/{quoteId}/service-items</td>
    <td> Obtiene todos los servicios de una cotización</td>
  </tr>
</table>


#### 5.2.3.7.Software Deployment Evidence for Sprint Review.

Aquí se verá el proceso del despliegue del backend durante el sprint.

**Backend**

Para esta entrega el backend fue desplegado en Render

![render-deploy](../assets/chapter-V/deployment-backend-render.png)

#### 5.2.3.8.Team Collaboration Insights during Sprint.

Esta sección demuestra la colaboración del equipo en la entrega del sprint actual, incluyendo las métricas de creación del backend.

### Backend

**Pulse**

![pulse-insights](../assets/chapter-V/pulse-insights-backend.png)

**Contributors**

![contributors-insights](../assets/chapter-V/contributors-insights-backend.png)

**Network**

![network-insights](../assets/chapter-V/network-insights-backend.png)


### 5.2.4. Sprint 4

Durante el este Sprint nuestro enfoque es desarrollar la versión final de los tres productos de nuestro proyecto: la landing page, el FrontEnd y el BackEnd. Para lograrlo, definimos en el sprint backlog diversas tareas relacionadas con las funcionalidades principales del negocio, como las cotizaciones para eventos y la creación de tareas que se llevarán a cabo durante su planificación. Además, se implementarán mejoras en la experiencia del usuario y se realizarán pruebas exhaustivas para garantizar un producto de alta calidad.

#### 5.2.4.1. Spring Planning 4.


|            Sprint #            |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             Sprint 4                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|:------------------------------:|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|
| **Sprint Planning Background** |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|              Date              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             01/07/25                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|              Time              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           11:40 horas                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|            Location            |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               Reunión presencial - Aula UPC VH107                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|          Prepared By           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 Omar Christian Berrocal Ramirez                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|           Attendees            |                                                                                                                                                                                                                                                                                                                                                                                                                                                     - Dayro Richard Rios Piñan   <br> - Deybbi Anderson Crisanto Calle  <br> - Fabrizio Alexander Cutiri Agüero  <br> - July Zelmira Paico Calderon                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|    Sprint 3 Review Summary     |                                                                                                                                                                                                                                                                          Se completó la documentación y el diseño de la estructura de la Landing Page y el Frontend de la aplicación web, definiendo las secciones principales e identificando los componentes esenciales para mostrar el funcionamiento de la plataforma. Además, se determinaron las tecnologías fundamentales para el proyecto: Angular en el frontend, y Java con Springboot en el backend, lo que garantiza una arquitectura robusta y escalable para la gestión de la aplicación.                                                                                                                                                                                                                                                                          |
| Sprint 3 Retrospective Summary |                                                                                                                                                                                                                                                                                                                                                            En el Sprint 3, se completó la integración inicial entre el frontend y backend, permitiendo el funcionamiento básico de características como generación de cotizaciones. Tambien se hizo hincapié en la importancia de seguir con los estándares de código para garantizar la escalabilidad del proyecto.                                                                                                                                                                                                                                                                                                                                                             |
| **Sprint Goal & User Stories** |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|         Sprint 4 Goal          | En este último sprint, nuestro enfoque es finalizar e integrar todos los componentes clave de la aplicación. Esto incluye presentar información clara sobre el proyecto y el equipo detrás del desarrollo, y optimizar el sitio web para convertir a los visitantes en usuarios activos. Se implementarán funcionalidades esenciales como la búsqueda de organizadores de eventos, suscripciones mensuales, notificaciones personalizadas, autenticación de usuarios y una API robusta para gestionar eventos, tareas y cotizaciones. Estas características están diseñadas para ofrecer una experiencia completa y escalable, pensada para atraer y retener distintos tipos de usuarios ,ya sean recurrentes, racionales o emocionales. El éxito de este sprint se validará cuando los usuarios puedan interactuar plenamente con el sistema: desde buscar organizadores y suscribirse a un plan, hasta recibir alertas y que los organizadores puedan administrar eficientemente sus actividades mediante la API implementada. |
|       Sprint 4 Velocity        |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 Velocidad de 20 - Cuarto Sprint                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|      Sum of Story Points       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    Sprint 4 - 22 Story Points                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |

#### 5.2.4.2. Aspect Leaders and Collaborators.

|             Team Member             |  GitHub Username   | ReviewManagement | ProfileManagement | QuoteManagement | Event Management | Subscription Management |
|:-----------------------------------:|:------------------:|:----------------:|:-----------------:|:---------------:|:----------------:|:-----------------------:|
|  Berrocal Ramirez, Omar Christian   |       OmBRz        |        L         |         C         |        C        |        C         |            C            | 
|   Crisanto Calle, Deybbi Anderson   |       Dacc03       |        C         |         L         |        C        |        C         |            C            |
|  Cutiri Agüero, Fabrizio Alexander  |      Fabrizio      |        C         |         C         |        L        |        C         |            C            |
|    Paico Calderon, July Zelmira     |       JulyP        |        C         |         C         |        C        |        L         |            C            |
|      Rios Piñan, Dayro Richard      |    Addicted2you    |        C         |         C         |        C        |        C         |            L            | 

#### 5.2.4.3. Sprint Backlog 4.

Para el sprint 4 usamos la herramienta trello para organizar las tareas del equipo.

![sprint-backlog 4](../assets/chapter-V/sprint-backlog-4.png)

Enlance: https://trello.com/b/raylAcjO/eventify-sprint-backlog-4

<table>
  <tr>
    <td> <strong>Sprint #</strong></td>
    <td align="center" colspan="7"> <strong>Sprint 4</strong> </td>
  </tr>

   <tr>
    <td align="center" colspan="2"> <strong>User Story</strong></td>
    <td align="center" colspan="6"> <strong>Work-item/Task</strong></td>
  </tr>
  <tr>
    <td align="center"> <strong>ID</strong> </td>
    <td align="center"> <strong>Title</strong></td>
    <td align="center"> <strong>ID</strong> </td>
    <td align="center"> <strong>Title</strong></td>
    <td align="center"> <strong>Description</strong></td>
    <td align="center"> <strong>Estimation (Hours)</strong></td>
    <td align="center"> <strong>Assigned To</strong></td>
    <td align="center"> <strong> Status (To-do/In-Process/To-Review/Done)  </strong></td>
  </tr>
  <!---------------------------------------------------------------------- -->
  <tr>
    <td rowspan="1" align="center"> US01 </td>
    <td rowspan="1" align="center"> Navegación sencilla</td>
    <td align="center"> TA01 </td>
     <td align="center"> Implementar el lenguaje por defecto</td>
    <td align="center"> Quiero que el landing page esté en ingles por defecto</td>
    <td align="center"> 2</td>
    <td align="center"> Crisanto Calle, Deybbi Anderson</td>
    <td align="center">Done</td>
  </tr>
<!----------------------------------------------->
  <tr>
    <td rowspan="1" align="center"> US05 </td>
    <td rowspan="1" align="center"> Llamada a la acción</td>
    <td align="center"> TA02 </td>
     <td align="center"> Create call to action</td>
    <td align="center"> Quiero que el landing page tenga las llamadas a la acción para los tres tipos de visitantes</td>
    <td align="center"> 2</td>
    <td align="center"> Cutiri Agüero, Fabrizio Alexander</td>
    <td align="center">Done</td>
  </tr>
<!----------------------------------------------->
  <tr>
    <td rowspan="1" align="center"> US06 </td>
    <td rowspan="1" align="center"> Visualización de tutorial de la aplicación</td>
    <td align="center"> TA03 </td>
     <td align="center"> Add about the product video</td>
    <td align="center"> Quiero insertar un video sobre el producto en nuestra web de negocio.</td>
    <td align="center"> 1</td>
    <td align="center"> Cutiri Agüero, Fabrizio Alexander</td>
    <td align="center">Done</td>
  </tr>
<!----------------------------------------------->
  <tr>
    <td rowspan="1" align="center"> US10 </td>
    <td rowspan="1" align="center"> Diseño responsive</td>
    <td align="center"> TA04 </td>
     <td align="center"> Configure correct loading</td>
    <td align="center"> Quiero que el sitio web de negocio se cargue correctamente .</td>
    <td align="center"> 1</td>
    <td align="center"> Crisanto Calle, Deybbi Anderson</td>
    <td align="center">Done</td>
  </tr>
<!-------------------------------------------------->
  <tr>
    <td rowspan="2" align="center"> US19 </td>
    <td rowspan="2" align="center">  Gestión de presupuesto del evento</td>
    <td align="center"> TA05 </td>
    <td align="center"> Create an update operation for quote</td>
    <td align="center"> Quiero crear una operacion para actualizar cotizaciones.</td>
    <td align="center"> 2</td>
    <td align="center"> Cutiri Agüero, Fabrizio Alexander </td>
    <td align="center"> Done</td>
  </tr>
  <tr>
    <td align="center"> TA06 </td>
     <td align="center">Create service item for quote management.</td>
    <td align="center"> Quiero crear un service item para el manejo de las cotizaciones.</td>
    <td align="center"> 4</td>
    <td align="center"> Cutiri Agüero, Fabrizio Alexander</td>
    <td align="center">Done</td>
  </tr>
<!----------------------------------------------->
  <tr>
    <td rowspan="1" align="center"> US21 </td>
    <td rowspan="1" align="center"> Vista de cronograma del evento</td>
    <td align="center"> TA08 </td>
     <td align="center"> Update scheduler for events</td>
    <td align="center"> Quiero actualizar el calendario de los eventos.</td>
    <td align="center"> 2</td>
    <td align="center"> Berrocal Ramirez, Omar Christian.</td>
    <td align="center">Done</td>
  </tr>
<!----------------------------------------------->
  <tr>
    <td rowspan="1" align="center"> US27 </td>
    <td rowspan="1" align="center"> Editar reseña publicada</td>
    <td align="center"> TA07 </td>
     <td align="center">add update operation for reviews</td>
    <td align="center"> Quiero implementar un operación para actualizar las reseñas publicadas.</td>
    <td align="center"> 2</td>
    <td align="center"> Berrocal Ramirez, Omar Christian.</td>
    <td align="center">Done</td>
  </tr>
<!----------------------------------------------->
  <tr>
    <td rowspan="1" align="center"> US29 </td>
    <td rowspan="1" align="center"> Visualización de los evento</td>
    <td align="center"> TA09 </td>
     <td align="center">add update operation for social events</td>
    <td align="center"> Quiero implementar un operación para actualizar los registros de eventos sociales.</td>
    <td align="center"> 2</td>
    <td align="center"> Paico Calderon, July Zelmira.</td>
    <td align="center">In Progress</td>
  </tr>
<!----------------------------------------------->
  <tr>
    <td rowspan="1" align="center"> US28 </td>
    <td rowspan="1" align="center">Filtro de evento social</td>
    <td align="center"> TA10 </td>
     <td align="center">add querys for more event filters</td>
    <td align="center"> Quiero implementar más opciones de filtros para los eventos.</td>
    <td align="center"> 1</td>
    <td align="center"> Paico Calderon, July Zelmira.</td>
    <td align="center">In Progress</td>
  </tr>
  <!------------------------------------------------>
   <tr>
    <td rowspan="3" align="center"> US31 </td>
    <td rowspan="3" align="center">  Visualizar perfiles de organizadores	</td>
    <td align="center"> TA11 </td>
    <td align="center"> Create update opetarion for profile.</td>
    <td align="center"> Quiero implementar una operación para actualizar los perfiles.</td>
    <td align="center"> 2</td>
    <td align="center"> Crisanto Calle, Deybbi Anderson </td>
    <td align="center"> Done</td>
  </tr>
  <tr>
    <td align="center"> TA12 </td>
     <td align="center">Create a service catalog for profiles.</td>
    <td align="center"> Quiero crear un catálogo para los perfiles.</td>
    <td align="center"> 2</td>
    <td align="center">Crisanto Calle, Deybbi Anderson</td>
    <td align="center">Done</td>
  </tr>
  <tr>
    <td align="center"> TA13 </td>
    <td align="center"> Create album for profile.</td>
    <td align="center"> Quiero crear un album para los perfiles.</td>
    <td align="center"> 2</td>
    <td align="center"> Crisanto Calle, Deybbi Anderson</td>
    <td align="center"> Done</td>
  </tr>
  <!------------------------------------------------>
   <tr>
    <td rowspan="2" align="center">  </td>
    <td rowspan="2" align="center">  </td>
    <td align="center"> TA14 </td>
    <td align="center"> Deploy products.</td>
    <td align="center"> Quiero desplegar mis productos a un dominio público.</td>
    <td align="center"> 2 </td>
    <td align="center"> Cutiri Agüero, Fabrizio Alexander </td>
    <td align="center"> Done</td>
  </tr>
   <tr>
    <td align="center"> TA15 </td>
    <td align="center"> Implement security</td>
    <td align="center"> Quiero agregar autenticación para la plataforma web.</td>
    <td align="center"> 3 </td>
    <td align="center"> Rios Piñan, Dayro Richard </td>
    <td align="center">In Progress</td>
  </tr>


</table>

#### 5.2.4.4. Development Evidence for Sprint Review.


A continuación, se mostrarán los commits últimos registrados en el repositorio correspondiente al backend para el desarrollo del sprint 4.

<table>
  <tr>
    <td align ="center" > <strong>Repository</strong></td>
    <td  align ="center" > <strong>Branch</strong></td>
    <td  align ="center" > <strong>Commit ID</strong></td>
    <td  align ="center" > <strong>Commit message</strong></td>
    <td  align ="center" > <strong>Commit Masagge body</strong></td>
    <td  align ="center" > <strong>Commit on (date)</strong></td>
  </tr>

  <tr>
    <td rowspan="27" align="center"> https://github.com/AngelDevs-Open/eventify-platfom </td>
    <td align="center"> feature/quote-management</td>
    <td align="center"> e851915f3f54ed55c7cdb521fd3eaf268ce1f0d7</td>
    <td align="center"> feat(planning): add acl planning external profile service</td>
    <td align="center"> ---</td>
    <td align="center"> 05/07/2025</td>
  </tr>

  <tr>
    <td align="center">feature/profile-management</td>
    <td align="center" > c699202593a4593bb96af9d787690243d76da12f</td>
    <td align="center"> fix(pom): correct spelling of 'platform' in artifactId and name.</td>
    <td align="center"> ---</td>
    <td align="center"> 01/07/2025</td>
  </tr>

  <tr>
    <td align="center"> feature/reviews-management</td>
    <td align="center">e0ee6a9f679a46df2f638830f10a0de953170703</td>
    <td align="center"> fix: bean creation failure.</td>
    <td align="center"> ---</td>
    <td align="center"> 21/06/2025</td>
  </tr>

  <tr>
    <td align="center"> feature/event-management</td>
    <td align="center"> d3212ba217da342b3b4d99e6ad1c9e3291e80ad8</td>
    <td align="center"> feat(planning): add documentation for planning bounded context and social event management.</td>
    <td align="center"> ---</td>
    <td align="center">07/07/2025</td>
  </tr>

  <tr>
    <td align="center"> feature/develop</td>
    <td align="center"> 4166cc97eec4857b4008e1773bb55dd5cbcb7ae5</td>
    <td align="center"> feat(iam): check properties.</td>
    <td align="center"> ---</td>
    <td align="center">07/07/2025</td>
  </tr>

  <tr>
    <td align="center"> feature/iam</td>
    <td align="center"> d78e4e4d873057d88c8000bc2b7a0c2ffdc12385</td>
    <td align="center"> feat(iam): update application-prod.properties</td>
    <td align="center"> ---</td>
    <td align="center">07/07/2025</td>
  </tr>
</table>

<table>
  <tr>
    <td align ="center" > <strong>Repository</strong></td>
    <td  align ="center" > <strong>Branch</strong></td>
    <td  align ="center" > <strong>Commit ID</strong></td>
    <td  align ="center" > <strong>Commit message</strong></td>
    <td  align ="center" > <strong>Commit Message body</strong></td>
    <td  align ="center" > <strong>Commit on (date)</strong></td>
  </tr>

  <tr>
    <td rowspan="27" align="center"> https://github.com/AngelDevs-Web/eventify-front-end </td>
    <td align="center"> feature/develop</td>
    <td align="center"> 051b1907d086f53f1e745007186623da9bc1ab61</td>
    <td align="center"> Merge branch 'feature/event-management' into develop</td>
    <td align="center"> ---</td>
    <td align="center"> 07/07/2025</td>
  </tr>

  <tr>
    <td align="center">feature/event-management</td>
    <td align="center" > 35a6eac8dad523388984eadc38fd2bb03eb7a521</td>
    <td align="center"> refactor(calendar): refactor calendar view path and integrate FullCalendar.</td>
    <td align="center"> ---</td>
    <td align="center"> 07/07/2025</td>
  </tr>

  <tr>
    <td align="center"> feature/iam</td>
    <td align="center">3d8198364a60a020a3f2f35af491242b26a0c4a5</td>
    <td align="center"> feat(iam): add authentication section in navigation bar component</td>
    <td align="center"> ---</td>
    <td align="center"> 07/07/2025</td>
  </tr>

  <tr>
    <td align="center"> feature/profile-management</td>
    <td align="center"> 916bc3e3171e128c64c16edd415086d6629c5555</td>
    <td align="center"> feat(base-service): add unit tests for BaseService with TestService implementation.</td>
    <td align="center"> ---</td>
    <td align="center">21/06/2025</td>
  </tr>

  <tr>
    <td align="center"> feature/quotes-management</td>
    <td align="center"> 62258159bd17a3ab0aca2b30e651cad5cd511247</td>
    <td align="center"> feat(service-item): add update service item functionality</td>
    <td align="center"> ---</td>
    <td align="center">07/07/2025</td>
  </tr>
</table>



<table>
  <tr>
    <td align ="center" > <strong>Repository</strong></td>
    <td  align ="center" > <strong>Branch</strong></td>
    <td  align ="center" > <strong>Commit ID</strong></td>
    <td  align ="center" > <strong>Commit message</strong></td>
    <td  align ="center" > <strong>Commit Message body</strong></td>
    <td  align ="center" > <strong>Commit on (date)</strong></td>
  </tr>

  <tr>
    <td rowspan="27" align="center"> https://github.com/AngelDevs-Web/eventify-landing-page </td>
    <td align="center"> develop</td>
    <td align="center"> d655cbc4b5c8a03a035c167cc050d7c915c6634a</td>
    <td align="center"> refactor(paths): refactor assets paths in html.</td>
    <td align="center"> ---</td>
    <td align="center"> 05/07/2025</td>
  </tr>

  <tr>
    <td rowspan="27" align="center"> https://github.com/AngelDevs-Web/eventify-landing-page </td>
    <td align="center"> main</td>
    <td align="center"> a27215605323f59a313455f164e3aa2bb2af7f8c</td>
    <td align="center"> refactor(assets): refactor developers profiles.</td>
    <td align="center"> ---</td>
    <td align="center"> 05/07/2025</td>
  </tr>

</table>


#### 5.2.4.5. Execution Evidence for Sprint Review.
#### 5.2.4.6. Services Documentation Evidence for Sprint Review.
#### 5.2.4.7. Software Deployment Evidence for Sprint Review.
#### 5.2.4.8. Team Collaboration Insights during Sprint.

## 5.3. Validation Interviews.
### 5.3.1. Diseño de Entrevistas.

A continuación se presentan las preguntas de validación utilizadas para las entrevistas con usuarios. El objetivo es evaluar tanto la landing page como la aplicación web de Eventify para asegurar que la experiencia de navegación sea clara, coherente y útil para quienes organizan y gestionan eventos.


#### Preguntas sobre la Landing Page

- ¿Al ingresar a la landing page, entiendes rápidamente qué es Eventify y a quién está dirigido?
- ¿La información sobre las funcionalidades de la plataforma te resulta clara y atractiva?
- ¿El diseño visual (colores, imágenes, tipografías) te transmite confianza y profesionalismo?
- ¿Consideras que la estructura de la landing page está bien organizada y fácil de navegar?
- ¿Te motivaría registrarte o saber más sobre Eventify luego de explorar la landing page?
- ¿Hay algo que te gustaría ver en la landing que actualmente no está presente?

#### Preguntas sobre la Aplicación Web

- ¿Nota coherencia visual y funcional entre las distintas secciones (perfil, eventos, cotizaciones, etc.)?
- ¿El proceso de creación o edición de sus albums incluidos en su perfil es claro y sencillo?
- ¿Le resulta fácil acceder y gestionar las cotizaciones dentro de la plataforma?
- ¿Cómo evalúa la sección de eventos? ¿Le permite organizar y visualizar la información de manera efectiva?
- ¿La vista de calendario cubre sus expectativas para programar y revisar actividades importantes?
- ¿El tablero estilo Kanban para tareas le ayuda a organizar su flujo de trabajo? ¿Es intuitivo?
- ¿Le resulta fácil identificar el estado de cada tarea (pendiente, en progreso, finalizada)?
- ¿Hay algo que le haya confundido o que no funcionó como esperabas?
- ¿Qué mejoraría de la experiencia general al usar la aplicación web?



### 5.3.2. Registro de Entrevistas.
### 5.3.3. Evaluaciones según heurísticas.
## 5.4. Video About-the-Product
