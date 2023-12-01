# Guia de Git

> Bienvenido al maravilloso mundo de git, espero que aprendas a utilizar una de las herramientas más importantes del mundo del desarrollo de software con esta pequeña guia casera.

> Si tienes curiosidad, antes de empezar con lo bueno te recomiento algo de contexto sobre que es git y de donde viene ya que todo aquello que aprendemos a hacer con contexto lo entendemos mejor.

> [Página de wikipedia de Git](https://es.wikipedia.org/wiki/Git)

> [Guía de Git de la empresa Atlassian](https://www.atlassian.com/es/git/tutorials/what-is-version-control)

> [Git explicado en 100 segundos](https://www.youtube.com/watch?v=hwP7WQkmECE)

> Una advertencia antes de continuar, esto es una guia simplificada y que no te enseñara todo lo que este software te permite hacer, la idea de esto es que empieces a usarlo no que seas un experto. Una vez completada toda la guía si quieres saber más habrá otros recursos a tu disposición.

## Instalación de Git
> Antes de poder usar nada debemos instalar el software necesario, en el caso de Git tenemos la página del propio software para adquirirlo. Ten en cuenta que este es un software del tipo *free and open source* lo que implica que es gratuito y mantenido por la comunidad sin animo de lucro. Como curiosidad también te diré que su creador es el famoso Linus Torvalds, creador del kernel de linux.

> [Página web de Git](https://git-scm.com/).

> En la propia página te vienen instrucciones concretas para instalarlo tengas el OS que tengas. En el caso de windows es con el clasico ejecutable, en MacOS se puede instalar con homebrew y en Linux esta disponible en distintos package managers.

> En el caso de windows tienes la posibilidad de instalar tambien Git Bash que sería una interfaz para linea de comandos que esta interesante aunque yo personalmente no la uso demasiado.

> Una vez instalado te recomiendo que reinicies y despues hagas la clasica comprobación mediante la consola con el comando `git -v`.

## Primeros pasos en Git
> El primer paso que creo que debes tomar es crear una cuenta en alguno de los principales servicios de repositorios en la nube que usan Git. Personalmente te recomiendo GitHub (Propiedad de Microsoft) o GitLab (Open source).

- GitHub es la más grande de las dos, donde están la mayoría de proyectos open source y donde se mueve la mayoría de la gente. Tiene infinidad de herramientas para desarrollar tus proyectos y participar en proyectos open source. Personalmente creo que actualmente es indispensable tener una cuenta de GitHub.

- GitLab es la opción open source, más pequeña pero más cuidada, esta enfocada a un usuario más especializado y que busca tener más control y herramientas especializadas para mantener repositorios. Una opción muy valida sobre todo de cara a proyectos más serios y que requieren más cuidado.

> Una vez tomada la decisión es hora de empezar a usar Git y tomar esos primeros pasos es super facil. Lo primero que necesitas es crear una carpeta en tu sistema. Después debes decidir si hacer todo mediante la consola de comandos o la interfaz grafica que incluyen la mayoría de IDEs o editores de texto enfocados al desarrollo como es Visual Studio Code (herramienta que por cierto es la que he usado para crear esta guía).

> Antes de continuar hay que hacer una pequeña configuración desde la linea de comandos. Abre tu consola y escribe los siguientes comandos cambiando los datos entre comillas dobles por tu mail y usuario que utilices en la plataforma en la quieras guardar tus repositorios (si vas a usar más de una plataforma no incluyas --global):

- git config --global user.email "you@example.com"
- git config --global user.name "Your Name"

> Si eres nuevo en este mundo de la programación y no te sientes comodo con el uso de comandos puedes empezar con la interfaz y con el tiempo, cuando ganes comfianza empezar a usar comandos.

### Creación del repositorio mediante GUI
> Para crear el repositorio solamente debemos acudir al apartado especifico para ello. En el caso de VS Code lo encontraremos en la barra lateral, se trata de un simbolo con un circulo inferior del que parten dos lineas que se unen a otros dos circulos en la parte superior. En dicho apartado nos saldra una ventana similar a esta.

![img-interfaz-vsc](https://imageshack.com/i/pn48dljZp)

> Desde aquí, simplemente pulsando en Iniciar repositorio podemos crear el primer repositorio de git y ya estaría, ya hemos creado nuestro primer repositorio git, el sistema automaticamente detectara todos los archivos que estan incluidos en la carpeta origen del repositorio y te los mostrara en el apartado cambios, si son nuevos, vendran con una U verde a la derecha. 

>Cuando tengamos todos los archivos que queremos subir en ese apartado cambios debemos escribir un mensaje que sera un pequeño resumen de lo que vamos a incluir en el commit que realizaremos y podemos darle a confirmación.

![img-interfaz2-vsc](https://imageshack.com/i/pn85t7ZQp)
![img-stage-changes](https://imageshack.com/i/poF4x0mZp)

### Creación del repositorio mediante CLI