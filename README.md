# Operador-Desconocido
Este repositorio se utilizara para investigar el operador "->" que es algo con punteros 

### Codigo no probado
```c++
struct estructura {
  String nombre;
  int numero;
};


void setup()
{
  Serial.begin(11500);

  struct estructura s1;
  struct estructura *ptr;

  ptr = &s1;
  ptr->nombre = "Diego";
  ptr->numero = 20;

  delay(5000);

  Serial.println("Nombre: " + ptr->nombre);
  Serial.println("Numero: " + ptr->numero);
}

void loop()
{

}
```
