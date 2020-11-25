# Epidemic-Replication

<h2>Descripción</h2>
Este proyecto trata de crear un servidor compuesto por tres capas de nodos. Los cientes que hacen peticiones al servidor pueden actualizar o leer los datos. En este caso el servidor contiene únicamente 9 elementos, y cada elemento contiene números.<br>
<br>

<h2>Entorno</h2>
<br>
1) Un Servidor compuesto por 3 capas diferentes de nodos:<br>
    Primera Capa: Nodos Core (A)<br>
    Segunda Capa: Nodos B<br>
    Tercera Capa: Nodos C<br>
<br>
2) Hay uno o multiples Clientes que interactúan con los nodos.<br>
<br>

<img width="567" alt="Entorno" src="https://user-images.githubusercontent.com/24244834/100252744-fb812000-2f1e-11eb-9161-7f3276a6a00c.png">


<h2>Requisitos</h2>

*Los clientes leen un archivo de configuración para determinar si quieren leer o actualizar información del servidor. Luego se hacen las peticiones pertinentes al servidor.<br>
    Consultas lectura: se selecciona cualquier nodo de forma aleatoria para consultar el dato<br>
    Consultas escritura: se selecciona un nodo de la capa A de forma aleatoria para escribir el dato<br>
*Las peticiones de actualización solo llegan a los nodos de la capa A y estos se encargan de replicarla a los demás nodos.<br>
*Las peticiones de lectura llegan a cualquier nodo. Es posible que dos nodos contengan información diferente, ya que un nodo puede estar desactualizado. Esto es así por diseño. En un determinado tiempo X todos los nodos quedarán actualizados.<br>
*Una petición que llega a un nodo A es replicada inmediatamente a otros nodos A. Después de 10 peticiones recividas, los nodos A replican la información a sus nodos B
*Los nodos B replican su informacion a los nodos C cada 10 segundos.
*Hay que mostrar los cambios en un web mediante websockets.

<h2>Resultados</h2>

Web - Estado Inicial

<img width="600" alt="web-estado-inicial" src="https://user-images.githubusercontent.com/24244834/100253606-156f3280-2f20-11eb-81fd-24aba25ac04b.png">

Web - Replicaciones

<img width="699" alt="web-replicaciones" src="https://user-images.githubusercontent.com/24244834/100253618-1c964080-2f20-11eb-8870-2d33e5848edd.png">

Consola Cliente - Consultas a los diferentes nodos

<img width="613" alt="consola-clientes-consulta-datos" src="https://user-images.githubusercontent.com/24244834/100253639-23bd4e80-2f20-11eb-9e9b-51ecec91f053.png">





