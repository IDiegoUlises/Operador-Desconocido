# Operador Flecha

```c++
struct estructura {
  String nombre;
  int numero;
};

void setup()
{
  Serial.begin(115200);
  
  struct estructura s1;
  struct estructura *ptr;
  
  ptr = &s1;

  (*ptr).nombre = "Diego";
  (*ptr).numero = 20;
  
  delay(5000);

  Serial.println((*ptr).nombre);
  Serial.println((*ptr).numero);
}

void loop()
{

}
```
* En este codigo se esta utilizando el operador punto que es (*)

### Este codigo es equivalente al anterior
```c++
//Estructura
struct estructura {
  String nombre;
  int numero;
};


void setup()
{
  //Se declara el puerto serial
  Serial.begin(115200);

  //Se declara la variable estructura
  struct estructura s1;

  //Declara el puntero de estructura
  struct estructura *ptr;

  //Almacena la direccion de la variable de estructura en el puntero estructura
  ptr = &s1;

  //Establece los valores
  ptr->nombre = "Diego";
  ptr->numero = 20;

  //Retardo de cinco segundos
  delay(5000);

  //Imprime el valor del miembro de la estructura
  Serial.println(ptr->nombre);
  Serial.println(ptr->numero);
}

void loop()
{

}
```

* En este codigo se utiliza el operador flecha que es ``` -> ```
* En la definicion ``` (*ptr).nombre ``` es equivalente a ``` ptr->nombre ```
* El motivo porque se utiliza el el operador flecha es simplemente porque es mas sencillo para programar
