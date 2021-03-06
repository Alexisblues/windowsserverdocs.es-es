---
title: Guía de estilo de texto y diseño de la interfaz de usuario del centro de administración de Windows
description: Guía de estilo de texto y diseño de la interfaz de usuario del centro de administración de Windows SDK
ms.topic: article
author: jasongerend
ms.author: jgerend
ms.date: 01/17/2020
ms.localizationpriority: medium
ms.openlocfilehash: a784bdfdfbfbbc4f91579d40cedb22230a70b13a
ms.sourcegitcommit: 68444968565667f86ee0586ed4c43da4ab24aaed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/07/2020
ms.locfileid: "87993585"
---
# <a name="windows-admin-center-ui-text-and-design-style-guide"></a>Guía de estilo de texto y diseño de la interfaz de usuario del centro de administración de Windows

>Se aplica a: Windows Admin Center

En este tema se describe el enfoque general para escribir texto de la interfaz de usuario (UI) para el centro de administración de Windows, así como algunas convenciones y enfoques específicos que estamos llevando a cabo.

El centro de administración de Windows y todas las extensiones deben seguir los [principios de voz de Microsoft](/style-guide/brand-voice-above-all-simple-human) para que la experiencia sea fácil de usar y de fácil uso. Esta guía de estilo se basa en estos principios de voz, así como en la [Guía de estilo de escritura de Microsoft](/style-guide/welcome/), por lo que debe asegurarse de consultar ambos recursos para obtener información sobre aspectos como la [accesibilidad](/style-guide/accessibility/accessibility-guidelines-requirements), los [acrónimos](/style-guide/acronyms)y la [elección de palabras](/style-guide/word-choice/) , como [por](/style-guide/a-z-word-list-term-collections/p/please)ejemplo, y [lo sentimos](/style-guide/a-z-word-list-term-collections/s/sorry).

## <a name="buttons"></a>Botones

- Los botones deben ser una palabra siempre que sea posible, especialmente si tiene previsto localizar la herramienta. Dos o tres son correctos, pero intentan evitar más tiempo. Si tiene cuatro palabras o más, sería mejor utilizar un control de vínculo.
- Las etiquetas de los botones deben ser concisas, específicas y autoexplicativas. En lugar de un botón "enviar" genérico, use un verbo que se corresponda con la acción del usuario, como "crear", "eliminar", "agregar", "formato", etc.
- Si un botón sigue a una pregunta, su etiqueta debe corresponderse claramente a la pregunta (normalmente "sí" o "no").

## <a name="capitalization"></a>Uso de mayúsculas

Seguimos el estilo de Microsoft [para usar](/style-guide/capitalization) las mayúsculas y minúsculas con el estilo de oraciones en casi todo.

| Elemento de la interfaz de usuario              |Uso de mayúsculas|Comentarios|
|-------------------------|--------------|--------|
|Distintivos (como versión preliminar) |Todo mayúsculas      ||
|Todo lo demás          |Estilo de oraciones|Sin embargo, hay algunas excepciones en las que se muestran las propiedades de objeto de WMI o PowerShell que se encuentran fuera de nuestro control.|

## <a name="colons"></a>Dos puntos

Use dos puntos para introducir listas. Por ejemplo:

Elija alguna de las acciones siguientes:

Gatos de perros quokkas

No use signos de dos puntos en el texto de la interfaz de usuario cuando una etiqueta esté en una línea diferente de lo que se etiqueta o cuando haya una distinción clara entre la etiqueta y el elemento que tiene el etiquetado.

Use los dos puntos en el texto de la interfaz de usuario cuando una etiqueta esté en la misma línea que el texto que etiquete y necesite mantener juntos los dos elementos.

## <a name="confirmation-messages"></a>Mensajes de confirmación

Los cuadros de diálogo de confirmación son útiles cuando la continuación puede tener resultados inesperados, como la pérdida de datos. Deben contener información útil digitalizable con un resultado claro, especialmente para los eventos que no se pueden revertir.

