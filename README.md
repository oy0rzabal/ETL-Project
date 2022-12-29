# ETL Project
Proyecto de migracion de sistema crm a base de datos postgresql para disponibilizar la data

Se utilizara:

- Python
- Pandas

Pasos para poder resolver :

Generar tablas de: 

- Categorias

        Codigo para generar la tabla de ratings
  <pre><code> 
    #Scamos la columnas inncesarias
    new_table = rating.drop(columns=['timestamp', 'userId','movieId'])
    #empezamos a unir las columnas con movie
    new_table = pd.concat([new_table, movie], axis=1)
    #Empezamos a sacar los datos que no vayamos a necesitar:
    table = new_table.dropna()
                        </code></pre>
