# simba_eshop
## simba_eshop

```
import sqlite3

connection = sqlite3.connect('movies.db')

cursor = connection.cursor()
#inserting multiple values

# famousFilms = [('pulp fiction','quentin tarantino',1994),('backto the future','robert tarantino',1985),('moonrise','wes anderson',1994)]
# cursor.executemany('INSERT INTO movies VALUES(?,?,?)', famousFilms)
# cursor.execute('''SELECT * FROM movies''')
# print(cursor.fetchall())

#filtering db
release_year = (1985,)
cursor.execute("select * from movies where year=?", release_year)
print(cursor.fetchall())

#inserting single values
# cursor.execute('''INSERT INTO movies VALUES('taxi driver', 'martin scosense',1976)''')
# cursor.execute('''SELECT * FROM movies''')
# print(cursor.fetchone())

connection.commit()
connection.close()
```
