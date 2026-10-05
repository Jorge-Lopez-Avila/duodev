# Ficha de idea — DuoDev

## Ruta elegida y motivo
Aplicación móvil Android nativa desarrollada en Kotlin con Jetpack Compose.
Se elige Kotlin nativo porque la materia lo exige y porque permite una app
offline, sólida y sin dependencias de backend. DuoDev enseña fundamentos
del lenguaje C mediante lecciones cortas y ejercicios interactivos.

## Usuario y contexto
Estudiante de primer semestre de ingeniería o programación, entre 17 y 20
años, que cursa una materia de fundamentos de programación en C. Usa la
app en el transporte público, en ratos libres en el campus o en su casa,
en sesiones de 5 a 15 minutos, generalmente sin internet confiable.

## Problema observable (una frase)
Los estudiantes que empiezan a programar en C no tienen una forma corta,
diaria y móvil de practicar sintaxis y lógica, y terminan memorizando sin
retroalimentación inmediata.

## Alternativa actual
Ver videos largos, leer apuntes, copiar código del pizarrón y usar
compiladores de escritorio que no son portables ni ofrecen práctica guiada.

## Tarea principal
Completar una lección diaria de C (teoría breve + ejercicios interactivos)
para mantener la racha y ganar XP.

## Criterio de éxito
Un estudiante completa al menos 3 lecciones en una semana, su racha
aumenta y logra identificar correctamente al menos 5 conceptos nuevos
de C (variables, printf, if, while, funciones).

## Alcance de la primera versión
- Onboarding con meta diaria.
- Mapa de 3 unidades y ~20 lecciones.
- Lecciones con teoría breve y ejercicios interactivos.
- Tipos de ejercicio: opción múltiple, completar hueco, ordenar líneas,
  predecir salida, verdadero/falso, emparejar y seleccionar el error.
- Sistema de XP, niveles, racha y logros.
- Reto diario.
- Widget con racha y reto del día.
- Recordatorio diario.
- Funcionamiento 100% offline con Room + DataStore.

## Funciones aplazadas de forma deliberada
- Ejecución o compilación real de código C.
- Editor de código libre.
- Backend, login social, ranking online y pagos.
- Soporte para varios lenguajes de programación.
- Generación de contenido con IA.
- Tests automáticos avanzados.

## Hipótesis pendiente de validar
"Los estudiantes de primer semestre prefieren practicar C en el móvil en
sesiones cortas antes que en un compilador de escritorio."

## Evidencia
Hipótesis sin validar. Se planea aplicar una encuesta a 10–15 compañeros
de primer semestre para confirmar la preferencia de práctica móvil.

## Uso de asistentes de IA
Se utilizó ChatGPT para redactar borradores del docs/idea.md y para
generar los bosquejos de pantallas. Los textos finales y las anotaciones
de los bosquejos fueron revisados y ajustados por los integrantes.

## 1.2 Material visual

### Bosquejo del Home
![Bosquejo del Home](img/bosquejos/01-home.png)
*Bosquejo del Home. Generado con IA (ChatGPT) y anotado por Gutiérrez Prats Hervey Gabriel.*

### Bosquejo de la lección
![Bosquejo de la lección](img/bosquejos/02-leccion.png)
*Bosquejo de la lección. Generado con IA (ChatGPT) y anotado por Linares Villegas Gustavo.*

### Bosquejo de opción múltiple
![Bosquejo de opción múltiple](img/bosquejos/03-opcion-multiple.png)
*Bosquejo de opción múltiple. Generado con IA (ChatGPT) y anotado por López Avila Jorge.*

### Bosquejo de resultado
![Bosquejo de resultado](img/bosquejos/04-resultado.png)
*Bosquejo de resultado. Generado con IA (ChatGPT) y anotado por Gutiérrez Prats Hervey Gabriel.*

### Bosquejo de perfil
![Bosquejo de perfil](img/bosquejos/05-perfil.png)
*Bosquejo de perfil. Generado con IA (ChatGPT) y anotado por Linares Villegas Gustavo.*

### Estados no felices
![Estados no felices](img/bosquejos/06-estados-no-felices.png)
*Estados no felices: carga, lista vacía, error y datos inválidos. Generado con IA (ChatGPT) y anotado por López Avila Jorge.*

### Diagrama de recorrido del usuario
![Recorrido del usuario](img/recorrido.png)
*Diagrama de recorrido. Elaborado por Gutiérrez Prats Hervey Gabriel con Mermaid.*

## 1.3 Historia de usuario y criterio de aceptación

### Historia principal
Como estudiante de primer semestre que aprende C,
quiero completar una lección corta desde mi celular con ejercicios interactivos,
para practicar sintaxis y lógica, y recibir retroalimentación inmediata
sin depender de un computador.

### Criterio de aceptación
Dado que el estudiante está en el Home con una lección desbloqueada,
cuando responde correctamente todos los ejercicios de la lección,
entonces la app marca la lección como completada, suma el XP correspondiente
y actualiza la racha del día.

### Verificación
Otra persona puede abrir la app, completar esos pasos y responder sí o no
sin interpretar. El criterio es verificable.

### Historias secundarias
1. Como estudiante, quiero ver mi racha en el Home para motivarme a practicar
   todos los días. Dado que completé al menos una lección hoy, cuando abro el
   Home, entonces veo mi racha incrementada en 1.
2. Como estudiante, quiero recibir un recordatorio diario para no perder la
   racha. Dado que configuré una hora de recordatorio, cuando llega esa hora
   y no he practicado, entonces recibo una notificación.
3. Como estudiante, quiero ver mi progreso en el mapa de unidades para saber
   qué sigue. Dado que completé una lección, cuando vuelvo al Home, entonces
   la siguiente lección aparece desbloqueada.
