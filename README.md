<div align='center'>
  <h1>FCEN Aulas</h1>
  <h5>¿Qué aulas de la facu hay libres?</h5>
</div>

<div align='center'>
  Éste proyecto está dividido en dos repos:
    <table>
        <thead>
            <tr>
                <th colspan="1"><a href='https://www.github.com/joangq/fcen-aulas-dataserver'>Dataserver (Python)</a></th>
                <th colspan="1"><a href='https://www.github.com/joangq/fcen-aulas-endpoint'>Endpoint (Java)</a></th>
            </tr>
        </thead>
    </table>
</div>

La idea era tener una forma fácil de saber qué aulas hay libres en la facultad. Los horarios en los que las aulas están ocupadas son públicos, por ende originalmente ésto apuntaba a:
- Descargar automáticamente la última versión de los horarios
- Analizarlos
- Devolver una lista de las aulas libres para el momento actual.

Actualmente, el proyecto tiene dos partes:
- Un servidor _endpoint_ que maneja solicitudes web. La idea es proveer la página con las aulas libres como un "servicio" web. Actualmente está programado en Java usando Springboot.
- Un servidor interno (_dataserver_) que se encarga de automatizar la recolección, parseo y procesamiento de datos.

La idea es que la interacción entre ambas partes sea reactiva y responda a distintas solicitudes (Obtener, actualizar, etc). Actualmente simplemente se actualizan y preprocesan los datos después de un tiempo predeterminado; devolviendo la última versión ante el pedido.
