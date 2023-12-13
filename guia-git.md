# Guia de Git

Bienvenido al maravilloso mundo de git, espero que aprendas a utilizar una de las herramientas más importantes del mundo del desarrollo de software con esta pequeña guia casera.

Si tienes curiosidad, antes de empezar con lo bueno te recomiento algo de contexto sobre que es git y de donde viene ya que todo aquello que aprendemos a hacer con contexto lo entendemos mejor.

[Página de wikipedia de Git](https://es.wikipedia.org/wiki/Git)

[Guía de Git de la empresa Atlassian](https://www.atlassian.com/es/git/tutorials/what-is-version-control)

[Git explicado en 100 segundos](https://www.youtube.com/watch?v=hwP7WQkmECE)

> Una advertencia antes de continuar, esto es una guia simplificada y que no te enseñara todo lo que este software te permite hacer, la idea de esto es que empieces a usarlo no que seas un experto. Una vez completada toda la guía si quieres saber más habrá otros recursos a tu disposición.

## Instalación de Git
Antes de poder usar nada debemos instalar el software necesario, en el caso de Git tenemos la página del propio software para adquirirlo. Ten en cuenta que este es un software del tipo *free and open source* lo que implica que es gratuito y mantenido por la comunidad sin animo de lucro. Como curiosidad también te diré que su creador es el famoso Linus Torvalds, creador del kernel de linux.

[Página web de Git](https://git-scm.com/).

En la propia página te vienen instrucciones concretas para instalarlo tengas el OS que tengas. En el caso de windows es con el clasico ejecutable, en MacOS se puede instalar con homebrew y en Linux esta disponible en distintos package managers.

En el caso de windows tienes la posibilidad de instalar tambien Git Bash que sería una interfaz para linea de comandos que esta interesante aunque yo personalmente no la uso demasiado.

Una vez instalado te recomiendo que reinicies y despues hagas la clasica comprobación mediante la consola con el comando `git -v`.

## Primeros pasos en Git
El primer paso que creo que debes tomar es crear una cuenta en alguno de los principales servicios de repositorios en la nube que usan Git. Personalmente te recomiendo GitHub (Propiedad de Microsoft) o GitLab (Open source).

- GitHub es la más grande de las dos, donde están la mayoría de proyectos open source y donde se mueve la mayoría de la gente. Tiene infinidad de herramientas para desarrollar tus proyectos y participar en proyectos open source. Personalmente creo que actualmente es indispensable tener una cuenta de GitHub.

- GitLab es la opción open source, más pequeña pero más cuidada, esta enfocada a un usuario más especializado y que busca tener más control y herramientas especializadas para mantener repositorios. Una opción muy valida sobre todo de cara a proyectos más serios y que requieren más cuidado.

Una vez tomada la decisión es hora de empezar a usar Git y tomar esos primeros pasos es super facil. Lo primero que necesitas es crear una carpeta en tu sistema. Después debes decidir si hacer todo mediante la consola de comandos o la interfaz grafica que incluyen la mayoría de IDEs o editores de texto enfocados al desarrollo como es Visual Studio Code (herramienta que por cierto es la que he usado para crear esta guía).

Antes de continuar hay que hacer una pequeña configuración desde la linea de comandos. Abre tu consola y escribe los siguientes comandos cambiando los datos entre comillas dobles por tu mail y usuario que utilices en la plataforma en la quieras guardar tus repositorios (si vas a usar más de una plataforma no incluyas --global):

- `git config --global user.email "you@example.com"`
- `git config --global user.name "Your Name"`

> Si todo ha salido bien no saldrá ningun mensaje, solo saltara otra linea en la consola.

Si eres nuevo en este mundo de la programación y no te sientes comodo con el uso de comandos puedes empezar con la interfaz y con el tiempo, cuando ganes comfianza empezar a usar comandos.

**Para hacer esta guía voy a hacerlo todo en el entorno VS Code con GitHub ya que al ser ambos propiedad de Microsoft son la opción que menos fallos suele dar y la mejor para familiarizarse con la herramienta.**

## Uso de la GUI

### Creación del repositorio mediante GUI

Para crear el repositorio solamente debemos acudir al apartado especifico para ello. En el caso de VS Code lo encontraremos en la barra lateral, se trata de un simbolo con un circulo inferior del que parten dos lineas que se unen a otros dos circulos en la parte superior. En dicho apartado nos saldra una ventana similar a esta.

![img-interfaz-vsc](https://imageshack.com/i/pn48dljZp)

Desde aquí, simplemente pulsando en Iniciar repositorio podemos crear el primer repositorio de git y ya estaría, ya hemos creado nuestro primer repositorio git, el sistema automaticamente detectara todos los archivos que estan incluidos en la carpeta origen del repositorio y te los mostrara en el apartado cambios, si son nuevos, vendran con una U verde a la derecha, si ya existen y van a ser actualizados con una M naranja y si van a ser borrados con una D roja. 

![img-interfaz2-vsc](https://imageshack.com/i/pn85t7ZQp)

Cuando tengamos todos los archivos que queremos subir en ese apartado cambios debemos escribir un mensaje que sera un pequeño resumen de lo que vamos a incluir en el commit que realizaremos y podemos darle a confirmación.

![img-stage-changes](https://imageshack.com/i/poF4x0mZp)

Es posible que nos pida dar permisos para el servicio que usemos (GitHub en el caso de este ejemplo), autorizamos y elegimos si deseamos que el repositorio sea publico o privado y ya esta, hemos publicado nuestro primer repositorio git. Ahora es el momento de empezar a compartir nuestro trabajo con el mundo.

![img-public-private-repo](https://imageshack.com/i/pmf403zYp)

### Como clonar y aportar a un repositorio

Después de crear un repositorio lo siguiente que se puede trabajar es clonar el de otra persona para tener acceso a ese repositorio y así aprovechar su trabajo o aportar tu granito de arena y hacer que sea todavía mejor. Para clonarlo debemos ir a la página del repositorio en GitHub donde se muestra una página similar a esta. Aquí podemos ver toda la información del repositorio, desde que contiene a cuanta gente lo ha guardado, cuantos han hecho un fork para trabajar sobre él, hace cuanto se creo y cuando fue la última modificación y el README.md que sería la carta de presentación del repositorio con su explicaicón, resumen e instrucciones para participar. 

Aquí la interfaz da la opción de entre otras cosas, crear una nueva rama que sería una copia del repositorio en un momento concreto en la cual podemos trabajar, podremos descargar el código al sistema para trabajarlo desde ahí, crear un fork que sería copiar todo el repositorio en nuestro perfil de GitHub para gestionarlo desde allí y demás opciones. Por ahora centremos la atención en el botón grande y verde con el texto Code que nos invita a ser pulsado.

![img-github-repo-page](https://imageshack.com/i/pmZOpjGvp)

Este botón despliega un menu con dos pestañas, local y codespaces. Codespaces permite trabajar en un editor online de VS Code dentro de GitHub pero en la que me centrare será Local ya que permite clonar el repositorio en el equipo.

En Local se muestran varias opciones, las más importantes son la primera, clone, y download ZIP. Si usas Visual Studio (el del entorno .net, no VS Code) tambien puede ser util la opcion open with Visual Studio que abre la aplicación y permite realizar la clonación directamente desde ahí.

El apartado clone muestra 3 pestañas HTTPS/SSH/Github CLI: 
- La primera ofrece el link que permite clonar el repositorio mediante la consola. 
- SSH permite hacer una copia usando una clave que se puede generar desde el apartado settings del perfil de GitHub, esta opción puede ser necesaria en entornos MacOS y Linux. 
- Por último GitHub CLI permite la copia mediante la interfaz de comandos de GitHub (yo personalmente nunca he usado esta opción).

![pestanya-code](https://imageshack.com/i/pmZNgRR7p)

Para clonar el repositorio en el equipo copiamos este link HTTPS, ir a la CLI e introducir el siguiente comando: `git clone <link https>`, pulsamos enter y el sistema nos generara todos los archivos necesarios.

![cli-clone](https://imageshack.com/i/pnnUqs0ip)

**IMPORTANTE**

**Muchos repositorios usan recursos externos que hay que instalar para trabajar en ellos, recuerda  siempre la documentación antes de empezar a trabajar.**

Y con esto ya puedes empezar a trabajar con repositorios publicos y empezar a colaborar con el mundo.

## Uso de la CLI

### Creación del repositorio mediante CLI