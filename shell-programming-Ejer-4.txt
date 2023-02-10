#!/bin/bash

function sucesion(){

        var0=$1
        shift
        while [ $# -gt 2 -a $(($1+var0)) -eq $2 ]
        do
                shift
        done
        if [ $# -eq 2 -a $2 -eq $(($1+var)) ]
        then
                echo "Los argumentos sí cumplen la sucesión"
        else
                echo "Los argumentos no cumplen la sucesión"
        fi

}

function contar(){

        echo "Introduce el nombre de un nuevo directorio"
        read dir1
        [ -d $dir1 ] && ls $dir1 | wc -l > recuento || echo "Este directorio no existe"

}

function potencia(){

        echo "Introduce un número entero positivo mayor que 0"
        read num1
        for i
        do
                echo $i elevado a $num1 $(($i**$num1))
        done
}


if [ $# -lt 3 ]
then
        echo "Error de sintaxis"
else
        while
                echo "Menu:"
                echo "[S] Sucesion"
                echo "[C] Contar"
                echo "[P] Potencia"
                echo "[F] Fin"
                echo -n "Introduce opción"
                read op
                [ "$op" != "F" -a "$op" != "f" ]
        do
                case $op in
                        S|s) sucesion $*;;
                        C|c) contar;;
                        P|p) potencia $*;;
                        F|f) echo "Fin del programa";;
                        *) echo "Opción incorrecta";;
                esac
        done
fi