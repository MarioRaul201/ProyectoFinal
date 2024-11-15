El comando chmod en Unix y sistemas similares (como Linux) se usa para modificar los permisos de archivos y directorios, controlando quién puede leer, escribir o ejecutar un archivo.

Tipos de permisos:

1.	Lectura (r): Permite leer el contenido del archivo o listar los archivos dentro de un directorio.
2.	Escritura (w): Permite modificar el contenido del archivo o agregar/eliminar archivos en un directorio.
3.	Ejecución (x): Permite ejecutar un archivo como un programa o acceder a un directorio.

Clases de usuarios:

- u: Usuario propietario (owner).
- g: Grupo al que pertenece el archivo.
- o: Otros usuarios (no propietarios ni del grupo).
- a: Todos los usuarios (equivale a u, g y o).

Formatos de uso:

1.	Notación simbólica:

Se especifican permisos mediante símbolos:
	
- Estructura: chmod [clase][operador][permisos] archivo
- Operadores:
- +: Agregar permisos.
- -: Quitar permisos.
- =: Asignar permisos exactos.
- Ejemplos:
- chmod u+x archivo: Añade permiso de ejecución al propietario.
- chmod g-w archivo: Quita permiso de escritura al grupo.
- chmod a=r archivo: Asigna permisos de solo lectura a todos.

2.	Notación numérica (octal):

Los permisos se representan con un número de 3 dígitos, donde cada dígito define los permisos para usuario, grupo y otros
- Valores:
	•	4 = Lectura (r).
	•	2 = Escritura (w).
	•	1 = Ejecución (x).
- Los valores se suman para combinar permisos.
	- Ejemplo:
	- chmod 754 archivo:
		- 7 (4+2+1): Usuario puede leer, escribir y ejecutar.
		- 5 (4+1): Grupo puede leer y ejecutar.
		- 4: Otros pueden solo leer.