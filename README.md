# Sorteio Top 250 IMDb

Aplicação web de página única para sortear filmes entre os 250 títulos mais bem avaliados do IMDb. O projeto utiliza apenas HTML, CSS e JavaScript, sem necessidade de instalação, servidor ou dependências externas.

## Funcionalidades

- **Sorteio aleatório de filmes:** seleciona um filme da lista e apresenta uma animação de embaralhamento antes do resultado.
- **Top 250 IMDb:** exibe a posição no ranking, o título em português quando há uma versão oficial de lançamento no Brasil, o título original em inglês e o ano de lançamento.
- **Controle de filmes assistidos:** filmes já marcados como assistidos deixam de participar dos próximos sorteios, evitando repetições.
- **Avaliação por estrelas:** permite avaliar os filmes assistidos de 0,5 a 5 estrelas, incluindo avaliações com meia estrela.
- **Histórico de filmes assistidos:** apresenta os filmes marcados recentemente, com título, ano, posição no ranking e avaliação.
- **Progresso:** informa quantos filmes já foram assistidos e quantos ainda estão disponíveis para sorteio.
- **Persistência local:** os dados são salvos automaticamente no navegador, sem necessidade de login, servidor ou conexão com banco de dados.

## Como executar

### Execução local

1. Baixe o arquivo `index.html`.
2. Abra o arquivo diretamente no navegador.
3. O aplicativo funciona offline e não requer instalação ou hospedagem.

### Publicação no GitHub Pages

Para disponibilizar a aplicação online gratuitamente:

1. Crie um novo repositório no GitHub.
2. Adicione o arquivo `index.html` à raiz do repositório.
3. Acesse **Settings → Pages**.
4. Em **Source**, selecione a branch `main` e a pasta `/ (root)`.
5. Salve a configuração.

Após a publicação, a aplicação estará disponível em um endereço no formato:

`https://seu-usuario.github.io/nome-do-repositorio/`

## Persistência de dados

A aplicação utiliza o `localStorage` do navegador para armazenar os filmes assistidos e suas respectivas avaliações.

Isso significa que:

- Os dados ficam armazenados no navegador e dispositivo utilizados.
- O progresso não é sincronizado automaticamente entre diferentes dispositivos.
- Não é necessário utilizar servidor, banco de dados ou conta de usuário.
- A limpeza dos dados do site ou do navegador pode apagar o progresso armazenado.

### Possível evolução

Caso seja necessário sincronizar o progresso entre dispositivos, o armazenamento pode ser adaptado para utilizar um serviço externo, como o Firebase. Nesse cenário, as funções `loadWatched()` e `saveWatched()` podem ser substituídas por operações de leitura e gravação no Firestore.

## Limpeza do histórico

A aplicação possui a opção **Limpar lista de assistidos** no rodapé.

Para evitar exclusões acidentais, a ação exige duas confirmações. No primeiro clique, é exibida uma mensagem solicitando uma nova confirmação durante quatro segundos. O segundo clique remove definitivamente os dados armazenados.

## Fonte e atualização da lista

A lista de filmes foi construída a partir de uma fonte que replica o ranking do IMDb, com atualização em agosto de 2026. O acesso automatizado ao ranking diretamente pelo IMDb não estava disponível no momento da construção da lista.

Por esse motivo, a ordem e os títulos podem apresentar pequenas diferenças em relação ao ranking atual do site caso ocorram alterações posteriores no IMDb.

Alguns filmes mais recentes ou que não possuem distribuição oficial no Brasil podem aparecer somente com o título original em inglês.

## Tecnologias

O projeto foi desenvolvido utilizando:

- HTML
- CSS
- JavaScript

Não são utilizados frameworks, bibliotecas externas, ferramentas de build ou dependências de terceiros.
