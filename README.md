# linuxmin multimedia edition
## Distribución live/instalable para música
### ¡¡¡ última versión 25/feb/2024 !!!
### ¡¡¡En breve video explicativo !!!

 Con configuración para rendimiento, personalización y utilidades para música, plugins vst/lv2, con samples sfz e impulse responses gratuitos, esenciales y de calidad.
> - Componentes: Openbox, slim, lxpanel, xterm, pcmanfm, featherpad, firefox, pcmanfm como root, wifi manager, botones: cerrar sesión, reiniciar y apagar.
> - Personalización, temas y aspecto
> - Slim (inicio de sesión): Escritorio Linuxmin o Openbox pulsando tecla F1
> - Repositorios Debian, Kxstudio y paquetes individuales.
> - Qasmixer (mixer), nm-applet (red)
> - Kernel RT y rtirq (rendimiento para audio) y jack iniciado en el inicio de sesión del usuario.
> - jackdbus realtime y a2jmidid para ver los dispositivios alsamidi en jack, Alsa a jack, firewire/alsa/jack
> - No pulseaudio / jack a alsa
> - 2 modos en música: jack o reaper
> - jack -> carla o sfizz: sfz (colección de soundfonts) o plugins
>   - qjackctl (establecer tarjeta sonido)
>   - Cadence/catia/claudia/carla
> - reaper -> plugins vst, lv2 (carla o sfizz -> sfz), etc.
> - App/Plugins (~/.vst): 
>   - Instrumentos: Vital(vst/vst3), Helm(lv2/vst), Dexed(lv2), Monique(vst/jack), Surge XT(lv2/vst3/jack), U-HE(vst), TAL(vst), Tunefish4(vst), setBfree(lv2/vst/jack), Brigton(jack), non-mixer/non-timeline/nom-sequencer (jack)
>   - Efectos: LSP(lv2/vst/jack), GVST(vst), calf(lv2/jack), TAL(vst3/vst), reaper
>   - Guitarra: Guitarix(lv2/jack), Rakarrack(jack)
>   - Util: jack-keyboard (teclado virtual), Tonespace (vst/jack acordes), Hypercyclic (vst/jack arpegiador), Graillon (lv2 autotune), jackass (vst a jack), aj-snapshot (jack)
> - mixxx (dj), audacity (editor de sonido)
> - Bancos sonido SFZ (/usr/share/sounds/sfz):
>   - Básicos (bateria + piano)
>   - Bajos  (sounds4u, FreeDrumKits, Roadstar, swagbass)
>   - Drumkits (Analogue drums, AVL, Ken, G&S, Rogers)
>   - GM (FluidR3)
>   - Guitarras (emilyguitar, Guitar DI, GuitarChord, sounds4u, LP-SGC)
>   - Percusión (AVL, Black Swamp Tambourine, Reactor)
>   - Pianos (sound4u: Yamaha C5, dynamic, dark, mellow, bright, classic, etc)
>   - Virtual Playing Orchestra 3
> - Impulse responses (/usr/share/sounds/ir): para lsp-plugin, reareverb
> - Menú linuxmin: Configuración jack/ffado, de DPI de las pantallas y disposición de los monitores, etc.

## Tutorial de jack

Por defecto jack no está en marcha. Hay que borrar el fichero **~/.nojack** para que al iniciar sesión se cargue jack.

En el menú de linuxmin está la utilidad "fix" que permiten configurar jack/ffado

-**jackon** lo activa con la última configuración.

-**jackoff** stop.

-**jackstatus**

-**jackreset**

-**jackdefault** o **jackdefaultfw** lo activa pero con la configuración básica: Alsa o Firewire/hw:0/48Khz/24b/256 samples/2 buffers.

Se puede predescubrir si se tiene tarjeta firewire. Para activar jack con tarjetas de sonido firewire lo mejor es **jackdefaultfw** o configurar con **qjackctl** o **cadence** estableciendo firewire en vez de alsa.

Para configurar el mixer de inicio cargar *ffado-mixer* y usar el comando **ffado-set-mixer-init** para registrar las acciones. 

**ffado-init-mixer** se carga si exites **~/.ffadorc** con el resultado del comando anterior

Si no funciona es necesario un reinicio o usar linuxmin -> fix: jack/ffado

Cuando jack está en marcha las aplicaciones que usan alsa como salida de sonido disponen del Mixer2 para controlar el volumen. Alsamixer o Qmixer

## Descarga
### **Basado en Debian 12 bookworm**

> **Aquí puedes descargar el live/instalador**: [linuxmin12_me.iso](https://upvedues-my.sharepoint.com/:u:/g/personal/jmpolo_upv_edu_es/EZEI1_awZ8ZLmYrr5dfIr14BNzSyA6J78d_wDao8qMY8gw?e=JE8Esd)

(*usuario*: **user**, *contraseña* **live**) 

![](img/me%20(1).png)

![]img/(me%20(2).png)

![](img/me%20(3).png)

![](img/me%20(4).png)

![](img/me%20(5).png)

![](img/me%20(6).png)

![](img/me%20(7).png)

![](img/me%20(8).png)

![](img/me%20(9).png)

![](img/me%20(10).png)

![](img/me%20(11).png)

#

# linuxmin (básico)
## Distribución live/instalación personalización básica de escritorio: Linux Mínimo
### ¡¡¡ última versión 25/feb/2024 !!!

## **Basada en debian 12 bookworm**
Aquí puedes descargar el live/instalador: [linuxmin12.iso](https://upvedues-my.sharepoint.com/:u:/g/personal/jmpolo_upv_edu_es/EdDLdwuVKMpOo4zJ7b3JTygB7cUZ6qVrvszKL-LoiVekHw?e=gaNfKu)

(*usuario*: **user**, *contraseña* **live**) 

## Pantallazos

![](img/screen%20(1).png)

![](img/screen%20(2).png)

![](img/screen%20(3).png)

![](img/screen%20(4).png)

![](img/screen%20(5).png)

# si no hacer lo siguiente.... (obsoleto)

Instalar Debian 11 firmware version [aquí](https://cdimage.debian.org/cdimage/unofficial/non-free/cd-including-firmware/current/amd64/iso-cd/)

NO instalar ningún paquete

![](img/linuxmin_install.png)

[Configurar la wifi o continuar en el punto siguiente para cable](http://phmmusic.blogspot.com/2022/05/debian-11-basico.html)

sudo apt update && sudo apt upgrade -y

sudo apt install git

git clone https://github.com/libertyrock/linuxmin

cd linuxmin

chmod +x ./instal

./instal

## Teclas

Windows + T XTerm (Terminal)

Windows + F Firefox (Navegador de internet)

Windows + e pcmanfm (Explorador de ficheros)

## Tamaño imagen

2,3 GB

## Contenido

bash-completion git

xserver-xorg-core openbox xinit slim tint2

pcmanfm featherpad feh xarchiver firefox-esr-l10n-es-es
