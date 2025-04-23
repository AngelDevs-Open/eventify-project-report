# Chapter IV: Product Design

## 4.1. Style Guidelines

### 4.1.1. General Style Guidelines
Esta sección presenta las decisiones visuales y comunicativas que definen la identidad de Eventify. Se explican aspectos clave como el uso del logo, la tipografía elegida, la paleta de colores, el sistema de espaciado y el tono de comunicación aplicado.

**Brand Overview**

La identidad visual de Eventify transmite claridad, organización y confianza desde el primer vistazo. El logo está compuesto por un ícono de calendario con un check en el centro, que representa la idea de tener un evento agendado y confirmado con éxito. A la derecha del ícono aparece el nombre de la marca en mayúsculas: **EVENTIFY**.

El color principal del logo es un tono verde claro y vibrante que destaca sobre distintos fondos, y que transmite frescura, dinamismo

![brand-overview](/assets/chapter-IV/brand-overview-eventify.png)

**Typography**

La tipografía principal de Eventify es **Poppins**, una fuente sans-serif moderna y amigable que aporta claridad, equilibrio visual y un toque contemporáneo a la experiencia del usuario.

Elegida por su legibilidad y estética geométrica, Poppins permite mantener un diseño limpio, funcional y coherente en todos los tamaños de pantalla.

![typography](/assets/chapter-IV/typography-eventify.png)

**Colors**

La paleta de colores de Eventify combina profesionalismo, frescura y dinamismo, reforzando el enfoque moderno y accesible de la plataforma.

![colors-eventify](/assets/chapter-IV/colors-eventify.png)

