# Creator

El agente que fabrica herramientas para Allkin. Le describes lo que quieres; te hace sus
preguntas en un **formulario**, escribe la herramienta, el servicio o la competencia según el
estándar Allkin, la **comprueba** y la depura contigo. Creator no tiene página propia: es un
agente, en la lista de agentes, con el que se habla.

## Para qué sirve

- **Crear una herramienta**: un programa que funciona en continuo, una página, una parte de la
  interfaz de Allkin, un agente dedicado — o varios a la vez.
- **Crear un servicio**: enseñar a Allkin cómo llegar a una API externa, para que tus agentes la
  llamen con tu clave.
- **Crear una competencia**: un saber hacer que un agente carga a demanda.

Todo lo que Creator escribe respeta el **estándar Allkin**, incluido con la herramienta
(`standard/PLUGIN-STANDARD.md`, `standard/SERVICE-STANDARD.md`, `standard/SKILL-STANDARD.md`),
y lo comprueba él mismo tras cada cambio.

## Puesta en marcha

1. Instala Creator y concede sus tres permisos en su página. El agente **Creator** y tu
   repositorio local se crean en ese momento.
2. Abre la conversación del agente Creator (está en la lista de agentes, en rosa como todo
   agente de una herramienta) y dile lo que quieres.
3. Te hace sus preguntas de una vez, en un formulario; responde, él escribe los archivos, los
   comprueba y termina diciéndote qué hacer: instalar, conceder un permiso, recargar la página,
   arrancar el servicio.
4. Para instalar lo que escribió: página **Herramientas**, tu repositorio «Creator» es una de sus
   fuentes; **Instalar**, luego los permisos en la página de la herramienta. Un servicio se
   conecta desde la página **Servicios**; una competencia desde la página **Competencias**.

## Depurar

Cuando una herramienta no hace lo que debe, díselo a Creator: lee el registro del servicio
(`read_tool_log`), vuelve a lanzar la comprobación (`check_project`), corrige, sube la versión y
te dice qué rehacer. Dale el error exacto que ves: es lo que más le ayuda.

## Dónde están tus archivos

En la carpeta de trabajo del agente: `~/.allkin/plugin-data/creator/workspace/`, con una carpeta
`plugins/`, una carpeta `services/` y una carpeta `skills/`. Esa carpeta es un **repositorio
local**: aparece en la ventana *Repositorios* de las páginas Herramientas, Servicios y
Competencias, y tus creaciones se listan allí con la etiqueta «Creator».

Esa carpeta **no se borra** al desinstalar Creator. Para publicar una creación, copia su carpeta
en tu repositorio de herramientas.

## Permisos solicitados

| Permiso | Por qué |
|---------|---------|
| Agente dedicado | El agente Creator, que escribe los archivos. No tiene acceso a la máquina fuera de su carpeta de trabajo |
| Repositorio | Hacer de la carpeta de trabajo una fuente de herramientas, servicios y competencias para este Allkin |
| Red | Dejar que el agente lea la documentación en línea de las API |

## Si no funciona

- **El agente Creator no aparece**: falta conceder un permiso. Abre la página de la herramienta.
- **Instalar no cambia nada**: la versión no ha cambiado. Pide a Creator que la suba.
- **La interfaz de la herramienta no aparece**: concede sus permisos en su página y recarga.
- **El agente no responde**: comprueba tu proveedor de IA en los Ajustes de Allkin.
