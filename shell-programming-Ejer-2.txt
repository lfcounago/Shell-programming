#!/bin/bash

#Apartado a)
while `test $# != 0`
do
        echo $*
        shift 1
done

#Apartado b)
for((i=0;i<100;i++))
do
        echo $i
done

#Apartado c)
sum=0
mul=1
for((j=1;j<=$#;j++))
do
        ((sum=$sum+$j))
        ((mul=$mul*$j))
done
echo Suma: $sum
echo Producto: $mul