- Asegúrese de que es necesario realizar una confirmación. Si no hay información nueva para ofrecer (por ejemplo, "¿está seguro?"), es posible que no sea necesario un mensaje de confirmación.
- Compruebe que el cliente desea continuar con la acción.
- Asegúrese de que la instrucción principal (encabezado) y el texto explicativo (cuerpo) no son redundantes.
- En el encabezado, defina los resultados posibles como una pregunta o una instrucción sobre lo que ocurrirá a continuación. Por ejemplo, "borrar todos los datos de esta unidad? o bien, "está a punto de borrar todos los datos".
- Agregue detalles en el cuerpo. Si hay una variable, como el nombre del elemento que se va a cambiar, inclúyalo aquí.
- Incluya una pregunta sencilla (ya sea en el encabezado o en el cuerpo) que enmarque una opción clara entre dos botones de acción.
- Para una elección compleja, use los botones sí/no, que fomentan una lectura cuidadosa. Para una opción más sencilla, use los botones que son específicos de la acción, como eliminar todos o cancelar.

## <a name="first-run-experiences"></a>Experiencias de primera ejecución

La primera vez que un usuario visita una página, tiene la oportunidad de ayudarle a empezar a trabajar con la herramienta. Esto podría ser:

- Una cadena de texto en una página vacía con instrucciones breves sobre cómo empezar, por ejemplo, "seleccione" agregar "para agregar una aplicación".
- Un vínculo al control que obtiene el usuario iniciado, por ejemplo, "agregar una aplicación para empezar".
- Animaciones o vídeos pequeños y cortos que muestran al usuario Cómo empezar

Estas son algunas sugerencias de nuestra guía de estilo de Windows:

### <a name="1-be-helpful"></a>1. ser útil

- Evite el estilo de marketing y el idioma.
- Cuando Demo o sugiera algo, asegúrese de que el resultado final es claro; con solo mostrar al cliente cómo hacer algo no es efectivo si no saben por qué lo hacen.
- No presente sugerencias si el cliente no las necesita.

### <a name="2-show-dont-tell"></a>2. Mostrar, no decir

Mantenga el texto lo más sencillo posible (cree animaciones o vídeos pequeños).

### <a name="3-dont-overwhelm"></a>3. no sobrecargar

- Limite los elementos emergentes y sugerencias a 4 por cada sesión de uso combinada, incluidas las notificaciones del sistema y las notificaciones de Shell.
- Asegúrese de que el control de tiempo de los elementos emergentes sea útil.
- No Evite que el cliente haga algo.
- Asegúrese de que los elementos emergentes se descartan fácilmente.

### <a name="4-keep-it-contextual"></a>4. mantener contextual

- Los momentos de enseñanza son más eficaces cuando se presentan en el momento adecuado.
- Si crea tutoriales o presentaciones de diapositivas, mantenga la información concreta.
- Sin Marketing "desenfadados", se centra en consejos y trucos específicos.
- Proporcionar una manera para que los clientes vuelvan al tutorial más adelante, si es pertinente (a menudo, las personas no conservan la información por primera vez, pero las instrucciones de configuración pueden ser solo relevantes una vez).
- La mensajería en estado vacío es un lugar natural para el aprendizaje o la alegría, por lo que es muy sencillo e informativo.

### <a name="5-minimize-painful-setup"></a>5. minimice la configuración complicada

Cuando necesite que el cliente realice otra acción para experimentar el valor completo (inicio de sesión en un servicio en línea, etc.), haga que sea tan sencillo como sea posible.

- La mensajería debe ser breve y directa.
- Evite enviarlos. Si es posible, proporcione un medio para conectarse desde donde estén.
- Si es posible, permita la opción para hacerlo más adelante y, a continuación, recuérdeles que lo hagan más adelante.
- Si saca provecho de su experiencia, proporcione una manera de volver rápida y fácilmente.

