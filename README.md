![](https://github.com/NoeRoson/Sharks/blob/main/Image/Portada.png)
# W2 Project - Data cleaning "Sharks Attacks"

**Objetivo**: Limpieza de un conjunto de datos relativos a ataques de tiburones y pequeño análisis de los mismos.

# Check-list:
**1. Importar librerías necesarias para la limpieza y el análisis.**

**2. Importar el dataset y hacer una copia sobre la que trabajar.**

**3. Cumplir la condición de que tenga al menos 2500 filas y 23 columnas.**

**4. Exploración de los datos y las columnas:**
   + Case number: Indice de los casos.
   + Case Number.1 y Case Number.2: Copias del índice (Case Number)
   + Date: Fecha en la que se produce el ataque.
   + Year: Año en el que se produce el ataque.
   + Type: Situación en que se produce.
   + Country: País en el que sucede.
   + Area: Región en la que sucede.
   + Location: Lugar concreto del ataque.
   + Activity: Actividad que estaba realizando la víctima.
   + Name: Nombre de la persona atacada.
   + Sex: Indica el sexo de la persona atacada.
   + Age: Indica la edad de la persona atacada.
   + Injury: Descripción de las lesiones causadas.
   + Fatal (Y/N): Indica Y si el ataque fue mortal y N si no.
   + Time: Indica la hora a la que se produjo el ataque.
   + Species: Indica la especie del tiburón.
   + Investigator or Source: Persona o instituación responsable de la investigación del ataque.
   + pdf: Nombre del pdf asociado al accidente.
   + href formula y href: Link al pdf del accidente.
   + original order: Orden original de los casos.

**5. Exploración de los valores nulos:**
   + Se eliminan las columnas donde todos los valores son nulos (Unnamed: 22 y Unnamed: 23).
   + Se eliminan las filas donde más del 75% de los datos son nulos.
   + Se exploran los nulos columna a columna, rellenando en algunos casos por el valor correcto y, en otros, por 'Unknown'.

**6. Eliminación de duplicados.**

**7. Limpieza por columnas:**
   + 'Year' y 'original order': pasamos a enteros. En 'Year' además se rellenan los valores  = 0 con el año que aparece en la columna 'Date'.
   + 'Time': se extraen todos los datos posibles y se categorizan por franjas horarias: morning, afternoon, evening y night.
   + 'Species': se transforman los nulos a 'Unknown'.
   + 'Age': se extraen todos los valores posibles y se pasan a enteros. Los nulos se transforman en la moda para no interferir demasiado en la descripción estadística posterior.
   + 'Sex': se unifican en M: hombres y F: mujeres.
   + 'Fatal (Y/N)': se unifican en Y: ataque mortal, N: ataque no mortal y 'UNKNOWN'.
   + 'Type': se unifican en 'Boating', 'Unprovoked', 'Invalid', 'Provoked', 'Questionable', 'Sea Disaster'.
   + 'Name': se transforman en 'Unknown' aquellos que contenían female o male.
   + 'Country': se unifican los repetidos, se eliminan espacios
   + 'Date': se elimina ya que esa información se contiene en otras columnas.

**8. Creación de nuevas columnas:**
   + 'Month': se extrae esta información de la columna 'Case Number'.
   + 'Continent': se crea un diccionario con los países para clasificarlos por continente.

**9. Análisis de datos:**
   +  Se analizan atendiendo a las columnas Month, Year, Time, Continent, Sex, Age y Fatal (Y/N).

**10. Visualización de los datos.**

**11. Conclusiones.**
