# P1-Comandos-de-Docker
Crea un novo repositorio público en git, coo nome da tarefa, clónao e engade un arquivo readme2.md en local que poña unha frase á túa elección.

Para facer este punto se ha creado dende github un repositorio público co nome de "P1-Comandos-de-Docker", logo dende a nosa consola de comandos realizaremos a clonación con `git clone...`.
Para añadir un arquivo chamado readme2.md entramos na nosa carpeta có comando `cd`, posteriormente un `echo` e redireccionamos a salida ao noso ficheriro readme2.md.
i 
Facendo uso de VScode, Docker e a imaxe de ubuntu da práctica anterior, describe no arquivo readme.md, cun formato claro, os pasos e comandos para:
1. Descargar e comprobar que unha imaxe está no teu equipo

No meus caso quixen descargar a imaxe nginx, para realizalo na terminal de VSCode utilicei o comando `docker pull nginx`.
Posteriormente para a comprobación das novas imaxes o comando é `docker images`. 

2. Crear un contenedor sen nome, queda arrincado?, cómo obtés o nome?

Para crear un contenedor sen nome escribimos `docker run -d nginx` neste caso nginx xa que é a imaxe selecionada, noutro caso escribiriamos a imaxe en cuestión. Sí que queda arrincado xa que por defecto docker asiganlle un nome a cada un dos contenedores sen a necesidade de ter que darlle un anterior á creación, para obter o seu nome utilziamos o comando `docker ps -a` dende a terminal ou ven imos ao apartado de docker de VSCode e vemos o nome dado ao contenedor.

3. Crea un contenedor coo nome 'u1', cómo accedes a el?

Para crear un contenedor cun nome definido polo usuario añadiremos --name ao comando do punto anterior. O comando quedaría da seguinte forma `docker run -d --name u1 nginx`.
Para acceder a este contenedor poderemos facelo de dúas formas. A primeira a través da nosa terminal executando o comando `docker exec -it u1 /bin/bash` ou por outro lado facendo click dereito sobre o noso contenedor en VSCode e seleccionando "Attach shell"

4. Comproba a súa ip e fai ping a google.com

Este proceso levouse a cabo a través da terminal de VSCode polo que tivemos alguns fallos que houbo que solucionar. Para solucionalos instalaronse certas ferramentas ou aplicacións para poder mirar o contenido de rede do noso equipo e poder facer o ping.
O primeiro comando utilizado é `apt install -y net-tools` este é un conxunto de ferramentas para a administración de red do equipo, contiene utilidades como: ifconfig, route, netstat, arp, ... O seguinte comando utilizado é `apt install -y iputils-ping` para instalar o ping no noso sistema de pruebas de Ubuntu. Tamén se levou a cabo un `apt update` anterior á instalación das dúas ferramentas anteriores.
Unha vez feito o anterior para comprobar sua IP utilizamos o comando `ifconfig` y para facer o ping `ping google.com`.

5. Crea un contenedor coo nome 'bono', pódes facer ping entre os contenedores?

Para crear un contenedor co nome dado executaremos o comando `docker run -d --name bono nginx`.
Para facer ping entre os contenedores creados utilizamos o comando `ping (IP do outro contenedor)`, estos se comunican se están na misma red.

6. Se pechas as terminales, qué pasa coo contenedor?

Se pechamos as terminales o contenedor sigue en funcionamento, non inflúe no seu estado.

7. Cánta memoria no disco duro ocupaches? usa docker para calculalo

Para calcular a memoria executaremos o comando `docker system df` é nos mostrará o tamaño das imaxes, contenedores... A memoria ocupada no meu disco duro é de 426,3 MB

8. Cánta RAM ocupan os contenedores? Crea varios para calculalo

Para revisar canta RAM ocupan os contenedor utilizaremos o comando `docker stats`, no meu caso ocupa 0,1%.

9. Cómo fixeches para clonar o repositorio

Para a clonacion dun repositorio utilizaremos o comando `git clone (direción do repositorio)`.

10. Cómo engades o arquivo readme2.md

Para añadir o arquivo "readme2.md" primeiro añadiremolo ao directorio do repositorio e posteriormente executaremos o comando `git add -A readme2.md`.

11. Os pasos a seguir para subir o arquivo que estás editando e o arquivo readme2.md

Primeiro de todo faremos o punto nº10. Posteriormente faremos un `git add` para gardar os cambios feitos logo `git commit` e por ultimo un `git push` para subir o arquivo. 

12. Cómo comprobarías que existen diferencias entre o teu repositorio local e o remote.



