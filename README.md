# Template-Cydia
Repo Cydia Template With Script
<pre>
Este es un Repositorio de Cydia con scripts para facilitar la creacion y actualizacion de la repo.

Requisitos para su uso


Mac OS: (Posiblemente funcione no se anexa guia)

iOS:  iPhone/iPad (Probado en 11.3.1 JB)
* Tweaks : Filza + NewTerm2
* Debe instalar Perl de la repo http://repo.bingner.com/  
* json.pm se encuentra en la carpeta Extra



Debian/Linux: (Cualquier distro deberia funcionar)


Windows 10 Debian Terminal:

En esta ocacion Realice la Guia Bajo Windows 10 Decargando Debian
https://www.microsoft.com/en-us/p/debian-gnu-linux/9msvkqc78pk6?activetab=pivot:overviewtab


Una vez instalado abrimos el terminal de debian y configuramos el usuario y contraseña.

Comandos por Orden:

--------------<b>GUIA</b>-------------------

<b>sudo -s</b>  (Utilizaremos para no estar escribiendo sudo en cada comando)

<b>apt-get update</b> (actualizar lista de paquetes en debian para instalar)

$<b>apt-get install git</b>
$<b>apt-get install git-core</b>
$<b>apt-get install dpkg-dev</b>
$<b>apt-get install bzip2</b>

$<b>mkdir repo</b>
$<b>cd repo</b>
$<b>git clone https://github.com/sharklatan/Template-Cydia</b>



//////////////////<b>opcional</b>//////////////////////


(opcional por si no sabes manejar mucho terminal, demora en instalar)
$<b>apt-get install nautilus</b>

(Instalar complemento Windows para ver ventanas de Linux grafico)
https://sourceforge.net/projects/xming/

cuando instales estos 2 paquetes en la terminal ejecuta estos comando (asegurate de que xming este iniciado)

$<b>export DISPLAY=:0</b>
$<b>nautilus</b>

(con este comando se abrira nautilus que es un explorador para ver carpetas y archivos graficamente y poderlos manipular)


///////////////////////////////


Colocar todos los <b>*.deb</b> debtro de la carpeta deb

ejecutar el comando

$<b>./generar.sh</b>

Este creara los archivos <b>Packages.bz2</b> y <b>Packages</b> en base a los archivos contenidos en deb/*.deb 


$<b>./last_updates.sh</b>
Genera un archivo <b>last.updates</b> que contiene los 5 ultimos paquete.
(Para usarlo necesitara el modulo PP de Perl intenta con el comando $<b>cpan install pp</b>)

