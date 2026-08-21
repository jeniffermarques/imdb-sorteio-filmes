# 🎬 Sorteio Top 250 IMDb

Um app simples de página única (HTML/CSS/JS puro, sem instalação) para sortear
qual filme assistir dentre os 250 melhores do IMDb, conforme avaliado pelos
eleitores regulares do site.

## ✨ Funcionalidades

- **Sortear filme**: clique no botão e o app escolhe aleatoriamente um filme
  da lista, com efeito de "embaralhando" antes de revelar o escolhido
- **250 filmes com título em português e original**: posição no ranking,
  título (em português quando existe versão oficial de lançamento no Brasil),
  título original em inglês e ano
- **Marcar como assistido**: uma vez marcado, o filme para de entrar no
  sorteio — assim você vai naturalmente esgotando a lista sem repetir
- **Nota de 0,5 a 5 estrelas**: avalie cada filme assistido, com suporte a
  meias-estrelas
- **Últimos assistidos**: lista com os últimos filmes marcados, mostrando
  título, ano, posição no ranking e a nota dada
- **Contador de progresso**: quantos você já assistiu e quantos faltam
- Tudo salvo automaticamente no seu navegador — não precisa de login nem
  de conexão com servidor nenhum

## 🚀 Como usar

### Opção 1 — Só abrir localmente
Baixe o arquivo `index.html` e abra com dois cliques no navegador. Funciona
offline, sem precisar hospedar nada.

### Opção 2 — Hospedar no GitHub Pages (grátis)
1. Crie um repositório novo no GitHub
2. Suba este arquivo com o nome `index.html` na raiz do repositório
3. Vá em **Settings → Pages**
4. Em "Source", selecione a branch `main` e a pasta `/ (root)`, e salve
5. Em 1–2 minutos o link estará disponível em
   `https://seu-usuario.github.io/nome-do-repositorio/`

## 💾 Como os dados são salvos

O app usa o `localStorage` do navegador para guardar quais filmes você já
assistiu e as notas dadas. Isso significa:

- Os dados ficam salvos **naquele navegador e dispositivo específico**
- Não sincroniza automaticamente entre celular, computador, etc.
- Não requer servidor, banco de dados ou conta de nenhum tipo
- Limpar o cache/dados do site no navegador apaga o progresso

Se quiser sincronizar entre dispositivos futuramente, é possível adaptar o
armazenamento para usar um serviço como o **Firebase** (plano gratuito Spark),
trocando as funções `loadWatched()` e `saveWatched()` do código por chamadas
ao Firestore.

## 🗑️ Limpar a lista de assistidos

Há um botão "Limpar lista de assistidos" no rodapé do app. Por segurança,
ele pede duas confirmações: o primeiro clique avisa "Clique de novo para
confirmar" (por 4 segundos) e só o segundo clique realmente apaga tudo.

## 📝 Sobre a lista de filmes

A lista foi construída a partir de uma fonte que replica o ranking do IMDb
(atualizada em agosto de 2026), já que o próprio imdb.com bloqueia acesso
automatizado. A ordem e os títulos devem estar bem próximos do ranking atual
do site, mas pequenas defasagens podem existir caso o IMDb tenha mudado algo
desde então. Alguns títulos mais raros (filmes muito recentes ou sem
distribuição oficial no Brasil) aparecem apenas com o nome original em inglês.

## 🛠️ Tecnologias

Apenas HTML, CSS e JavaScript puro — nenhuma dependência externa, framework
ou build necessário.
