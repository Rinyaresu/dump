# Complexidade Temporal

Complexidade temporal diz respeito a **quanto tempo um algoritmo leva para executar**, dependendo do tamanho dos dados de entrada.

## Exemplo prático

Se eu tiver um array com 3 elementos e fizer um `puts` para cada nome, o código vai rodar 3 vezes, uma para cada item:

```ruby
arr = ["Kaique", "Ana", "Bruno"]
puts arr
# Saída:
# Kaique
# Ana
# Bruno
```

Se esse array tiver 1000 nomes, vai rodar 1000 vezes.  
Ou seja, o **tempo de execução cresce linearmente** com o tamanho da lista.

**Complexidade temporal:**  
- O algoritmo executa uma vez para cada elemento da entrada: **O(n)**

Se eu tiver um array com 10 números e quiser achar o maior valor, vou precisar:

- Passar por cada índice do array
- Comparar o valor atual com o maior encontrado até agora
- Atualizar se encontrar um valor maior

```ruby
arr = (1..10).to_a.shuffle
maior = arr[0]
indice_maior = 0

arr.each_with_index do |num, idx|
  if num > maior
    maior = num
    indice_maior = idx
  end
end

puts "Maior valor: #{maior}, índice: #{indice_maior}"
```

Durante a execução, o algoritmo precisa **percorrer todo o array** uma vez, então o tempo de execução também é **O(n)**.

## Resumindo

- **Complexidade temporal** foca em como o tempo de execução cresce conforme aumenta o tamanho da entrada.
- Se o algoritmo faz uma operação para cada elemento, é **O(n)** (linear).
- Se faz a mesma quantidade de operações independente do tamanho da entrada, é **O(1)** (constante).
- Se tem loops aninhados que percorrem todos os pares possíveis, é **O(n²)** (quadrática).