## <a name="help-links"></a>Vínculos a la Ayuda

Estas son algunas sugerencias de nuestra guía de estilo de Windows:

### <a name="when-should-we-provide-a-help-link"></a>¿Cuándo se debe proporcionar un vínculo de ayuda?

Casi nunca. Proporcione un vínculo de ayuda solo cuando:

- Hay una pregunta obvia y evidente que es probable que tengan los clientes mientras están en la interfaz de usuario, la respuesta a la que les ayudará en la tarea de interfaz de usuario.
- No hay espacio suficiente en la interfaz de usuario para proporcionar la cantidad de información necesaria para que los usuarios se ejecuten correctamente en la tarea de la interfaz de usuario.

### <a name="where-should-help-links-appear"></a>¿Dónde deberían aparecer los vínculos de ayuda?

- Los vínculos de texto deben aparecer tan cerca del elemento de la interfaz de usuario a la que se dirige la ayuda en la medida de lo posible.
- Si debe proporcionar un vínculo de texto que se aplique a toda la pantalla de la interfaz de usuario, colóquelo en la parte inferior izquierda de la pantalla.
- Si proporciona un vínculo a través de un botón ayuda (?), la información sobre herramientas debe ser "ayuda".

### <a name="what-url-should-we-use"></a>¿Qué dirección URL debería usar?

No vincule nunca directamente a una dirección web; en su lugar, use un servicio de redireccionamiento.

Los desarrolladores de Microsoft deben usar un FWLink, excepto cuando se trata de un vínculo de ayuda que es posible que los usuarios tengan que escribir manualmente, en cuyo caso se usa un vínculo de aka.ms (siempre que el destino de la dirección URL sea un sitio web que reconozca automáticamente la configuración regional del explorador, como Docs.microsoft.com)

### <a name="text-guidelines"></a>Instrucciones de texto

- Usar oraciones completas.
- No incluya signos de puntuación finales salvo los signos de interrogación.
- No es necesario usar el mismo texto que el título de la tarea. Use texto que tenga sentido en el contexto de la interfaz de usuario, pero asegúrese de que hay una conexión lógica entre los dos. Por ejemplo:
- Vínculo de ayuda: ¿Cuál es el riesgo de permitir excepciones?
- Título del tema de ayuda: "permitir que un programa se comunique a través de Firewall de Windows"
- Sea lo más específico posible sobre el contenido del tema de ayuda.
    - Nuestro estilo
        - ¿Cómo ayuda Firewall de Windows a proteger el equipo?
        - Por qué los resaltados pueden mejorar una imagen
    - No es nuestro estilo
        - Más información sobre Firewall de Windows
        - Más información sobre la administración del color
        - Más información
- Use la oración completa para el texto del vínculo, no solo las palabras clave.
    - Nuestro estilo
        - [¿Cuáles son los riesgos de permitir excepciones?]()
    - No es nuestro estilo
        - ¿Cuáles son los [riesgos de permitir excepciones]()?

## <a name="error-messages"></a>Mensajes de error

Esta es una guía que se adapta a la guía de estilo de Windows:

Escribir un buen mensaje es un equilibrio entre proporcionar una explicación suficiente pero no ser demasiado técnica; entre ser casual y personable, pero no molestar o ofensivo.

### <a name="general-guidelines"></a>Directrices generales

Use un mensaje por caso de error.

#### <a name="headings"></a>Encabezados

- Manténgalo en breve y explique de manera concisa cuál es el problema o lo que es **ideal**. <br>Algunas superficies de la interfaz de usuario pueden tener encabezados que se truncan en lugar de ajustarse cuando son demasiado largos, por lo que hay que hacer un vistazo.
- Use la solución en el encabezado si se trata de un paso sencillo.
- Asegúrese de que el encabezado se relaciona directamente con el botón en caso de que el lector omita el texto del cuerpo.
- Evite el uso de "se produjo un problema" en los encabezados, a menos que no tenga ninguna otra opción. Sea más específico sobre el problema.
- Evite el uso de variables (como nombres de archivo, carpeta y aplicación) en los encabezados. Colóquelos en el cuerpo.

