# Complexidade Espacial

Complexidade espacial diz respeito à **quantidade de memória adicional** que um algoritmo utiliza para executar sua tarefa, além dos dados de entrada.

## Exemplo prático

Se eu tiver um array com 10 números e quiser pegar o maior número desse array, vou precisar:

- Percorrer cada índice do array
- Comparar o valor atual com o maior encontrado até agora
- Atualizar se encontrar um valor maior

```ruby
arr = [1,2,3,4,5,6,7,8,9,10].shuffle
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

### Análise

Durante a execução, o algoritmo só precisa de **duas variáveis extras** (`maior` e `indice_maior`), independente se o array tem 10, 1000 ou 1 milhão de elementos.  
Ou seja, a **quantidade de memória adicional é constante**.

**Complexidade espacial:**  
- O algoritmo ocupa espaço extra fixo (constante): **O(1)**

## Resumindo

- **Complexidade espacial** foca na memória extra usada, não no tempo de execução.
- Se o algoritmo precisa de espaço extra que **não aumenta** com o tamanho da entrada, é **O(1)**.
- Se precisa criar uma estrutura proporcional ao tamanho da entrada (por exemplo, uma cópia do array), é **O(n)**.
