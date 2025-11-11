EXAMEN QA – CASO DE PRUEBA (Saga Ripley )

ID del Caso: SR-PAG-REG-001
Nombre del Caso: Validar flujo de compra con cupón de descuento tras actualización del módulo de pagos
Tipo de Prueba: Regresión Funcional 
Prioridad: Alta
Severidad: Critica
Ambiente: QA
Precondiciones: Usuario Logueado, producto disponible, cupones configurados (valido expirado) , conexión estable con pasarela 

Cobertura de Flujos 

	Campo		Descripción
ID	SR-PAG-REG-001-FH
Objetivo	Verificar que el flujo de compra con cupón válido funcione correctamente tras la actualización del módulo de pagos.
Precondiciones

	Usuario logueado, producto disponible y cupón vigente.

	
Datos de Prueba

	
Pasos	1)	Iniciar sesión
2)	Agregar producto al carrito 
3)	Ingresar al  checkout
4)	Aplicar cupón
5)	Aplicar pago con visa
Resultado Esperado 	Se aplica descuento -20%, se procesa el pago correctamente y se muestra el mensaje “Compra realizada con éxito”
Resultado Obtenido	Exitoso
Evidencia	 





CUPÓN EXPIRADO

Campo	Descripción
	ID	SR-PAG-REG-001-FA
Objetivo	Verificar que el sistema muestre mensaje de error si el cupón esta vencido 
Precondiciones	Usuario logueado y cupón expirado.


	Datos de Prueba	Cupón: 
Pasos	1)	Iniciar sesión
2)	Agregar producto 
3)	Aplicar cupón expirado
4)	Continuar checkout
Resultado esperado	Mensaje: “El cupón ingresado ha expirado”
Resultado Obtenido	
Evidencia	 


Caso de Prueba: Flujo de Error – Falla en pasarela

Campo	Descripción
ID		SR-PAG-REG-001-FE
Objetivo		Verificar el comportamiento del sistema ante un fallo de conexión con la pasarela de pago.
Precondiciones 	Cupón válido y entorno con pasarela simulada con error (timeout).
Datos de prueba 	Cupon:
Pasos	1)Iniciar sesión 
2)Agregar al carrito
3)Aplicar cupon 
4)Error de pasarela
5)Confirmar compra
Resultado Esperado	Mensaje: “No se pudo procesar el pago, por favor intente nuevamente.”
	Resultado Obtenido	
Evidencia	 






PREGUNTA 2 : YouTube

Flujo Feliz
Campo	Descripción


id	YT-UP-001-FH
Objetivo	Verificar que un video válido se suba correctamente a YouTube y aparezca en la lista de videos del usuario.
	Precondiciones	Usuario logueado en YouTube, conexión estable, video en formato permitido (.mp4, .mov, .avi) y menor a 128 GB.
Datos de Prueba	  

Nombre del video 
Titulo : “Curso QA Nivel Intermedio”
Descripción: “Video de prueba”
Pasos	
1Ingresar a YouTube y abrir el botón “Subir video” 
2️Seleccionar archivo válido 
3️ Completar título y descripción 
4️ Seleccionar visibilidad (público) 
5️ Hacer clic en “Subir”
Resultado esperado	El video se sube correctamente, se muestra barra de progreso completa, y aparece en la lista de videos del usuario con mensaje “Video subido con éxito”.
Resultado Obtenido	Video subido correctamente
Evidencia	 

 Caso 2: Flujo Alterno – Error por conexión inestable

 
Evidencia :  




Caso 3: Flujo de Error – Archivo no compatible

 
