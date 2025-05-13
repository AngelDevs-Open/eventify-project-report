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
- Organización: [https://github.com/AngelDevs-Web](https://github.com/AngelDevs-Open)
- Reporte: [https://github.com/AngelDevs-Web/eventify-project-report](https://github.com/AngelDevs-Open/eventify-project-report)
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
    <td align="center"> <strong>Title<strong></td>
    <td align="center"> <strong>ID</strong> </td>
    <td align="center"> <strong>Title<strong></td>
    <td align="center"> <strong>Description<strong></td>
    <td align="center"> <strong>Estimation (Hours)<strong></td>
    <td align="center"> <strong>Assigned To<strong></td>
    <td align="center"> <strong> Status (To-do/In-Process/To-Review/Done)  <strong></td>
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
    <td rowspan="27" align="center">https://github.com/AngelDevs-Open/eventify-landing-page </td>
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
