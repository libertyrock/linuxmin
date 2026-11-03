### LINUXMIN 13
Distribución **linuxmin 13**, basada en Debian 13, proporciona una versión de Linux con una **interfaz** gráfica más **sencilla y fácil de usar**. Este sistema operativo está especializado para **sonido profesional y multimedia**.

¡¡¡ Puede funcionar en equipos con menos de 1GB de RAM !!!
### ¡¡¡ última versión 2/nov/2026 !!!
 

> Aquí puedes descargar el live/instalador completo: [linuxmin13.iso](https://upvedues-my.sharepoint.com/:u:/r/personal/jmpolo_upv_edu_es/Documents/linuxmin/linuxmin13.iso?csf=1&web=1&e=3fs5DV)

>Aquí puedes descargar el live/instalador mínimo: [linuxmin13-min.iso](https://upvedues-my.sharepoint.com/:u:/r/personal/jmpolo_upv_edu_es/Documents/linuxmin/linuxmin13-min.iso?csf=1&web=1&e=v4GB8G)

(*usuario*: **user**, *contraseña* **live**) 

### ¡¡¡ En breve video explicativo !!!

 Elige el sistema de sonido para tu linuxmin: **pipewire, pulseaudio, jack, ffado o alsa**.

 Con configuración para rendimiento, personalización y utilidades para música, plugins vst/lv2, con samples sfz e impulse responses gratuitos, esenciales y de calidad.

> Características:
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

## Contenido
### _Comandos y teclas_

```
linuxmin help
=============

https://github.com/libertyrock/linuxmin

Keys: (C-A) o W
W-h ..... Help
W-ESC ... Menu
W-l ..... Logout menu
W-r ..... Execute
W-t ..... Terminal
W-e ..... Pcmanfm
W-f ..... Firefox
W-y ..... Terminal (root)
W-s ..... PcmanFM (root)
W-0 ..... Poweroff
W-9 ..... Reboot
W-1 ..... Logoff
W-u ..... linuxmin_update
PrintScr ... Screen capture
A-PrintScr ... Zone capture

linuxmin:
linuxmin_util ....... linuxmin util
linuxmin_update ..... Update system
linuxmin_launch ..... Load and connect jack apps
linuxmin_logout ..... Logout Menu
linuxmin_dpiset ..... DPI zoom
linuxmin_monto ...... Monitor Config
linuxmin_gov ........ Goverment performance
linuxmin_cpuinfo .... CPUInfo
linuxmin_help ....... Help
linuxmin_deskentry .. Manqage other menu
linuxmin_deskcolor .. Desktop & login window color
linuxmin_sessionset . Set session default
linuxmin_timedate ... Update TimeDate
linuxmin_update_menu  Update openbox menu
linuxmin_perfserv ...... Performance system services
linuxmin_perfservuser .. Performance user services
linuxmin_grub ....... Performance grub config
linuxmin_users ...... add o del users

pcmanfm_root ........ PcmanFm root
xterm_root .......... Terminal root

lmopenbox ........... Openbox Desktop
lmdesk .............. Linuxmin Desktop
lmdeskreset ......... Reset Desktop
lmmodeaudio ......... MODE AUDIO
lmmodenormal ........ MODE NORMAL

Audio:
linuxmin_audio ...... Audio Util
linuxmin_alsa ....... Alsa Util
linuxmin_ffado ...... ffado Util

linuxmin_jack ....... Jack Util
linuxmin_jackalias .. Jack Alias Util
linuxmin_jackparams . Jack Params Util
linuxmin_jackset .... Jack set
linuxmin_dps ........ Jack params set
linuxmin_netjack .... NetJack Util

linuxmin_pipewire ... Pipewire Util
linuxmin_pipeparams . Pipewire params Util
linuxmin_pipepipe ... Pipewire config
linuxmin_pipejack ... Pipewire jack config
linuxmin_pipeffado .. Pipewire ffado config

linuxmin_pulse ...... Pulse Util
linuxmin_pulseset ... Pulse set
linuxmin_pulsevol ... Pulse Volume
linuxmin_pulsevol_input ... Pulse input Volume
linuxmin_pulseicon .. Pulse device set icon
linuxmin_vol ........ Sample volume ffado device
linuxmin_pulseprofile ..... Profiles of devices

audioinit ........... linuxmin audio init
audioinitoff ........ Audio init off
audioiniton ......... Audio init on
audioreset .......... Audio system reset
audiostatus ......... Audio system status
linuxmin_to_alsa .... Audio system alsa
linuxmin_to_jack .... Audio system jack
linuxmin_to_pulse ... Audio system pulse
linuxmin_to_pipewire  Audio system pipewire

alsadefault ......... Set Alsa default device
alsalist ............ List alsa devices
alsasave ............ Set Alsa device default
alsastatus .......... Show Alsa default device

ffadodiscover ....... Firewire Discover
ffadomixerload ...... Load mixer conf
ffadomixerloadfile .. Load mixer conf from file
ffadomixersetdef .... Set default load
ffadomixerset ....... Set a mixer conf
ffadoon ............. Firewire audio on
ffadooff ............ Firewire audio off
ffadooclean ......... Clean ffado conf
ffadostatus ......... ffado status
fwalsa_root ......... blacklist snd_*

jackon .............. Jack on
jackoff ............. Jack off
jackreset ........... Jack reset
jackstatus .......... Jack show status
jackoffinit ......... Jack off when init session
jackoninit .......... Jack on when init session
jackdefault ......... Jack Alsa default
jackdefaultfw ....... Jack Firewire default
jackdefaultnet ...... Jack net client default
jacknoff ............ Jack network off
jacknon ............. Jack network on
jackreset ........... Reset Jack & ffado

jackaliasload ....... load defaults
jackaliasloadfile ... file load
jackaliaslist ....... list
jackaliassave ....... save
jackaliasclean ...... clean
jackaliasfix ........ fix error
jackaliassetdef ..... set default load

pulseoff ............ pulse off
pulseon ............. pulse on
pulsestatus ......... pulse status
pulsereset .......... pulse reset
pulse

pipewireclean ....... pipewire clean 
pipewiredefault ..... pipewire default
pipewireoff ......... pipewire off
pipewireon .......... pipewire on
pipewirestatus ...... pipewire status
pipewirereset ....... pipewire reset

Debug:
linuxmin_debug ...... linuxmin debug terminal
lmdebug_init ........ set init debug
lmdebug_show ........ show from init to now journal

Variables:
$ export LMDEBUG=1 # debug on terminal

Monitor:
linuxmin_mon ........ linuxmin monitors
linuxmin_monalsa .... linuxmin alsa monitor
linuxmin_monffado ... linuxmin ffado monitor
linuxmin_monjack .... linuxmin jack monitor
linuxmin_monpulse ... linuxmin pulse monitor
linuxmin_monpipe .... linuxmin pipe monitor

```