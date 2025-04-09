---
layout: default
---
# ⭐ **Bienvenido al blog de HMIS del equipo 04** ⭐

<br>

## Nuestro objetivo

Este blog contendrá información relacionada con **Herramientas y Métodos de Ingeniería Informática**, con el fin de expandir el conocimiento de las prácticas que sustentan esta disciplina. En los post encontrarás conceptos, técnicas y herramientas esenciales que todo ingeniero informático que se respeta debe conocer.
 
<br>

# ✨ Últimos posts ✨

<ul style="list-style-type: none; padding: 0;">
  {% for post in site.posts %}
    <li style="margin-bottom: 10px; padding-bottom: 10px; border-bottom: 1px solid rgba(0, 0, 0, 0.1);">
      <a href="{{ post.url }}" style="font-size: 1.5em; font-weight: bold;">{{ post.title }}</a>
      <p style="font-style: italic;">Fecha de publicación: {{ post.date | date: "%d/%m/%Y" }}</p>
    </li>
  {% endfor %}
</ul>

<br>

## ¡Te invitamos a conocernos! ☆*: .｡. o(≧▽≦)o .｡.:*☆
Somos José Miranda Ibáñez y Giovanna Yamile Nuño Rodríguez, estudiantes de Ingeniería Informática apasionados por la tecnología. Nos puedes encontrar bajo los nombres de usuario jmi240 y gnr267. 

Si te interesa saber más de nosotros podrás encontrar información en las páginas individuales dedicadas a los miembros del equipo.