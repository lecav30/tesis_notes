Projects Panel:
- [ ] *Recents* **title** se *corta*
- [ ] El widget de proyectos no tiene la misma altura del **button** *New*

Creation Assistant:
- [ ] *Default language* ocultar
- [ ] *Create git repository* 
	- [ ] Añadir propiedad booleana **versions** o similar para indicar que soportara versiones con Git (Realizar cambios en SQLite)
	- [ ] Iniciar repositorio Git en el **projectPath**

Backend Dashboard:
- [ ] Cargar *fields* automáticamente según el currentTransaction (transaction[0])
- [ ] DB
	- [ ] Create Table Dialog
		- [ ] Limpiar input luego de ingresar un **Transaction**
	- [ ] Crear un widget personalizado para las tablas listadas para poder acceder a los botones de editar y eliminar **o** al igual que en la parte de *fields* agregar los botones en la parte superior
- [ ] Fields
	- [ ] Add Field Dialog
		- [ ] Limpiar input luego de ingresar un **Field**
		- [ ] No se debería poder elegir más Primary Key
		- [ ] En el caso de marcar como Foreign Key, mostrar un ComboBox o algún campo extra para elegir a que tabla haría referencia [Se requiere añadir lógica]
		- [ ] Cambiar el ComboBox de los constraints por algo que permita elección múltiple (puede ser nulo, unique y otros a la vez) [Se requiere cambiar lógica]
	- [ ] Buttons
		- [ ] El ícono *Edit* debería hacer posible la edición, por ejemplo: doble click para la edición de los cambios de nombre, aparecer un ComboBox para el cambio de tipo, permitir hacer el check o quitarlo en el foreign key (acá habría que revisar la lógica detrás) y mostrar otro ComboBox para los constraints
		- [ ] El ícono *Eliminar* debería permitir seleccionar elementos para removerlos al guardar.
		- [ ] Para ambos botones, como modifican el comportamiento de la tabla, se tendría que ver si agregar un botón extra que sirva para guardar esos cambios o si al momento de activar alguna opción cambiar el ícono por el de "guardar" para que al volver a presionarlo se guarden los cambios.
- [ ] Methods
	- [ ] Los checks deberían reflejarse en el código, o sea, agregar validaciones en las plantillas Inja, ejemplo: si no se desea una ruta para eliminar, se desactiva el checkbox de *delete*. Una propiedad booleana debería cambiar a false y hacer que la plantilla Inja no considere dicha ruta.