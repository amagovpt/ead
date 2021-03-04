---
title: The score of AccessMonitor
---
<!-- start to translate to EN
A disadvantage of metrics based on failure rate is that they often put us in a difficult position when it comes to determining the total number of situations to which the test applies. In many tests it is difficult, if not impossible, to determine the total number of applicable situations.
-->
<p lang="en">Note: this article was taken from <em lang="es">Libro Blanco de eXaminator</em>, written by Carlos Benavidez, author of Web validators such as Hera, eXaminator and AccessMonitor. The book was published on June 1, 2012. Carlos was the great mentor of the validation tools we use in the Portuguese Public Administration. A work that we started in 2005 and that lasted until the day of his death (19 October 2016). Remembering him is a simple tribute to the enormous legacy he left us.</p>

<p lang="en">Everything that is said below about the eXaminator's score applies to the score of AccessMonitor. The original text is in Spanish.</p>

<p>(...)</p>

<div lang="es">

<h2>Información técnica</h2>

<p>En el tema anterior ya me ocupé de alertar hasta la exageración sobre las limitaciones que pueden tener las calificaciones automáticas. Aún así, necesitamos contar con una métrica numérica que resuma el resultado de las pruebas automáticas en un dato único que nos permita ordenar y comparar esos resultados. Es el momento de explicar las ideas básicas en el diseño de eXaminator y las operaciones que se realizan para evaluar la accesibilidad de las páginas web.</p>

<h2>Antecedentes</h2>

<p>Cuando me dispuse a desarrollar la versión de eXaminator para las WCAG 2.0 - publicadas a principios de diciembre de 2008 - era el momento propicio para modificar de raíz la metodología de revisión y cálculo que usaba hasta ese momento. El sistema consistía básicamente en adjudicar un puntaje a situaciones relacionadas con buenas y malas prácticas de diseño. Por ejemplo, si todas las imágenes tenían el atributo <code>alt</code> la nota era 10, si se encontraba 1 imagen sin <code>alt</code> la nota era 3 y, si había más de una imagen sin <code>alt</code>, la nota era 1. Una metodología sencilla y con bastantes limitaciones.</p>

<p>En ese entonces contaba también con algunas buenas referencias externas, especialmente la Metodología Unificada de Evaluación Web (UWEM) [<a href="#n17" title="UWEM">17</a>] que contenía una métrica numérica para las evaluaciones automáticas. Otra referencia importante era el trabajo sobre Métricas Cuantitativas para Medir la Accesibilidad Web presentado en <span lang="en">W4A 2007</span> porque no sólo proponía una nueva metodología de medición denominada WAQM [<a href="#n18" title="WAQM">18</a>] sino que presentaba y analizaba otros trabajos similares. <strong>Todos estos sistemas, aunque con diferencias significativas entre sí, se basan en la tasa de fallo, es decir, la relación entre el número de errores encontrados y el total de pruebas realizadas.</strong></p>

<p>Había trabajado también en el prototipo de una herramienta basada en UWEM cuyo desarrollo quedó inconcluso debido a la aparición de las WCAG 2.0 (el proyecto UWEM tenía previsto migrar a la nueva versión de las pautas y era más sensato esperar su actualización). Aquí experimenté eso de que el diablo está en los detalles al no saber cómo se resolvían algunas pruebas a pesar de que UWEM contiene una documentación muy completa. Pero aún ese fracaso servía como antecedente para saber qué hacer en la nueva versión de eXaminator y qué obstáculos debía evitar.</p>

<p>(...)</p>

<h2>Fórmulas de cálculo</h2>

<p>Un inconveniente de las métricas que miden la tasa de fallo es que nos ponen en aprietos al tratar de resolver las pruebas cuando es difícil o imposible definir el número total de pruebas realizadas. En el test sobre las alternativas textuales no hay problemas porque el total de pruebas es el número de imágenes que hay en una página y el número de errores son las imágenes sin el atributo <code>alt</code>.</p>

<p>Los problemas aparecen, por ejemplo, al intentar calificar los errores de validación porque disponemos del número de errores pero no existe un total de pruebas que nos permita calcular el porcentaje de errores. También tenemos una situación indefinida cuando encontramos atributos HTML obsoletos porque podríamos considerar como total de casos el número de elementos de la página o solamente el número de elementos que tienen asignado atributos mediante HTML.</p>

