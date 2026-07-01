------------------ENGLISH/SPANISH--------------------

*Problem

I arrived at the property and the first thing I thought was:

"I'm going to use WiFiman to see where the access points are."

When I opened WiFiman, I noticed there were literally zero Wi-Fi signals. It looked as if every AP was powered off.

The ticket mentioned there should be 7 access points, so I started looking for them the old-fashioned way by opening closets, utility rooms, and checking around the house.

I found:

6 APs inside the main house.
1 AP in the pool house.

Every AP had power, and the CTRL LED was blinking.

My first thought was:

"Okay... the controller LED is blinking, so maybe the ticket is right and the controller is the problem."

*First Steps

At first I simply started following the ticket.

I factory reset two APs.

Before resetting the third one, I stopped for a second and thought:

"Instead of resetting everything, let me see if I can learn a little more about what's actually happening."

I unplugged one AP and used that same Cat6 cable to connect my laptop directly into the switch port.

*Network Verification

Once connected, I checked my network first.

I ran:

ipconfig

to verify what IP address I received.

I noticed I was getting a 10.0.1.x address, while earlier I had been on 10.0.2.x.

That immediately made me wonder:

"Did I move to another subnet? Am I plugged into the wrong VLAN?"

To verify that, I logged into the switch and checked the port configuration.

After confirming the port configuration looked correct, I continued testing.

I also ran:

ping 8.8.8.8

to verify Internet connectivity.

Then I pinged the AP's IP address to make sure I could actually reach it before wasting time trying to log into it.

*Identifying the APs

The documentation wasn't very complete, so I used OvrC to identify:

IP addresses
MAC addresses
Manufacturers

That helped me confirm I was working with the correct devices.

*Management Access

At this point I honestly wasn't sure what was happening.

After resetting the APs, I couldn't access their web interface.

Since this was my first time dealing with this type of Ruckus deployment, I called one of my coworkers who usually handles the Wi-Fi and network troubleshooting.

I explained everything I had done.

He immediately told me:

"You have to flash them all. Download the Unleashed firmware."

I had never done a ZoneDirector to Unleashed migration before, so I started reading the Ruckus documentation while also asking ChatGPT questions whenever I wasn't sure about something.

That actually helped me relax because now I knew there was a clear direction.

*SSH Issue

While trying to SSH into the APs, I ran into another problem.

The AP was offering the old ssh-rsa algorithm, so I couldn't connect using the default Windows SSH settings.

After figuring that out, I was finally able to log into one AP through SSH.

Inside the AP I verified:

Firmware version
Controller status
Standalone mode

I also confirmed the AP was still running ZoneDirector firmware.

*Flashing the AP

After downloading the correct R650 Unleashed firmware, I uploaded it through the AP web interface.

The AP successfully started building the Unleashed network.

*Another Problem

Two APs still weren't behaving correctly.

I couldn't log into them using the default credentials.

I called my manager and explained what was happening.

He checked remotely and noticed those APs were still reporting their old IP addresses.


His first thought was:

"Maybe the reset didn't actually happen."

He was right.

My helper (who is also pretty new) hadn't held the reset button correctly.

The LED turned red, but he kept holding it long enough for the AP to return to normal instead of completing the factory reset.

After performing the reset correctly, those APs received new IP addresses and behaved exactly as expected.

*Final Testing

Once every AP was online, we walked the entire property testing Wi-Fi coverage.

Everything was working correctly.

Right when we thought we were done, we found another issue.

The two wall-mounted iPads were frozen on the home screen.

Since they're mounted inside the wall, I had to:

Remove the wall plate.
Pull the iPad out.
Force restart it using the Power + Volume buttons.

Both iPads booted normally afterward.

*Root Cause
Failed ZoneDirector controller.
APs needed to be migrated from ZoneDirector firmware to Unleashed.
Two APs had not actually been factory reset because the reset procedure wasn't completed correctly.

*Lessons Learned
Never assume a factory reset was successful. Always verify it.

Before blaming the device, verify my own connectivity first (ipconfig, switch port/VLAN, Internet access, and ping).

Just because an AP responds to ping doesn't mean all of its management services (HTTPS, GUI, SSH) are fully available.

At first, I thought running get https was what made the web interface work. After resetting another AP and going straight to the GUI, I realized get https only checks the HTTPS status—it doesn't enable or restart the service.

When working with an unfamiliar platform, it's important to understand the architecture first (in this case, ZoneDirector vs. Unleashed) before making configuration changes.

During a ZoneDirector to Unleashed migration, only one AP needs to become the Unleashed Master. The remaining APs can join after being factory reset.

Always perform a complete end-to-end test before closing the job. Fixing the main issue doesn't guarantee everything else is working, as shown by the two wall-mounted iPads that were frozen after the Wi-Fi was restored.


----------------------spanish--------------------


*Problema

Llegué a la propiedad y lo primero que pensé fue:

"Voy a usar WiFiman para encontrar dónde están los access points."

Cuando abrí WiFiman me di cuenta de que había literalmente cero señales de Wi-Fi. Era como si todos los APs estuvieran apagados.

Entonces mi siguiente paso fue buscarlos a la antigua.

El ticket decía que había 7 access points, así que empecé a abrir closets, cuartos y puertas hasta encontrarlos.

Encontré:

6 APs dentro de la casa.
1 AP en la pool house.

Todos tenían alimentación y el LED de CTRL estaba parpadeando.

En ese momento pensé:

