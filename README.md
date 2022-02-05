# Python

Sesión tomada en Google Colab

[Google Colaboratory](https://colab.research.google.com/drive/1cfM9Z5mEqh84W0Xn3vHhekocBkaglILU)

## ¿Qué es Python?

Python es un lenguaje de programación **interpretado**, lo que significa que un *interpretador* ejecuta y ejecuta su código línea por línea en lugar de compilarlo.

Python tiene una sintaxis elegante que te obliga a **aplicar sangría a tu código para construir bloques de código**, por lo que Python no usa `{}` para bloques de código. No es común usar punto y coma en Python (`;`) al final de cualquier oración. Otra cosa interesante de Python es que no necesita declarar variables, solo las define, y sucede que Python **se escribe dinámicamente**.

## Luego de practicar en el Colab, hacer el ejercicio 5

Ejemplo 5

Función **ValidarFecha**: Recibe un día, mes y año correspondiente a una fecha y devuelve si la fecha es correcta o no. Simplemente miramos si el día indicado es mayor que 1 y menor que los días del mes. Si introducimos un mes incorrecto, la función **DiasDelMes** devuelve 0 por lo tanto la fecha va a ser incorrecta. 

- Parámetros de entrada: día, mes y año
- Dato devuelto: Valor lógico indicando si es correcta (Verdadero) o no (Falso)

```python
# Merengue
# Funcion para validar fecha
def DiasDelMes(dia, mes, año):
  if dia*mes*año <= 0:
    valor = 0
  mes_31 = [1,3,5,7,8,10,12]
  mes_30 = [4,6,9,11]
  if mes == 2:
    valor = dia <= 29
  elif mes in mes_30:
    valor = dia <= 30
  elif mes in mes_31:
    valor = dia <= 31
  else:
    valor = 0
  return valor

def ValidarFecha(valor):
  if valor == 0:
    valor = False
    print('Error en la fecha \n', valor)
  else:
    print('La fecha es correcta \n', valor)

print('Ingrese la fecha, use los números de los meses\n')
dia = int(input('Ingrese el dia: '))
mes = int(input('Ingrese el mes: '))
año = int(input('Ingrese el año: '))

valor = DiasDelMes(dia,mes,año)
ValidarFecha(valor)
```

Obtenemos la siguiente salida

![Untitled.png](Python%207bc0f6653e1a43fca187b5af10952b2d/Untitled.png)

Repositorio propio de los programas + el reto.