<p>Para sortear estas dificultades, eXaminator usa distintas fórmulas para resolver los resultados. Estas fórmulas definen 4 tipos de test que explico en detalle más adelante. El criterio para seleccionar el tipo de test a aplicar en cada caso es que debe permitir que la calificación se ajuste a estos juicios de valor:</p>

<ul title="juicios de valor">
 <li>Muy mal: 1</li>
 <li>Mal: 2 ó 3</li>
 <li>Regular: 4 ó 5</li>
 <li>Bien: 6 ó 7</li>
 <li>Muy bien: 8 ó 9</li>
 <li>Excelente: 10</li>
</ul>

<p><strong>Las calificaciones son empíricas</strong>. Están apoyadas por mi experiencia como revisor y desarrollador de herramientas de evaluación pero existe un componente subjetivo en las decisiones y también una pizca de arbitrariedad. La escala anterior sirve como guía para determinar las calificaciones pero decidir si un error merece 3 ó 5 es siempre discutible. De todos modos, aquí, la tiranía del desarrollador es tan comprensible e inevitable como la de cualquier profesor al tomar exámenes.</p>

<h3>Número de errores</h3>

<p><strong>La repetición de los errores es un dato importante que se debe tener en cuenta en las calificaciones</strong>. Un único error se puede deber a una equivocación o un desliz pero varios errores del mismo tipo indican claramente un concepto equivocado o un gran descuido en el desarrollo. Además, las barreras de accesibilidad aumentan en proporción directa al número de errores.</p>

<p>Cuando existe un total de pruebas bien definido, como es el caso de las imágenes y el atributo <code>alt</code>, se utiliza la tasa de fallo para que la calificación resulte menor cuanto mayor es la cantidad de errores detectados. Para los errores de validación, por ejemplo, se aplica otra fórmula que también disminuye la nota a medida que aumenta el número de errores pero en este caso la escala de disminución es fija, no relacionada a ningún porcentaje.</p>

<p>A veces se deben considerar varios factores para elegir la fórmula más adecuada. Por ejemplo, en el caso de los elementos HTML obsoletos sería posible calcular el porcentaje tomando como total el número de atributos HTML usados. El problema es que, a mayor cantidad de atributos HTML - posiblemente en detrimento del uso de propiedades de CSS - mejoraría la calificación. En un caso así, parece más apropiado considerar el número de errores sin apelar a los porcentajes y usar una escala predeterminada para disminuir la nota de acuerdo a la cantidad de errores.</p>

<p>Hay pruebas que sólo pueden tener resultados binarios. Por ejemplo, el error que consiste en usar el elemento meta para refrescar la página sólo puede tener dos resultados: bien o mal. También existen casos en los que la contabilización de los errores, aunque posible, no es significativa. Por ejemplo, el uso del elemento marquee es un error grave porque provoca movimientos en el contenido, es un elemento anticuado, no estándar y - ¿por qué no que decirlo? - su uso denota un concepto de diseño bastante estúpido. Por eso, poco importa que se use uno o más veces y simplemente merece ser calificado siempre con la peor nota.</p>

<h3>Ponderación de las pruebas</h3>

<p>En el cálculo se debe tener en cuenta que no todas las pruebas tienen la misma importancia, de modo que es necesario ponderarlas para que su peso relativo refleje esas diferencias. La Ponderación (P), que puede tener valores entre 0 y 1, es el producto del grado de Confianza (C) y el Valor relativo de la prueba (V):</p>

<p>P=C*V</p>

<h3>Valor</h3>

<p>El valor de cada prueba se calcula de acuerdo al nivel del Criterio de Conformidad con que se relaciona la técnica revisada. Si la técnica está relacionada con varios criterios de conformidad, se usa el de mayor nivel (si son dos los criterios relacionados, uno de nivel A y otro de nivel doble A, se utiliza el primero).</p>

<ul title="valor de cada prueba">
 <li>Nivel A: 0.9</li>
 <li>Nivel AA: 0.5</li>
 <li>Nivel AAA: 0.1</li>
</ul>
 
<p>Si la técnica se relaciona con más de un Criterio de Conformidad, su valor aumenta 0.1 y disminuye 0.1 cuando es sólo una técnica sugerida y se relaciona con un único Criterio de Conformidad. <strong>(De todas las decisiones que se deben tomar al definir el sistema de medición, esta escala es, claramente, la más arbitraria.)</strong></p>

