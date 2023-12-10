
# Exercícios - Programação Assíncrona

## 1. Cálculo de frete
## 2. API Pokemon




## API de Cálculo de Frete

Esta API permite calcular o frete de um produto com base em regras específicas.

## Rotas

### Listagem de Produtos

- **Rota:** `GET /produtos`
- **Descrição:** Lista os produtos disponíveis.
  
### Detalhamento de Produto por ID

- **Rota:** `GET /produtos/:idProduto`
- **Parâmetros de rota:**
  - `idProduto`: ID do produto desejado.
- **Descrição:** Detalha um produto específico com base no ID fornecido.
  
### Cálculo de Frete por Produto e CEP

- **Rota:** `GET /produtos/:idProduto/frete/:cep`
- **Parâmetros de rota:**
  - `idProduto`: ID do produto para o cálculo do frete.
  - `cep`: CEP para encontrar o estado referente.
- **Descrição:** Calcula o frete do produto de acordo com as regras estabelecidas.
  
## Regras para Cálculo de Frete

- Valor padrão do frete: `12%` do valor do produto.
- Para os estados `BA, SE, AL, PE e PB`, o frete será de `10%`.
- Para os estados `SP e RJ`, o frete será de `15%`.

## Exemplo de Resposta

Ao chamar a rota `GET /produtos/1/frete/41256250`, a resposta será:

```json
{
    "produto": {
        "id": 1,
        "nome": "Teclado mecânico Keychron K2",
        "valor": 100000
    },
    "estado": "BA",
    "frete": 10000
}
```
#

# Pokémons

## Detalhar Pokémon por ID ou Nome





Este arquivo define as rotas para manipulação de informações relacionadas a Pokémons na sua aplicação.

## Rotas


### Listar Pokémons

- **Rota:** `GET /pokemon`
- **Descrição:** Lista Pokémons com base nos parâmetros de consulta fornecidos.

- **Rota:** `GET /pokemons/:idOuNome`
- **Parâmetros de rota:**
- `idOuNome`: ID ou Nome do Pokémon desejado.
- **Descrição:** Detalha informações específicas sobre um Pokémon com base no ID ou Nome fornecido.

## Endpoints

### Listar Pokémons

- **Rota:** `GET /pokemons`
- **Parâmetros de consulta:**
  - `pagina` (opcional): Número da página a ser listada (padrão: 1).
- **Descrição:** Lista Pokémons com base na página especificada.


