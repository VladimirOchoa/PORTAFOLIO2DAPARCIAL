## Problemas resueltos en clase con DFD
### Ejercicio 1. Contar del 1 hasta el 10 y sumar los valores. (FOR)
#### 1.1 Analisis. 
Contar del 1 al 10 dentro de una condicional, posteriormente sumar los valores en un proceso.

Se necesita utilizar el símbolo de proceso para asignar la variable suma=0, después utilizar el símbolo de ciclo de for para hacer un contador de i=1; i<=10; i++, en caso de que i sea menor a 10 se utiliza otro símbolo de proceso para ingresar s=s+i y se regressa al ciclo hasta que i sea mayor a 10 y al final se utiliza un símbolo de salida para imprimir la suma de los números.
#### 1.2 DFD
![1 (for)](https://user-images.githubusercontent.com/113395327/197660653-0f384b1e-6c99-4a26-8613-03f91649be32.png)
#### 1.3 Prueba de escritorio
|s=0|i  |i<=10|i++|s=s+i|s|
|---|---|-----|---|-----|-|
|0  |1  |si   |1  |1    |1|
|0  |1  |si   |2  |2    |2|
|0  |2  |si   |3  |3    |3|
|0  |3  |si   |4  |4    |4|
|0  |4  |si   |5  |5    |5|
|0  |5  |si   |6  |6    |6|
|0  |6  |si   |7  |7    |7|
|0  |7  |si   |8  |8    |8|
|0  |8  |si   |9  |9    |9|
|0  |9  |si   |10 |10   |10|
|0  |10 |si   |11 |     |55|
|0  |11 |no   |

#### 1.4 Entradas.
No tiene ninguna entrada.
#### 1.5 Salidas.
55.
#### 1.6 Codigo.
```dart
void main(List<String> args) {
  int s = 0;
  for (var i = 1; i <= 10; i++) {
    s += i;
  }
  print("La suma de los valores es: $s");
}
```
### Ejercicio 1. Contar del 1 hasta el 10 y sumar los valores. (WHILE)
#### 1.1 Analisis. 
Utilizar un proceso para las variables de suma y contados, despues con una condicion validar la suma de los valores del 1 al 10.

Se necesita utilizar el símbolo de proceso para asignar la variable de s=0 y c=1, después se utiliza un símbolo de decisión para preguntar si c<=10, en caso de que si sea asi se utiliza un símbolo de proceso que asigna las variables de s=c+s, después se utiliza otro símbolo de proceso que asigna las variables de c=c+1, después de regresa al símbolo de decisión y así repetidamente hasta que c sea mayor a 10 y finalmente utilizamos un símbolo de salida para imprimir s.
#### 1.2 DFD
![1 (While)](https://user-images.githubusercontent.com/113395327/197660681-49bfc8f7-5ed8-49f0-988d-490046d78f77.png)
#### 1.3 Prueba de escritorio 
|s=0|c=1|C<=10|s=s+c|c=c+1|s|
|---|---|-----|-----|-----|-|
|0  |1  |si   |1    |2    |1|
|   |   |si   |2    |3    |2|
|   |   |si   |3    |4    |3|
|   |   |si   |4    |5    |4|
|   |   |si   |5    |6    |5|
|   |   |si   |6    |7    |6|
|   |   |si   |7    |8    |7|
|   |   |si   |8    |9    |8|
|   |   |si   |9    |10   |9|
|   |   |si   |10   |11   |10|
|   |   |no   |     |     |55|

#### 1.4 Entradas.
No tiene ninguna entrada.
#### 1.5 Salidas.
55.
#### 1.6 Codigo.
```dart
void main(List<String> args) {
  int s = 0, c = 1;
  while (c <= 10) {
    s += c;
    c++;
  }
  print("El resultado de la suma de los valores es:$s");
}
```
### Ejercicio 1. Contar del 1 hasta el 10 y sumar los valores. (DO-WHILE)
#### 1.1 Analisis. 
En Utilizar un proceso para las varibles de contador y suma, despues con otro proceso hacer la suma, y luego el contador para validar las veces.

Se necesita utilizar el símbolo de proceso para asignar la variable de s=0 y c=1, después se utiliza otro símbolo de proceso para asignar s=c+s, volvemos a utilizar otro símbolo de proceso para asignar c=c+1, después se utiliza un símbolo de decisión para preguntar si c<=10, en caso de que si sea así se regresa al símbolo de proceso de s=c+s, hasta que c sea = a 10 y finalmente utilizamos un símbolo de salida para imprimir s.
#### 1.2 DFD
![1 (Do-While)](https://user-images.githubusercontent.com/113395327/197660698-c39d7d57-68ec-4d22-b9dc-0f7546518bfd.png)
#### 1.3 Prueba de escritorio 
|s=0|c=1|s=c+s|c=c+1|c<=10|s|
|---|---|-----|-----|-----|-|
|0  |1  |1    |2    |si   |1|
|   |   |2    |3    |si   |2|
|   |   |3    |4    |si   |3|
|   |   |4    |5    |si   |4|
|   |   |5    |6    |si   |5|
|   |   |6    |7    |si   |6|
|   |   |7    |8    |si   |7|
|   |   |8    |9    |si   |8|
|   |   |9    |10   |si   |9|
|   |   |10   |11   |no   |10|
|   |   |     |     |     |55|

#### 1.4 Entradas.
No tiene ninguna entrada.
#### 1.5 Salidasl.
55.
#### 1.6 Codigo.
```dart
void main(List<String> args) {
  int s = 0, c = 1;
  do {
    s += c;
    c++;
  } while (c <= 10);
  print("El resultado de la suma de los valores es:$s");
}
```
### Ejercicio 2. Obtenga la suma de los primeros 5 numeros pares. (FOR)
#### 1.1 Analisis. 
Sumar los numeros pares del 1 al 10.

Se necesita utilizar el símbolo de proceso para asignar la variable suma=0, después utilizar el símbolo de ciclo de for para hacer un contador de i=2; i<=10; i=i+2, en caso de que i sea menor a 10 se utiliza otro símbolo de proceso para ingresar s=s+i y se regressa al ciclo hasta que i sea mayor a 10 y al final se utiliza un símbolo de salida para imprimir la suma de los números.
#### 1.2 DFD
![2 (for)](https://user-images.githubusercontent.com/113395327/197660736-9a97e4f3-b28f-404a-9f6d-fd035279e3b0.png)
#### 1.3 Prueba de escritorio 
|s=0|i  |i<=10|i+2|s=s+i|s|
|---|---|-----|---|-----|-|
|0  |2  |si   |2  |2    |2|
|0  |4  |si   |4  |4    |4|
|0  |6  |si   |6  |6    |6|
|0  |8  |si   |8  |8    |8|
|0  |10 |si   |10 |10   |10|
|0  |   |si   |12 |     |30|
|0  |   |no   |

#### 1.4 Entradas.
No tiene ninguna entrada.
#### 1.5 Salidas.
30.
#### 1.6 Codigo.
```dart
void main(List<String> args) {
  int s = 0;
  for (var i = 2; i <= 10; i = i + 2) {
    s = s + i;
  }
  print("resultado de la suma de numeros pares es:$s");
}
```
### Ejercicio 2. Obtenga la suma de los primeros 5 numeros pares. (WHILE)
#### 1.1 Analisis.
Sumar los numeros pares del 1 al 10.

Se necesita utilizar el símbolo de proceso para asignar la variable de s=0 y c=1, después se utiliza un símbolo de decisión para preguntar si c<=5, en caso de que si sea así se utiliza un símbolo de proceso que asigna las variables de s=s+C*2, después se utiliza otro símbolo de proceso que asigna las variables de c=c+1, después de regresa al símbolo de decisión y así repetidamente hasta que c sea mayor a 5 y finalmente utilizamos un símbolo de salida para imprimir s.
#### 1.2 DFD
![2 (While)](https://user-images.githubusercontent.com/113395327/197660764-11511194-e0b1-4a00-aae3-68b54143865d.png)
#### 1.3 Prueba de escritorio 
|s=0|c=1|C<=5 |s=s+c*2|c=c+1|s|
|---|---|-----|-----|-----|-|
|0  |1  |si   |2    |2    |2|
|   |   |si   |4    |3    |4|
|   |   |si   |6    |4    |6|
|   |   |si   |8    |5    |8|
|   |   |si   |10   |6    |10|
|   |   |no   |     |     |30|

#### 1.4 Entradas.
No tiene ninguna entrada.
#### 1.5 Salidas.
30.
#### 1.6 Codigo.
```dart
void main(List<String> args) {
  int s = 0, c = 1;
  while (c <= 5) {
    s = s + c * 2;
    c = c + 1;
  }
  print("resultado de la suma de numeros pares:$s");
}
```
### Ejercicio 2. Obtenga la suma de los primeros 5 numeros pares. (DO-WHILE)
#### 1.1 Analisis.
Sumar los numeros pares del 1 al 10.

Se necesita utilizar el símbolo de proceso para asignar la variable de s=0 y c=1, después se utiliza otro símbolo de proceso para asignar s=s+c*2, volvemos a utilizar otro símbolo de proceso para asignar c=c+1, después se utiliza un símbolo de decisión para preguntar si c<=5, en caso de que si sea así se regresa al símbolo de proceso de s=s+c*2, hasta que c sea mayor a 5 y finalmente utilizamos un símbolo de salida para imprimir s.
#### 1.2 DFD
![2 (Do-While)](https://user-images.githubusercontent.com/113395327/197660837-9c64bda6-9519-44c1-b2ae-735a8ee688c1.png)
#### 1.3 Prueba de escritorio 
|s=0|c=1|s=s+c*2|c=c+1|c<=5|s|
|---|---|-----|-----|-----|-|
|0  |1  |2    |2    |si   |2|
|   |   |4    |3    |si   |4|
|   |   |6    |4    |si   |6|
|   |   |8    |5    |si   |8|
|   |   |10   |6    |no   |10|
|   |   |     |     |     |30|

#### 1.4 Entradas.
No tiene ninguna entrada.
#### 1.5 Salidas.
30.
#### 1.6 Codigo.
```dart
void main(List<String> args) {
  int s = 0, c = 1;
  do {
    s = s + c * 2;
    c = c + 1;
  } while (c <= 5);
  print("la suma de numeros pares es:$s");
}
```
### Ejercicio 3. Almacene en un array el numero n leido del teclado, el tamaño del array es de 10. (FOR)
#### 1.1 Analisis. 
Debemos almacenar en 10 espacios el numero n.

Se necesita utilizar el símbolo de proceso para asignar el array A[10], después se utiliza el símbolo de entrada para almacenar los elementos en n, después utilizar el símbolo de ciclo de for para hacer un contador de i=0; i<=9; i=i+1, en caso de que i sea menor a 10 se utiliza otro símbolo de proceso para ingresar A [i]= N, y se regressa al ciclo hasta que i sea mayor a 10 y al final se utiliza un símbolo de salida para imprimir A.
#### 1.2 DFD
![3 (for)](https://user-images.githubusercontent.com/113395327/197660869-62d12335-0cbe-471c-87e0-1b17ae9c1cf6.png)
#### 1.3 Prueba de escritorio 
|A[10]|i  |i<10 |i+1|A[i]=N|A |
|-----|---|-----|---|------|--|
|0   |0   |0<10 |   |0     |0 |
|1   |1   |1<10 |1  |1     |1 |
|2   |2   |2<10 |2  |2     |2 |
|3   |3   |3<10 |3  |3     |3 |
|4   |4   |4<10 |4  |4     |4 |
|5   |5   |5<10 |5  |5     |5 |
|6   |6   |6<10 |6  |6     |6 |
|7   |7   |7<10 |7  |7     |7 |
|8   |8   |8<10 |8  |8     |8 |
|9   |9   |9<10 |9  |9     |9 |

#### 1.4 Entradas.
n.
#### 1.5 Salidas.
A.
#### 1.6 Codigo.
```dart
void main() {
  var arra = new List.filled(10, 0);
  stdout.write("Dame diez numeros\n ");
  stdout.write("----------\n");
  for (var i = 0; i <= 9; i++) {
    String? s = stdin.readLineSync();
    if (s != null) {
      int n = int.parse(s);
      arra[i] = n;
    }
  }
  stdout.write("aqui esta la lista, $arra");
}
```
### Ejercicio 3. Almacene en un array el numero n leido del teclado, el tamaño del array es de 10. (WHILE)
#### 1.1 Analisis. 
Debemos almacenar en 10 espacios el numero n.

Se necesita utilizar el símbolo de proceso para asignar el array A[10], después se utiliza el símbolo de entrada para almacenar los elementos en n, DESPUES VOLVEMOS A UTILIZAR EL SIMBOLO DE PROCESO PARA ASIGANAR C=0, DESPUES UTILIZAMOS UN SIMBOLO DE DECISION PARA PREGUNTAR SI C<=9, EN CASO DE QUE SI SE ASI ENTONCES ASIGNAMOS UN  SIMBOLO DE PROCESO DONDE A[C]=N, POSTERIORMENTE SE VUELVE A UTILIZAR OTRO SIMBOLO DE PROCESO PARA ASIGNAR C AL ARRAY A[C]= N, VOLVEMOS A UTILIZAR OTRO SIMBOLO DE PROCESO PARA ASIGNAR A[C]=N, POSTERIORMENTE UTILIZAMOS OTRO SIMBOLO DE PROCESO PRA INGRESAR C=C+1 Y SE REGRESA AL SIMBOLO DE DECISION Y ASI SUSCIVAMENTE HASTA QUE C SEA IGUAL A 9 Y FINALMENTE INGRESAMOS UN SIMBOLO DE SALIDA PARA IMPRIMIR A.
#### 1.2 DFD
![3 (While)](https://user-images.githubusercontent.com/113395327/197660901-d4ae6f43-b708-4ab3-9157-f1160f8b80af.png)
#### 1.3 Prueba de escritorio 
|A[10]|N |C=0|C<=9|A[C]=N |C=C+1|A |
|-----|--|---|------|------|----|--|
|0    |0 |0  |0<=9     |0     |1|[0]|
|1    |1 |1  |1<=9     |1     |2|[0,1]|
|2    |2 |2  |2<=9     |2     |3|[0,1,2]|
|3    |3 |3  |3<=9     |3     |4|[0,1,2,3]|
|4    |4 |4  |4<=9     |4     |5|[0,1,2,3,4]
|5    |5 |5  |5<=9     |5     |6|[0,1,2,3,4,5]|
|6    |6 |6  |6<=9     |6    |7|[0,1,2,3,4,5,6]|
|7    |7 |7  |7<=9     |7     |8|[0,1,2,3,4,5,6,7]|
|8    |8 |8  |8<=9     |8     |9|[0,1,2,3,4,5,6,7,8]|
|9    |9 |9  |9<=9     |9     |10|[0,1,2,3,4,5,6,7,8,9]|

#### 1.4 Entradas.
n.
#### 1.5 Salidas.
A.
#### 1.6 Codigo.
```dart
void main() {
  var arra = new List.filled(10, 0);
  stdout.write("Dame diez numeros\n ");
  stdout.write("----------\n");
  int i = 0;
  while (i <= 9) {
    String? s = stdin.readLineSync();
    if (s != null) {
      int ner = int.parse(s);
      arra[i] = ner;
    }
    i++;
  }
  stdout.write("Tu lista es, $arra ");
}
```
### Ejercicio 3. Almacene en un array el numero n leido del teclado, el tamaño del array es de 10. (DO-WHILE)
#### 1.1 Analisis. 
Debemos almacenar en 10 espacios el numero n.

Se necesita utilizar el símbolo de proceso para asignar el array A[10], después se utiliza el símbolo de entrada para almacenar los elementos en n, DESPUES VOLVEMOS A UTILIZAR EL SIMBOLO DE PROCESO PARA ASIGANAR C=0, POSTERIORMENTE SE VUELVE A UTILIZAR OTRO SIMBOLO DE PROCESO PARA ASIGNAR C AL ARRAY A[C]= N, VOLVEMOS A UTILIZAR OTRO SIMBOLO DE PROCESO PARA ASIGNAR C=C+1, DESPUES UTILIZAMOS UN SIMBOLO DE DECISION PARA PREGUNTAR SI C<=9, EN CASO DE QUE SI SE ASI ENTONCES NOS REGRESAMOS AL SIMBOLO DE PROCESO DONDE A[C]=N, Y ASI SUCESIVAMENTE HASTA QUE C SEA =9 Y FINALMENTE UTILIZAMOS UN SIMBOLO DE SALIDA PARA IMPRIMIR A.
#### 1.2 DFD
![3 (Do-While)](https://user-images.githubusercontent.com/113395327/197660916-b013d497-3144-4e52-a095-cefebc079a15.png)
#### 1.3 Prueba de escritorio 
|A[10]|N |C=0|A[C]=N|C=C+1 |C<=9|A |
|-----|--|---|------|------|----|--|
|0    |0 |0  |0     |0     |0<=9|[0]|
|1    |1 |1  |1     |1     |1<=9|[0,1]|
|2    |2 |2  |2     |2     |2<=9|[0,1,2]|
|3    |3 |3  |3     |3     |3<=9|[0,1,2,3]|
|4    |4 |4  |4     |4     |4<=9|[0,1,2,3,4]
|5    |5 |5  |5     |5     |5<=9|[0,1,2,3,4,5]|
|6    |6 |6  |6     |6     |6<=9|[0,1,2,3,4,5,6]|
|7    |7 |7  |7     |7     |7<=9|[0,1,2,3,4,5,6,7]|
|8    |8 |8  |8     |8     |8<=9|[0,1,2,3,4,5,6,7,8]|
|9    |9 |9  |9     |9     |9<=9|[0,1,2,3,4,5,6,7,8,9]|

#### 1.4 Entradas.
n.
#### 1.5 Salidas.
A.
#### 1.6 Codigo.
```dart
void main() {
  var arra = new List.filled(10, 0);
  stdout.write("Dame diez numeros\n ");
  stdout.write("----------\n");
  int i = 0;
  do {
    String? s = stdin.readLineSync();
    if (s != null) {
      int n = int.parse(s);
      arra[i] = n;
      i++;
    }
  } while (i <= 9);
  stdout.write("Tu lista es $arra ");
}
```
### Ejercicio 4. Almacene los n numeros leidos del teclado en un vector de 10 elementos. (FOR)
#### 1.1 Analisis. 
Almacenar en 10 espacios diferentes numeros leidos del teclado.

Se necesita utilizar el símbolo de proceso para asignar el array A[10], después utilizar el símbolo de ciclo de for para hacer un contador de i=0; i<=9; i=i+1, en caso de que i sea menor a 10 se utiliza el símbolo de entrada para almacenar los elementos en n, después se utiliza otro símbolo de proceso para ingresar A [i]= N, y se regressa al ciclo hasta que i sea mayor a 10 y al final se utiliza un símbolo de salida para imprimir A.
#### 1.2 DFD
![4 (for)](https://user-images.githubusercontent.com/113395327/197660974-b31154a6-6d29-4622-815a-8f9d47ea0af1.png)
#### 1.3 Prueba de escritorio 
|A[10]|i  |i<10 |i+1|A[i]=N|A |
|-----|---|-----|---|------|--|
|0   |0   |0<10 |   |0     |[0] |
|1   |1   |1<10 |1  |1     |[0,1] |
|2   |2   |2<10 |2  |2     |[0,1,2] |
|3   |3   |3<10 |3  |3     |[0,1,2,3]|
|4   |4   |4<10 |4  |4     |[0,1,2,3,4]|
|5   |5   |5<10 |5  |5     |[0,1,2,3,4,5]|
|6   |6   |6<10 |6  |6     |[0,1,2,3,4,5,6]|
|7   |7   |7<10 |7   |7    |[0,1,2,3,4,5,6,7]|
|8   |8   |8<10 |8  |8     |[0,1,2,3,4,5,6,7,8]|
|9   |9   |9<10 |9  |9     |[0,1,2,3,4,5,6,7,8,9]|

#### 1.4 Entradas.
n.
#### 1.5 Salidas.
A.
#### 1.6 Codigo.
```dart
void main() {
  var arra = new List.filled(10, 0);
  stdout.write("Dame diez numeros\n ");
  stdout.write("----------\n");
  for (var i = 0; i <= 9; i++) {
    String? s = stdin.readLineSync();
    if (s != null) {
      int n = int.parse(s);
      arra[i] = n;
    }
  }
  stdout.write("aqui esta la lista, $arra");
}
```
### Ejercicio 4. Almacene los n numeros leidos del teclado en un vector de 10 elementos. (WHILE)
#### 1.1 Analisis. 
Almacenar en 10 espacios diferentes numeros leidos del teclado.

Se necesita utilizar el símbolo de proceso para asignar el array A[10],  DESPUES VOLVEMOS A UTILIZAR EL SIMBOLO DE PROCESO PARA ASIGANAR C=0, DESPUES UTILIZAMOS UN SIMBOLO DE DECISION PARA PREGUNTAR SI C<=9, EN CASO DE QUE SI SE ASI ENTONCES se utiliza el símbolo de entrada para almacenar los elementos en n, después ASIGNAMOS UN  SIMBOLO DE PROCESO DONDE A[C]=N, POSTERIORMENTE UTILIZAMOS OTRO SIMBOLO DE PROCESO PRA INGRESAR C=C+1 Y SE REGRESA AL SIMBOLO DE DECISION Y ASI SUSCIVAMENTE HASTA QUE C SEA IGUAL A 9 Y FINALMENTE INGRESAMOS UN SIMBOLO DE SALIDA PARA IMPRIMIR A.
#### 1.2 DFD
![4 (While)](https://user-images.githubusercontent.com/113395327/197661015-dfd2ed45-979d-4fe4-a6bb-a96e2114497e.png) 
#### 1.3 Prueba de escritorio 
|A[10]|N |C=0|C<=9|A[C]=N |C=C+1|A |
|-----|--|---|------|------|----|--|
|0    |0 |0  |0<=9|0     |1|[0]|
|1    |1 |1  |1<=9     |1     |2|[0,1]|
|2    |2 |2  |2<=9     |2     |3|[0,1,2]|
|3    |3 |3  |3<=9     |3     |4|[0,1,2,3]|
|4    |4 |4  |4<=9     |4     |5|[0,1,2,3,4]
|5    |5 |5  |5<=9     |5     |6|[0,1,2,3,4,5]|
|6    |6 |6  |6<=9     |6    |7|[0,1,2,3,4,5,6]|
|7    |7 |7  |7<=9     |7     |8|[0,1,2,3,4,5,6,7]|
|8    |8 |8  |8<=9     |8     |9|[0,1,2,3,4,5,6,7,8]|
|9    |9 |9  |9<=9     |9     |10|[0,1,2,3,4,5,6,7,8,9]|

#### 1.4 Entradas.
n.
#### 1.5 Salidas.
A.
#### 1.6 Codigo.
```dart
void main() {
  var arra = new List.filled(10, 0);
  stdout.write("Dame diez numeros\n ");
  stdout.write("----------\n");
  int i = 0;
  while (i <= 9) {
    String? s = stdin.readLineSync();
    if (s != null) {
      int ner = int.parse(s);
      arra[i] = ner;
    }
    i++;
  }
  stdout.write("Tu lista es, $arra ");
}
```
### Ejercicio 4. Almacene los n numeros leidos del teclado en un vector de 10 elementos. (DO-WHILE)
#### 1.1 Analisis. 
Almacenar en 10 espacios diferentes numeros leidos del teclado.

Se necesita utilizar el símbolo de proceso para asignar el array A[10],  DESPUES SE  UTILIZA EL SIMBOLO DE PROCESO PARA ASIGANAR C=0, después utilizar el símbolo de entrada para almacenar los elementos en n, POSTERIORMENTE SE VUELVE A UTILIZAR OTRO SIMBOLO DE PROCESO PARA ASIGNAR C AL ARRAY A[C]= N, VOLVEMOS A UTILIZAR OTRO SIMBOLO DE PROCESO PARA ASIGNAR C=C+1, DESPUES UTILIZAMOS UN SIMBOLO DE DECISION PARA PREGUNTAR SI C<=9, EN CASO DE QUE SI SE ASI ENTONCES NOS REGRESAMOS AL SIMBOLO DE PROCESO DONDE A[C]=N, Y ASI SUCESIVAMENTE HASTA QUE C SEA =9 Y FINALMENTE UTILIZAMOS UN SIMBOLO DE SALIDA PARA IMPRIMIR A.
#### 1.2 DFD
![4 (Do-While)](https://user-images.githubusercontent.com/113395327/197661041-c8b0f699-fc49-4158-aa3a-0135523b7921.png)
#### 1.3 Prueba de escritorio 
|A[10]|N |C=0|A[C]=N|C=C+1 |C<=9|A |
|-----|--|---|------|------|----|--|
|0    |0 |0  |0     |0     |0<=9|[0]|
|1    |1 |1  |1     |1     |1<=9|[0,1]|
|2    |2 |2  |2     |2     |2<=9|[0,1,2]|
|3    |3 |3  |3     |3     |3<=9|[0,1,2,3]|
|4    |4 |4  |4     |4     |4<=9|[0,1,2,3,4]
|5    |5 |5  |5     |5     |5<=9|[0,1,2,3,4,5]|
|6    |6 |6  |6     |6     |6<=9|[0,1,2,3,4,5,6]|
|7    |7 |7  |7     |7     |7<=9|[0,1,2,3,4,5,6,7]|
|8    |8 |8  |8     |8     |8<=9|[0,1,2,3,4,5,6,7,8]|
|9    |9 |9  |9     |9     |9<=9|[0,1,2,3,4,5,6,7,8,9]|

#### 1.4 Entradas.
n.
#### 1.5 Salidas.
A
#### 1.6 Codigo.
```dart
void main() {
  var arra = new List.filled(10, 0);
  stdout.write("Dame diez numeros\n ");
  stdout.write("----------\n");
  int i = 0;
  do {
    String? s = stdin.readLineSync();
    if (s != null) {
      int n = int.parse(s);
      arra[i] = n;
      i++;
    }
  } while (i <= 9);
  stdout.write("Tu lista es $arra ");
}
```
### Ejercicio 5. Almacene un contador negativo en un vector, el conteo es de 10 a 0. (FOR)
#### 1.1 Analisis. 
Almacenar en 10 espacios un conteo regresivo del 10 al 0.

Se necesita utilizar el símbolo de proceso para asignar el array A[11], después utilizar el símbolo de ciclo de for para hacer un contador de i=10; i>=0; i=i-1, en caso de que i sea mayor o igual a 0, se utiliza el símbolo de entrada para almacenar los elementos en n, después se utiliza otro símbolo de proceso para ingresar A [10-i]= N, y se regressa al ciclo hasta que i sea igual a 0 y al final se utiliza un símbolo de salida para imprimir A.
#### 1.2 DFD
![5 (for)](https://user-images.githubusercontent.com/113395327/197661066-18a0fe4e-25fa-49df-bd17-369867a17e66.png)
#### 1.3 Prueba de escritorio 
|A[11]|i  |i>=0 |N  |A[10-i]=N|i-1|A  |
|-----|---|-----|---|---------|---|---|
|0    |10 |10>=0|10 |A[10-10] |9  |[0]|
|1    |9  |9>=0 |9  |A[10-9]  |8  |[0,1]|
|2    |8  |8>=0 |8  |A[10-8]  |7  |[0,1,2]|
|3    |7  |7>=0 |7  |A[10-7]  |6  |[0,1,2,3]|
|4    |6  |6>=0 |6  |A[10-6]  |5  |[0,1,2,3,4]|
|5    |5  |5>=0 |5  |A[10-5]  |4  |[0,1,2,3,4,5]|
|6    |4  |4>=0 |4  |A[10-4]  |3  |[0,1,2,3,4,5,6]|
|7    |3  |3>=0 |3  |A[10-3]  |2  |[0,1,2,3,4,5,6,7]|
|8    |2  |2>=0 |2  |A[10-2]  |1  |[0,1,2,3,4,5,6,7,8]|
|9    |1  |1>=0 |1  |A[10-1]  |0  |[0,1,2,3,4,5,6,7,8,9]|
|10   |0  |0>=0 |0  |A[10-0]  |-1 |[0,1,2,3,4,5,6,7,8,9,10]|

#### 1.4 Entradas.
No tiene entradas.
#### 1.5 Salidas.
A.
#### 1.6 Codigo.
```dart
void main() {
  var arr = <int>[0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
  for (var i = 10; i >= 0; i--) {
    arr[10 - i] = i;
  }
  print(arr);
}
```
### Ejercicio 5. Almacene un contador negativo en un vector, el conteo es de 10 a 0. (WHILE)
#### 1.1 Analisis. 
Almacenar en 10 espacios un conteo regresivo del 10 al 0.

Se necesita utilizar el símbolo de proceso para asignar el array A[11],  DESPUES VOLVEMOS A UTILIZAR EL SIMBOLO DE PROCESO PARA ASIGANAR C=10, DESPUES UTILIZAMOS UN SIMBOLO DE DECISION PARA PREGUNTAR SI C>=0, EN CASO DE QUE SI SE ASI ENTONCES ASIGNAMOS UN  SIMBOLO DE PROCESO DONDE A[10-C]=A, POSTERIORMENTE UTILIZAMOS OTRO SIMBOLO DE PROCESO PRA INGRESAR C=C-1 Y SE REGRESA AL SIMBOLO DE DECISION Y ASI SUSCIVAMENTE HASTA QUE C SEA IGUAL 
#### 1.2 DFD
![5 (While)](https://user-images.githubusercontent.com/113395327/197661093-1e30accc-8788-4e69-99fa-6ae602d16809.png)
#### 1.3 Prueba de escritorio 
|A[11]|C  |C>=0     |A[10-C]=A|C=C-1 |A |  
|-----|---|---------|---------|------|--|
|0    |10 |10>=0    |A[10-10] |9     |[0]|
|1    |9  |9>=0     |A[10-9]  |8     |0,1]|
|2    |8  |8>=0     |A[10-8]  |7     |[0,1,2]|
|3    |7  |7>=0     |A[10-7]  |6     |[0,1,2,3]|
|4    |6  |6>=0     |A[10-6]  |5     |[0,1,2,3,4]|
|5    |5  |5>=0     |A[10-5]  |4     |[0,1,2,3,4,5]
|6    |4  |4>=0     |A[10-4]  |3     |[0,1,2,3,4,5,6]|
|7    |3  |3>=0     |A[10-3]  |2     |[0,1,2,3,4,5,6,7]|
|8    |2  |2>=0     |A[10-2]  |1     |[0,1,2,3,4,5,6,7,8]|
|9    |1  |1>=0     |A[10-1]  |0     |[0,1,2,3,4,5,6,7,8,9]|
|10   |0  |0>=0     |A[10-0]  |1>=0  |[0,1,2,3,4,5,6,7,8,9,10]|

#### 1.4 Entradas.
No tiene entradas.
#### 1.5 Salidas.
A.
#### 1.6 Codigo.
```dart
void main() {
  var arr = <int>[0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
  int c = 10;
  while (c >= 0) {
    arr[10 - c] = c;
    c = c - 1;
  }
  print(arr);
}
```
### Ejercicio 5. Almacene un contador negativo en un vector, el conteo es de 10 a 0. (DO-WHILE)
#### 1.1 Analisis. 
Almacenar en 10 espacios un conteo regresivo del 10 al 0.

Se necesita utilizar el símbolo de proceso para asignar el array A[11],  DESPUES SE  UTILIZA EL SIMBOLO DE PROCESO PARA ASIGANAR C=10, POSTERIORMENTE SE VUELVE A UTILIZAR OTRO SIMBOLO DE PROCESO PARA ASIGNAR C AL ARRAY A[C]= N, VOLVEMOS A UTILIZAR OTRO SIMBOLO DE PROCESO PARA ASIGNAR C=C-1, DESPUES UTILIZAMOS UN SIMBOLO DE DECISION PARA PREGUNTAR SI C>=0, EN CASO DE QUE SI SE ASI ENTONCES NOS REGRESAMOS AL SIMBOLO DE PROCESO DONDE A[C]=N, Y ASI SUCESIVAMENTE HASTA QUE C SEA =0 Y FINALMENTE UTILIZAMOS UN SIMBOLO DE SALIDA PARA IMPRIMIR A.
#### 1.2 DFD
![5 (Do-While)](https://user-images.githubusercontent.com/113395327/197661111-4c8e2d90-88c6-4952-a8f8-ebe2f856e4ad.png)
#### 1.3 Prueba de escritorio 
|A[11]|C  |A[10-C]=A|C=C-1 |C>=0 |A |
|-----|---|---------|------|-----|--|
|0    |10 |A[10-10] |9     |10>=0|[0]|
|1    |9  |A[10-9]  |8     |9>=0 |0,1]|
|2    |8  |A[10-8]  |7     |8>=0 |[0,1,2]|
|3    |7  |A[10-7]  |6     |7>=0 |[0,1,2,3]|
|4    |6  |A[10-6]  |5     |6>=0 |[0,1,2,3,4]
|5    |5  |A[10-5]  |4     |5>=0 |[0,1,2,3,4,5]|
|6    |4  |A[10-4]  |3     |4>=0 |[0,1,2,3,4,5,6]|
|7    |3  |A[10-3]  |2     |3>=0 |[0,1,2,3,4,5,6,7]|
|8    |2  |A[10-2]  |1     |2>=0 |[0,1,2,3,4,5,6,7,8]|
|9    |1  |A[10-1]  |0     |1>=0 |[0,1,2,3,4,5,6,7,8,9]|
|10   |0  |A[10-0]  |      |0>=0 |[0,1,2,3,4,5,6,7,8,9,10]|

#### 1.4 Entradas.
No tiene entradas.
#### 1.5 Salidas.
A.
#### 1.6 Codigo.
```dart
void main() {
  var arr = <int>[0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
  int c = 10;
  do {
    arr[10 - c] = c;
    c = c - 1;
  } while (c >= 0);
  print(arr);
}
```
### Ejercicio 6. Almacene en un vector de tamaño 10, todos los numeros pares capturados hasta completar todos. (FOR)
#### 1.1 Analisis. 
Tenemos que insertar numero pares y almacenarlos en 10 espacios.

Se necesita utilizar el símbolo de proceso para asignar el vector A[10],  después utilizar el símbolo de ciclo de for para hacer un contador de i=0; i<=9; i=i+1, en caso de que i sea mayor o menor a 10, se utiliza el símbolo de entrada para almacenar los elementos en n, después se utiliza un símbolo de decisión para preguntar si N%2=0, en caso de que no sea así se ingresa un símbolo de salida que dice que el numero tiene que ser par y se regresa al símbolo de entrada, en caso de que si sea así se ingresa un símbolo de proceso para ingresar A [i]= N, y se regressa al ciclo hasta que i sea igual a 9 y al final se utiliza un símbolo de salida para imprimir A.
#### 1.2 DFD
![image](https://user-images.githubusercontent.com/113395327/197382216-7f05339c-b12f-4d84-9978-8caa04a7534f.png)
#### 1.3 Prueba de escritorio 
|A[10]|i  |i<=9 |N  |N%2=0  |A[i]=N   |i+1|A  |
|-----|---|-----|---|-------|---------|---|---|
|0    |0  |0<=9 |0  |NO     |         |1  ||
|1    |1  |1<=9 |1  |NO     |         |2  ||
|2    |2  |2<=9 |2  |SI     |A[2]     |3  |[2]|
|3    |3  |3<=9 |3  |NO     |         |4  |[2]|
|4    |4  |4<=9 |4  |SI     |A[4]     |5  |[2,4]|
|5    |5  |5<=9 |5  |NO     |         |6  |[2,4]|
|6    |6  |6<=9 |6  |SI     |A[6]     |7  |[2,4,6]|
|7    |7  |7<=9 |7  |NO     |         |8  |[2,4,6]|
|8    |8  |8<=9 |8  |SI     |A[8]     |9  |[2,4,6,8]|
|9    |9  |9<=9 |9  |NO     |         |10 |[2,4,6,8]|

#### 1.4 Entradas.
n.
#### 1.5 Salidas.
A.
#### 1.6 Codigo.
```py
numeros = [2, 4, 6, 8, 10, 12, 14, 16, 18, 20]
def extraer_pares(lista):
    pares = []
    for n in lista:
        if n % 2 == 0:
            pares.append(n)
    return pares
print()
resultado = extraer_pares(numeros)
print("Contenido de la variable`resultado`:", resultado)
print("Cantidad de elementos en la lista `resultado`:", len(resultado))
```
### Ejercicio 6. Almacene en un vector de tamaño 10, todos los numeros pares capturados hasta completar todos. (WHILE)
#### 1.1 Analisis. 
Tenemos que insertar numero pares y almacenarlos en 10 espacios.

Se necesita utilizar el símbolo de proceso para asignar el array A[10],  DESPUES SE  UTILIZA EL SIMBOLO DE PROCESO PARA ASIGANAR C=0, DESPUES UTILIZAMOS UN SIMBOLO DE DECISION PARA PREGUNTAR SI C<=9, SI ES ASI ENTONCES UTILIZAMOS OTRO SIMBOLO DE PROCESO PARA ASIGNAR C=C+1,DESPUES SE UTILIZA UN SIMBOLO DE ENTRADA PARA ASIGNAR LOS VALORES A N, SE VUELVE A UTILIZAR OTRO SIMBOLO DE DECISION PARA PREGUNTAR SU N%2=0, EN CASO DE QUE NO SEA ASI ENTONCES SE UTILIZA UN SIMBOLO DE SALIA QUE IMPRIME "TIENE QUE SER PAR" Y SE REGRESA AL SIMBOLO DE PROCESO PARA PEDIR OTRO NUMERO, EN CASO DE QUE N%2=0 SI SEA ASI, SE UTILIZA OTRO SIMBOLO DE PROCESO PARA ASIGNAR C AL VECTOR A[C]= N, Y SE REGRESA AL SIMBOLO DE DECISION QUE DICE C<=9, Y ASI SUCESIVAMENTE HASTA QUE C SEA IGUAL A 9, SI EN EL SIMBOLO DE DECISION DE C<=9 NO SEA ASI SE INGRESA UN SIMBOLO DE SALIDA QUE IMPRIME A.
#### 1.2 DFD
![image](https://user-images.githubusercontent.com/113395327/197382230-a9f1f438-30d8-44c4-9d04-78c41acc7111.png)
#### 1.3 Prueba de escritorio 
|A[10]|C  |C<=9 |C=C+1 |N  |N%2=0  |A[C]=N   |A  |
|-----|---|-----|------|---|-------|---------|---|
|0    |0  |0<=9 |1     |1  |NO     |         ||
|1    |1  |1<=9 |2     |2  |SI     |A[2]     |[2]|
|2    |2  |2<=9 |3     |3  |NO     |         |[2]|
|3    |3  |3<=9 |4     |4  |SI     |A[4]     |[2]|
|4    |4  |4<=9 |5     |5  |NO     |         |[2,4]|
|5    |5  |5<=9 |6     |6  |SI     |A[6]     |[2,4]|
|6    |6  |6<=9 |7     |7  |NO     |         |[2,4,6]|
|7    |7  |7<=9 |8     |8  |SI     |A[8]     |[2,4,6]|
|8    |8  |8<=9 |9     |9  |NO     |         |[2,4,6,8]|
|9    |9  |9<=9 |10    |10 |SI     |A[10]    |[2,4,6,8,10]|

#### 1.4 Entradas.
n.
#### 1.5 Salidas.
A.
#### 1.6 Codigo.
```py
numeros = [2, 4, 6, 8, 10, 12, 14, 16, 18, 20]
def extraer_pares(lista):
    pares = []
    for n in lista:
        if n % 2 == 0:
            pares.append(n)
    return pares
print()
resultado = extraer_pares(numeros)
print("Contenido de la variable`resultado`:", resultado)
print("Cantidad de elementos en la lista `resultado`:", len(resultado))
```
### Ejercicio 6. Almacene en un vector de tamaño 10, todos los numeros pares capturados hasta completar todos. (DO-WHILE)
#### 1.1 Analisis. 
Tenemos que insertar numero pares y almacenarlos en 10 espacios.

Se necesita utilizar el símbolo de proceso para asignar el array A[10],  DESPUES SE  UTILIZA EL SIMBOLO DE PROCESO PARA ASIGANAR C=0, VOLVEMOS A UTILIZAR OTRO SIMBOLO DE PROCESO PARA ASIGNAR C=C+1, DESPUES UTILIZAMOS UN SIMBOLO DE DECISION PARA PREGUNTAR SI C<=9, EN CASO DE QUE SI SEA ASI SE UTILIZA UN SIMBOLO DE ENTRADA PARA ASIGNAR LOS VALORES A N, SE UTILIZA OTRO SIMBOLO DE DECISION PARA PREGUNTAR SU N%2=0, SI EN NO ENTONCES SE UTILIZA UN SIMBOLO DE SALIA QUE IMPRIME "TIENE QUE SER PAR" Y SE REGRESA AL SIMBOLO DE PROCESO PARA PEDIR OTRO NUMERO, EN CASO DE QUE N%2=0 SI SEA ASI, SE UTILIZA OTRO SIMBOLO DE PROCESO PARA ASIGNAR C AL VECTOR A[C]= N, Y SE REGRESA AL SIMBOLO DE PROECESO QUE DICE C=C+1, Y ASI SUCESIVAMENTE HASTA QUE C SEA IGUAL A 9, SI EN EL SIMBOLO DE DECISION DE C<=9 NO SEA ASI SE INGRESA UN SIMBOLO DE SALIDA QUE IMPRIME A.
#### 1.2 DFD
![image](https://user-images.githubusercontent.com/113395327/197382249-ea63e694-11ef-47fc-bf5b-5f4173ad7766.png)
#### 1.3 Prueba de escritorio 
|A[10]|C  |C=C+1 |C<=9 |N  |N%2=0  |A[C]=N   |A  |
|-----|---|------|-----|---|-------|---------|---|
|0    |0  |      |0<=9 |0  |NO     |         ||
|1    |1  |1     |1<=9 |1  |NO     |         ||
|2    |2  |2     |2<=9 |2  |SI     |A[2]     |[2]|
|3    |3  |3     |3<=9 |3  |NO     |         |[2]|
|4    |4  |4     |4<=9 |4  |SI     |A[4]     |[2,4]|
|5    |5  |5     |5<=9 |5  |NO     |         |[2,4]|
|6    |6  |6     |6<=9 |6  |SI     |A[6]     |[2,4,6]|
|7    |7  |7     |7<=9 |7  |NO     |         |[2,4,6]|
|8    |8  |8     |8<=9 |8  |SI     |A[8]     |[2,4,6,8]|
|9    |9  |9     |9<=9 |9  |NO     |         |[2,4,6,8]|

#### 1.4 Entradas.
n.
#### 1.5 Salidas.
A.
#### 1.6 Codigo.
```dart
import 'dart:io';
import 'dart:async';
void main() {
  var array = [];
  var c = 0;
  do {
    int n = int.parse(stdin.readLineSync()!);
    if (n % 2 == 0) {
      array.add(n);
      c = c + 1;
    }
  } while (c <= 9);
  print(array);
}
```
### Ejercicio 7. Obtener el promedio de las calificaciones aprobatorias y la cantidad de alumnos reprobados. La calificación entre 0 y 10 y el maximo de alumnos es de 15. (FOR)
#### 1.1 Analisis.
Sumar las calificaiones de los alumnos aprobados y sacarles el promedio, despues contar la cantidad de reprobados mayores a 5.

Se necesita utilizar el símbolo de proceso para asignar el vector A[15], después utilizar el símbolo de ciclo de for para hacer un contador de i=0; i<15; i=i+1, en caso de que i sea mayor o menor a 15, se utiliza el símbolo de entrada para almacenar los elementos en ALUMNO, después se utiliza un símbolo de decisión para preguntar si ALUMNO_CAL>=6, en caso de que no sea así se ingresa un símbolo de salida que IMPRIME "REPROBADO" y se regresa al símbolo de entrada, en caso de que si sea asi se ingresa un símbolo de proceso para ingresar A [i]= APROBADO, y se regressa al ciclo hasta que i sea igual a 14 y al final se utiliza un símbolo de salida para imprimir A.
#### 1.2 DFD
![7 (for)](https://user-images.githubusercontent.com/113395327/197688395-c0923fad-0ca5-4de4-82d6-1bab7203d080.png)
#### 1.3 Prueba de escritorio 
|A[15]|i  |i<15 |ALUMNO|ALUMNO_CAL>=6|A[i]=APROBADO|i+1|A  |
|-----|---|-----|------|-------------|-------------|---|---|
|0    |0  |0<15 |0     |NO           |REPROBO      |1  |   |
|1    |1  |1<15 |1     |NO           |REPROBO      |2  |   |
|2    |2  |2<15 |2     |NO           |REPROBO      |3  ||
|3    |3  |3<15 |3     |NO           |REPROBO      |4  ||
|4    |4  |4<15 |4     |NO           |REPROBO      |5  ||
|5    |5  |5<15 |5     |NO           |REPROBO      |6  ||
|08   |6  |6<15 |6     |SI           |A[6]         |7  ||
|06   |7  |7<15 |7     |SI           |A[7]         |8  ||
|07   |8  |8<15 |8     |SI           |A[8]         |9  ||
|08   |9  |9<15 |9     |SI           |A[9]         |10 ||
|09   |10 |10<15|10    |SI           |A[10]        |11 ||
|08   |11 |11<15|11    |SI           |A[11]        |12 ||
|09   |12 |12<15|12    |SI           |A[12]        |13 ||
|10   |13 |13<15|13    |SI           |A[13]        |14 ||
|10   |14 |14<15|14    |SI           |A[14]        |   |[9]|

#### 1.4 Entradas.
Cal.
#### 1.5 Salidas.
P_A; C_R.
#### 1.6 Codigo.
```py
alumnos = list(range(15))
p_aprobados = 0
j = 0
for i in alumnos: 
    while(True):
        calificacion = int(input("Ingresa la calificación >>"))
        if (calificacion >= 0 and calificacion <= 10):
            break
        else:
            print("Calificación fuera de rango. Intenta de nuevo")
 
    if (calificacion < 6):
     alumnos[i] = "R"
    else:
     p_aprobados = calificacion + p_aprobados
     j = j + 1
     alumnos[i] = "A"
print("\033[33;1m",alumnos,"\033[39m")
print("El promedio de calificación de los aprobados es de >>",round(p_aprobados/j,2))
print("El total de aprobados fueron >> ",j)
print("El total de reprobados fueron >> ",(len(alumnos)-j))
```

### Ejercicio 7. Obtener el promedio de las calificaciones aprobatorias y la cantidad de alumnos reprobados. La calificación entre 0 y 10 y el maximo de alumnos es de 15. (WHILE)
#### 1.1 Analisis. 
Sumar las calificaiones de los alumnos aprobados y sacarles el promedio, despues contar la cantidad de reprobados mayores a 5.

Se necesita utilizar el símbolo de proceso para asignar el vector A[15], DESPUES SE  UTILIZA EL SIMBOLO DE PROCESO PARA ASIGANAR C=0, DESPUES UTILIZAMOS UN SIMBOLO DE DECISION PARA PREGUNTAR SI C<15, EN CASO DE QUE SI SEA ASI SE UTILIZA UN SIMBOLO DE ENTRADA PARA ASIGNAR LOS VALORES A ALUMNO,VOLVEMOS A UTILIZAR OTRO SIMBOLO DE PROCESO PARA ASIGNAR C=C+1, después se utiliza un símbolo de decisión para preguntar si ALUMNO_CAL>=6, en caso de que no sea así se ingresa un símbolo de salida que IMPRIME "REPROBADO" y se regresa al símbolo de entrada, en caso de que si sea así se ingresa un símbolo de proceso para ingresar A [i]= APROBADO, y se regressa al SIMBOLO DE DECISION DE C<15 Y ASI SUCECIVAMENTE HASTA QUE C SEA IGUAL A 14 Y FINALMENTE SE IMPRIME A.
#### 1.2 DFD
![7 (While)](https://user-images.githubusercontent.com/113395327/197688455-e00cb974-0a95-45e3-9181-aef805bd31be.png)
#### 1.3 Prueba de escritorio 
|A[15]|C  |C<15  |ALUMNO|ALUMNO_CAL>=6|A[C]=APROBADO|C=C+1 |A  |
|-----|---|------|------|-------------|-------------|------|---|
|0    |0  |0<15  |0     |NO           |REPROBO      |1     |   |
|1    |1  |1<15  |1     |NO           |REPROBO      |2     |   |
|2    |2  |2<15  |2     |NO           |REPROBO      |3     |   |
|3    |3  |3<15  |3     |NO           |REPROBO      |4     |   |
|4    |4  |4<15  |4     |NO           |REPROBO      |5     |   |
|5    |5  |5<15  |5     |NO           |REPROBO      |6     |   |
|08   |6  |6<15  |6     |SI           |A[6]         |7     |   |
|06   |7  |7<15  |7     |SI           |A[7]         |8     |   |
|07   |8  |8<15  |8     |SI           |A[8]         |9     |   |
|08   |9  |9<15  |9     |SI           |A[9]         |10    |   |
|09   |10 |10<15 |10    |SI           |A[10]        |11    |   |
|08   |11 |11<15 |11    |SI           |A[11]        |12    |   |
|09   |12 |12<15 |12    |SI           |A[12]        |13    |   |
|10   |13 |13<15 |13    |SI           |A[13]        |14    |   |
|10   |14 |14<15 |14    |SI           |A[14]        |      |[9]   |

#### 1.4 Entradas.
Cal.
#### 1.5 Salidas.
P_A; C_R.
#### 1.6 Codigo.
```py
alumnos = list(range(15))
p_aprobados = 0
j = 0
for i in alumnos: 
    while(True):
        calificacion = int(input("Ingresa la calificación >>"))
        if (calificacion >= 0 and calificacion <= 10):
            break
        else:
            print("Calificación fuera de rango. Intenta de nuevo")
 
    if (calificacion < 6):
     alumnos[i] = "R"
    else:
     p_aprobados = calificacion + p_aprobados
     j = j + 1
     alumnos[i] = "A"
print("\033[33;1m",alumnos,"\033[39m")
print("El promedio de calificación de los aprobados es de >>",round(p_aprobados/j,2))
print("El total de aprobados fueron >> ",j)
print("El total de reprobados fueron >> ",(len(alumnos)-j))
```
### Ejercicio 7. Obtener el promedio de las calificaciones aprobatorias y la cantidad de alumnos reprobados. La calificación entre 0 y 10 y el maximo de alumnos es de 15. (DO-WHILE)
#### 1.1 Analisis. 
Sumar las calificaiones de los alumnos aprobados y sacarles el promedio, despues contar la cantidad de reprobados mayores a 5.

Se necesita utilizar el símbolo de proceso para asignar el vector A[15], DESPUES SE  UTILIZA EL SIMBOLO DE PROCESO PARA ASIGANAR C=0, DESPUES UTILIZAMOS UN SIMBOLO DE DECISION PARA PREGUNTAR SI C<15, EN CASO DE QUE SI SEA ASI SE UTILIZA UN SIMBOLO DE ENTRADA PARA ASIGNAR LOS VALORES A ALUMNO,VOLVEMOS A UTILIZAR OTRO SIMBOLO DE PROCESO PARA ASIGNAR C=C+1, después se utiliza un símbolo de decisión para preguntar si ALUMNO_CAL>=6, en caso de que no sea así se ingresa un símbolo de salida que IMPRIME "REPROBADO" y se regresa al símbolo de entrada, en caso de que si sea así se ingresa un símbolo de proceso para ingresar A [i]= APROBADO, y se regressa al SIMBOLO DE DECISION DE C<15 Y ASI SUCECIVAMENTE HASTA QUE C SEA IGUAL A 14 Y FINALMENTE SE IMPRIME A.
#### 1.2 DFD
![7 (Do-While)](https://user-images.githubusercontent.com/113395327/197688485-7cbe452b-ac52-43d2-9b69-d36af9fc360f.png)
#### 1.3 Prueba de escritorio 
|A[15]|C  |C<15  |ALUMNO|ALUMNO_CAL>=6|A[C]=APROBADO|C=C+1 |A  |
|-----|---|------|------|-------------|-------------|------|---|
|0    |0  |0<15  |0     |NO           |REPROBO      |1     |   |
|1    |1  |1<15  |1     |NO           |REPROBO      |2     |   |
|2    |2  |2<15  |2     |NO           |REPROBO      |3     |   |
|3    |3  |3<15  |3     |NO           |REPROBO      |4     |   |
|4    |4  |4<15  |4     |NO           |REPROBO      |5     |   |
|5    |5  |5<15  |5     |NO           |REPROBO      |6     |   |
|08   |6  |6<15  |6     |SI           |A[6]         |7     |   |
|06   |7  |7<15  |7     |SI           |A[7]         |8     |   |
|07   |8  |8<15  |8     |SI           |A[8]         |9     |   |
|08   |9  |9<15  |9     |SI           |A[9]         |10    |   |
|09   |10 |10<15 |10    |SI           |A[10]        |11    |   |
|08   |11 |11<15 |11    |SI           |A[11]        |12    |   |
|09   |12 |12<15 |12    |SI           |A[12]        |13    |   |
|10   |13 |13<15 |13    |SI           |A[13]        |14    |   |
|10   |14 |14<15 |14    |SI           |A[14]        |      |[9]   |

#### 1.4 Entradas.
Cal.
#### 1.5 Salidas.
P_A; C_R.
#### 1.6 Codigo.
```dart
import 'dart:io';
import 'dart:async';
void main() {
  double PromA = 0;
  var contr = 0;
  double sumaA = 0;
  double contA = 0;
  double cal1 = 0;
  double cal2 = 1;
  var cont = 0;
  stdout.write("Dame las calificaciones\n ");
  stdout.write("----------\n");
  do {
    double c = double.parse(stdin.readLineSync()!);
    cont = cont +1;
    if (c > 10) {
      print('La calificacion no puede ser mayor a 10');
      cont = cont - 1;
    }
    if (c < 0) {
      print('La calificacion no puede ser menor a 0');
      cont = cont - 1;
    }
    if (c < 6 && c > 0) {
      contr = contr + 1;
    }
    if (c <= 10 && c >= 6) {
      cal1 = c;
      sumaA = sumaA + cal1;
      contA++;
    }
    if (cal1 > cal2) {
      cal2 = cal1;
    }
  } while (cont <= 14);
  PromA = sumaA / contA;
  print('El promedio de aprobados es $PromA');
  print('La calificacion mas alta es $cal2');
  print('La cantidad de reprobados son $contr');
}
```
### Ejercicio 8. 
CAPTURE N NUMEROS  EN EL RANGO [LI,LS] DEONDE:  LI= LIMITE INFERIOR Y LS= LIMITE SUPERIOR, PARA LS>LI Y LI>0. 
OBTENGA: 

CANTIDAD DE NUMEOS PARES Y SU PROMEDIO.

CANTIDAD DE NUMEROS IMPARES Y SU PROMEDIO.

¿QUE PROMEDIO ES MAYOR? (FOR)
#### 1.1 Analisis.
Capturar una cantidad de numeros dentro de un rango establecido, para despues calcular la cantidad de numeros pares y impares para posteriormente calcular su promedio por separado y decir cual promedio es mayor. 

SE NECESITA UTILIZAR UN SIMBOLO DE PROCESO PARA INGRESAR SP=0, SI=0, CP=0, CI=0, PP=0, PI=0, DESPUES SE UTLIZA UN SIMBOLO DE SALIDA PARA PEDIR EL LIMITE INFERIOR, DESPUES SE UTILIZA UN SIMBOLO DE ENTRADA PARA INGRESAR EL LI, DESPUES SE UTLIZA UN SIMBOLO DE DECISION PARA PREGUNTAR SI LI>0, EN CASO DE QUE NO SEA ASI SE UTILIZA UN SIMBOLO DE SALIDA PARA IMPRIMIR QUE EL LS TIENE QUE SER MAYO A 0 Y SE REGRESA AL SIMBOLO DE SALIDA PARA PEDIR OTRO LI, EN CASO DE QUE SI SEA ASI ENTONCES SE UTILZA UN SIMBOLO DE SALIDA PARA PEDIR EL LIMITE SUPERIOR, DESPUES SE UTILIZA UN SIMBOLO DE ENTRADA PARA INGRESAR EL LS, DESPUES SE VUELVE A UTILZAR UN SIMBOLO DE DECISION PARA PREGUNTAR SI LS>LI, EN CASO DE QUE NO SEA ASI SE UTILIZA UN SIMBOLO DE SALIDA PARA IMPRIMIR QUE EL LS TIENE QUE SER MAYOR A LI Y SER REGRESA AL SIMBOLO DE SALIDA PARAA PEDIR OTRO LS, EN CASO DE QUE LS SI SEA MAYOR A LI ENTONCES SE UTILIZA UN SIMBOLO DE SALIDA PARA PREGUNAR CUANTOS NUMEROS INGRESARA, DESPUES SE UTILIZA UN SIMBOLO DE ENTRADA PARA INGRESAR LA CANTIDAD DE NUMEROROS EN N, DESPUES SE UTILIZA UN SIMBOLO DE DECISION PARA PREGUNTAR SI N>0, EN CASO DE QUE NO SEA ASI ENTONCES SE UTILIZA OTRO SIMBOLO DE SALIDA QUE DICE QUE EL N TIENE QUE SER MAYOR A 0 Y SE REGRESA AL SIMBOLO DE SALIDA PARA PEDIR OTRA CANTIDAD DE NUMEROS, EN CASO DE QUE N SI SEA MAYOR A 0 ENTONCES SE UTILIZA UN SIMBOLO DE CICLO DONDE i=0; i>=N; i++, DESPUES SE UTILIZA UN SIMBOLO DE SALIDA PARA PEDIR UN NUMERO DE N, Y ESE NUMERO SE INGRESA EN UN SIMBOLO DE ENTRADA COMO NUM, POSTERIORMENTE SE UTILIZA UN SIMBOLO DE DECISION PARA PREGUNTAR SI NUM>=LI, AND, NUM<=LS, EN CASO DE QUE NO SEA ASI SE UTILIZA UN SIMBOLO DE SALIDA PARA IMPRIMIR QUE EL NUM TIENE QUE ESTAR ENTRE EL LI Y EL LS, PERO SI SI ES ASI SE UTILIZA OTRO SIMBOLO DE DECISION PARA DECIR SI NUM%2=0 SI LA RESPUETA ES NO ENTONCES SE UTILIZA UN SIMBOLO DE PROCESO PARA DECIR QUE S=SI+NUM, DESPUES SE UTILIZA OTRO SIMBOLO DE PROCESO PARA DECIR QUE CI=CI+1, EN CASO DE QUE LA RESPUESTA SEA SI SE UTILIZA UN SIMBOLO DE PROCESO PARA DECIR QUE SP=SP+NUM, DESPUES UTILIZAMOS OTRO SIMBOLO DE ROCESO PARA DECIR QUE CP=CP+1, DESPUES NOS REGRESAMOS AL CICLO FOR, Y ASI SUCESIVAMENTE HASTA QUE i SEA IGUAL A N, DESPUES SE UTILIZA UN CIMBOLO DE PROCESO PARA INGRESAR EL CP, CI, DESPUES UTILIZAMOS OTRO SIMBOLO DE PROCESO PARA DECIR QUE EL PP=SP/CP Y EL PI=SI/CI, DESPUES EL PP Y EL PI LO INGRESAMOS EN UN SIMBOLO DE ENTRADA, DESPUES UTILIZAMOS UN SIMBOLO DE DECISION PARA PREGUNTAR SI PP>PI, EN CASO DE QUE NO SEA ASI SE UTILIZA UN SIMBOLO DE SALIDA QUE IMPRIME QUE EL PI ES MAYOR A PP, PERO SI LA RESPUESTA ES SI ENTONCES SE UTILIZA UN SIMBOLO DE SALIDA QUE IMPRIME QUE EL PP ES MAYOR A PI.

#### 1.2 DFD
![8 (For)](https://user-images.githubusercontent.com/113395327/197688541-2d6416ea-fe06-41cf-b2b4-55418564b7e8.png)
#### 1.3 Prueba de escritorio
|SP |CP |PP |SI |CI |PI |LI |LI>0|LS |LS>LI|N  |N>0|i=1|i<=N|NUM|NUM>=LI, NUM<=LS|NUM%2=0|SP=SP+NUM|CP=CP+1|SI=SI+NUM|CI=CI+1|i++|PP=SP/CP|PI=SI/CI|PP>PI|
|---|---|---|---|---|---|---|----|---|-----|---|---|---|----|---|----------------|-------|---------|-------|---------|-------|---|--------|--------|-----|
|0  |0  |0  |0  |0  |0  |5  |SI  |99 |SI   |4  |SI |1  |1<=4|6  |6>=5, 6<=99     |SI     |6        |1      |0        |0      |2  |        |        |     |
|6  |1  |0  |0  |0  |   |   |    |   |     |   |   |2  |2<=4|87 |87>=5, 87<=99   |NO     |6        |1      |87       |1      |3  |        |        |     |
|6  |1  |0  |87 |1  |0  |   |    |   |     |   |   |3  |3<=4|98 |98>=5, 98<=99   |SI     |104      |2      |87       |1      |4  |        |        |     |
|104|2  |0  |87 |1  |0  |   |    |   |     |   |   |4  |4<=4|77 |77>=5, 77<=99   |NO     |104      |2      |164      |2      |4  |104/2   |164/2   |52>81|

#### 1.4 Entradas.
No tiene entrada
#### 1.5 Salidas.
 "LIMITE INFERIOR"
 
 "LIMITE SUPERIOR"
 
 "EL PP ES MAYOR A PI"
 
 "EL PI ES MAYOR AL PP"

#### 1.6 Codigo.
```py
sp=0
cp=0
pp=0
si=0
ci=0
pi=0
li=-1
ls=-1
n=-1
num=-1
while(li<0):
    li = int(input("Limite inferior: "))
    
    if(li<0):
        print("Tiene que ser mayor a 0")
        
while(ls<li):
    ls = int(input("Limite superior: "))
    
    if(ls<li):
        print("Tiene que ser mayor que el limite inferior")
        
while(n<0):
    n = int(input("¿Cuantos numeros? "))
    
    if(n<0):
        print("Tiene que ser mayor a 0")
    
for i in range(n): 
    while(num<=li or num>=ls):
        num = int(input("Dame un numero de LI y LS: "))
        
        if(num<=li or num>=ls):
            print("Tiene que estar dentro del LI al LS")
    if(num%2==0):
        sp=sp+num
        cp=cp+1
    else:
        si=si+num
        ci=ci+1
        
    num=-1       
         
if(sp==0 or cp==0):
    pp=0
else:
    pp=sp/cp
    
if(si==0 or ci==0):
    pi=0
else:
    pi=si/ci
    
if(pp>pi):
    print("El PP es mayor que el PI")
else:
    print("El PI es mayor que el PP")
```
### Ejercicio 8. 
CAPTURE N NUMEROS  EN EL RANGO [LI,LS] DEONDE:  
LI= LIMITE INFERIOR Y LS= LIMITE SUPERIOR, PARA LS>LI Y LI>0.

OBTENGA: 

*CANTIDAD DE NUMEOS PARES Y SU PROMEDIO.

*CANTIDAD DE NUMEROS IMPARES Y SU PROMEDIO.

*¿QUE PROMEDIO ES MAYOR? (WHILE)

#### 1.1 Analisis.
Capturar una cantidad de numeros dentro de un rango establecido, para despues calcular la cantidad de numeros pares y impares para posteriormente calcular su promedio por separado y decir cual promedio es mayor. 

SE NECESITA UTILIZAR UN SIMBOLO DE PROCESO PARA INGRESAR C=0, SP=0, SI=0, CP=0, CI=0, PP=0, PI=0, DESPUES SE UTLIZA UN SIMBOLO DE SALIDA PARA PEDIR EL LIMITE INFERIOR, DESPUES SE UTILIZA UN SIMBOLO DE ENTRADA PARA INGRESAR EL LI, DESPUES SE UTLIZA UN SIMBOLO DE DECISION PARA PREGUNTAR SI LI>0, EN CASO DE QUE NO SEA ASI SE UTILIZA UN SIMBOLO DE SALIDA PARA IMPRIMIR QUE EL LS TIENE QUE SER MAYO A 0 Y SE REGRESA AL SIMBOLO DE SALIDA PARA PEDIR OTRO LI, EN CASO DE QUE SI SEA ASI ENTONCES SE UTILZA UN SIMBOLO DE SALIDA PARA PEDIR EL LIMITE SUPERIOR, DESPUES SE UTILIZA UN SIMBOLO DE ENTRADA PARA INGRESAR EL LS, DESPUES SE VUELVE A UTILZAR UN SIMBOLO DE DECISION PARA PREGUNTAR SI LS>LI, EN CASO DE QUE NO SEA ASI SE UTILIZA UN SIMBOLO DE SALIDA PARA IMPRIMIR QUE EL LS TIENE QUE SER MAYOR A LI Y SER REGRESA AL SIMBOLO DE SALIDA PARAA PEDIR OTRO LS, EN CASO DE QUE LS SI SEA MAYOR A LI ENTONCES SE UTILIZA UN SIMBOLO DE SALIDA PARA PREGUNAR CUANTOS NUMEROS INGRESARA, DESPUES SE UTILIZA UN SIMBOLO DE ENTRADA PARA INGRESAR LA CANTIDAD DE NUMEROROS EN N, DESPUES SE UTILIZA UN SIMBOLO DE DECISION PARA PREGUNTAR SI N>0, EN CASO DE QUE NO SEA ASI ENTONCES SE UTILIZA OTRO SIMBOLO DE SALIDA QUE DICE QUE EL N TIENE QUE SER MAYOR A 0 Y SE REGRESA AL SIMBOLO DE SALIDA PARA PEDIR OTRA CANTIDAD DE NUMEROS, EN CASO DE QUE N SI SEA MAYOR A 0 ENTONCES SE UTILIZA UN SIMBOLO DE PROCESO PARA DECIR QUE C=C+1, DESPUES SE UTILIZA UN SIMBOLO DE SALIDA PARA PEDIR UN NUMERO DE N, Y ESE NUMERO SE INGRESA EN UN SIMBOLO DE ENTRADA COMO NUM, POSTERIORMENTE SE UTILIZA UN SIMBOLO DE DECISION PARA PREGUNTAR SI NUM>=LI, AND, NUM<=LS, EN CASO DE QUE NO SEA ASI SE UTILIZA UN SIMBOLO DE SALIDA PARA IMPRIMIR QUE EL NUM TIENE QUE ESTAR ENTRE EL LI Y EL LS, PERO SI SI ES ASI SE UTILIZA OTRO SIMBOLO DE DECISION PARA DECIR SI NUM%2=0 SI LA RESPUETA ES NO ENTONCES SE UTILIZA UN SIMBOLO DE PROCESO PARA DECIR QUE S=SI+NUM, DESPUES SE UTILIZA OTRO SIMBOLO DE PROCESO PARA DECIR QUE CI=CI+1, EN CASO DE QUE LA RESPUESTA SEA SI SE UTILIZA UN SIMBOLO DE PROCESO PARA DECIR QUE SP=SP+NUM, DESPUES UTILIZAMOS OTRO SIMBOLO DE ROCESO PARA DECIR QUE CP=CP+1, DESPUES NOS REGRESAMOS AL SMBOLO DE PROCESO DE C=C+1, Y ASI SUCESIVAMENTE HASTA QUE C SEA IGUAL A N, DESPUES SE UTILIZA UN SIMBOLO DE PROCESO PARA INGRESAR EL CP, CI, DESPUES UTILIZAMOS OTRO SIMBOLO DE PROCESO PARA DECIR QUE EL PP=SP/CP Y EL PI=SI/CI, DESPUES EL PP Y EL PI LO INGRESAMOS EN UN SIMBOLO DE ENTRADA, DESPUES UTILIZAMOS UN SIMBOLO DE DECISION PARA PREGUNTAR SI PP>PI, EN CASO DE QUE NO SEA ASI SE UTILIZA UN SIMBOLO DE SALIDA QUE IMPRIME QUE EL PI ES MAYOR A PP, PERO SI LA RESPUESTA ES SI ENTONCES SE UTILIZA UN SIMBOLO DE SALIDA QUE IMPRIME QUE EL PP ES MAYOR A PI.
#### 1.2 DFD
![8 (While)](https://user-images.githubusercontent.com/113395327/197688584-5ca91bc8-9620-431c-a661-81d7ff09acbb.png)
#### 1.3 Prueba de escritorio 
|C  |SP |CP |PP |SI |CI |PI |LI |LI>0|LS |LS>LI|N  |N>0|C+1|C<=N|NUM|NUM>=LI, NUM<=LS|NUM%2=0|SP=SP+NUM|CP=CP+1|SI=SI+NUM|CI=CI+1|PP=SP/CP|PI=SI/CI|PP>PI|
|---|---|---|---|---|---|---|---|----|---|-----|---|---|---|----|---|----------------|-------|---------|-------|---------|-------|--------|--------|-----|
|0  |0  |0  |0  |0  |0  |0  |5  |SI  |99 |SI   |4  |SI |1  |1<=4|6  |6>=5, 6<=99     |SI     |6        |1      |0        |0      |        |        |     |
|1  |6  |1  |0  |0  |0  |   |   |    |   |     |   |   |2  |2<=4|87 |87>=5, 87<=99   |NO     |6        |1      |87       |1      |        |        |     |
|2  |6  |1  |0  |87 |1  |0  |   |    |   |     |   |   |3  |3<=4|98 |98>=5, 98<=99   |SI     |104      |2      |87       |1      |        |        |     |
|3  |104|2  |0  |87 |1  |0  |   |    |   |     |   |   |4  |4<=4|77 |77>=5, 77<=99   |NO     |104      |2      |164      |2      |104/2   |164/2   |52>81|

#### 1.4 Entradas.
LI

LS

N

NUM

PP

PI


#### 1.5 Salidas.
"LIMITE INFERIOR"

"LIMITE SUPERIOR"

"EL PP ES MAYOR A PI"

"EL PI ES MAYOR AL PP"

#### 1.6 Codigo.
```py
print("Dame Límite inferior: ")
Li = int(input())
while Li<0:
    print("El límite inferior debe ser mayor a 0")
    print("Dame Límite inferior: ")
    Li = int(input())
print("Dame límite superior: ")
Ls = int(input())
while Ls<=Li:
    print("El límite superior no puede ser menor o igual al limite inferior")
    print("Dame límite superior: ")
    Ls = int(input())
pares = 0
impares = 0
lista=[]
for x in range(10):
    valor=int(input("Ingrese un valor entero: "))
    lista.append(valor)
print(lista)
for a in lista:
    if a % 2 == 0:
        pares = pares + a
    else:
        impares = impares + a
print("La suma de los números pares es: ",pares)
print("La suma de los números impares es: ",impares)
prom_pares = pares / a
prom_impares = impares / a
print("El promedio de los números pares es: ",prom_pares)
print("El promedio de los números impares es: ",prom_impares)
if prom_pares > prom_impares:
    print("El promedio de los pares es mayor que el promedio de los impares.")
else:
    print("El promedio de los números impares es mayor que el promedio de los pares.")
```
### Ejercicio 8. 
CAPTURE N NUMEROS  EN EL RANGO [LI,LS] DEONDE:  
LI= LIMITE INFERIOR Y LS= LIMITE SUPERIOR, PARA LS<LS Y LI>0.

OBTENGA: 

*CANTIDAD DE NUMEOS PARES Y SU PROMEDIO.

*CANTIDAD DE NUMEROS IMPARES Y SU PROMEDIO.

*¿QUE PROMEDIO ES MAYOR? (DO/WHILE)

#### 1.1 Analisis. 
Capturar una cantidad de numeros dentro de un rango establecido, para despues calcular la cantidad de numeros pares y impares para posteriormente calcular su promedio por separado y decir cual promedio es mayor. 

SE NECESITA UTILIZAR UN SIMBOLO DE PROCESO PARA INGRESAR C=0, SP=0, SI=0, CP=0, CI=0, PP=0, PI=0, DESPUES SE UTLIZA UN SIMBOLO DE SALIDA PARA PEDIR EL LIMITE INFERIOR, DESPUES SE UTILIZA UN SIMBOLO DE ENTRADA PARA INGRESAR EL LI, DESPUES SE UTLIZA UN SIMBOLO DE DECISION PARA PREGUNTAR SI LI>0, EN CASO DE QUE NO SEA ASI SE UTILIZA UN SIMBOLO DE SALIDA PARA IMPRIMIR QUE EL LS TIENE QUE SER MAYO A 0 Y SE REGRESA AL SIMBOLO DE SALIDA PARA PEDIR OTRO LI, EN CASO DE QUE SI SEA ASI ENTONCES SE UTILZA UN SIMBOLO DE SALIDA PARA PEDIR EL LIMITE SUPERIOR, DESPUES SE UTILIZA UN SIMBOLO DE ENTRADA PARA INGRESAR EL LS, DESPUES SE VUELVE A UTILZAR UN SIMBOLO DE DECISION PARA PREGUNTAR SI LS>LI, EN CASO DE QUE NO SEA ASI SE UTILIZA UN SIMBOLO DE SALIDA PARA IMPRIMIR QUE EL LS TIENE QUE SER MAYOR A LI Y SER REGRESA AL SIMBOLO DE SALIDA PARAA PEDIR OTRO LS, EN CASO DE QUE LS SI SEA MAYOR A LI ENTONCES SE UTILIZA UN SIMBOLO DE SALIDA PARA PREGUNAR CUANTOS NUMEROS INGRESARA, DESPUES SE UTILIZA UN SIMBOLO DE ENTRADA PARA INGRESAR LA CANTIDAD DE NUMEROROS EN N, DESPUES SE UTILIZA UN SIMBOLO DE DECISION PARA PREGUNTAR SI N>0, EN CASO DE QUE NO SEA ASI ENTONCES SE UTILIZA OTRO SIMBOLO DE SALIDA QUE DICE QUE EL N TIENE QUE SER MAYOR A 0 Y SE REGRESA AL SIMBOLO DE SALIDA PARA PEDIR OTRA CANTIDAD DE NUMEROS, EN CASO DE QUE N SI SEA MAYOR A 0 ENTONCES SE UTILIZA UN SIMBOLO DE PROCESO PARA DECIR QUE C=C+1, DESPUES SE UTILIZA UN SIMBOLO DE SALIDA PARA PEDIR UN NUMERO DE N, Y ESE NUMERO SE INGRESA EN UN SIMBOLO DE ENTRADA COMO NUM, POSTERIORMENTE SE UTILIZA UN SIMBOLO DE DECISION PARA PREGUNTAR SI NUM>=LI, AND, NUM<=LS, EN CASO DE QUE NO SEA ASI SE UTILIZA UN SIMBOLO DE SALIDA PARA IMPRIMIR QUE EL NUM TIENE QUE ESTAR ENTRE EL LI Y EL LS, PERO SI SI ES ASI SE UTILIZA OTRO SIMBOLO DE DECISION PARA DECIR SI NUM%2=0 SI LA RESPUETA ES NO ENTONCES SE UTILIZA UN SIMBOLO DE PROCESO PARA DECIR QUE S=SI+NUM, DESPUES SE UTILIZA OTRO SIMBOLO DE PROCESO PARA DECIR QUE CI=CI+1, EN CASO DE QUE LA RESPUESTA SEA SI SE UTILIZA UN SIMBOLO DE PROCESO PARA DECIR QUE SP=SP+NUM, DESPUES UTILIZAMOS OTRO SIMBOLO DE ROCESO PARA DECIR QUE CP=CP+1, DESPUES NOS REGRESAMOS AL SMBOLO DE PROCESO DE C=C+1, Y ASI SUCESIVAMENTE HASTA QUE C SEA IGUAL A N, DESPUES SE UTILIZA UN SIMBOLO DE PROCESO PARA INGRESAR EL CP, CI, DESPUES UTILIZAMOS OTRO SIMBOLO DE PROCESO PARA DECIR QUE EL PP=SP/CP Y EL PI=SI/CI, DESPUES EL PP Y EL PI LO INGRESAMOS EN UN SIMBOLO DE ENTRADA, DESPUES UTILIZAMOS UN SIMBOLO DE DECISION PARA PREGUNTAR SI PP>PI, EN CASO DE QUE NO SEA ASI SE UTILIZA UN SIMBOLO DE SALIDA QUE IMPRIME QUE EL PI ES MAYOR A PP, PERO SI LA RESPUESTA ES SI ENTONCES SE UTILIZA UN SIMBOLO DE SALIDA QUE IMPRIME QUE EL PP ES MAYOR A PI.
#### 1.2 DFD
![8 (Do-While)](https://user-images.githubusercontent.com/113395327/197688603-78d031c0-5bca-476a-830a-75663f4353c6.png)
#### 1.3 Prueba de escritorio 
|C  |SP |CP |PP |SI |CI |PI |LI |LI>0|LS |LS>LI|N  |N>0|C+1|C<=N|NUM|NUM>=LI, NUM<=LS|NUM%2=0|SP=SP+NUM|CP=CP+1|SI=SI+NUM|CI=CI+1|PP=SP/CP|PI=SI/CI|PP>PI|
|---|---|---|---|---|---|---|---|----|---|-----|---|---|---|----|---|----------------|-------|---------|-------|---------|-------|--------|--------|-----|
|0  |0  |0  |0  |0  |0  |0  |5  |SI  |99 |SI   |4  |SI |1  |1<=4|6  |6>=5, 6<=99     |SI     |6        |1      |0        |0      |        |        |     |
|1  |6  |1  |0  |0  |0  |   |   |    |   |     |   |   |2  |2<=4|87 |87>=5, 87<=99   |NO     |6        |1      |87       |1      |        |        |     |
|2  |6  |1  |0  |87 |1  |0  |   |    |   |     |   |   |3  |3<=4|98 |98>=5, 98<=99   |SI     |104      |2      |87       |1      |        |        |     |
|3  |104|2  |0  |87 |1  |0  |   |    |   |     |   |   |4  |4<=4|77 |77>=5, 77<=99   |NO     |104      |2      |164      |2      |104/2   |164/2   |52>81|

#### 1.4 Entradas.
LI

LS

N

NUM

PP

PI

#### 1.5 Salidas.
"LIMITE INFERIOR"

"LIMITE SUPERIOR"

"EL PP ES MAYOR A PI"

"EL PI ES MAYOR AL PP"

#### 1.6 Codigo.
```dar
import 'dart:io';
void main() {
  double sumap = 0;
  double sumai = 0;
  var contp = 0;
  var conti = 0;
  double promp = 0;
  double promi = 0;
  print('Introduce el limite inferior, mayor a 0');
  var li = int.parse(stdin.readLineSync()!);
  if (li < 0) {
    print('tu limite inferior debe ser mayor a 0');
  }
  if (li > 0) {
    print('Ahora introduce un limite superior');
    var ls = int.parse(stdin.readLineSync()!);
    if (ls < li) {
      print('tu limite superior debe ser mayor a tu limite inferior');
    }
    var cont = li;
    do {
      if (cont <= ls) {
        sumai = sumai + cont;
        conti = conti + 1;
      }
      if (cont % 2 == 0) {
        sumap = sumap + cont;
        contp = contp + 1;
        sumai = sumai - cont;
        conti = conti - 1;
      }
      cont = cont + 1;
    } while (cont <= ls);
    promi = sumai / conti;
    print('los impares son $conti y su promedio es $promi');
    promp = sumap / contp;
    print('los pares son $contp y su promedio es $promp');
    if (promp < promi) {
      print('$promi es mayor');
    }
    if (promp > promi) {
      print('el promedio $promp es mayor');
    }
  }
}
```
### Ejercicio 9. 
OBTEN LA FRECUENCIA DE N CALIFICACIONES ENTRE [1,10], INDIQUE LA CANTIDAD DE REPROBADOS Y LA CANTIDAD DE APROBADOS, EL PROMEDIO DE APROBADOS Y PROMEDIO GENERAL. (FOR)
#### 1.1 Analisis. 
OBTENER LA FRECUENCIA DE UNA CANTIDAD DE CALIFICACIONES, PARA DESPUES INDICAR LA CANTIDAD DE REPROBADOS Y LA CANTIDAD DE APROBADOS, FINALMENTE CALCULAR EL PROMEDIO DE LOS REPROBADOS Y EL GENERAL.

SE NECESITA UTILIZAR UN SIMBOLO DE PROCESO PARA INDICAR QUE EL VECTOR SERA CALIFICAIONES [1,10], DESPUES SE UTILIZA UN SIMBOLO DE SALIDA PARA PREGUNTAR CUANTAS CALIICAIONES, DESPUES SE UTILIZA UN SIMBOLO DE ENTARADA PARA INGRESAR LAS CANTIDADES EN LA VARIABLE N, DESPUES SE UTILIZA UN SIMBOLO DE DECISION PARA PREGUNTAR SI N>0, SI NO ES MAYOR SE UTILIZA UN SMBOLO DE SALIDA QUE DICE QUE TIENE QUE SER MAYOR A 0, Y SI SI ES MAYOR SE UTILIZA UN SIMBOLO DE CICLO DE FOR QUE DICE i=0; i<=N; i++; DESPUES SE UTILIZA UN SIMBOLO DE PROCESO QUE DIE QUE CALIFICACION [1,10], DESPUES EL VALOR SE ALMACENA EN C EN UN SIMBOLO DE ENTRADA, DESPUES SE UTILIZA UN SIMBOLO DE DECISION QUE PREGUNTA SI C>, AND C<=10, SI NO ES ASI ENTONCES  SE UTILIZA UN SIMBOLO DE SALIDA QUE IMPRIME QUE C TIENE QUE ESTAR ENTRE 1,10], EN CASO DE QUE SI SEA ASI ENTONCES SE UTILIZA UN SIMBOLO DE PROCESO QUE DICE QUE CAL[C]++, Y SE REGRESA AL CICLO Y ASI SUCESIVAMENTE HASTA QUE i SEAA <=N, DESPUES SE UTLIZA UN SIMBOLO DE SALIDA QUE IMPRIME CAL, DESPUES SE UTILIZA UN SIMBOLO DE PROCESO QUE ALMACENA LOS VALORES: CR=0, CA=0, PA=0, PR=0, SR=0 SA=0, DESPUES VOLVEMOS A LLAMAR LA VARIABLE N EN UN SIMBOLO DE ENTRADA, DESPUES INSERTAMOS UN CICLO PARA INDICAR QUE i=0; i<=N; i++, DESPUES SE UTILIZA UN SIMBOLO DE SALIDA PARA PEDIR UN NUMERO DEL 1 AL 10, DESPUES ESE NUMERO SE ALMACENA EN LA VARIBLE NUM EN UN SIMBOLO DE ENTRADA, DESPUES SE UTILIZA UN SIMBOLO DE DECISION PARA PREGUNTAR SI NUM>0, NUM<=10, SI ES NO SE UTILIZA UN SIMBOLO DE SALIDA QUE IMPRIME UE NUM TIENE QUE ESTAR ENTRE 1 Y 10, SI ES I ENTONCES SE UTILIZA UN SIMBOLO DE DECISION QUE PREGUNTA SI NUM>=6, SI ES CORRECTO SE UTILIZA UN SIMBOLO DE PROCESO QUE INDICA QUE SA=SA+NUM, CA=CA+1, LA RESPUESTA ES NO ENTONCES SE UTILIZA UN SIMBOLO DE PROCESO QUE DICE QUE SR=SR+NUM, CR=CR+1, DESPUES NOS REGRESEAMOS AL CICLO FOR Y ASI SUCECIVANMENTE HASTA QUE i=N, DESPUES UTILIZAMOS UN SIMBOLO DE PROCESO PARA INDICAR QUE PA=SP/CA, PR=SR/CR, FINALMENTE AGREGAMOS OTRO SIMBOLO DE SALIDA QUE INDICA QUE PR=(PA+PR)/2.
#### 1.2 DFD
![9 (For)](https://user-images.githubusercontent.com/113395327/197688637-9a00679f-1399-4b3b-8943-94b722e29fac.png)
#### 1.3 Prueba de escritorio 
|CAL[1,10]|N  |N>0 |i  |i<=N|CAL[1,10]|C  |C>0, C<=10|CAL[C]++|i++|CAL|
|---------|---|----|---|----|---------|---|----------|--------|---|---|
|9        |4  |4>0 |0  |0<=4| 0        |9  |9>0, 9<=0 |10      |1  |9  |
|9        |   |    |1  |1<=4|1         |9  |9>0, 9<=0 |10      |2  |9  |
|8        |4  |4>0 |0  |2<=4| 2        |8  |8>0, 8<=0 |9       |3  |8  |
|7        |   |    |1  |3<=4|  3       |7  |7>0, 7<=0 |8       |4  |7  |




|CR |CA |PR |PA |PG |SR |SA |N  |i  |i<=n|NUM|NUM>0,NUM<=10|NUM>=6|CA+1|SA+NUM|CR+1|SR+NUM|i++|PA=SA/CA|PR=SR/CR|PG=(PR+PA)/2|PG |
|---|---|---|---|---|---|---|---|---|----|---|-------------|------|----|------|----|------|---|--------|--------|------------|---|
|0  |0  |0  |0  |0  |0  |0  |4  |0  |0< 4|8  |8>=0,8<=10   |8>=6  |1   |8     |0   |0     |1  |
|0  |1  |0  |0  |0  |0  |8  |4  |1  |1< 4|5  |5>=0,5<=10   |5>=6  |1   |8     |1   |5     |2  |
|1  |1  |0  |0  |0  |5  |8  |4  |2  |2< 4|9  |9>=0,9<=10   |9>=6  |2   |17    |1   |5     |3  |
|1  |2  |0  |0  |0  |5  |7  |4  |3  |3< 4|3  |3>=0,3<=10   |3>=6  |2   |17    |2   |8     |4  |17/2    |8/4     |(8.5+4)/2   |6.25|


#### 1.4 Entradas.
N

C

NUM

#### 1.5 Salidas.
CR, CA

CAL

#### 1.6 Codigo.
```py
Calificaciones=int(input("Ingrese la cantidad de calificaciones"))
vec=[]
n=0
for i in range(1,Calificaciones+1):
    calificacion=int(input("Calificacion: "))
    n=n+calificacion
    vec.append(calificacion)
promedio=n/len(vec)
npromedio=0
for j in vec:
    if j>promedio:
        npromedio=npromedio+1
aprobado=0
#Primero inicializas el contador
promedioAprobados = 0
for h in vec:
    if h>5:
        aprobado=aprobado+1
        #Va sumando cada unas de las notas
        promedioAprobados = promedioAprobados + h
#Luego saca el promedio sumatoria / cantidad de aprobados 
promedioAprobados = promedioAprobados / aprobado
reprobado=0
for k in vec:
    if k<5:
        reprobado=reprobado+1
print("Max Calificacion", max(vec))
print("Min calificacion", min(vec))
print("Promedio:", promedio)
print("Superiores a promedio:", npromedio)
print("Cantidad de aprobados:", aprobado)
print("Promedio de aprobados:", promedioAprobados)
print("Desaprobados:", reprobado)
```
### Ejercicio 9. 
OBTEN LA FRECUENCIA DE N CALIFICACIONES ENTRE [1,10], INDIQUE LA CANTIDAD DE REPROBADOS Y LA CANTIDAD DE APROBADOS, EL PROMEDIO DE APROBADOS Y PROMEDIO GENERAL. (WHILE)

#### 1.1 Analisis. 
OBTENER LA FRECUENCIA DE UNA CANTIDAD DE CALIFICACIONES, PARA DESPUES INDICAR LA CANTIDAD DE REPROBADOS Y LA CANTIDAD DE APROBADOS, FINALMENTE CALCULAR EL PROMEDIO DE LOS REPROBADOS Y EL GENERAL.

SE NECESITA UTILIZAR UN SIMBOLO DE PROCESO PARA INDICAR QUE EL VECTOR SERA CALIFICAIONES [1,10] Y C=0, DESPUES SE UTILIZA UN SIMBOLO DE SALIDA PARA PREGUNTAR CUANTAS CALIICAIONES, DESPUES SE UTILIZA UN SIMBOLO DE ENTARADA PARA INGRESAR LAS CANTIDADES EN LA VARIABLE N, DESPUES SE UTILIZA UN SIMBOLO DE DECISION PARA PREGUNTAR SI N>0, SI NO ES MAYOR SE UTILIZA UN SMBOLO DE SALIDA QUE DICE QUE TIENE QUE SER MAYOR A 0, Y SI SI ES MAYOR SE UTILIZA UN SIMBOLO DEPROCESO PARA INDICAR CALIFICACION [1,10], DESPUES EL VALOR SE ALMACENA EN C EN UN SIMBOLO DE ENTRADA, DESPUES SE UTILIZA UN SIMBOLO DE DECISION QUE PREGUNTA SI C>, AND C<=10, SI NO ES ASI ENTONCES  SE UTILIZA UN SIMBOLO DE SALIDA QUE IMPRIME QUE C TIENE QUE ESTAR ENTRE [1,10], EN CASO DE QUE SI SEA ASI ENTONCES SE UTILIZA UN SIMBOLO DE PROCESO QUE DICE QUE CAL[C]++ Y C=C+1, DESPUES SE UTILIZA UN SIMBOLO DE DECISION PARA PREGUNTAR SI C<=N, SI ES ASI SE REGRESA AL SIMBOLO DE PORCESO DE CALIFICACION [1,10,], PERO SI ES NO ENTONCES SE UTILIZA UN SIMBOLO DE SALIDA QUE IMPRIME CAL, DESPUES SE UTILIZA UN SIMBOLO DE PROCESO QUE ALMACENA LOS VALORES: C=0, CR=0, CA=0, PA=0, PR=0, SR=0, SA=0, DESPUES VOLVEMOS A LLAMAR LA VARIABLE N EN UN SIMBOLO DE ENTRADA, DESPUES UTILIZAMOS OTRO SIMBOLO DE DECISION PARA PREGUNTAR SI C<=N, SI NO ES ASI SE DESPUES SE UTILIZA UN SIMBOLO DE SALIDA PARA PEDIR UN NUMERO DEL 1 AL 10, DESPUES ESE NUMERO SE ALMACENA EN LA VARIBLE NUM EN UN SIMBOLO DE ENTRADA, DESPUES SE UTILIZA UN SIMBOLO DE DECISION PARA PREGUNTAR SI NUM>0, NUM<=10, SI ES NO SE UTILIZA UN SIMBOLO DE SALIDA QUE IMPRIME UE NUM TIENE QUE ESTAR ENTRE 1 Y 10, SI ES ASI ENTONCES SE UTILIZA UN SIMBOLO DE DECISION QUE PREGUNTA SI NUM>=6, SI ES CORRECTO SE UTILIZA UN SIMBOLO DE PROCESO QUE INDICA QUE SA=SA+NUM, CA=CA+1, LA RESPUESTA ES NO ENTONCES SE UTILIZA UN SIMBOLO DE PROCESO QUE DICE QUE SR=SR+NUM, CR=CR+1, PERO SI EL SIMBOLO DE DECISION DE C<=N ES NO ES SI ENTONCES  UTILIZAMOS UN SIMBOLO DE PROCESO PARA INDICAR QUE PA=SP/CA, PR=SR/CR, FINALMENTE AGREGAMOS OTRO SIMBOLO DE SALIDA QUE INDICA QUE PR=(PA+PR)/2.
#### 1.2 DFD
![9 (While)](https://user-images.githubusercontent.com/113395327/197688668-601d5b47-281d-4231-9cb2-e656611b73b9.png)
#### 1.3 Prueba de escritorio 
|CAL[1,10]|N  |N>0 |C  |C<=N|CAL[1,10]|C  |C>0, C<=10|CAL[C]++|C+1|CAL|
|---------|---|----|---|----|---------|---|----------|--------|---|---|
|9        |4  |4>0 |0  |0<=4|0        |9  |9>0, 9<=0 |10      |1  |9  |
|9        |   |    |1  |1<=4|1        |9  |9>0, 9<=0 |10      |2  |9  |
|8        |4  |4>0 |0  |2<=4|2        |8  |8>0, 9<=0 |9       |3  |8  |
|7        |   |    |1  |3<=4|3        |7  |7>0, 9<=0 |8       |4  |7  |




|CR |CA |PR |PA |PG |SR |SA |N  |C  |C<=n|NUM|NUM>0,NUM<=10|NUM>=6|CA+1|SA+NUM|CR+1|SR+NUM|C+1|PA=SA/CA|PR=SR/CR|PG=(PR+PA)/2|PG |
|---|---|---|---|---|---|---|---|---|----|---|-------------|------|----|------|----|------|---|--------|--------|------------|---|
|0  |0  |0  |0  |0  |0  |0  |4  |0  |0< 4|8  |8>=0,8<=10   |8>=6  |1   |8     |0   |0     |1  |
|0  |1  |0  |0  |0  |0  |8  |4  |1  |1< 4|5  |5>=0,5<=10   |5>=6  |1   |8     |1   |5     |2  |
|1  |1  |0  |0  |0  |5  |8  |4  |2  |2< 4|9  |9>=0,9<=10   |9>=6  |2   |17    |1   |5     |3  |
|1  |2  |0  |0  |0  |5  |7  |4  |3  |3< 4|3  |3>=0,3<=10   |3>=6  |2   |17    |2   |8     |4  |17/2    |8/4     |(8.5+4)/2   |6.25|

#### 1.4 Entradas.
N

C

NUM


#### 1.5 Salidas.
CR, CA

CAL
#### 1.6 Codigo.
```py
Calificaciones=int(input("Ingrese la cantidad de calificaciones"))
vec=[]
n=0
cont = 0
while(cont < Calificaciones):
    calificacion=int(input("Calificacion: "))
    n=n+calificacion
    vec.append(calificacion)
    cont += 1
promedio=n/len(vec)
npromedio=0
for j in vec:
    if j>promedio:
        npromedio=npromedio+1
aprobado=0
#Primero inicializas el contador
promedioAprobados = 0
for h in vec:
    if h>5:
        aprobado=aprobado+1
        #Va sumando cada unas de las notas
        promedioAprobados = promedioAprobados + h
#Luego saca el promedio sumatoria / cantidad de aprobados 
promedioAprobados = promedioAprobados / aprobado
reprobado=0
for k in vec:
    if k<5:
        reprobado=reprobado+1
print("Max Calificacion", max(vec))
print("Min calificacion", min(vec))
print("Promedio:", promedio)
print("Superiores a promedio:", npromedio)
print("Cantidad de aprobados:", aprobado)
print("Promedio de aprobados:", promedioAprobados)
print("Desaprobados:", reprobado)
```
### Ejercicio 9. 
OBTEN LA FRECUENCIA DE N CALIFICACIONES ENTRE [1,10], INDIQUE LA CANTIDAD DE REPROBADOS Y LA CANTIDAD DE APROBADOS, EL PROMEDIO DE APROBADOS Y PROMEDIO GENERAL. (DO/WHILE)

#### 1.1 Analisis. 
OBTENER LA FRECUENCIA DE UNA CANTIDAD DE CALIFICACIONES, PARA DESPUES INDICAR LA CANTIDAD DE REPROBADOS Y LA CANTIDAD DE APROBADOS, FINALMENTE CALCULAR EL PROMEDIO DE LOS REPROBADOS Y EL GENERAL.

SE NECESITA UTILIZAR UN SIMBOLO DE PROCESO PARA INDICAR QUE EL VECTOR SERA CALIFICAIONES [1,10] Y C=0, DESPUES SE UTILIZA UN SIMBOLO DE SALIDA PARA PREGUNTAR CUANTAS CALIICAIONES, DESPUES SE UTILIZA UN SIMBOLO DE ENTARADA PARA INGRESAR LAS CANTIDADES EN LA VARIABLE N, DESPUES SE UTILIZA UN SIMBOLO DE DECISION PARA PREGUNTAR SI N>0, SI NO ES MAYOR SE UTILIZA UN SMBOLO DE SALIDA QUE DICE QUE TIENE QUE SER MAYOR A 0, Y SI SI ES MAYOR SE UTILIZA UN SIMBOLO DEPROCESO PARA INDICAR CALIFICACION [1,10], DESPUES EL VALOR SE ALMACENA EN C EN UN SIMBOLO DE ENTRADA, DESPUES SE UTILIZA UN SIMBOLO DE DECISION QUE PREGUNTA SI C>, AND C<=10, SI NO ES ASI ENTONCES  SE UTILIZA UN SIMBOLO DE SALIDA QUE IMPRIME QUE C TIENE QUE ESTAR ENTRE [1,10], EN CASO DE QUE SI SEA ASI ENTONCES SE UTILIZA UN SIMBOLO DE PROCESO QUE DICE QUE CAL[C]++ Y C=C+1, DESPUES SE UTILIZA UN SIMBOLO DE DECISION PARA PREGUNTAR SI C<=N, SI ES ASI SE REGRESA AL SIMBOLO DE PORCESO DE CALIFICACION [1,10,], PERO SI ES NO ENTONCES SE UTILIZA UN SIMBOLO DE SALIDA QUE IMPRIME CAL, DESPUES SE UTILIZA UN SIMBOLO DE PROCESO QUE ALMACENA LOS VALORES: C=0, CR=0, CA=0, PA=0, PR=0, SR=0, SA=0, DESPUES VOLVEMOS A LLAMAR LA VARIABLE N EN UN SIMBOLO DE ENTRADA, DESPUES SE UTILIZA UN SIMBOLO DE SALIDA PARA PEDIR UN NUMERO DEL 1 AL 10, DESPUES ESE NUMERO SE ALMACENA EN LA VARIBLE NUM EN UN SIMBOLO DE ENTRADA, DESPUES SE UTILIZA UN SIMBOLO DE DECISION PARA PREGUNTAR SI NUM>0, NUM<=10, SI ES NO SE UTILIZA UN SIMBOLO DE SALIDA QUE IMPRIME UE NUM TIENE QUE ESTAR ENTRE 1 Y 10, SI ES ASI ENTONCES SE UTILIZA UN SIMBOLO DE DECISION QUE PREGUNTA SI NUM>=6, SI ES CORRECTO SE UTILIZA UN SIMBOLO DE PROCESO QUE INDICA QUE SA=SA+NUM, CA=CA+1, LA RESPUESTA ES NO ENTONCES SE UTILIZA UN SIMBOLO DE PROCESO QUE DICE QUE SR=SR+NUM, CR=CR+1, DESPUES UTILIZAMOS OTRO SIMBOLO DE DECISION PARA PREGUNTAR SI C<=N, SI ES NO SE REGRESA AL SIMBOLO DE ENTRADA PARA PEDIR OTRO NUMERO, PERO SI ES SI ENTONCES  UTILIZAMOS UN SIMBOLO DE PROCESO PARA INDICAR QUE PA=SP/CA, PR=SR/CR, FINALMENTE AGREGAMOS OTRO SIMBOLO DE SALIDA QUE INDICA QUE PR=(PA+PR)/2.
#### 1.2 DFD
![9 (Do-While)](https://user-images.githubusercontent.com/113395327/197688706-f4036b1b-f435-472c-b2ac-520327f67105.png)
#### 1.3 Prueba de escritorio 
|CAL[1,10]|N  |N>0 |C  |C<=N|CAL[1,10]|C  |C>0, C<=10|CAL[C]++|C+1|CAL|
|---------|---|----|---|----|---------|---|----------|--------|---|---|
|9        |4  |4>0 |0  |0<=4|0        |9  |9>0, 9<=0 |10      |1  |9  |
|9        |   |    |1  |1<=4|1        |9  |9>0, 9<=0 |10      |2  |9  |
|8        |4  |4>0 |0  |2<=4|2        |8  |8>0, 9<=0 |9       |3  |8  |
|7        |   |    |1  |3<=4|3        |7  |7>0, 9<=0 |8       |4  |7  |




|CR |CA |PR |PA |PG |SR |SA |N  |C  |C<=n|NUM|NUM>0,NUM<=10|NUM>=6|CA+1|SA+NUM|CR+1|SR+NUM|C+1|PA=SA/CA|PR=SR/CR|PG=(PR+PA)/2|PG |
|---|---|---|---|---|---|---|---|---|----|---|-------------|------|----|------|----|------|---|--------|--------|------------|---|
|0  |0  |0  |0  |0  |0  |0  |4  |0  |0< 4|8  |8>=0,8<=10   |8>=6  |1   |8     |0   |0     |1  |
|0  |1  |0  |0  |0  |0  |8  |4  |1  |1< 4|5  |5>=0,5<=10   |5>=6  |1   |8     |1   |5     |2  |
|1  |1  |0  |0  |0  |5  |8  |4  |2  |2< 4|9  |9>=0,9<=10   |9>=6  |2   |17    |1   |5     |3  |
|1  |2  |0  |0  |0  |5  |7  |4  |3  |3< 4|3  |3>=0,3<=10   |3>=6  |2   |17    |2   |8     |4  |17/2    |8/4     |(8.5+4)/2   |6.25|

#### 1.4 Entradas.
N

C

NUM

#### 1.5 Salidas.
CR, CA

CAL

#### 1.6 Codigo.
```py
Calificaciones=int(input("Ingrese la cantidad de calificaciones"))
vec=[]
n=0
cont = 0
while(True):
    calificacion=int(input("Calificacion: "))
    n=n+calificacion
    vec.append(calificacion)
    cont += 1
    if(cont>=Calificaciones):
        break;
        
aprobado=0
promedioAprobados = 0
for h in vec:
    if h>=5:
        aprobado=aprobado+1
        promedioAprobados = promedioAprobados + h
promedioAprobados = promedioAprobados / aprobado
reprobado=0
for k in vec:
    if k<=5:
        reprobado=reprobado+1
print("Cantidad de aprobados:", aprobado)
print("Cantidad de reprobados:", reprobado)
print("Promedio de aprobados:", promedioAprobados)
```

### Ejercicio 10. 
CATURE 10 NUMEROS ENTEROS POSITIVOS, DIGA CUAL ES MAYOR Y CUAL ES MENOR.
#### 1.1 Analisis. 
CAPTURAR 10 NUMEROS ENTEROS POSITIVOS, DESPUES CALCULAR CUAL NUMERO ES MAYOR Y CUAL ES MENOR.

SE UTILIZA UN SIMBOLO DE PROCESO DONDE A[11], DESPUES SE UTILIZA EL CICLO FOR i=1; i<=10; i++, DESPUES SE UTILIZA EL SIMBOLO DE ENTRADA PARA N, DESPUES SE UTILIZA EL SIMBOLO DE DECISION PARA PREGUNTAR SI N>0 SI NO ES ASI SE UTILIZA UN SIMBOLO DE SALIDA PARA IMPRIMIR QUE N TIENE QUE SER MAYOR A 0 Y SE REGRESA AL SIMBOLO DE ENTRADA PARA PEDIR OTRAN, EN CASO DE QUE N SI SEA MAYOR A 0 SE UTILIZA UN SIMBOLO DE PROCESO DONDE NUM[i]=N, DESPUES SE REGRESA AL CICLO FOR Y ASI SUECIVAMENTE HASTA QUE I SEA 10 Y FINALMENTE SE IMPRIME NUM, DESPUES SE UTILIZA UN SIMBOLO DE PROCESO DONDE MAYOR=0, DESPUES SE UTILIZA OTRO SIMBOLO DE CICLO PARA i=1; i<=10; i++; DESPUES SE PREGUNTA SI MAYOR>NUM[i], SI NO ES ASI SE UTILIZA UN SIMBOLO DE PROCESO DONDE MAYOR=NUM[i], Y EN CASO DE QUE MAYOR SI SEA MAYOR A NUM[i] SE REGRESA AL CICLO Y ASI SUCECIBAMENTE HASTA QUE I SEA 10, DESPUES SE UTILIZA UN SIMBOLO DE SALIDA PARA IMPRIMIR MAYOR, DESPUES SE UTILIZA UN SIMBOLO DE PROCESO DONDE MENOR=MAYOR, DESPUES VOLVEMOS A UTILIZAR UN SIMBOLO FOR PARA PREGUNTAR SI MENOR<NUM[i], EN CASO DE QUE NO SEA ASI SE UTILIZA UN SIMBOLO PROCESO DONDE MENOR=NUM[i], DESPUES SE REGRESA AL SIMBOLO DE FOR, FINALMENTE IMPRIMIMOS MENOR.
#### 1.2 DFD.
[![44.jpg](https://i.postimg.cc/htK5gzBt/44.jpg)](https://postimg.cc/ykrPyNxM)
#### 1.3 Prueba de escritorio 
|A[11] |i=1 |i<=10|N |A[i]|N>0|NUM[i]=N|i++|NUM|MAYOR|i |i<=10|MAYOR>NUM[i]|MAYOR=NUM[i]|i++|MAYOR|MENOR=MAYOR|i |i<=10|MENOR<NUM[i]|MENOR=NUM[i]|i++|MENOR|
|------|----|-----|--|----|---|--------|---|---|-----|--|-----|------------|------------|---|-----|-----------|--|-----|------------|------------|---|-----|
|0     |1   |1<=10|1 |1   |1>0|1       |2  |1  |0    |1 |1<=10|0>1         |1           |2  |     |10         |1 |1<=10|10<1        |1           |2  |     |
|1     |2   |2<=10|2 |2   |2>0|2       |3  |2  |1    |2 |2<=10|1>2         |2           |3  |     |           |2 |2<=10|1<2         |            |3  |     |
|2     |3   |3<=10|3 |3   |3>0|3       |4  |3  |2    |3 |3<=10|2>3         |3           |4  |     |           |3 |3<=10|1<3         |            |4  |     |     
|3     |4   |4<=10|4 |4   |4>0|4       |5  |4  |3    |4 |4<=10|3>4         |4           |5  |     |           |4 |4<=10|1<4         |            |5  |     |
|4     |5   |5<=10|5 |5   |5>0|5       |6  |5  |4    |5 |5<=10|4>5         |5           |6  |     |           |5 |5<=10|1<5         |            |6  |     |
|5     |6   |6<=10|6 |6   |6>0|6       |7  |6  |5    |6 |6<=10|5>6         |6           |7  |     |           |6 |6<=10|1<6         |            |7  |     |
|6     |7   |7<=10|7 |7   |7>0|7       |8  |7  |6    |7 |7<=10|6>7         |7           |8  |     |           |7 |7<=10|1<7         |            |8  |     |
|7     |8   |8<=10|8 |8   |8>0|8       |9  |8  |7    |8 |8<=10|7>8         |8           |9  |     |           |8 |8<=10|1<8         |            |9  |     |
|8     |9   |9<=10|9 |8   |9>0|9       |10 |9  |8    |9 |9<=10|8>9         |9           |10 |     |           |9 |9<=10|1<9         |            |10 |     |
|9     |10  |10<=10|10|9  |10>0|10     |   |10 |9    |10|10<=10|9>10       |10          |   |10   |           |10|10<=10|1<10       |            |   |1    | 


#### 1.4 Entradas
Ninguna

#### 1.5 Salidas.
NUM

MAYOR

MENOR

#### 1.6 Codigo.
```py
lista = [10]
cant = int(input("¿Cuantos numeros desea capturar?"))
i=1
while i <= cant:
    n = int(input(f"{i} Ingrese un numero: "))
    lista.append(n)
    i+=1
print("Numero mayor es ",max(lista))
print("Numero menor es ",min(lista))
```

### Ejercicio 11. 
OBTEN LA DISTANCIA MAYOR ENTRE 2 NUMEROS CONCECUTIVOS EN UNA LISTA DE 10 NUMEROS.
#### 1.1 Analisis.
Insertar 10 numeros, posteriormente calcular la distancia de 2 en 2 numeros y decir cual es la mayor distancia.

SE UTILIZA UN SIMBOLO DE PROCESO DONDE DIS[9] Y NUM[10], DESPUES SE UTILIZA EL CICLO FOR i=1; i<=9; i++, DESPUES SE UTILIZA EL SIMBOLO DE ENTRADA PARA N, DESPUES SE UTILIZA EL SIMBOLO DE DECISION PARA PREGUNTAR SI N>0 SI NO ES ASI SE UTILIZA UN SIMBOLO DE SALIDA PARA IMPRIMIR QUE N TIENE QUE SER MAYOR A 0 Y SE REGRESA AL SIMBOLO DE ENTRADA PARA PEDIR OTRAN, EN CASO DE QUE N SI SEA MAYOR A 0 SE UTILIZA UN SIMBOLO DE PROCESO DONDE NUM[i]=N, DESPUES SE REGRESA AL CICLO FOR Y ASI SUECIVAMENTE HASTA QUE I SEA 9, DESPUES SE UTILIZA OTRO CICLO DE FOR DONDE i=1; i<9; i++, DESPUES SE UTILIZA UN SIMBOLO DE PROCESO DONDE NUM[i]-NUM[i+1], despues se utiliza un simbolo de decision donde DIS<=, SI NO ES ASI SE UTILIZA UN SIMBOLO DE PROCESO DONDE D[i]=DIS, EN CASO DE QUE SEA SI SE UTILIZA UN SIMBOLO DE PROCESO DONDE D[i]=DIS*-1, Y SE REGRESA AL CICLO HASTA QUE i SEA 9, DESPUES SE UTILIZA UN SIMBOLO DE PROCESO DONDE MAYOR=0, DESPUES SE UTILIZA OTRO SIMBOLO DE CICLO PARA i=1; i<9; i++; DESPUES SE PREGUNTA SI MAYOR>NUM[i], SI NO ES ASI SE UTILIZA UN SIMBOLO DE PROCESO DONDE MAYOR=NUM[i], Y EN CASO DE QUE MAYOR SI SEA MAYOR A NUM[i] SE REGRESA AL CICLO Y ASI SUCECIBAMENTE HASTA QUE I SEA 8, DESPUES SE UTILIZA UN SIMBOLO DE SALIDA PARA IMPRIMIR MAYOR.
#### 1.2 DFD
![12](https://user-images.githubusercontent.com/113395327/197684202-afbcfb05-e77c-4657-97aa-c9c7c5377989.png)
#### 1.3 Prueba de escritorio 
|DIS[9],NUM[10]|i=1 |i<=9 |N |N>0|NUM[i]=N|i++|i  |i<9|DIS=NUM[i]-NUM[i+1]|DIS<0|D[i]=DIS|D[i]=DIS*-1|i++|
|--------------|----|-----|--|---|--------|---|---|---|-------------------|-----|--------|-----------|---|
|0             |1   |1<=9 |1 |1>0|1       |2  |1  |1<9|1                  |1<0  |        |           |2  |
|1             |2   |2<=9 |2 |2>0|2       |3  |2  |2<9|1                  |1<0  |||3| 
|2             |3   |3<=9 |3 |3>0|3       |4  |3  |3<9|1                  |1<0  |||4|
|3             |4   |4<=9 |4 |4>0|4       |5  |4  |4<9|1                  |1<0  |||5|
|4             |5   |5<=9 |5 |5>0|5       |6  |5  |5<9|1                  |1<0  |||6|
|5             |6   |6<=9 |6 |6>0|6       |7  |6  |6<9|1                  |1<0  |||7|
|6             |7   |7<=9 |7 |7>0|7       |8  |7  |7<9|1                  |1<0  |||8|
|7             |8   |8<=9 |8 |8>0|8       |9  |8  |8<9|1                  |1<0  |||9|
|8             |9   |9<=9 |9 |9>0|9       |   |9  |   |1                  |1<0  |1       |  
|9             |


|MAYOR|i |i<9|MAYOR>D[i]|MAYOR=D[i]|i++|MAYOR|
|-----|--|---|----------|----------|---|-----|
|O    |1 |1<9|0>1       |1|2|
|1    |2 |2<9|1<2       | 2 |3|
|2    |3 |3<9|2<3       | 3|4|
|3    |4 |4<9|3<4       |4|5|
|4    |5 |5<9|4<5       |5|6|
|5    |6 |6<9|5<6       |6|7|
|6    |7 |7<9|6<7       |7|8|
|7    |8 |8<9|7<8       |8|9|
|8    |  |   |          |||9|

#### 1.4 Entradas.
n.
#### 1.5 Salidas.
mayor=d[i].
#### 1.6 Codigo.
```dart
import 'dart:io';
import 'dart:core';
void main() {
  var Re = 0;
  var mayor = 0;
  stdout.write('Ingresa tus numeros \n');
  var lista = List.filled(10, 0);
  for (var i = 0; i <= 9; i++) {
    int Entrada = int.parse(stdin.readLineSync()!);
    lista[i] = Entrada;
  }
  var diferencias = List.filled(9, 0);
  for (var j = 0; j <= 8; j++) {
    diferencias[j] = (lista[j] - lista[j + 1]);
  }
  mayor = diferencias[0];
  for (var k = 0; k <= 8; k++) {
    if (mayor < diferencias[k]) {
      mayor = diferencias[k];
    } else {}
  }
  stdout.write("Tu lista es ");
  print(lista);
  stdout.write("y sus diferencias son ");
  print(diferencias);
  print('La diferencia mayor es ');
  print(mayor);
}
```

### Ejercicio 12. Almacene en un vector el resultado de una tabla (10 numeros)
#### 1.1 Analisis. 
Al tamaño del array sera de 10, validaremos el numero de la tabla, en una condición de termino.
#### 1.2 DFD
![13](https://user-images.githubusercontent.com/113395327/197684095-af2797a3-870a-44fe-a951-5756dbb6a704.png)
#### 1.3 Prueba de escritorio 
|n|n>0|i|i<=9|A[i]= n * i|i+1|A|
|-|-|-|-|-|-|-|
|5|5>0|0|0<=9|A[0]= 5 * 0|0+1|0|
| |   |1|1<=9|A[1]= 5 * 1|1+1|5|
| |   |2|2<=9|A[2]= 5 * 2|2+1|10|
| |   |3|3<=9|A[3]= 5 * 3|3+1|15|
| |   |4|4<=9|A[4]= 5 * 4|4+1|20|
| |   |5|5<=9|A[5]= 5 * 5|5+1|25|
| |   |6|6<=9|A[6]= 5 * 6|6+1|30|
| |   |7|7<=9|A[7]= 5 * 7|7+1|35|
| |   |8|8<=9|A[8]= 5 * 8|8+1|40|
| |   |9|9<=9|A[9]= 5 * 9|9+1|45|
#### 1.4 Entradas.
n.
#### 1.5 Salidas.
Mayor.
#### 1.6 Codigo.
```dart
import 'dart:io';
void main(List<String> args) {
  var array = [];
  int n = int.parse(stdin.readLineSync()!);
  for (var i = 0; i < 11; i++) {
    array.add(i);
    array[i] = n * i;
  }
  print('$array');
}
```

### Ejercicio 13. 
Escriba un dfd que escriba el siguiente dibujo.
#### 1.1 Analisis. 
Desarrollar el siguiente diagrama de flujo.

SE UTILIZA UN SIMBOLO DE CICLO DE FOR DONDE i=1; i<=5; i++, DESPUES SE UTILIZA OTRO CICLO DE FOR DONDE j=1; j<=i;j++, después se utiliza un símbolo de salida para imprimir 1 y se regresa al segundo ciclo y del segundo ciclo al primero.

#### 1.2 DFD
![14](https://user-images.githubusercontent.com/113395327/197684075-b7439c57-f658-44ec-b8d3-cb3a0f734614.png)
#### 1.3 Prueba de escritorio 
|i  |i<=5|j  |j<=i|1     |i++ |j++ |
|---|----|---|----|------|----|----|
|1  |1<=5|1  |1<=1|1     |1   |1   | 
|2  |2<=5|2  |2<=2|11    |2   |2   |
|3  |3<=5|3  |3<=3|111   |3   |3   |
|4  |4<=5|4  |4<=4|1111  |4   |4   |
|5  |5<=5|5  |5<=5|11111 |5   |5   |

#### 1.4 Entradas.
No tiene ninguna entrada
#### 1.5 Salidas.
 *
#### 1.6 Codigo.
```dart
import 'dart:io';
void main() {
  var n = 5;
  for (var i = 1; i <= 5; i++) {
    for (var j = 1; j <= i; j++) {
      stdout.write('*');
    }
    print('');
  }
}
#### Gracias por leer
...