<h3>Confianza</h3>

<p>Indica la seguridad que se le otorga a la prueba. Como todas las pruebas ofrecen entre una buena y una muy buena seguridad de no fallar (de otro modo serían, lógicamente, descartadas), en una escala de 0 a 1, todas merecerían un valor muy elevado, haciendo que la escala fuera poco significativa.</p>

<p>Para ampliar esa escala basada en un criterio válido, se toman en cuenta los pasos indicados en los procedimientos de revisión de las técnicas relacionadas. Por ejemplo, si el primer enlace de la página tiene como referencia un ancla en la propia página, la técnica G1 [<a href="#n19" title="la técnica G1">19</a>] parece satisfecha pero, observando los procedimientos de revisión manual, vemos que faltaría verificar si el enlace es siempre visible, si el texto del enlace es correcto y si efectivamente el salto es hacia el contenido principal. Por cada uno de esos pasos que no es posible verificar automáticamente se disminuye 0.1 y la confianza de esa prueba será 0.7. Este criterio no es estricto pero proporciona la estrategia necesaria para resolver con cierta coherencia la confianza de cada prueba.</p>

<h3>Tipos de prueba</h3>

<p>eXaminator está desarrollado en PHP y usa una matriz para guardar toda la información necesaria sobre cada una de las pruebas. Esto permite agregar, eliminar y modificar cada prueba individualmente con mucha facilidad, de modo que sería posible generar distintos modos de revisión. Voy a explicar el significado de algunas variables definidas en la matriz de datos de cada prueba porque ayudarán a entender las fórmulas que definen los resultados.</p>

<dl>
 <dt>Elemento (E)</dt>
<dd>Identifica un elemento del lenguaje HTML o un conjunto de estos elementos. Por ejemplo, el elemento Controles de formulario que requieren etiquetas asociadas comprende a los input de tipos text, checkbox, radio, file y password, más los elementos textarea y select. La prueba es aplicable sólo cuando el elemento existe en la página. El elemento all es especial e indica que la prueba resulta siempre aplicable.</dd>
 <dt>Situación (S)</dt>
 <dd>Identifica un elemento del lenguaje HTML o un conjunto de estos elementos que cumplen determinada condición. Siempre se trata de un subconjunto de elemento, excepto cuando elemento es all. Se debe encontrar al menos 1 situación para que la prueba sea aplicable, excepto en las pruebas de tipo falso que se aplica cuando no se encontró ninguna situación en la página.</dd>
 <dt>Nota (N)</dt>
 <dd>Es la calificación de la prueba. En las pruebas de resultado variable, es la calificación inicial a partir de la cual se efectuarán los cálculos posteriores. En otras palabras, es la calificación que se aplica a la primera situación detectada.</dd>
 <dt>Tolerancia (T)</dt>
 <dd>En las pruebas de tipo decreciente indica el umbral de tolerancia a los errores, es decir, el
  valor a partir del cual se comenzará a disminuir la nota inicial.</dd>
 <dt>Fracción (F)</dt>
<dd>En las pruebas de tipo decreciente indica la cantidad de errores que disminuyen en un punto la nota inicial. Tolerancia y Fracción son datos exclusivos para las pruebas de tipo decreciente en las cuales cada situación identifica siempre un error.</dd>
 </dl>
 
<h3>Pruebas de tipo verdadero/falso</h3>

<p>Ambas pruebas consisten en evaluar una condición y, si esa condición se cumple, el Resultado (R) es el producto de la Nota (N) y la Ponderación (P):</p>

<p>R=N*P</p>

<p>Ambas pruebas son idénticas en todo sentido excepto que la condición se debe evaluar como verdadera en un caso y como falsa en el otro para que la prueba resulte aplicable.</p>

<h3>Prueba de tipo proporcional</h3>

<p>En esta prueba, la nota inicial disminuye en proporción al cociente entre Situación (S) y Elemento (E).</p>

<p>R=N*(1-S/E)*P</p>

<p>Veamos como ejemplo la prueba sobre las alternativas textuales en las imágenes. Aquí, Elemento (E) son las imágenes y Situación (S) son las imágenes sin alt. La prueba es aplicable cuando existen ambos. La Nota (N) es la calificación inicial atribuida a este tipo de errores (en esta prueba la nota es 3 porque se considera que está mal sin importar cuántas imágenes sin <code>alt</code> se encuentren).</p>