#### <a name="body"></a>Body

- Si el encabezado explica de manera suficiente el problema o la solución, no necesita texto de cuerpo.
- No repita el título en el mensaje con un texto ligeramente diferente.
- Comunique de forma clara y concisa cuál es la solución.
- Céntrese primero en asignar los hechos.
- No se preocupe por el error.
- Si hay un código de error asociado al error y piensa que, si se incluye el código de error, el cliente o el servicio de soporte técnico de Microsoft pueden investigar el problema, incluirlo directamente debajo del texto del cuerpo y escribirlo de la manera siguiente:

    Código de error: ####

    Si el cliente tiene toda la información necesaria para resolver el error sin el código, no es necesario incluirlo.

#### <a name="buttons"></a>Botones

- Escriba el texto del botón para que sea una respuesta específica a la instrucción principal. Si no es posible, use "cerrar" para el texto del botón descartado (en lugar de "Aceptar" o "listo").
- Si tiene más de un botón, haga que el botón situado más a la izquierda sea la acción que el usuario debe realizar. Haga que el botón situado más a la derecha sea la acción más conservadora, como "Cancelar".

#### <a name="help-links"></a>Vínculos a la Ayuda

Tenga en cuenta solo los vínculos de ayuda para los mensajes de error que no puede hacer específicos y que se puedan realizar en acción.

## <a name="null-state-text"></a>Texto de estado null

Esta es la ayuda de la guía de estilo de Windows.

El estado NULL se produce cuando los datos o el contenido del cliente no están presentes en una aplicación o característica, cuando no se devuelve ningún resultado después de una búsqueda o cuando falta información necesaria en un formulario, como la información de facturación de una transacción.

### <a name="guidelines"></a>Instrucciones

- Si es posible, utilice situaciones de estado NULL como una oportunidad para enseñar a las personas cómo usar la característica (por ejemplo, cómo agregar música, dónde buscar imágenes, etc.).
  - Si tiene un título en la interfaz de usuario, explique la acción que se debe realizar para "corregir" el estado null (por ejemplo, "agregar música")
  - Diviértase con el texto. Este espacio puede ser una oportunidad para proporcionar alegría, ya que probablemente no se verá varias veces.
  - Evite "se no hay nada aquí". Es Sad y se ha sobreutilizado.
  - ¿Desea evitar preguntas como "¿no ha conectado la impresora?" Está bien para usarse una vez, pero este formato tiende a ser sobreutilizado y las preguntas ponen en exceso la carga y la presión sobre el cliente. También puede sentir un descenso.
  - La variedad en el texto de estado NULL es una buena cosa.

### <a name="examples"></a>Ejemplos

- "Agregue a alguien como favorito y podrá verlos aquí".
- "¿Tiene algún logros o clips de juegos en los que esté especialmente orgullosos? Agréguelos a la presentación ".
- "Nadie en una entidad todavía. Empiece una vez. "
- "Si alguien lo agrega como amigo, los verá aquí".
- "Cuando haga cosas como desbloquear logros, grabar clips de juegos y agregar amigos, lo verá aquí".
- "Sus amigos favoritos aparecerán aquí, por lo que puede ver cuándo están en línea y en qué se encuentran."

## <a name="punctuation"></a>Signos de puntuación

- Sin puntuación final (puntos, signos de interrogación) para los encabezados o oraciones incompletas. Una excepción se encuentra en un cuadro de diálogo de confirmación donde el encabezado hace la pregunta
- Use la guía de Microsoft Style Guide para [puntos](/style-guide/punctuation/periods) y [signos de interrogación](/style-guide/punctuation/question-marks).

## <a name="status-messages"></a>Mensajes de estado

