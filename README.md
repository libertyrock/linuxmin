# linuxmin multimedia edition 13
## Distribución live/instalable para música
### ¡¡¡ última versión 10/nov/2025 !!!
 Con **pipewire, ffado, pulseaudio y jack nativo**
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
### **Basado en Debian 13 trixie**

> **Aquí puedes descargar el live/instalador**: [linuxmin13.iso](https://upvedues-my.sharepoint.com/:u:/r/personal/jmpolo_upv_edu_es/Documents/linuxmin/linuxmin13.iso?csf=1&web=1&e=3fs5DV)

(*usuario*: **user**, *contraseña* **live**) 

![](img/image(1).png)

![](img/image(2).png)

![](img/image(3).png)

![](img/image(4).png)

![](img/image(5).png)

![](img/image(6).png)

![](img/image(7).png)

![](img/image(8).png)

![](img/image(9).png)

![](img/image(10).png)

![](img/image(11).png)

#

# linuxmin (básico)
## Distribución live/instalación personalización básica de escritorio: Linux Mínimo
### ¡¡¡ última versión 10/nov/2025 !!!

## **Basada en debian 13 trixie**
Aquí puedes descargar el live/instalador: [linuxmin13-min.iso](https://upvedues-my.sharepoint.com/:u:/r/personal/jmpolo_upv_edu_es/Documents/linuxmin/linuxmin13-min.iso?csf=1&web=1&e=v4GB8G)

(*usuario*: **user**, *contraseña* **live**) 

## Teclas

Windows + T XTerm (Terminal)

Windows + F Firefox (Navegador de internet)

Windows + e pcmanfm (Explorador de ficheros)

## Tamaño imagen

5 GB o 2 GB aprox. 