"Ok... si el LED del controlador está parpadeando, probablemente el problema sí sea el controlador, tal como decía el ticket."

*Primeros pasos

Al principio simplemente seguí lo que decía el ticket.

Comencé reseteando dos APs.

Cuando iba por el tercero pensé:

"Antes de seguir reseteando todo, voy a probar si puedo entender un poco mejor qué está pasando."

Desconecté el cable Cat6 de uno de los APs y usé ese mismo puerto para conectar mi laptop.

Verificando la red

Lo primero que hice fue revisar mi conexión.

Corrí:

ipconfig

para verificar qué dirección IP había recibido.

Noté que antes estaba en la red 10.0.2.x y ahora estaba en 10.0.1.x.

Mi primer pensamiento fue:

"¿Estoy en otra subred? ¿Será que me conecté al VLAN equivocado?"

Entonces entré al switch para revisar cómo estaba configurado ese puerto.

Después de confirmar que el puerto era el correcto seguí haciendo pruebas.

También corrí:

ping 8.8.8.8

para asegurarme de que tenía conectividad a Internet.

Después hice ping a la IP del access point para confirmar que realmente podía llegar hasta él antes de seguir intentando entrar por la interfaz web.

*Identificando los equipos

Como prácticamente nada estaba documentado en OvrC, lo utilicé para identificar:

Direcciones IP.
Direcciones MAC.
Fabricante de cada equipo.

Eso me ayudó a confirmar que estaba trabajando con los access points correctos.

Cuando ya no sabía qué hacer

En ese momento, sinceramente ya no sabía exactamente qué estaba pasando.

Después de resetear los APs no podía entrar a la página web de ninguno.

Como nunca había trabajado con una migración de ZoneDirector hacia Unleashed, llamé a un compañero que normalmente hace todo el troubleshooting de Wi-Fi y redes.

Le expliqué todo lo que había hecho.

Él me dijo:

"You have to flash them all. Download the Unleashed firmware."

Nunca había hecho ese procedimiento, así que empecé a buscar el firmware correcto y a leer cómo funcionaba el proceso.

Al mismo tiempo empecé a preguntarle a ChatGPT las dudas que me iban saliendo.

La verdad eso me ayudó bastante porque ya sentía que tenía una dirección clara y dejé de sentir que estaba completamente perdido.

*Problema con SSH

Después apareció otro problema.

No podía entrar por SSH debido a un problema con el algoritmo ssh-rsa.

Al principio pensé que tal vez estaba escribiendo mal el usuario o la contraseña porque lo intenté varias veces.

Después descubrí que realmente era un problema de compatibilidad con SSH.

Una vez solucionado, pude entrar al AP por consola.

Ahí verifiqué:

La versión del firmware.
El estado del controlador.
Que el AP estaba funcionando en modo Standalone.

También confirmé que seguía corriendo firmware de ZoneDirector.

*Migración

Después descargué el firmware correcto de R650 Unleashed.

Lo subí desde la interfaz web del AP y comenzó el proceso de migración hacia Unleashed.

*Otro problema

Todavía tenía dos APs que seguían comportándose raro.

No podía entrar utilizando las credenciales por defecto.

Llamé a mi manager y le expliqué lo que estaba pasando.

Él revisó remotamente y notó que esos dos APs seguían apareciendo con sus direcciones IP antiguas.

Me dijo que probablemente el factory reset no había funcionado.

Y tenía razón.

Mi helper (que igual es junior como yo) no estaba haciendo correctamente el procedimiento de reset.

Cuando el LED cambiaba a rojo seguía contando más tiempo y el AP terminaba arrancando normalmente otra vez, así que realmente nunca se completaba el factory reset.

Volvimos a hacer el procedimiento correctamente.

Esta vez los APs sí cambiaron de IP y comenzaron a comportarse como esperábamos.

*Verificación final

Después recorrimos toda la propiedad comprobando que el Wi-Fi funcionara correctamente.

Todo quedó funcionando.

Cuando ya pensábamos que habíamos terminado encontramos otro problema.

Los dos iPads que están empotrados en la pared estaban congelados en la pantalla principal.

Como están montados dentro de la pared tuve que:

Quitar la tapa.
Sacar el iPad.
Forzar un reinicio utilizando Power + Volumen.

Después de reiniciarlos ambos arrancaron normalmente y volvieron a funcionar.

* Causa raíz
Falló el controlador ZoneDirector.
Fue necesario migrar los APs a Unleashed.
Dos access points nunca habían sido reseteados correctamente porque el procedimiento de factory reset no se había completado.

*Lo que aprendí
No asumir que un factory reset realmente se completó; siempre verificarlo.
Antes de culpar un dispositivo, verificar mi propia conectividad (ipconfig, switch, VLAN, Internet y ping).

Si un AP responde a ping, no significa que todos sus servicios (HTTPS, GUI) ya estén listos.
get https solo muestra el estado del servicio, no lo habilita. Al principio pensé que ese comando había solucionado el problema, pero después comprobé que no era así al resetear otro AP y entrar directamente por HTTPS.

Cuando un problema es nuevo para mí, primero entender la arquitectura (en este caso, ZoneDirector vs. Unleashed) antes de empezar a cambiar configuraciones.

En una migración a Unleashed, basta con convertir un AP en Master; los demás pueden unirse después de un factory reset.

Siempre hacer una prueba final de todo el sistema, porque pueden existir problemas adicionales no relacionados con la falla principal (como los iPads congelados).
