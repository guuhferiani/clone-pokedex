# Pokedex

Projeto com HTML e CSS e JavaScript de uma Pokédex de POKEMON! Contém os pokemons até a 5º Geração e é interativa.


## Tecnologias
- HTML
- CSS
- Javascript
- Github


# Estrutura do Código da Pokédex

## 1. Seleção de Elementos
O código seleciona elementos do DOM que representam informações e interações da Pokédex:

- **`pokemonName`, `pokemonNumber`, `pokemonImage`:** Exibem o nome, número e imagem do Pokémon.
- **`form`, `input`:** Permitem que o usuário insira o nome ou número de um Pokémon para buscá-lo.
- **`buttonPrev`, `buttonNext`:** Navegam pelos Pokémons anteriores ou próximos.

---

## 2. Variável Global
- **`searchPokemon`:** Armazena o ID do Pokémon atual, inicializado com o valor 1.

---

## 3. Funções Principais

### **`fetchPokemon(pokemon)`**
- Faz uma chamada à API [PokeAPI](https://pokeapi.co/) para buscar informações do Pokémon solicitado.
- Retorna os dados se a requisição for bem-sucedida (`status == 200`).

### **`renderPokemon(pokemon)`**
- Atualiza o DOM com os dados do Pokémon.
  - Mostra o **nome**, **número** e **imagem animada** do Pokémon, se os dados forem encontrados.
  - Exibe uma mensagem de **"Não encontrado!"** se o Pokémon não existir.

---

## 4. Eventos

### **`form.addEventListener('submit')`**
- Captura o envio do formulário.
- Impede o comportamento padrão (recarregar a página).
- Busca o Pokémon digitado pelo usuário.

### **`buttonPrev.addEventListener('click')`**
- Decrementa o ID do Pokémon e renderiza o Pokémon anterior, desde que o ID seja maior que 1.

### **`buttonNext.addEventListener('click')`**
- Incrementa o ID do Pokémon e renderiza o Pokémon seguinte.

---

## 5. Inicialização
A função **`renderPokemon(searchPokemon)`** é chamada ao final para carregar o Pokémon inicial.
