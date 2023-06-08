# Operador-Desconocido
Este repositorio se utilizara para investigar el operador "->" que es algo con punteros 

### Utilizando punteros en estructuras

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

### Este codigo es equivalente al anterior
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
  ptr->nombre = "Diego";
  ptr->numero = 20;

  delay(5000);

  Serial.println(ptr->nombre);
  Serial.println(ptr->numero);
}

void loop()
{

}
```

ptr->campo es equivalente a (*ptr).campo
