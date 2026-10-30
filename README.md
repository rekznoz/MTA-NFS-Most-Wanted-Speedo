# MTA NFS Most Wanted Speedo

Velocímetro de estilo Need for Speed: Most Wanted para MTA:SA, con velocidad digital, cuentarrevoluciones e indicadores de vida del vehículo y nitro.

- Velocidad digital en km/h, marcha N/R y cuentarrevoluciones estimado.
- Arco superior: vida del vehículo, ámbar/naranja/rojo según el daño. Un vehículo reparado (1000 HP) marca 100%; el umbral de incendio (250 HP) marca 0%.
- Arco verde: nivel real del nitro. Sin nitro queda vacío; este recurso no instala ni recarga NOS.
- Aguja inferior: empuje/turbo simulado. Parte del centro, aumenta progresivamente hacia la derecha al acelerar y vuelve al centro al soltar. Al circular marcha atrás se desplaza hacia la izquierda según la velocidad. Funciona también sin NOS y se reinicia al cambiar de vehículo.
- Se oculta a pie, al morir y mientras el mapa está abierto.

## Activación

1. Copia la carpeta completa `MTA-NFS-Most-Wanted-Speedo-main` en la carpeta `resources` de tu servidor.
2. En la consola del servidor ejecuta `refresh` y después `start MTA-NFS-Most-Wanted-Speedo-main`.
3. Para arrancar el recurso con el servidor, añade `<resource src="MTA-NFS-Most-Wanted-Speedo-main" startup="1" protected="0" />` en `mtaserver.conf`.

El velocímetro está **activado por defecto** para cada jugador y aparece al entrar en un vehículo, también si el recurso se inicia cuando el jugador ya está dentro.

Escribe **`/nfsmw`** en el chat para desactivarlo y repite el comando para volver a activarlo. En la consola F8 utiliza `nfsmw` sin la barra. El cambio solo afecta al jugador que ejecuta el comando, se mantiene al cambiar de vehículo o reaparecer y se restablece a activado al reiniciar el recurso o reconectarse.

La tabla `CFG` de `client.lua` permite ajustar el nombre del comando (sin `/`), ancho, márgenes y límite de RPM. El reloj se ancla abajo a la derecha y se adapta a la resolución. Las otras tres escalas RPM suministradas se conservan, aunque este diseño utiliza la de 10000 RPM de la referencia.
