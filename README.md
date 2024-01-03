# **API Intermediária**

## Curso **API**

O CURSO API é uma aplicação Django intermediária que gerencia cursos e avaliações, oferecendo endpoints robustos para interação. Abaixo, você encontrará informações essenciais para configurar e utilizar esta API.

### **Estrutura do Projeto**

O projeto é organizado em torno de dois principais aplicativos: **`cursos`** e **`escola`**. Os cursos representam as entidades de cursos e avaliações, enquanto a aplicação **`escola`** contém as configurações globais do projeto.

### **Requisitos**

Certifique-se de ter o Python e o Django instalados em seu ambiente. Você pode instalar as dependências usando o arquivo **`requirements.txt`**. Execute o seguinte comando:

```bash

pip install -r requirements.txt

```

### **Configuração do Ambiente**

### Banco de Dados

O projeto utiliza um banco de dados SQLite por padrão. Para aplicar as migrações e criar o banco de dados, execute:

```bash

python manage.py migrate

```

### Executando o Servidor

Inicie o servidor de desenvolvimento Django com o seguinte comando:

```bash

python manage.py runserver

```

A API estará acessível em http://127.0.0.1:8000/.

### **Endpoints**

### Cursos

- **Listar Todos os Cursos**
    - Método: GET
    - Endpoint: **`/api/v1/cursos/`**
- **Criar um Novo Curso**
    - Método: POST
    - Endpoint: **`/api/v1/cursos/`**

### Avaliações

- **Listar Todas as Avaliações**
    - Método: GET
    - Endpoint: **`/api/v1/avaliacoes/`**
- **Criar uma Nova Avaliação**
    - Método: POST
    - Endpoint: **`/api/v1/avaliacoes/`**

### **Administração**

O painel de administração do Django está disponível em http://127.0.0.1:8000/admin/. Você pode fazer login usando as credenciais de superusuário.

---

## **API V1 - Views Baseadas em Classe e Funções**

Esta versão da API utiliza views baseadas em classes e funções para manipular requisições HTTP. Oferece endpoints básicos para interação com cursos e avaliações.

- **Cursos**
    - Listar Todos os Cursos: **`/api/v1/cursos/`**
    - Criar um Novo Curso: **`/api/v1/cursos/`**
- **Avaliações**
    - Listar Todas as Avaliações: **`/api/v1/avaliacoes/`**
    - Criar uma Nova Avaliação: **`/api/v1/avaliacoes/`**

---

## **API V2 - Views Baseadas em Conjuntos de Modelos**

A versão 2 da API introduz uma abordagem mais poderosa e flexível, utilizando views baseadas em conjuntos de modelos. Proporciona uma estrutura mais organizada e endpoints mais ricos.

- **Cursos**
    - Listar Todos os Cursos: **`/api/v2/cursos/`**
    - Criar, Atualizar, Recuperar e Excluir Curso: **`/api/v2/cursos/<id>/`**
    - Listar Avaliações de um Curso: **`/api/v2/cursos/<id>/avaliacoes/`**
- **Avaliações**
    - Listar Todas as Avaliações: **`/api/v2/avaliacoes/`**
    - Criar, Atualizar, Recuperar e Excluir Avaliação: **`/api/v2/avaliacoes/<id>/`**
    - Listar Avaliações de um Curso: **`/api/v2/avaliacoes/<id>/`**

### **Diferenças e Justificativas**

- **Views Baseadas em Conjuntos de Modelos (V2)**
    - A versão 2 adota views baseadas em conjuntos de modelos, proporcionando uma estrutura mais modular e eficiente para manipular operações CRUD.
- **Riqueza de Funcionalidades (V2)**
    - A API V2 oferece operações mais avançadas, como atualização e exclusão de cursos e avaliações, proporcionando maior flexibilidade e controle ao usuário.
- **Melhoria na Estrutura do Projeto**
    - A reformulação visa uma estrutura mais organizada, com a separação de responsabilidades entre os aplicativos **`cursos`** e **`escola`**.

---

### **Observações**

- **Autenticação**
    - A API utiliza autenticação de sessão por padrão. Certifique-se de incluir as credenciais ao acessar endpoints protegidos.
- **Paginação**
    - A resposta da API pode ser paginada. Consulte a documentação para informações sobre como acessar páginas específicas.
- **Validação de Dados**
    - Observe as restrições nos tipos de dados aceitos e os campos obrigatórios durante a interação com a API.
- **Testes Unitários**
    - Testes unitários podem ser encontrados no diretório adequado. Execute-os para garantir a integridade da API.
- **Atualizações**
    - Mantenha-se atualizado com as mudanças na API consultando regularmente a documentação.

Divirta-se utilizando a API! Se encontrar problemas ou tiver sugestões, sinta-se à vontade para contribuir ou entrar em contato.