Los mensajes de estado se componen de mensajes emergentes (notificación del sistema) y notificaciones.

|Tipo de cadena         | Notas                               |
|------------        |-------------------------------------|
|Notificación del sistema               |Caso de oración con puntuación final: idealmente con una variable de objeto para que los usuarios puedan comprender a qué objeto se aplica el mensaje en caso de que se haya desplazado fuera del objeto|
|Encabezado de la notificación (título) |Caso de oración sin puntuación final (es un encabezado), idealmente con una variable de objeto|
|Detalles de la notificación|Oraciones completas, idealmente con un vínculo a la interfaz de usuario que muestra el objeto|

Estas son algunas recomendaciones detalladas para los mensajes de notificación:

|Tipo de cadena         | Notas                               |
|------------        |-------------------------------------|
|Iniciado             |Omitir cuando sea posible: normalmente puede pasar al mensaje en curso para minimizar el número de distracciones.|
|En curso         |Comience con el verbo de la acción que está llevando a cabo y termine con puntos suspensivos para indicar una operación en curso. Este es un ejemplo:<br> *Creando el volumen ' datos del cliente '...* <br><br>Cuando haya varias variables, use este patrón: <br>*Eliminando la siguiente máquina virtual: {0} ; Organizar{1}* |
|Correcto             |Comience con "correctamente" y acabe con lo que acaba de hacer el software. Este es un ejemplo:<br> *El volumen ' datos del cliente ' se creó correctamente.*|
|Error             |Comience con "no se pudo" y termine con lo que el software no pudo hacer. Este es un ejemplo:<br> *No se pudo crear el volumen ' datos del cliente '.*|

## <a name="tooltips"></a>Información sobre herramientas

Una buena información sobre herramientas describe brevemente los controles sin etiqueta o proporciona un poco de información adicional para los controles etiquetados, cuando esto resulta útil. También pueden ayudar a los clientes a navegar por la interfaz de usuario ofreciendo información adicional, no redundante, sobre etiquetas de control, iconos, vínculos, etc.

La información sobre herramientas debe usarse con moderación o no. Pueden ser una interrupción para el cliente, por lo que no incluya una información sobre herramientas que simplemente repite una etiqueta o indica el obvio. Siempre debe agregar información valiosa.

|    Context                                 |    Cómo escribir la información sobre herramientas    |
|    -----------------------                 |    -------------------------    |
|Cuando un control o un elemento de la interfaz de usuario no tiene etiqueta...|Use una frase de nombre simple y descriptiva. Por ejemplo:<br> Lápiz de resaltado |
|Cuando se etiqueta un elemento de la interfaz de usuario, pero su propósito necesita aclaración...|<ul><li>Describa brevemente lo que puede hacer con este elemento de la interfaz de usuario. </li><li>Use el formulario de verbo imperativo. Por ejemplo, "buscar texto en este archivo" (no "busca texto en este archivo").</li><li>No incluya signos de puntuación finales a menos que haya varias oraciones completas.</li> </ul>|
|Cuando una etiqueta de texto se trunca o es probable que se trunque en algunos lenguajes...|<ul><li>Proporcione la etiqueta untruncada en la información sobre herramientas.</li><li>Opcional: en otra línea, proporcione una descripción clara, pero solo si es necesario.</li><li>No proporcione información sobre herramientas si la información no truncada se proporciona en otra parte de la página o el flujo.</li></ul>|
|Si hay disponible un método abreviado de teclado...|<ul><li>Opcional: proporcione el método abreviado de teclado entre paréntesis después de la etiqueta o frase descriptiva, por ejemplo, "Imprimir (Ctrl + P)" o "buscar texto en este archivo (Ctrl + F)".</li><li>Es correcto agregar un método abreviado de teclado útil a la información sobre herramientas de clarificación, pero evite agregar información sobre herramientas solo para mostrar un método abreviado de teclado. </li></ul>|