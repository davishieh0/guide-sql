# Passo a passo: Mysql connector + Flask
## Siga os passos 0 a 3 para realizar o processo

### 0. Instalar mysql connector (terminal)

```bash
pip install mysql-connector-python
```

### 1. Importe o mysql connector e estabeleça a conexão

```python
import mysql.connector

conexao = mysql.connector.connect(
    host='127.0.0.1',
    user='root',
    password='Davi1712',
    database='bd_betinha',
)

cursor = conexao.cursor()
	
```

### 2. Consultas / SELECT

```python
app.route('/visualizar_eventos', methods=['GET', ])
def visualizar_eventos():
	cursor.execute('SELECT * FROM Eventos')
	meus_eventos = cursor.fetchall() # adiciona a lista na var meus_eventos
	
return make_response(
	jsonify(
		mensagem='lista de eventos.',
		dados=meus_eventos
	)
)

```
### 2. Inserções, atualizações e exclusões / INSERT

```python

app.route('/adicionar_eventos', methods=['POST', ])
def adicionar_eventos():
	my_cursor = mydb.cursor() #Ligando o cursor
	sql = <comando>
	my_cursor.execute(sql)
	mydb.commit()

```

### 3. Fechando a conexão

Sempre que terminar de usar o banco de dados, é importante fechar a conexão e o cursor.

```python
cursor.close()
conexao.close()
```


### obs
Fazer isso pra formatar os bgl
```python
	meus_eventos = list()
	for evento in meus_eventos:
		evento.append(
			{
				'id': carro[0],
				'marca': carro[1],
				'modelo': carro[2],
				'ano': carro[3]
			}
			)
```