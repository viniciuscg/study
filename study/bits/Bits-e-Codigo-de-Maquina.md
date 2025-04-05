# 🧠 Bits, Binários e Código de Máquina

> Um guia completo e essencial para entender como computadores realmente funcionam por trás dos panos.

---

## 🧩 1. O que são Bits e Bytes

- **Bit** (binary digit): menor unidade de informação computacional, pode ser `0` ou `1`.
	- **Byte**: grupo de 8 bits (ex: `10101010`)
- Cada bit representa **uma escolha binária** (ligado/desligado, verdadeiro/falso).

---

## 🔢 2. Sistemas de Numeração

### Decimal (Base 10)
- Usa dígitos de 0 a 9.
- Ex: 123 = 1×10² + 2×10¹ + 3×10⁰

### Binário (Base 2)
- Usa somente 0 e 1.
- Ex: 1101 = 1×2³ + 1×2² + 0×2¹ + 1×2⁰ = **13**

### Hexadecimal (Base 16)
- Usa dígitos de 0 a 9 e letras de A a F.
- Muito usado para representar bytes de forma compacta.
- Ex: `0xFF` = `11111111` = 255

---

## 🧮 3. Operações Binárias

| Operação | Símbolo | Exemplo (bin) | Resultado |      |      |
| -------- | ------- | ------------- | --------- | ---- | ---- |
| AND      | `&`     | 1100 & 1010   | 1000      |      |      |
| OR       | `       | `             | 1100      | 1010 | 1110 |
| XOR      | `^`     | 1100 ^ 1010   | 0110      |      |      |
| NOT      | `~`     | ~1100         | 0011      |      |      |
| SHIFT L  | `<<`    | 0010 << 1     | 0100      |      |      |
| SHIFT R  | `>>`    | 0100 >> 1     | 0010      |      |      |

---

## 💾 4. Como os dados são armazenados

### Inteiros (sem sinal)
- `uint8`: 0 a 255 → 8 bits
- `uint16`: 0 a 65.535 → 16 bits

### Inteiros com sinal (Complemento de dois)
- Permite representar negativos.
- MSB (most significant bit) indica o sinal:
  - `0` → positivo
  - `1` → negativo

| Decimal | Binário (8 bits) |
|---------|------------------|
| 0       | 00000000         |
| -1      | 11111111         |
| -2      | 11111110         |

### Ponto flutuante (IEEE 754)
- Representa números decimais em 32 ou 64 bits:
  - Sinal | Expoente | Mantissa
- Exemplo (simplificado):
  - `42.5` → `01000010 01010000 00000000 00000000`

### Caracteres (ASCII e Unicode)
- ASCII: 7 bits para 128 símbolos (A, B, a, b, etc.)
- Unicode (UTF-8): suporta todos os idiomas (até emojis)

---

## 🧠 5. Representação na Memória

- A memória é uma **sequência de endereços** com dados armazenados em bytes.
- Um array como `int arr[4] = {0,1,2,3}` é armazenado assim (em C):

```
Endereço     Conteúdo (4 bytes por int)
0x1000       00000000 00000000 00000000 00000000 (0)
0x1004       00000000 00000000 00000000 00000001 (1)
0x1008       00000000 00000000 00000000 00000010 (2)
0x100C       00000000 00000000 00000000 00000011 (3)
```

---

## 🧠 6. Ponteiros e Acesso à Memória

- Um ponteiro armazena o **endereço de outro dado**.
- Se `int *p = &x;`, `p` armazena o endereço de `x`.
- Com aritmética de ponteiros é possível navegar pela memória contígua (ex: arrays).

---

## ⚙️ 7. Como o Código Vira Binário

### Fases da transformação:

1. **Código-fonte** → (C, Go, Rust...)
2. **Compilador** → Gera **Assembly**
3. **Assembler** → Transforma em **código de máquina** (binário)
4. **CPU** → Executa instruções binárias via registradores

### Exemplo (C para máquina):

```c
int x = 5 + 3;
```

Assembly:
```
mov eax, 5
add eax, 3
```

Binário (exemplo hipotético):
```
10111000 00000101
00000011
```

---

## 🧠 8. Registradores e CPU

- A CPU possui **registradores** (pequena memória interna ultra-rápida).
- Ex: `eax`, `ebx`, `rsp` (stack pointer)
- O **ciclo de instrução**:
  1. Buscar instrução
  2. Decodificar
  3. Executar
  4. Armazenar resultado

---

## 📦 9. Extras e Conceitos Avançados

- **Mascaramento de bits**: ativa/desativa bits com AND e OR
- **Endianess**: ordem de armazenamento de bytes (little vs big endian)
- **Flags**: dados representados como conjuntos de bits ativados
- **Representação compacta**: às vezes se usa cada bit para representar estados

---

## ✅ 10. Checklist de Conhecimentos Essenciais

- [x] O que é bit e byte
- [x] Representações numéricas (decimal, binário, hexadecimal)
- [x] Operações bitwise
- [x] Complemento de dois
- [x] Representação de ponto flutuante
- [x] ASCII e Unicode
- [x] Como arrays funcionam na memória
- [x] Ponteiros e acesso à memória
- [x] Compilação e código de máquina
- [x] Registradores, CPU e instruções

---

## 🧪 Recomendações de Prática

- Tente converter números decimal ↔ binário ↔ hexadecimal manualmente
- Experimente operar com bits usando C, Python ou Go
- Visualize o código Assembly com [godbolt.org](https://godbolt.org/)
- Use [binaryconvert.com](https://www.binaryconvert.com/) para testes

---
