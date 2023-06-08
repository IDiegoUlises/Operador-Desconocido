# Operador-Desconocido
Este repositorio se utilizara para investigar el operador "->" que es algo con punteros 

### Codigo que funciona utilizando el operador de flecha ->
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

### El codigo anterior es equivalente
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
