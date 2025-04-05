# 📌 Entendendo a Complexidade de Algoritmos

A **complexidade de um algoritmo** mede o quão rápido ele executa e quanta memória ele usa conforme a quantidade de dados cresce. Isso ajuda a entender **se um algoritmo é eficiente ou não**.

## ⏳ Complexidade de Tempo (Velocidade do Algoritmo)

A complexidade de tempo nos diz **quantos passos o algoritmo precisa dar** para resolver um problema, dependendo do tamanho da entrada.

### 🔹 **O(1) - Tempo Constante**

- **O tempo de execução não muda, não importa o tamanho da entrada.**
    
- Exemplo: Acessar o primeiro elemento de uma lista.
    
    ```python
    lista = [10, 20, 30, 40]
    print(lista[0])  # Sempre pega o primeiro elemento, em um único passo.
    ```
    

### 🔹 **O(log n) - Tempo Logarítmico**

- **O tempo de execução cresce devagar, mesmo se a entrada aumentar muito.**
    
- Exemplo: **Busca Binária** (quando procuramos algo em uma lista ordenada, cortando a busca pela metade a cada passo).
    
    ```python
    def busca_binaria(lista, alvo):
        esquerda, direita = 0, len(lista) - 1
        while esquerda <= direita:
            meio = (esquerda + direita) // 2
            if lista[meio] == alvo:
                return meio
            elif lista[meio] < alvo:
                esquerda = meio + 1
            else:
                direita = meio - 1
        return -1
    ```
    

### 🔹 **O(n) - Tempo Linear**

- **O tempo de execução cresce na mesma proporção que a entrada.**
    
- Exemplo: Percorrer uma lista para procurar um número.
    
    ```python
    def busca_linear(lista, alvo):
        for i in range(len(lista)):
            if lista[i] == alvo:
                return i
        return -1
    ```
    

### 🔹 **O(n log n) - Tempo Linearítmico**

- **Mais rápido que O(n²), mas ainda não ideal para entradas gigantes.**
    
- Exemplo: **Merge Sort** e **QuickSort**, usados para ordenar listas de forma eficiente.
    
    ```python
    def merge_sort(lista):
        if len(lista) <= 1:
            return lista
        meio = len(lista) // 2
        esquerda = merge_sort(lista[:meio])
        direita = merge_sort(lista[meio:])
        return merge(esquerda, direita)
    ```
    

### 🔹 **O(n²) - Tempo Quadrático**

- **Lento para grandes entradas, pois o número de operações cresce rapidamente.**
    
- Exemplo: **Bubble Sort** (ordenar uma lista comparando e trocando elementos).
    

### 🔹 **O(2ⁿ) - Tempo Exponencial**

- **O tempo dobra a cada novo elemento na entrada.**
    
- Exemplo: Resolver Fibonacci de forma ineficiente.
    
    ```python
    def fibonacci(n):
        if n <= 1:
            return n
        return fibonacci(n-1) + fibonacci(n-2)
    ```
    

### 🔹 **O(n!) - Tempo Fatorial**

- **Muito lento!** Usado em problemas de permutação, como o Caixeiro Viajante.
    

## 🧠 Complexidade de Memória (Uso de Espaço)

Além do tempo, é importante ver **quanta memória o algoritmo usa**.

### **O(1) - Memória Constante**

- O algoritmo usa sempre a mesma quantidade de memória, independentemente do tamanho da entrada.
    
- Exemplo: Algoritmo que apenas troca elementos dentro de uma lista.
    

### **O(n) - Memória Linear**

- O espaço usado cresce conforme o tamanho da entrada.
    
- Exemplo: Criar uma nova lista baseada na original.
    

### **O(n²), O(2ⁿ), O(n!) - Uso Explosivo de Memória**

- Algoritmos que armazenam muitas combinações podem usar MUITA memória.
    

## 🔥 Tabela Resumo

|Notação|Tempo de Execução|Memória Usada|Exemplo|
|---|---|---|---|
|O(1)|Constante|Constante|Acesso a um array `arr[0]`|
|O(log n)|Logarítmico|Constante|Busca Binária|
|O(n)|Linear|Linear|Percorrer um array|
|O(n log n)|Linearítmico|Linear|Merge Sort|
|O(n²)|Quadrático|Quadrático|Bubble Sort|
|O(2ⁿ)|Exponencial|Exponencial|Fibonacci Recursivo|
|O(n!)|Fatorial|Fatorial|Caixeiro Viajante|

## 🎯 Conclusão

- Sempre que possível, prefira **O(log n) ou O(n)**.
    
- **O(n log n)** é aceitável para ordenações eficientes.
    
- Evite **O(n²) ou pior**, pois ficam lentos rapidamente.
    
- Considere também o **uso de memória**, principalmente em algoritmos recursivos!
    

Com esse conhecimento, você pode escolher algoritmos melhores para seus problemas e tornar seu código mais **rápido e eficiente**! 🚀