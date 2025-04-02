# API de Restaurantes com FastAPI

## Introdução

Este projeto tem como objetivo criar uma API que retorna informações sobre restaurantes e seus cardápios utilizando FastAPI. Também exploramos conceitos de ambientes virtualizados e manipulação de dados JSON com Python.
Explorei POO com herança, métodos especiais e uso de super() Para herdar da classe mae/pai. Desenvolvi um sistema de cardápio usando classes e métodos abstratos, aplicando descontos. Aprendi a criar e gerenciar ambientes virtuais com venv e criei APIs com FastAPI, desenvolvendo rotas, documentação automática e requisições HTTP.
---

## Configuração do Ambiente Virtual (VENV)

### Criando o ambiente virtual
```sh
python -m venv nome_da_venv
```

### Ativando o ambiente virtual
```sh
venv\Scripts\activate.bat
```

### Desativando o ambiente virtual
```sh
deactivate
```

---

## Instalação das Dependências

Instale as bibliotecas necessárias com:
```sh
pip install fastapi
pip install uvicorn
pip install requests
```

---

## Estrutura do Projeto

O projeto é composto por dois arquivos principais:
- `app.py`: Responsável por manipular os dados JSON dos restaurantes.
- `main.py`: Contém a API criada com FastAPI.

### `app.py`

1. Importamos a biblioteca `requests` para obter dados de uma URL remota.
2. Criamos uma variável `url` contendo o link da API de restaurantes.
3. Realizamos uma requisição GET para obter os dados JSON.
4. Verificamos se a resposta foi bem-sucedida (`status_code == 200`).
5. Criamos um dicionário para armazenar os restaurantes e seus itens.
6. Iteramos pelos dados JSON, extraindo informações sobre cada restaurante.
7. Salvamos os dados em arquivos JSON individuais.

### `main.py`

1. Importamos `FastAPI` e `Query`.
2. Criamos uma instância da API com `app = FastAPI()`.
3. Definimos um endpoint simples `/api/hello`.
4. Criamos um endpoint `/api/restaurante/` para retornar informações sobre os restaurantes.
5. Utilizamos `Query` para permitir busca por restaurante específico na URL.
6. Se nenhum restaurante for informado, retornamos todos os dados.
7. Caso um nome seja fornecido, filtramos os resultados e retornamos apenas os dados daquele restaurante.

---

## Como Executar o Projeto

1. Inicialize o ambiente virtual:
   ```sh
   venv\Scripts\activate.bat
   ```
2. Execute o servidor FastAPI:
   ```sh
   uvicorn main:app --reload
   ```

---

## Testando a API

### Listar todos os restaurantes
```sh
http://127.0.0.1:8000/api/restaurante/
```

### Buscar um restaurante específico (ex: KFC)
```sh
http://127.0.0.1:8000/api/restaurante/?restaurante=KFC
```

### Acessar a documentação interativa
```sh
http://127.0.0.1:8000/docs
```

Nessa interface, é possível testar os endpoints diretamente.

---

## Conceitos Abordados

### Ambientes Virtualizados
- Criamos e ativamos um ambiente virtual com `venv`.
- Exploramos o uso do `requirements.txt` para documentar dependências.

### Manipulação de JSON
- Extraímos dados JSON de uma API.
- Filtramos e armazenamos dados localmente.

### FastAPI
- Criamos uma API simples para manipulação de dados.
- Utilizamos `Query` para criar endpoints flexíveis.
- Exploramos as ferramentas de documentação automática (`docs` e `redoc`).

---
## Informaçoes Adicionais
Ler os arquivos: 
- OqAprendemos.txt
- explicaçaodetalhada.txt
- note.txt
- note2.txt
  
## Conclusão
Este projeto demonstrou como criar uma API utilizando FastAPI, manipular JSON e estruturar um ambiente virtualizado para desenvolvimento em Python. Essas práticas são essenciais para criar sistemas robustos e bem documentados.

---

**Autor:** Lucas César Lorena
