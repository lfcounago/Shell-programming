#!/bin/bash
function ordenados(){

        while [ $1 -le $2 -a $# -gt 2 ]
        do
                shift
        done

        if [ $1 -le $2 -a $# -eq 2 ]
        then
                echo "Están ordenados"
        else
                echo "No están ordenados"
        fi

}

function directorio(){

        echo "Introduce un el nombre de un directorio existente"
        read dir1

        for i
        do
                [ -x $i ] && ln $i $dir1/$i || echo "No es un fichero ejecutable"
        done

}

function listado(){

        dirs=0
        files=0
        for i
        do
                if [ -d $i ]
                then
                        ((dirs++))
                elif [ -s $i ]
                then
                        ((files++))
                else
                        echo "No es un fichero no vacío o directorio"
                fi
        done

        echo "Total dirs = $dirs"
        echo "Total files = $files"

}

function resto(){

        while [ $# -gt 1 ]
        do
                if [ $2 -ne 0 ]
                then
                        echo "Resto entre $1 / $2 $(($1%$2))"
                fi
                shift
        done

}

function contar(){

        echo -n "Introduce nuevo fichero"
        read fich1
        [ ! -f $fich1 ] && wc $* > $fich1 || echo "El fichero ya existe"

}

if [ $# -lt 2 ]
then
        echo Error de sintaxis
else
        while
                echo "Menu:"
                echo "[O] Ordenados"
                echo "[D] Directorio"
                echo "[L] Listado"
                echo "[R] Resto"
                echo "[C] Contar"
                echo "[F] Fin"
                echo "Introduce opción"

                read op
                [ "$op" != "F" -a "$op" != "f" ]
        do
                case $op in
                        O|o) ordenados $*;;
                        D|d) directorio $*;;
                        L|l) listado $*;;
                        R|r) resto $*;;
                        C|c) contar $*;;
                        F|f) echo Fin del programa;;
                        *) echo Opción incorrecta;;
                esac
        done
fi
