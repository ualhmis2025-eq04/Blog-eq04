---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---
# ✨ Bienvenido al blog de HMIS del equipo 04 ✨

## Nuestro objetivo 

Este blog contendrá información relacionada con las **Herramientas y Métodos de Ingeniería Informática**, con el fin de expandir el conocimiento de las prácticas que sustentan esta disciplina. En los post encontrarás conceptos, técnicas y herramientas esenciales que todo ingeniero informático que se respeta debe conocer. 

## ⭐ Últimos posts 

<ul>
  {% for post in site.posts %}
    <li>
      <strong>{{ post.date | date: "%d-%m-%Y" }}</strong> - 
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>


## ¡Te invitamos a conocernos! ☆*: .｡. o(≧▽≦)o .｡.:*☆
Somos José Miranda Ibáñez y Giovanna Yamile Nuño Rodríguez, estudiantes de Ingeniería Informática apasionados por la tecnología.

Si te interesa saber más de nosotros podrás encontrar información en las páginas individuales dedicadas a los miembros del equipo.