* **Azul oscuro (#1C2541) / Azul medio (#3A506B)**: <br><br> Aplicados en la barra de navegación, el footer y fondos de secciones principales. Estos tonos transmiten confianza, estabilidad y orden, características clave para una plataforma de organización de eventos.


* **Blanco (#FFFFFF)**: <br><br> Utilizado como fondo neutro para alternar secciones, aporta limpieza visual y mejora la legibilidad de los contenidos.


* **Turquesa claro (#6FFFE9) y verde azulado (#5BC0BE)**: <br><br> Funcionan como colores de acento e interacción. Se emplean en los títulos de sección y al hacer hover sobre botones.

<br>

**Spacing**

La relación de espaciado utilizada, tanto en la aplicación como en la landing page, se basa en un múltiplo de 8 píxeles. Este sistema permite mantener una estructura visual ordenada y coherente en todo el diseño.
![spacing-eventify](/assets/chapter-IV/spacing-eventify.png)

<br>

**Comunication Tone**

La comunicación está diseñada para ser cercana, clara y con un toque entusiasta, buscando conectar emocionalmente tanto con anfitriones como con organizadores de eventos, sin perder profesionalismo. Se adopta un lenguaje que guía, motiva y transmite confianza,

<br>

### 4.1.2. Web Style Guidelines

La interfaz web de Eventify está diseñada bajo principios de diseño responsive, garantizando una experiencia de usuario óptima en todos los dispositivos, desde smartphones hasta pantallas de escritorio. El objetivo es ofrecer una navegación fluida, intuitiva y visualmente coherente.

Para organizar el contenido se utilizó el patrón en Z, un esquema visual que guía naturalmente la mirada del usuario desde la parte superior izquierda hasta la inferior derecha, ideal para estructurar información de forma clara y persuasiva.

![web-style-z-pattern](/assets/chapter-IV/web-style-z-pattern.png)


## 4.2. Information Architecture

### 4.2.1. Organization Systems


### 4.2.2. Labeling Systems


### 4.2.3. SEO Tags and Meta Tags

En el desarrollo de Eventify, la optimización para motores de búsqueda (SEO) juega un papel crucial para mejorar la visibilidad de la plataforma en línea. Los SEO tags y meta tags son herramientas esenciales que ayudan a los motores de búsqueda a comprender y clasificar el contenido de las páginas de la plataforma, asegurando que los usuarios encuentren Eventify de manera eficiente. Estos elementos permiten proporcionar información relevante, como el título de la página, la descripción, las palabras clave, y los datos específicos para mejorar la experiencia del usuario y atraer tráfico cualificado.

En este apartado, exploraremos los diferentes tipos de meta tags y SEO tags implementados en Eventify, cómo se utilizan para optimizar la indexación de nuestras páginas y las mejores prácticas que siguen los motores de búsqueda más utilizados.

#### 🌐 Landing Page (Sitio Web Estático)

- **Title Tag: <br>**
El title tag es uno de los factores más importantes en SEO, ya que determina el título que aparece en los resultados de búsqueda. Por eso decidimos que sea breve, relevante y que contenenga las palabras clave para mejorar una mejor visibilidad.
```html
<title>Eventify - Conecta, organiza y celebra tus eventos</title>
```
- **Meta Description: Tag <br>**
La meta description proporciona un resumen conciso del contenido de la página. Es importante que sea atractiva y contenga palabras clave relevantes para aumentar la tasa de clicks en Eventify.
```html
<meta name="description" content="Eventify es la plataforma donde anfitriones encuentran al organizador ideal y organizadores hacen crecer su negocio. Conecta, organiza y celebra con confianza.">
```
- **Meta Keywords Tag: <br>**
El meta keywords tag es menos relevante hoy en día, pero aún es útil para proporcionar información adicional sobre el contenido de la página. En este caso, hemos incluido palabras clave relacionadas con la organización de eventos y la conexión entre anfitriones y organizadores.
```html
<meta name="keywords" content="eventos, organización, anfitriones, organizadores, bodas, celebraciones, gestión de eventos, planificación de eventos">
```
- **Meta Author Tag: <br>**
El meta author tag se utiliza para especificar el autor del contenido de la página. Aunque no impacta directamente en el SEO, lo consideramos útil para proporcionar transparencia y credibilidad.
```html
<meta name="author" content="Equipo Eventify">
```
- **Meta Viewport Tag: <br>**
  El Meta Viewport Tag es esencial para garantizar que el sitio se vea correctamente en dispositivos móviles. Asegura que la página sea responsiva, ajustando su escala según el tamaño de la pantalla del dispositivo. Decidimos implementarlo en Eventify para mejorar la experiencia del usuario en dispositivos móviles.
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
- **Favicon: <br>**
  El favicon es el ícono que aparece en la pestaña del navegador. Es una forma sencilla de personalizar la apariencia de la página y mejorar la experiencia del usuario. Decidimos incluirlo en Eventify para ayudar a los usuarios a identificar nuestra plataforma de manera visual en múltiples pestañas.
```html
<link rel="icon" href="/assets/chapter-IV/eventify_logo.png" type="image/png">
```

### ⚙️ Web Application (Aplicación Web Interactiva)
- **Title Tag: <br>**
  El title tag define el título que aparecerá en el navegador y en los resultados de búsqueda cuando los usuarios interactúen directamente con la aplicación. Decidimos usar un título dinámico que refleje la acción principal del usuario en la aplicación Eventify.
```html
<title>Eventify - Organiza tu evento</title>
```
- **Meta Description: <br>**
  La meta description proporciona un resumen conciso del contenido de la página. Es importante que sea atractiva y contenga palabras clave relevantes para aumentar la tasa de clicks en Eventify.
```html
<meta name="description" content="Usa Eventify para planificar, coordinar y comunicarte con organizadores o anfitriones en tiempo real. Todo desde una única plataforma eficiente y fácil de usar.">
```
- **Meta Keywords Tag: <br>**
  El meta keywords tag es menos relevante hoy en día, pero aún es útil para proporcionar información adicional sobre el contenido de la página. En este caso, hemos incluido palabras clave relacionadas con la organización de eventos y la conexión entre anfitriones y organizadores.
```html
<meta name="keywords" content="gestión de eventos, mensajería, proformas, seguimiento del evento, anfitriones, organizadores, Eventify app">
```
- **Meta Author Tag: <br>**
  El meta author tag se utiliza para especificar el autor del contenido de la página. Aunque no impacta directamente en el SEO, lo consideramos útil para proporcionar transparencia y credibilidad.
```html
<meta name="author" content="Equipo Eventify">
```
- **Meta Viewport Tag: <br>**
  El meta viewport tag es fundamental para que la aplicación web sea responsiva. Asegura que Eventify se vea y funcione correctamente en dispositivos móviles, ajustando el contenido al ancho de la pantalla del usuario. Decidimos incluirlo para ofrecer una experiencia fluida en cualquier dispositivo.
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

### 4.2.4. Searching Systems


### 4.2.5. Navigation Systems


## 4.3. Landing Page UI Design

### 4.3.1. Landing Page Wireframe
En esta sección se presentan las representaciones de bajo nivel **(wireframes)** del landing page, diseñadas para dispositivos móviles y de escritorio. [Wireframe - Eventify](https://www.figma.com/design/uPtLATLNkVL8P5xY7wBOc2/Eventify---Landing-page?node-id=0-1&t=yRuZCtcaOfFtQUmB-1)

**Desktop Web Browser**

![eventify-wireframe-desktop](/assets/chapter-IV/eventify-wireframe-desktop.jpg)

<br>

**Mobile Web Browser**

![eventify-wireframe-mobile](/assets/chapter-IV/eventify-wireframe-mobile.jpg)

### 4.3.2. Landing Page Mock-up

En esta sección se muestran los mock-ups del landing page, que sirven como una representación visual de alta fidelidad para anticipar cómo se verá y funcionará la interfaz final. Están diseñados tanto para dispositivos móviles como para escritorio. [Mock Ups - Eventify](https://www.figma.com/design/uPtLATLNkVL8P5xY7wBOc2/Eventify---Landing-page?node-id=0-1&t=yRuZCtcaOfFtQUmB-1)

**Desktop Web Browser**

![eventify-mockup-desktop](/assets/chapter-IV/eventify-mockup-desktop.jpg)

<br>

**Mobile Web Browser**

![eventify-mockup-mobile](/assets/chapter-IV/eventify-mockup-mobile.jpg)

## 4.4. Web Applications UX/UI Design

### 4.4.1. Web Applications Wireframes


### 4.4.2. Web Applications Wireflow Diagrams


### 4.4.3. Web Applications Mock-ups


### 4.4.4. Web Applications User Flow Diagrams


## 4.5. Web Applications Prototyping


## 4.6. Domain-Driven Software Architecture

### 4.6.1. Software Architecture Context Diagram


### 4.6.2. Software Architecture Container Diagrams


### 4.6.3. Software Architecture Components Diagrams


## 4.7. Software Object-Oriented Design

### 4.7.1. Class Diagrams


### 4.7.2. Class Dictionary


## 4.8. Database Design

### 4.8.1. Database Diagram
