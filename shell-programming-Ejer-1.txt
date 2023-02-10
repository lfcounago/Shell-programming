#!/bin/bash

opcion=0

while [ $opcion != 3 ]
do
        echo "Menu:
                1) Visualizar un listado largo del directorio de trabajo
                2) Visualizar el directorio de trabajo
                3) Salir
                Pulse una Opcion:"

        read opcion

        case $opcion in
                1) echo `ls -l`;;
                2) echo `ls`;;
                3) echo "Fin del programa";;
                *) echo "Opción errónea";;
        esac
done