<p>Pero la calificación puede aún ser menor si consideramos la extensión de los errores. Entonces, se calcula la tasa de fallo y luego el porcentaje a sustraer de la nota inicial. Si las imágenes son 8 y hay 4 sin alt, sin tomar en cuenta la ponderación, el cálculo sería:</p>

<p>R=3*(1-4/8)=3*(1-0.5)=3*0.5=1.5</p>

<p>La calificación inicial (3) se reduce a la mitad (1.5) porque el error está presente en el 50% de las imágenes encontradas.</p>

<h3>Prueba de tipo decreciente</h3>

<p>En esta prueba, la nota inicial va disminuyendo a medida que aumenta la cantidad de errores. La Tolerancia (T) indica cuántos errores se permiten antes de comenzar a restar de la nota; superado el umbral de tolerancia, cada Fracción (F) disminuye en 1 punto la nota inicial.</p>

<p>R=(N-(S-T)/F)*P</p>

<p>Por ejemplo, cuando existen errores de validación, la nota inicial es 5 y la tolerancia es 10. Es decir, se considera que hasta 10 errores de validación es una situación que se puede calificar como regular (la tolerancia es bastante alta por el efecto de arrastre que tienen algunos errores). Si existen más de 10 errores, la nota comienza a disminuir 1 punto por cada fracción, que en esta prueba también es de 10. Suponiendo que encontramos 40 errores, sin tener en cuenta la ponderación, sería:</p>

<p>R=5-(40-10)/10=5-30/10=5-3=2</p>

<p>Entonces, la calificación es 5 cuando existen entre 1 y 10 errores; con 40 errores la nota baja a 2 y así, si se encuentran más de 50 errores de validación la nota sería 1, la mínima.</p>

<h3>Promedio</h3>

<p>Por último, la puntuación de una página resulta de la división de la sumatoria de las pruebas realizadas por la sumatoria de las respectivas ponderaciones. Esto se puede expresar en una fórmula muy sencilla para quienes saben interpretar las notaciones matemáticas e incomprensible para quienes no. Como pertenezco al último grupo, me abstengo de incluir dicha fórmula que, en realidad, poco agregaría a mis enredadas explicaciones. Prefiero mostrar un ejemplo práctico para explicar el efecto que tienen las ponderaciones sobre la puntuación final.</p>

<p>Tomemos como ejemplo sólo 2 pruebas: la prueba A con ponderación 1 y la prueba B con ponderación 0.1, de modo que la sumatoria de las ponderaciones es 1.1. Si la nota en ambas pruebas es 9, la puntuación final será, lógicamente, 9. El resultado ponderado de la prueba A es 9 (9*1) y el de la prueba B es 0.9 (9*0.1). La sumatoria de las pruebas ponderadas es 9.9 (9+0.9), que al dividirla por la sumatoria de las ponderaciones (1.1) nos da 9 (9.9/1.1).</p>

<p>Ahora bien, supongamos que la prueba A tiene un 2 como nota, de modo que la nota ponderada sería 2 (2*1) y la sumatoria de las pruebas sería 2.9 (2+0.9). En este caso, la puntuación sería 2.6 (2.9/1.1) luego de redonderar el resultado. Pero si es la prueba B la que tiene 2, la sumatoría de las pruebas nos daría 9.2 (9+0.2) y la puntuación sería 8.4 (9.2/1.1).</p>

<p>Con este ejemplo muy sencillo se puede apreciar la importancia de la ponderación de las pruebas. Si promediáramos simplemente las notas 9 y 2, obtendríamos 5.5 pero así estaríamos poniendo en un mismo nivel a las dos pruebas cuando las ponderaciones indican que la prueba A tiene un valor muy alto y es de máxima confianza, mientras que la prueba B es mucho menos significativa. Entonces es lógico que la prueba B tenga un peso mucho menor en la puntuación final. Observen que al promediar A, que tiene una nota de 2, con B, que tiene 9, la puntuación final es 2.6, es decir, el promedio queda muy cerca de 2, que es la nota de la prueba con mayor ponderación.</p>

