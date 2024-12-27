Aqui está um arquivo `README.md` completo para descrever e documentar o código fornecido:

---

# ScreenMatch Application

Este projeto é uma aplicação Java que permite consultar informações sobre séries e episódios usando a API do OMDB (Open Movie Database). A aplicação busca dados de séries, temporadas e episódios, organiza-os e exibe as informações para o usuário, incluindo um ranking dos melhores episódios.

## 📋 Funcionalidades

- Busca de informações detalhadas sobre séries e temporadas usando a API OMDB.
- Listagem de todos os episódios de uma série, organizados por temporada.
- Exibição dos **5 melhores episódios** com base nas avaliações.
- Filtro de episódios lançados a partir de um ano especificado pelo usuário.
- Conversão e manipulação de dados JSON para objetos Java.

---

## 🚀 Como executar o projeto

### Pré-requisitos

- **Java JDK 11 ou superior**.
- Uma IDE como **IntelliJ IDEA**, **Eclipse** ou **VS Code** configurada com suporte a Java.
- **Maven** ou outro gerenciador de dependências configurado (opcional).
- Conexão com a internet para acessar a API OMDB.

### Configuração da API

A aplicação utiliza a [OMDB API](https://www.omdbapi.com/). Você precisará de uma chave de API válida para realizar as consultas.

1. Crie uma conta no [OMDB API](https://www.omdbapi.com/apikey.aspx).
2. Obtenha sua chave de API gratuita ou premium.
3. Substitua o valor da variável `API_KEY` no código pela sua chave de API.

### Executando a aplicação

1. Clone o repositório ou copie os arquivos para o seu ambiente local.
2. Compile o código com o seguinte comando (caso não utilize uma IDE):
   ```bash
   javac -d bin src/br/com/alura/screenmatch/principal/Principal.java
   ```
3. Execute a aplicação:
   ```bash
   java -cp bin br.com.alura.screenmatch.principal.Principal
   ```
4. Siga as instruções exibidas no menu.

---

## 🛠 Estrutura do Projeto

A estrutura do projeto é organizada da seguinte forma:

```
src/
├── br/com/alura/screenmatch/
│   ├── model/         # Modelos de dados (série, temporada, episódio)
│   ├── service/       # Serviços para consumir API e converter dados
│   ├── principal/     # Classe principal para executar a aplicação
```

### Principais classes:

- **Principal.java**: Classe principal que contém o menu e executa a lógica do programa.
- **ConsumoApi.java**: Classe responsável por realizar chamadas HTTP para a API OMDB.
- **ConverteDados.java**: Classe que converte os dados JSON retornados pela API em objetos Java.
- **DadosSerie.java, DadosTemporada.java, DadosEpisodio.java**: Classes modelo para estruturar os dados de séries, temporadas e episódios.

---

## ⚙️ Configurações no Código

- **API Endpoint**: `https://www.omdbapi.com/`
- **Chave de API**: Substitua o valor de `API_KEY` por sua própria chave.
- **Parâmetros adicionais**: A busca de séries inclui parâmetros como `t` (título) e `season` (temporada).

---

## 📋 Fluxo da Aplicação

1. O usuário insere o nome de uma série no menu.
2. A aplicação consulta a API OMDB para buscar informações da série, temporadas e episódios.
3. As temporadas e episódios são exibidos no console.
4. A aplicação filtra os episódios com base na avaliação e exibe os **5 melhores episódios**.
5. O usuário pode filtrar episódios lançados a partir de um ano especificado.

---

## 🔧 Tecnologias Utilizadas

- **Java**: Linguagem principal para implementação do projeto.
- **OMDB API**: Para consulta de informações de séries.
- **Stream API**: Para manipulação e filtragem de coleções.
- **DateTime API**: Para manipulação de datas e formatações.

---

## 💡 Melhorias Futuras

- Implementar uma interface gráfica para facilitar a interação do usuário.
- Adicionar suporte a filmes, além de séries.
- Armazenar resultados em um banco de dados local para uso offline.
- Adicionar testes unitários para garantir a qualidade do código.

---

## 📝 Licença

Este projeto é apenas para fins educacionais e utiliza a API OMDB sob seus próprios termos de serviço. Certifique-se de consultar as políticas de uso da API antes de utilizá-la em produção.

---

Se precisar de mais ajuda ou deseja discutir melhorias no projeto, sinta-se à vontade para abrir uma issue ou entrar em contato!
