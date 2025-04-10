---
layout: post
title:  "¿Sabes usar Git?"
date:   2025-03-25 22:09:46 +0100
---

Git es una de las herramientas más utilizadas por desarrolladores de todo el mundo… y también una de las más temidas. Aunque casi todos lo usan a diario, **pocos entienden realmente cómo funciona por dentro**. Se vuelve una especie de caja negra: escribimos comandos que "mágicamente" sincronizan o guardan cambios, pero sin saber bien qué está ocurriendo en realidad.

El problema no es Git. Es que nunca nos explicaron cómo pensar Git.

La buena noticia es que **no necesitas saberlo todo para usarlo bien**. Solo hace falta entender unos conceptos clave y cómo interactúan entre sí. Con eso, tus proyectos serán más organizados, tus errores menos catastróficos y tu trabajo en equipo mucho más fluido.

<br>

## ¿Qué es un sistema de control de versiones?

Un sistema de control de versiones es como una **máquina del tiempo para tu código**. Permite:

- Registrar el historial de cambios.
- Volver a estados anteriores si algo sale mal.
- Comparar versiones y ramas.
- Trabajar en paralelo con otras personas y unificar cambios.

Git es un sistema de control de versiones **distribuido**, lo que significa que cada persona tiene una copia completa del repositorio (incluido el historial completo). Esto permite trabajar sin conexión y tener mucha más flexibilidad y seguridad que otros sistemas centralizados.

<br>

## El flujo de trabajo interno de Git

Para entender cómo trabaja Git, primero hay que conocer las tres áreas que conforman su flujo de trabajo:

1. **Directorio de trabajo (Working Directory):** Es donde haces cambios reales en los archivos del proyecto.
2. **Área de preparación (Staging Area o Index):** Aquí seleccionas los cambios que quieres incluir en el próximo commit.
3. **Repositorio (Git Directory):** Es la base de datos interna donde Git guarda el historial de versiones.

Este diseño permite mucha precisión: puedes modificar varios archivos y solo preparar algunos, o incluso porciones específicas de un archivo, para ser guardados.

<br>

![Flujo Git](/docs/assets/git-flow.png)

<br>

## Repositorios locales y remotos

**Repositorio local:** 

Es tu copia personal del proyecto. Contiene el historial completo y es totalmente funcional sin necesidad de estar conectado a internet.

**Repositorio remoto:** 

Es una copia central (habitualmente alojada en plataformas como GitHub, GitLab o Bitbucket), utilizada para colaborar y compartir los cambios.

<br>

Cuando clonas un repositorio remoto, Git crea una conexión que te permite sincronizar los cambios entre ambos mediante comandos como *push* y *pull*.

<br>

## **Los tres comandos clave**

### 1. *COMMIT* - Guardar tus cambios en el historial

**git commit** registra una "foto" de los archivos preparados. Pero para que eso ocurra, primero necesitas mover tus archivos desde el estado "modificado" al área de preparado usando **git add**.

#### Estados posibles de un archivo:

**Modificado (modified) -** Lo cambiaste, pero Git aún no lo considera listo para guardar.

**Preparado (staged) -** Usaste git add y ahora Git sabe que debe incluirlo en el próximo commit.

**Commiteado (committed) -** Ya está registrado en el historial.

**Sin modificar (unmodified) -** No ha cambiado desde el último commit.

Un flujo típico:

```bash
git add .                           # Todos los cambios pasan a estar staged
git commit -m "Mi primer commit!"   # Se guardan dichos cambios en el historial
```
<br>

### 2. *PUSH* - Subir tus cambios al remoto

Cuando haces un commit, ese cambio **solo está en tu máquina**. Para compartirlo con tu equipo, necesitas hacer un **git push**.

#### ¿Qué pasa internamente?

- Git verifica qué commits nuevos tienes en tu rama local.
- Se conecta con el repositorio remoto (por defecto llamado **origin**).
- Actualiza la rama remota para que apunte al mismo commit que tu rama local.

**HEAD** es un puntero que indica el último commit de la rama actual. Cuando haces push, estás diciendo: “actualiza la rama remota para que su HEAD apunte al mismo commit que mi HEAD”.

**Origin** es el nombre por defecto que Git le da al remoto desde el que clonaste el proyecto. Puedes tener varios remotos, pero origin suele ser el principal.

<br>

### 3. *PULL* - Traer los cambios del remoto a tu máquina

**git pull** es el comando que **sincroniza tu repositorio local** con el remoto, trayendo los commits nuevos que otros hayan subido.

Pero para entenderlo bien, primero hay que conocer dos formas en que Git puede "unir" esos cambios:
<br>

### *git merge* vs *git rebase*

| Git Merge                                         | Git Rebase                                              |
|--------------------------------------------------|---------------------------------------------------------|
| Une dos ramas y crea un commit de fusión         | Reescribe la historia para que tus commits parezcan los últimos |
| Mantiene el historial completo                   | Crea un historial más lineal y limpio                   |
| Ideal para proyectos compartidos                 | Ideal para ramas personales antes de hacer push        |

<br>

![rebase vs merge](/docs/assets/rebase-merge.png)

<br>

Cuando haces **git pull**, Git por defecto hace un **merge**. Pero puedes configurarlo para que use **rebase**, si prefieres evitar los commits de fusión innecesarios.

<br>

## ¡Ahora sabes un poco más de Git!
¿Antes sabías cómo funcionaba? Puede que sí, o puede que ahora entiendas todo mucho mejor. 

Te invitamos a probar por tu propia mano el funcionamiento de esta poderosa herramienta, entender Git cambia por completo tu experiencia como desarrollador. No se trata solo de memorizar comandos, sino de entender cómo interactúan.

Dominar estos conceptos te dará más control y confianza al momento de trabajar en tus proyectos, tanto solo como en equipo. Y como puedes observar, es más sencillo de lo que parece. 

¡Bienvenido al mundo de Git! ヾ(≧▽≦*)o