<p>En términos prácticos, las ponderaciones permiten establecer un necesario balance entre las pruebas e impiden que el resultado de una página dependa de una sola prueba, tal vez inexacta. Para obtener una mala puntuación el balance de las pruebas debe ser claramente desfavorable. Es necesario que se detecten varios errores y, por el contrario, que no se detecten buenas prácticas en la cantidad y con la ponderación suficiente como para compensar esos errores. No se puede achacar a la casualidad una puntuación muy baja así como una puntuación muy alta difícilmente se consiga por un golpe de suerte.</p>

<p>A veces es necesario establecer objetivos de trabajo en un sitio y las puntuaciones resultan un parámetro muy tentador. Tiene su atractivo poder decir, por ejemplo, "en tal fecha, todas las páginas evaluadas deberán alcanzar una puntuación mínima de 7" porque así la meta a alcanzar quedaría claramente definida. El problema es que no se puede usar la puntuación de un modo escolar, considerando que alcanza con 4 ó 6 para aprobar la materia.</p>

<p>Para establecer objetivos precisos es más útil considerar la ausencia de aquellos errores que se pueden verificar con mayor exactitud. El modo estricto de eXaminator es apropiado para estos casos porque, si bien calcula la puntuación de la página, pone mayor énfasis en la importancia de las pruebas y en el informe las muestra agrupadas por niveles de acuerdo a las WCAG 2.0. De este modo es sencillo poner como meta, por ejemplo, eliminar todos los errores de prioridad A y doble A antes de planificar las revisiones manuales de las páginas.</p>

<h3>Referencias</h3>

<p id="n1">1. Linkedin Carlos Benavidez. Sitio personal: carlos-benavidez.com.ar</p>
<p id="n2">2. Hera. Revisando la Accesibilidad con Estilo</p>
<p id="n3">3. Walidator (UWEM)</p>
<p id="n4">4. eXaminator</p>
<p id="n5">5. Wikipedia: Libro blanco</p>
<p id="n6">6. Accesibilidad es el arte de garantizar que, tan amplia y extensamente como sea posible,
los medios (como por ejemplo el acceso a la Web) estén disponibles para las personas,
tengan o no deficiencias de un tipo u otro. Tim Berners-Lee</p>
<p id="n7">7. Pautas de Accesibilidad al Contenido en la Web 1.0</p>
<p id="n8">8. Wikipedia Premios Stella (ridículas y escandalosas demandas judiciales)</p>
<p id="n9">9. WCAG 2.0 Traducción Candidata a ser la Oficial al Español</p>
<p id="n10">10. WCAG 2.0 Comprender las WCAG 2.0 (borrador)</p>
<p id="n11">11. WCAG 2.0 4.1.2 Nombre, función, valor</p>
<p id="n12">12. WCAG 2.0 H65: Using the title attribute to identify form controls when the label element
cannot be used (en inglés)</p>
<p id="n13">13. WCAG 2.0 G167: Using an adjacent button to label the purpose of a field (en inglés)</p>
<p id="n14">14. Wikipedia Roberto Arlt</p>
<p id="n15">15. Wikipedia Lord Kelvin</p>
<p id="n16">16. Wikipedia Medida ordinal</p>
<p id="n17">17. Unified Web Evaluation Methodology (UWEM) (en inglés)</p>
<p id="n18">18. Quantitative Metrics for Measuring Web Accessibility Vigo, M., Arrue, M., Brajnik, G.,
Lomuscio, R., and Abascal, J. (2007) (en inglés)</p>
<p id="n19">19. WCAG 2.0 G1: Adding a link at the top of each page that goes directly to the main
content area (en inglés)</p>
<p id="n20">20. Website Accessibility Conformance Evaluation Methodology 1.0 (en inglés)</p>
<p id="n21">21.Evaluating Websites for Accessibility (en inglés)</p>
<p id="n22">22. Unidade Acesso Acessibilidade eletrónica para cidadãos com necessidades especiais
(en portugués)</p>
<p id="n23">23. TAW Monitor</p>
<p id="n24">24. Linkedin Daniel Low</p>
<p id="n25">25. Linkedin Jorge Fernandes</p>
<p id="n26">26. Linkedin Cláudia Cardoso</p>
<p id="n27">27. UMIC Luis Magalhães</p>
<p id="n28">28.Linkedin Sofía Benavidez</p>
<p id="n29">29.Linkedin Ramiro Benavidez</p>

</div>
