# O(n)

## Visão geral

Um algoritmo é **O(n)** quando o número de operações cresce linearmente com o tamanho do input **n**.

## Quando usar

- Percorrer todos os elementos para imprimir, somar ou filtrar.
- Busca linear em listas ou arrays não ordenados.
- Validações que precisam olhar cada item (ex.: verificar se há elemento inválido).

## Complexidade Temporal

### Análise

- **Crescimento:** o loop percorre cada elemento exatamente uma vez → `n` iterações.
- **Todos os casos (melhor, médio, pior):** **O(n)**, pois não há atalhos em dados não ordenados.
- **Constantes ignoradas:** executar 2 × ou 5 × o mesmo loop (2 n, 5 n) continua sendo O(n).

### Fórmula final

**O(n)**

## Complexidade Espacial

### Análise

- Memória extra: apenas a variável de iteração → **O(1)** espaço adicional.
- O array de entrada já existe antes da execução; não conta como memória do algoritmo.

### Fórmula final

**O(1)**

## Exemplo de código

```ruby
array = (1..1000).to_a.shuffle  # tamanho de input = n

array.each do |value|
  puts value                  # executado n vezes
end
```
