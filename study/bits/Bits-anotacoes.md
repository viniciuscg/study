Utilizando o princípio dos bits, podemos dizer que uma série de operações lógicas, baseadas em 0 e 1, levou à execução de uma determinada ação. Por exemplo, ao pressionar uma tecla, diversos componentes do sistema — desde o hardware até o software — realizaram verificações e processamentos binários (sim/não, verdadeiro/falso) para que esse evento fosse detectado, interpretado e executado. Então podemos dizer que no final do dia tudo se resume a sim e não.


O bit é a menor unidade de informação computacional. É onde tudo começa. A partir dele, formamos combinações binárias que representam instruções, dados e decisões.
Por exemplo, com 1 bit, temos duas possibilidades:  
0 (NÃO) e 1 (SIM)

Com 2 bits, temos:  
00 (NÃO-NÃO), 01 (NÃO-SIM), 10 (SIM-NÃO), 11 (SIM-SIM)

Com 3 bits, temos:  
000 (NÃO-NÃO-NÃO), 001 (NÃO-NÃO-SIM), 010 (NÃO-SIM-NÃO), 011 (NÃO-SIM-SIM),  
e assim por diante.

Cada novo bit duplica o número de combinações possíveis. Isso é o que permite que sistemas digitais representem quantidades, instruções e até imagens e sons apenas com combinações de "NÃO" e "SIM", ou seja, 0s e 1s


### Inteiros (sem sinal)
- `uint8`: 0 a 255 → 8 bits
- `uint16`: 0 a 65.535 → 16 bits
porque 8 bits so pode ir ate 255 inteiros? porque os binarios entra, 8 bits comeca em 00000000, 00000001, 00000010 ....... 11111111 apos isso a necessidade de incrementacao

No sistema **RGB**, cada cor (Vermelho, Verde, Azul) é representada por **um valor de 0 a 255**.

Ou seja, para cada cor:

- Vermelho (R): `uint8` → de 0 a 255
    
- Verde (G): `uint8` → de 0 a 255
    
- Azul (B): `uint8` → de 0 a 255
## 🌐 2. **Endereços IP (IPv4)**

Um endereço IPv4 é formado por **4 blocos de 8 bits** (ou seja, 4 bytes), separados por pontos.

### Exemplo:
192.168.0.1
Cada parte (192, 168, etc.) é um número de **0 a 255**, exatamente porque são representados com **8 bits** cada um.

> Exemplo binário de `192.168.0.1`:
> 
> `11000000.10101000.00000000.00000001`