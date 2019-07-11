# Trabajadores Estresades

_**Ejercicio tipo parcial - Paradigma Lógico**_

Tenemos información de muchas personas y de las tareas que realiza la mayoría de ellas. Para simplificar, consideramos sólo tres tipos de tarea:

* Tomar examen: Se indica el tema del examen y el lugar.
* Hacer un discurso:  Se conoce el lugar y la cantidad de público presente.
* Meter un gol: Se registra el torneo en que se lo convirtió.

Una persona puede hacer varias tareas y una tarea puede ser hecha por diferentes personas. Se desea poder tratarlas indistintamente. Nos interesa también saber en qué fecha (día, mes y año) fue realizada la tarea por esa persona: A veces sucede que dos personas hicieron la misma tarea, pero en diferente fecha. Otras veces, en la misma fecha, una persona hace varias tareas. De todas las personas, hayan hecho alguna tarea o no, se conoce su lugar de nacimiento. 

Por ejemplo, Dani, Alf, y Nico nacieron en Buenos Aires. Dani hizo dos tareas: tomar en el aula 522 un examen del paradigma lógico en la fecha 10/8/2017, y meter un gol en primera división esa misma fecha (sí, así de groso). Alf, por otro lado, hizo un discurso en UTN para 0 espectadores, el 11/8/2017. 

Los lugares están relacionados en la base de conocimiento de acuerdo al siguiente ejemplo:

~~~
%% quedaEn(lugar, lugar)
quedaEn(venezuela, america).
quedaEn(argentina, america).
quedaEn(patagonia, argentina).
quedaEn(aula522, utn). % Sí, un aula es un lugar!
quedaEn(utn, buenosAires).
quedaEn(buenosAires, argentina).
~~~

### Dulce hogar
Se desea saber si un trabajador nunca salió de casa, que es cuando sólo realizó tareas en su lugar de nacimiento (exactamente ahí). 
Para poder resolver el punto, se deberá incluir en la base de conocimiento la información adicional del lugar donde se realiza cada tarea.

### Estrés nacional
Se quiere saber si una tarea es estresante, lo cual es independiente de quién la realice o cuándo. Una tarea para ser  estresante debe cumplir dos condiciones: realizarse en cualquier parte del territorio argentino, y además:
* Para los discursos, ser dados a más de 30000 personas.
* Para tomar exámenes, ser de un tema complejo.
* Por último, los goles siempre son estresantes (los hechos en territorio argentino).
Incluir en la base de conocimiento cuáles son los temas complejos. 


### Trabajadores alterados
En la medida que realizan tareas estresantes, a los trabajadores los puede calificar de diferentes maneras: 
* zen: aquellos que nunca realizaron tareas estresantes.
* locos: los que en 2017 realizaron sólo tareas estresantes.
* sabios: los que realizaron una única tarea estresante en su vida.
Queremos relacionar a cada persona con cada una de sus calificaciones, en caso que le corresponda.

### El más chapita
Se quiere averiguar a quién darle el premio "estrés de todos los tiempos", por ser la persona que más tareas estresantes ha realizado.

### Para pensar
* ¿Dónde se utilizó el polimorfismo? ¿Para qué fue útil? 
* ¿Son inversibles los predicados principales del punto 2 y 3? Justificar por qué y si era necesario que lo fueran.

Armar una base de conocimiento breve (que no hable ni de Alf ni de Nico ni de Dani), pero que permita mostrar ejemplos de consulta para todos los items. En particular, mostrar lo siguiente:
* Que haya alguien que sea loco y sabio
* Que no haya trabajadores zen.
* Que una persona tenga al menos una tarea estresante en 2017 y una en 2016 y otra persona tenga una tarea en 2016, de manera que la primera sea la ganadora del premio estrés de todos los tiempos.
