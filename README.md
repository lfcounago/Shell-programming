# Shell-programming

# Ejercicio 1
Realiza un script que muestre en pantalla el siguiente menú:
Menu
1) Visualizar un listado largo del directorio de trabajo
2) Visualizar el directorio de trabajo
3) Salir

Si el usuario pulsa una opción inexistente, el programa debe mostrar el mensaje opción errónea. El menú sólo se mostrará una vez. Si el usuario selecciona la opción 3 (Salir) se mostrará el mensaje Fin del programa. Modifica el script de forma que se muestre el menú en pantalla hasta que el usuario pulse la opción 3 (Salir). Además, el script debe permitir que el usuario también pueda introducir las distintas opciones del menú mediante literales (uno, dos, .., etc).

# Ejercicio 2
Escribe tres scripts:

a) Un script que devuelva los argumentos del script pero de la siguiente manera:
1ª línea - todos los argumentos
2ª línea - todos los argumentos menos el 1
3ª línea - todos los argumentos menos el 1 2
4ª línea - todos los argumentos menos el 1 2 3
última línea - el último argumento.

b) Un script que devuelva por pantalla todos los números que hay entre 0 y 99, ambos
inclusive.

c) Y por último otro que calcule la suma y el producto de los argumentos proporcionados al
script.

# Ejercicio 3
Crear un script con comandos de Linux que admita dos o más argumentos; de forma que si no es así debe visualizar el mensaje “Error de sintaxis”. Una vez comprobado esto, debe presentar el siguiente menú por pantalla y programar las opciones según se detallan a continuación. Una vez terminada cada opción debe volver a mostrarse el menú y así sucesivamente hasta que escoja la opción “Fin”:

Menú:

  [Uno] Sumar argumentos múltiplos de 3

  [Dos] Ficheros con permiso de escritura

  [Tres] Ocurrencias del nombre del script

  [Fin] Fin

Opciones:

  [U, Uno o uno]: Calcular y mostrar por pantalla la suma de los números múltiplos de 3 que se le pasan como argumentos al script.

  [D, Dos o dos]: Solicitar al usuario que introduzca el nombre de un fichero y comprobar que dicho fichero tiene permiso de escritura. Si se cumple esto, informar de ello mediante un mensaje que contenga el nombre del fichero. En el caso de que no se cumpla se visualizará el mensaje “No existe ese fichero o no tiene permiso de escritura”. No se puede usar la orden if.

  [T, Tres o tres]: Calcular y mostrar por pantalla el número de veces que el nombre del script coincide con los argumentos que se le pasan al script. Se deben usar las órdenes shift y until.

  [Fin]: Salir del menú. Al salir del menú se debe mostrar el mensaje “Fin del programa” y se acabará el script.

# Ejercicio 4
Crear un script con comandos de Linux que admita dos o más argumentos; de forma que si no es así debe visualizar el mensaje Error de sintaxis. Una vez comprobado esto, debe presentar el siguiente menú por pantalla y programar, mediante funciones, las opciones según se detallan a continuación. Una vez terminada cada opción debe volver a mostrarse el menú y así sucesivamente hasta que escoja la opción “FIN”:

Menú: 

  [O] Ordenados

  [D] Directorio

  [L] Listado

  [R] Resto

  [C] Contar

  [F] FIN

Opciones:

  O u o: Considerando los argumentos del script como números enteros, comprueba si están o no ordenados de forma ascendente, e informa mediante un mensaje de ello. Si algún argumento rompe el orden ascendente no se debe continuar comprobando el resto de argumentos.

  D o d: Solicita al usuario el nombre de un directorio existente y comprueba si cada argumento del script es o no un fichero que podemos ejecutar. En el caso de que sea un fichero ejecutable se debe crear un enlace de ese fichero en el directorio cuyo nombre se ha obtenido del usuario. En cualquier otro caso se visualizará el mensaje “No es un fichero o no puedo ejecutarlo”. No se puede usar la orden if.

  L o l: Muestra mediante distintos mensajes el número de directorios y ficheros no vacíos existentes entre los argumentos recibidos por el script. Si algún argumento no es un directorio o no es un fichero no vacío se visualizará el mensaje “No es un fichero no vacío o directorio”.

  R o r: Considerando los argumentos del script como números enteros, visualiza por pantalla el resto de dividir cada argumento con el siguiente argumento, es decir, el resto entre el primer y segundo argumento, resto entre el segundo y tercero, y así sucesivamente. Se debe tener en cuenta que no se puede dividir por cero.

  C o c: Solicitar al usuario que introduzca el nombre de un nuevo fichero y comprobar que no existe. Si se cumple esto, mediante un solo comando, almacenar en dicho fichero el número de líneas, palabras y bytes de todos los ficheros dados como argumentos del script (no es necesario comprobar si son o no ficheros). En el caso de que se trate de un fichero existente visualizar el mensaje “Ese fichero ya existe”. No se puede usar la orden if. F o f: Sale del menú. Al salir del menú se debe mostrar el mensaje “Fin del programa” y finalizará el script.

# Ejercicio 4
Crear un script con comandos de Linux que admita tres o más argumentos; de forma que si no es así debe visualizar el mensaje Error de sintaxis. Una vez comprobado esto, debe presentar el siguiente menú por pantalla y programar, mediante funciones, las opciones según se detallan a continuación. Una vez terminada cada opción debe volver a mostrarse el menú y así sucesivamente hasta que escoja la opción “FIN”:

Menú 

[S] Sucesión

[C] Contar

[P] Potencia

[F] FIN

Opciones:
 
S o s: Considerando los argumentos del script como números enteros, informa mediante un mensaje si los argumentos cumplen o no la siguiente sucesión: cada argumento, excepto el primero, se obtiene sumando al argumento anterior el valor del primer argumento. Si algún argumento rompe esta sucesión no se debe continuar comprobando el resto de argumentos.

C o c: Solicitar al usuario que introduzca el nombre de un nuevo directorio y comprobar que existe. Si se cumple esto, se debe suponer que todos los elementos contenidos en dicho directorio son ficheros, es decir, no es necesario comprobar si son o no ficheros. Almacenar en un fichero llamado recuento el número de ficheros que cuelgan de ese directorio. En el caso de que se trate de un directorio inexistente visualizar el mensaje “Ese directorio no existe”. No se puede usar la orden if.

P o p: Solicitar al usuario que introduzca un número entero positivo mayor que 0 (no es necesario comprobar que se cumple está condición) y presentar por pantalla el resultado de elevar cada argumento del script al número introducido. Los argumentos del script deben ser tratados como números. F o f: Sale del menú. Al salir del menú se debe mostrar el mensaje “Fin del programa” y finalizar el script.
