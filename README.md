# 🔍 Búsqueda Lineal (Linear Search) en Java

## 📖 ¿Qué es?

La **Búsqueda Lineal** es el algoritmo de búsqueda más simple. Consiste en recorrer un array elemento por elemento de forma secuencial hasta encontrar el valor deseado (target) o llegar al final del array.

### ✨ Características

- **Ventajas**: Simple de implementar, funciona con arrays no ordenados
- **Desventajas**: Ineficiente para arrays grandes

### 🎯 Casos de uso ideales

* Arrays pequeños
* Arrays no ordenados (unsorted)
* Cuando solo necesitas buscar una vez
* Datos no indexados

## 🛠️ El Algoritmo

La lógica es directa:

1. **Empieza** en el primer elemento (índice 0)
2. **Compara** el elemento actual con el valor buscado `x`
3. **Si coincide**: Devuelve el índice actual
4. **Si no coincide**: Pasa al siguiente elemento
5. **Si terminas** el array y no lo encontraste: Devuelve `-1`

## 💻 Código en Java

La implementación estándar y limpia que hay que saberse:

```java
class LinearSearch {
   
   /**
    * Método estático para realizar la búsqueda lineal
    * @param arr Array de enteros donde buscar
    * @param x Valor a buscar
    * @return Índice del elemento si se encuentra, -1 si no existe
    */
   public static int search(int[] arr, int x) {
       int n = arr.length;
       
       // Recorremos todo el array
       for (int i = 0; i < n; i++) {
           // Si encontramos el elemento, devolvemos su índice
           if (arr[i] == x) {
               return i;
           }
       }
       
       // Si llegamos aquí, el elemento no está en el array
       return -1;
   }

   public static void main(String[] args) {
       int[] data = { 2, 5, 8, 12, 16, 23, 38, 56, 72, 91 };
       int target = 23;

       int result = search(data, target);

       if (result == -1) {
           System.out.println("Elemento no encontrado.");
       } else {
           System.out.println("Elemento encontrado en el índice: " + result);
       }
   }
}
