# Proyecto: Solucionador de Simplex

Este proyecto es una aplicación web que permite resolver problemas de programación lineal mediante el método Simplex. Proporciona una interfaz gráfica amigable para que los usuarios puedan ingresar la función objetivo y las restricciones, y ver paso a paso el proceso de resolución.

## Descripción del Proyecto

El programa fue desarrollado utilizando JavaScript y Visual Studio Code, aprovechando las facilidades que este entorno brinda para ejecutar interfaces gráficas.

### Interpretación

Este programa resuelve variables de solución óptima mediante el método Simplex. Solo requiere que el usuario ingrese:

- La función objetivo.
- Las restricciones respectivas.
- El tipo de operación (Maximización o Minimización).

## Funcionamiento del Código

### Captura de Datos del Formulario

- El evento `submit` del formulario es capturado para prevenir la recarga de página.
- Se toman los valores de los campos de texto para la función objetivo, las restricciones y el tipo de optimización (maximizar o minimizar).
- Si no se han proporcionado datos suficientes (por ejemplo, si la función objetivo o las restricciones están vacías), se muestra un mensaje de alerta.
- Los datos de entrada son sanitizados para reemplazar caracteres como `≤` por `<=` y eliminar espacios en blanco.

### Solución del Problema usando Simplex

La función principal, `solveSimplex()`, resuelve el problema mediante el método Simplex. El proceso se divide en dos fases:

1. **Fase 1:** Se resuelve un problema auxiliar agregando variables artificiales, si es necesario, para hacer el problema factible.
2. **Fase 2:** Después de eliminar las variables artificiales, se resuelve el problema original utilizando la función objetivo dada.

#### Cada iteración de las fases realiza:

- **Búsqueda de la columna pivote:** Identifica la columna con el valor más negativo en la última fila (indicando que no se ha alcanzado la solución óptima).
- **Búsqueda de la fila pivote:** Determina qué fila debe pivotear basándose en las proporciones mínimas (regla de razón mínima).
- **Operaciones de pivotado:** Realiza las operaciones de pivote para actualizar la tabla.

Los pasos en cada iteración se registran y luego se muestran al usuario.

### Visualización de Resultados

Los resultados del algoritmo se muestran en un área de texto en la interfaz web. Se imprimen tanto las tablas del Simplex en cada iteración como el resultado óptimo final.

## Instrucciones de Uso

1. Navegar a la página principal del repositorio:  
   [https://github.com/aluacam10/Proyecto_IO_Primer_Parcial.git](https://github.com/aluacam10/Proyecto_IO_Primer_Parcial.git)
2. Hacer clic en `<>Code`.
3. Seleccionar la opción "Descargar ZIP" para descargar todo el proyecto bajo el nombre `Proyecto_IO`.
4. Si tienes un entorno con soporte para JavaScript, abre los archivos directamente. Si no, puedes usar el siguiente compilador en línea:  
   [https://codi.link](https://codi.link) y colocar cada código en su espacio correspondiente.
5. En el primer campo, ingresa el valor de la función objetivo.
6. En el siguiente campo, ingresa los valores de cada restricción y su tipo de valor.
7. Pulsa el botón **Resolver**, y la operación aparecerá con todos los procedimientos correspondientes y su solución óptima.

## Nombres de los Integrantes

- Erick M. Rodríguez del Ángel
- David C. López González
- Raúl R. Mena Tzel
- Felipe A. Yan Santos
