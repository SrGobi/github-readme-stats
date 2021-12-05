<p align="center">
 <h2 align="center">Estadísticas Léame de GitHub</h2>
 <p align="center">¡Obtenga estadísticas de GitHub generadas dinámicamente en sus archivos Léame!</p>

# GitHub Stats Card

Copie y pegue esto en su contenido de rebajas, y eso es todo. ¡Sencillo!

Cambiar el `?username=` valor al nombre de usuario de tu GitHub.

```md
[![Anurag's GitHub stats](https://github-readme-stats.vercel.app/api?username=SrGobi)](https://github.com/SrGobi/github-readme-stats)
```

_Nota: Los rangos disponibles son S + (1% superior), S (25% superior), A ++ (45% superior), A + (60% superior) y B + (todos).
Los valores se calculan utilizando el [cumulative distribution function](https://en.wikipedia.org/wiki/Cumulative_distribution_function) utilizando confirmaciones, contribuciones, problemas, estrellas, solicitudes de extracción, seguidores y repositorios propios.
La implementación se puede investigar en [src/calculateRank.js](./src/calculateRank.js)_

### Ocultar estadísticas individuales

Para ocultar estadísticas específicas, puede pasar un parámetro de consulta `?hide=` con valores separados por comas.

> Opciones: `&hide=stars,commits,prs,issues,contribs`

```md
![SrGobi GitHub stats](https://github-readme-stats.vercel.app/api?username=SrGobi&hide=contribs,prs)
```

### Agregar el recuento de contribuciones privadas al recuento total de confirmaciones

Puede agregar el recuento de todas sus contribuciones privadas al recuento total de confirmaciones utilizando el parámetro de consulta `?count_private=true`.

_Nota: Si está implementando este proyecto usted mismo, las contribuciones privadas se contarán de forma predeterminada; de lo contrario, debe elegir compartir sus recuentos de contribuciones privadas._

> Opciones: `&count_private=true`

```md
![SrGobi GitHub stats](https://github-readme-stats.vercel.app/api?username=SrGobi&count_private=true)
```

### Mostrando iconos

Para habilitar iconos, puede pasar `show_icons = true` en el parámetro de consulta, así:

```md
![SrGobi GitHub stats](https://github-readme-stats.vercel.app/api?username=SrGobi&show_icons=true)
```

### Temas

Con temas incorporados, puede personalizar el aspecto de la tarjeta sin hacer nada [manual customization](#personalización).

Usa `?theme=THEME_NAME` parámetro así :-

```md
![SrGobi GitHub stats](https://github-readme-stats.vercel.app/api?username=SrGobi&show_icons=true&theme=radical)
```

#### Todos los temas incorporados :-

dark, radical, merko, gruvbox, tokyonight, onedark, cobalt, synthwave, highcontrast, dracula

<img src="https://res.cloudinary.com/SrGobi/image/upload/v1595174536/grs-themes_l4ynja.png" alt="GitHub Readme Stats Themes" width="600px"/>

Puede ver una vista previa de [all available themes](./themes/README.md) o echa un vistazo al [theme config file](./themes/index.js) & **también puedes contribuir con nuevos temas** si quieres :D

### Personalización

Puede personalizar la apariencia de su `Stats Card` or `Repo Card` como quieras con los parámetros de URL.

#### Opciones comunes:

- `title_color` - Color del título de la tarjeta _(hex color)_
- `text_color` - Color del texto del cuerpo _(hex color)_
- `icon_color` - Color de los iconos si está disponible _(hex color)_
- `bg_color` - Color de fondo de la tarjeta _(hex color)_ **o** un degradado en forma de _angle,start,end_
- `hide_border` - Oculta el borde de la tarjeta _(boolean)_
- `theme` - nombre del tema, elija entre [all available themes](./themes/README.md)
- `cache_seconds` - configurar el encabezado de la caché manualmente _(min: 1800, max: 86400)_
- `locale` - configurar el idioma en la tarjeta _(e.g. cn, de, es, etc.)_

##### Degradado en bg_color

Puede proporcionar varios valores separados por comas en la opción bg_color para representar un degradado, el formato del degradado es :-

```
&bg_color=DEG,COLOR1,COLOR2,COLOR3...COLOR10
```

> Nota sobre el caché: las tarjetas Repo tienen un caché predeterminado de 4 horas (14400 segundos) si el recuento de bifurcaciones y el recuento de estrellas es inferior a 1k; de lo contrario, son 2 horas (7200 segundos). Además, tenga en cuenta que la caché está sujeta a un mínimo de 2 horas y un máximo de 24 horas.

#### Opciones exclusivas de la tarjeta de estadísticas:

- `hide` - Oculta los elementos especificados de las estadísticas _(Comma-separated values)_
- `hide_title` - _(boolean)_
- `hide_rank` - _(boolean)_ oculta el rango y cambia automáticamente el tamaño del ancho de la tarjeta
- `show_icons` - _(boolean)_
- `include_all_commits` - Cuente las confirmaciones totales en lugar de solo las confirmaciones del año actual _(boolean)_
- `count_private` - Contar confirmaciones privadas _(boolean)_
- `line_height` - Establece la altura de la línea entre el texto. _(number)_
- `custom_title` - Establece un título personalizado para la tarjeta
- `disable_animations` - Desactiva todas las animaciones de la tarjeta. _(boolean)_

#### Opciones exclusivas de la tarjeta Repo:

- `show_owner` - Muestra el nombre del propietario del repositorio _(boolean)_

#### Opciones exclusivas de la tarjeta de idioma:

- `hide` - Ocultar los idiomas especificados de la tarjeta _(Comma-separated values)_
- `hide_title` - _(boolean)_
- `layout` - Cambiar entre dos diseños disponibles `predeterminado` y `compacto`
- `card_width` - Establecer el ancho de la tarjeta manualmente _(number)_
- `langs_count` - Mostrar más idiomas en la tarjeta, entre 1 y 10, el valor predeterminado es 5 _(number)_
- `exclude_repo` - Excluir repositorios especificados _(Comma-separated values)_
- `custom_title` - Establece un título personalizado para la tarjeta

> :warning: **Importante:**
> Los nombres de los idiomas deben tener un escape de uri, como se especifica en [Percent Encoding](https://en.wikipedia.org/wiki/Percent-encoding)
> (i.e: `c++` debe convertirse `c%2B%2B`, `jupyter notebook` debería convertirse `jupyter%20notebook`, etc.) Puedes usar
> [urlencoder.org](https://www.urlencoder.org/) para ayudarlo a hacer esto automáticamente.

#### Opciones exclusivas de la tarjeta Wakatime:

- `hide_title` - _(boolean)_
- `line_height` - Establece la altura de la línea entre el texto. _(number)_
- `hide_progress` - Oculta la barra de progreso y el porcentaje _(boolean)_
- `custom_title` - Establece un título personalizado para la tarjeta
- `layout` - Cambiar entre dos diseños disponibles `predeterminado` y` compacto`
- `api_domain` - Establecer un dominio de API personalizado para la tarjeta

---

# Pines adicionales de GitHub

Los pines adicionales de GitHub le permiten anclar más de 6 repositorios en su perfil usando un perfil Léame de GitHub.

¡Hurra! Ya no está limitado a 6 repositorios anclados.

### Uso

Copie y pegue este código en su archivo Léame y cambie los enlaces.

Endpoint: `api/pin?username=SrGobi&repo=github-readme-stats`

```md
[![Readme Card](https://github-readme-stats.vercel.app/api/pin/?username=SrGobi&repo=github-readme-stats)](https://github.com/SrGobi/github-readme-stats)
```

### Demo

[![Readme Card](https://github-readme-stats.vercel.app/api/pin/?username=SrGobi&repo=github-readme-stats)](https://github.com/SrGobi/github-readme-stats)

Use [show_owner](#personalización) variable para incluir el nombre de usuario del propietario del repositorio

[![Readme Card](https://github-readme-stats.vercel.app/api/pin/?username=SrGobi&repo=github-readme-stats&show_owner=true)](https://github.com/SrGobi/github-readme-stats)

# Tarjeta de idiomas principales

La tarjeta de idiomas principales muestra los idiomas principales de un usuario de GitHub que más se han utilizado.

_NOTA: Top Languages no indica mi nivel de habilidad ni nada por el estilo, es una métrica de GitHub de qué idiomas tienen más código en GitHub. Es una nueva característica de github-readme-stats._

### Uso

Copie y pegue este código en su archivo Léame y cambie los enlaces.

Endpoint: `api/top-langs?username=SrGobi`

```md
[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=SrGobi)](https://github.com/SrGobi/github-readme-stats)
```

### Excluir repositorios individuales

Puedes usar `?exclude_repo=repo1,repo2` parámetro para excluir repositorios individuales.

```md
[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=SrGobi&exclude_repo=github-readme-stats,SrGobi.github.io)](https://github.com/SrGobi/github-readme-stats)
```

### Hide individual languages

You can use `?hide=language1,language2` parameter to hide individual languages.

```md
[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=SrGobi&hide=javascript,html)](https://github.com/SrGobi/github-readme-stats)
```

### Mostrar más idiomas

Puedes usar el `&langs_count=` opción para aumentar o disminuir el número de idiomas que se muestran en la tarjeta. Los valores válidos son números enteros entre 1 y 10 (inclusive) y el valor predeterminado es 5.

```md
[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=SrGobi&langs_count=8)](https://github.com/SrGobi/github-readme-stats)
```

### Diseño de tarjeta de idioma compacto

Puede utilizar la opción `& layout = compact` para cambiar el diseño de la tarjeta.

```md
[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=SrGobi&layout=compact)](https://github.com/SrGobi/github-readme-stats)
```

### Demo

[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=SrGobi)](https://github.com/SrGobi/github-readme-stats)

- Disposición compacta

[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=SrGobi&layout=compact)](https://github.com/SrGobi/github-readme-stats)

# Estadísticas de la semana de Wakatime

Cambie el valor `? Username =` por su [Wakatime](https://wakatime.com) username.

```md
[![SrGobi's wakatime stats](https://github-readme-stats.vercel.app/api/wakatime?username=srgobi)](https://github.com/SrGobi/github-readme-stats)
```

### Demo

[![SrGobi's wakatime stats](https://github-readme-stats.vercel.app/api/wakatime?username=srgobi)](https://github.com/SrGobi/github-readme-stats)

[![SrGobi's wakatime stats](https://github-readme-stats.vercel.app/api/wakatime?username=srgobi&hide_progress=true)](https://github.com/SrGobi/github-readme-stats)

- Disposición compacta

[![SrGobi's wakatime stats](https://github-readme-stats.vercel.app/api/wakatime?username=srgobi&layout=compact)](https://github.com/SrGobi/github-readme-stats)

---

### Todas las demostraciones

- Defecto

![SrGobi's GitHub stats](https://github-readme-stats.vercel.app/api?username=SrGobi)

- Ocultar estadísticas específicas

![SrGobi's GitHub stats](https://github-readme-stats.vercel.app/api?username=SrGobi&hide=contribs,issues)

- Mostrando iconos

![SrGobi's GitHub stats](https://github-readme-stats.vercel.app/api?username=SrGobi&hide=issues&show_icons=true)

- Incluir todas las confirmaciones

![SrGobi's GitHub stats](https://github-readme-stats.vercel.app/api?username=SrGobi&include_all_commits=true)

- Temas

Elija entre cualquiera de los [default themes](#temas)

![SrGobi's GitHub stats](https://github-readme-stats.vercel.app/api?username=SrGobi&show_icons=true&theme=radical)

- Degradado

![SrGobi's GitHub stats](https://github-readme-stats.vercel.app/api?username=SrGobi&bg_color=30,e96443,904e95&title_color=fff&text_color=fff)

- Personalizar la tarjeta de estadísticas

![SrGobi's GitHub stats](https://github-readme-stats.vercel.app/api/?username=SrGobi&show_icons=true&title_color=fff&icon_color=79ff97&text_color=9f9f9f&bg_color=151515)

- Configuración de la configuración regional de la tarjeta

![SrGobi's GitHub stats](https://github-readme-stats.vercel.app/api/?username=SrGobi&locale=es)

- Personalización de la tarjeta de repositorio

![Customized Card](https://github-readme-stats.vercel.app/api/pin?username=SrGobi&repo=github-readme-stats&title_color=fff&icon_color=f9f9f9&text_color=9f9f9f&bg_color=151515)

- Idiomas principales

[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=SrGobi)](https://github.com/SrGobi/github-readme-stats)

- Tarjeta de Wakatime

[![SrGobi wakatime stats](https://github-readme-stats.vercel.app/api/wakatime?username=srgobi)](https://github.com/SrGobi/github-readme-stats)

---

### Sugerencia rápida (alinear las tarjetas de repositorio)

Por lo general, no podrá diseñar las imágenes una al lado de la otra. Para hacer eso, puede utilizar este enfoque:

```md
<a href="https://github.com/SrGobi/github-readme-stats">
  <img align="center" src="https://github-readme-stats.vercel.app/api/pin/?username=SrGobi&repo=github-readme-stats" />
</a>
<a href="https://github.com/SrGobi/convoychat">
  <img align="center" src="https://github-readme-stats.vercel.app/api/pin/?username=SrGobi&repo=convoychat" />
</a>
```

## :sparkling_heart: Apoya el proyecto

Utilizo código abierto en casi todo lo que puedo y trato de responder a todos los que necesitan ayuda para usar estos proyectos. Obviamente,
esto lleva tiempo. Puede utilizar este servicio de forma gratuita.

Sin embargo, si está utilizando este proyecto y está satisfecho con él o simplemente quiere animarme a seguir creando cosas, hay algunas formas de hacerlo. :-

- Dar el crédito adecuado cuando usa github-readme-stats en su archivo Léame, vinculándolo de nuevo :D
- Protagonizar y compartir el proyecto :rocket:

Gracias! :heart:

---

Las contribuciones son bienvenidas! <3

Hecho con :heart: y JavaScript.
