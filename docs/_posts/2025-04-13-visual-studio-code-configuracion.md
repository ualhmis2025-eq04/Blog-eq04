---
layout: post
title:  "Como configurar un entorno de desarrollo local con Visual Studio Code"
date:   2025-04-13 23:22:46 +0100
---

# Cómo configurar un entorno de desarrollo local con Visual Studio Code

Visual Studio Code (VS Code) es uno de los editores de código más populares entre los desarrolladores web. Es rápido, extensible, gratuito y multiplataforma. En esta guía paso a paso aprenderás cómo configurar tu entorno local para comenzar a desarrollar sitios web de forma eficiente.

## Requisitos previos

Antes de comenzar, asegúrate de tener:

- Un sistema operativo que soporte VS Code (Windows, macOS o Linux)
- Conexión a internet
- Conocimientos básicos de HTML, CSS y/o JavaScript

## 1. Instalar Visual Studio Code

Dirígete a la [página oficial de Visual Studio Code](https://code.visualstudio.com/) y descarga la versión correspondiente a tu sistema operativo.

### En Windows o macOS

Sigue el instalador y acepta las opciones por defecto.

### En Linux

En distribuciones basadas en Debian/Ubuntu:

```bash
sudo apt update
sudo apt install software-properties-common apt-transport-https wget
wget -q https://packages.microsoft.com/keys/microsoft.asc -O- | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main"
sudo apt update
sudo apt install code
```

## 2. Instalar extensiones recomendadas

VS Code se potencia con extensiones. Aquí van algunas esenciales para desarrollo web:

- 🌐 **Live Server**: Levanta un servidor local con recarga automática.
- 🎨 **Prettier**: Formateador de código automático.
- 📄 **HTML/CSS Support**: Autocompletado y ayudas visuales.
- 🧪 **ESLint**: Linter para JavaScript y buenas prácticas.
- 🌈 **Color Highlight**: Muestra colores directamente en tu código CSS.

### ¿Cómo instalarlas?

1. Abre VS Code
2. Ve a la barra lateral izquierda (icono de extensiones o `Ctrl+Shift+X`)
3. Busca cada extensión y haz clic en “Instalar”

## 3. Configurar un proyecto básico

Puedes crear una carpeta nueva para tu proyecto:

```bash
mkdir mi-proyecto-web
cd mi-proyecto-web
code .
```

Crea un archivo `index.html` y escribe lo básico:

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Mi Proyecto</title>
</head>
<body>
  <h1>¡Hola, mundo!</h1>
</body>
</html>
```

## 4. Usar Live Server

Una vez instalada la extensión **Live Server**:

1. Abre tu `index.html`
2. Haz clic derecho → “**Open with Live Server**”
3. Se abrirá tu navegador en `http://127.0.0.1:5500` con tu sitio cargado

Cada vez que guardes el archivo (`Ctrl+S`), la página se recargará automáticamente.

## 5. Ajustes útiles en VS Code

Presiona `Ctrl+,` para abrir la configuración y busca estos ajustes:

- `"editor.formatOnSave": true` → Autoformatea al guardar
- `"liveServer.settings.port": 5500` → Fija el puerto del servidor
- `"emmet.includeLanguages"` → Añade soporte para Emmet en más lenguajes

También puedes configurar el archivo `.vscode/settings.json` así:

```json
{
  "editor.formatOnSave": true,
  "files.autoSave": "onWindowChange",
  "liveServer.settings.port": 5500
}
```
Se recomienda revisar que el puerto 5500 no esté siendo usado por otro servicio, y en caso de que lo esté, debe cambiarlo por otro puerto el cual esté seguro que no será usado.

## 6. Agregar Git (opcional)

Si desea usar Git debe seguir los siguientes pasos:

1. Instala Git desde git-scm.com
2. Inicia tu repositorio:
```Bash
git init
git add .
git commit -m "Inicio del proyecto"
```
3. Usa la integración nativa de Git en la barra lateral de VS Code para hacer commits y ver cambios.

## Recursos adicionales

En este apartado se ofrecen algunos enlaces que consideramos que pueden ser útiles para el desarrollo web en Visual Studio Code:

- [Documentación oficial de VS Code](https://code.visualstudio.com/docs)
- [Curso gratuito de Git y GitHub](https://learngitbranching.js.org/)
- [Guía completa de HTML5 y CSS3](https://developer.mozilla.org/es/docs/Web)

## Conclusión

Con Visual Studio Code y algunas extensiones clave puedes montar un entorno de desarrollo web en cuestión de minutos. Es flexible, ligero y perfecto tanto para principiantes como para desarrolladores avanzados. Esperamos que esto les haya ayudado a inciarse en el mundo del desarrollo web haciendo uso de Visual Studio Code.

