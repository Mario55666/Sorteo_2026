# Sorteo de Triunfo, Gloria y Esfuerzo

Aplicacion web interactiva para realizar sorteos de orden de presentacion con dos fechas, efectos visuales de espectativa y generacion de PDF para impresion. Desarrollada para el curso de Semiotica de la Imagen.

---

## Caracteristicas Principales

- **Dos fechas de presentacion** con numero configurable de premiados por fecha
- **Modo Individual**: agrega participantes o grupos de trabajo uno por uno
- **Modo Lista Completa**: pega multiples nombres en un textarea amplio (separados por comas o saltos de linea)
- **Persistencia automatica**: los datos se guardan en localStorage, no se pierden al recargar
- **Boton Limpiar Todo**: borra todos los datos con confirmacion
- **Generacion de PDF**: exporta los resultados en formato profesional listo para imprimir
- **Footer docente**: credito al Mg. Mario Quiroz y curso de Semiotica de la Imagen 2026

---

## Efectos de Espectativa Implementados

### 1. Revelacion Misteriosa (Efecto Hover)

Dos capas superpuestas donde la cubierta oculta el premio. Al pasar el cursor sobre el contenedor, la cubierta se desliza hacia arriba mediante una transicion CSS, revelando al premiado con un flash de camara y confeti dorado.

**Tecnica**: `position: absolute`, `transform: translateY(-100%)` en hover, transicion suave de 0.6s.

### 2. Boton 3D Tactil (Efecto de Presion)

El boton "INICIAR SORTEO" utiliza una sombra solida y gruesa en la parte inferior para crear volumen. Al pasar el cursor, el boton se mueve ligeramente hacia abajo y la sombra se acorta, simulando un boton fisico siendo presionado.

**Tecnica**: `box-shadow: 0px 8px 0px #8a6a1f` + `transform: translateY(4px)` en hover.

### 3. Resplandor Luminoso (Efecto Neon)

El boton "Generar PDF para Imprimir" es transparente con borde dorado. Al interactuar, se activan multiples capas de sombra difuminadas que simulan la emision de luz, creando un aura brillante dorada alrededor del elemento.

**Tecnica**: `box-shadow: 0 0 10px #d4a843, 0 0 40px #d4a843, 0 0 80px #d4a843` en hover.

---

## Como Usar

### 1. Configurar el Sorteo

1. Selecciona la **Fecha de Presentacion 1** y cuantos premiados tendra
2. Selecciona la **Fecha de Presentacion 2** y cuantos premiados tendra
3. Define el **tiempo de exposicion** por presentacion (en minutos)

### 2. Agregar Participantes

**Modo Individual:**
- Selecciona si es "Individual" o "Grupo"
- Escribe el nombre y presiona "Agregar"

**Modo Lista Completa:**
- Selecciona el tipo (Individuales o Grupos)
- Pega los nombres en el campo de texto, uno por linea o separados por comas
- Presiona "Agregar Participantes"

### 3. Realizar el Sorteo

- Una vez tengas suficientes participantes, aparecera el boton **INICIAR SORTEO**
- El sistema mezclara todos los participantes aleatoriamente (Fisher-Yates)
- Los primeros N participantes iran a la Fecha 1, los siguientes M a la Fecha 2

### 4. Revelar los Resultados

- Pasa el cursor sobre la **carta misteriosa** para revelar cada premiado
- Los efectos de confeti y resplandor se activan automaticamente
- Usa "Siguiente Premiado" para continuar o "Saltar" para ir al resumen

### 5. Exportar e Imprimir

- En la pantalla de resultados, presiona **"Generar PDF para Imprimir"**
- El PDF incluye tablas por fecha, tipo de participante, tiempo y orden de presentacion

---

## Estructura del Archivo

El proyecto es un **unico archivo HTML** autocontenido que incluye:

- HTML semantico y accesible
- CSS con los 3 efectos de espectativa + tema dorado oscuro
- JavaScript vanilla para toda la logica del sorteo
- Integracion con Canvas Confetti para efectos de celebracion
- Integracion con jsPDF + AutoTable para generacion de PDF
- Persistencia mediante localStorage

### Dependencias Externas (CDN)

| Libreria | Uso |
|----------|-----|
| Tailwind CSS | Utilidades de estilo base |
| Font Awesome 6.5 | Iconografia |
| Google Fonts (Cinzel + Inter) | Tipografia |
| canvas-confetti | Efectos de confeti dorado |
| jsPDF | Generacion de PDF |
| jspdf-autotable | Tablas en PDF |

---

## Tecnologias

- HTML5
- CSS3 (animaciones, transiciones, gradientes, backdrop-filter)
- JavaScript ES6+ (sin frameworks)
- Web Storage API (localStorage)

---

## Creditos

**Docente:** Mg. Mario Quiroz  
**Curso:** Semiotica de la Imagen  
**Ano:** 2026

---

## Licencia

Proyecto educativo para uso academico.
