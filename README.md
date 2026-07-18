*This project was created as part of the 42 curriculum by rosousa-.*

---

# Libft

[🇧🇷 Versão em Português](#portugues) | [🇺🇸 English Version](#english)

---

# <a id="portugues"></a>🇧🇷 Versão em Português

A **Libft** é o primeiro projeto do currículo da **42** e representa a base para praticamente todos os projetos desenvolvidos posteriormente. O objetivo consiste em recriar parte da biblioteca padrão da linguagem C (**libc**) e implementar um conjunto de funções utilitárias que poderão ser reutilizadas ao longo da formação.

Além de reproduzir o comportamento de funções já existentes, este projeto busca desenvolver uma compreensão aprofundada sobre gerenciamento de memória, manipulação de strings, ponteiros, alocação dinâmica e estruturas de dados fundamentais da linguagem C.

Ao final do projeto é gerada uma biblioteca estática (`libft.a`), permitindo que todas as funções implementadas sejam reutilizadas em projetos futuros.

---

# 📝 Descrição

Durante o desenvolvimento da **Libft**, diversos conceitos fundamentais da linguagem C foram estudados e aplicados, dentre eles:

- Manipulação de memória.
- Manipulação de strings.
- Conversão entre caracteres e inteiros.
- Ponteiros e ponteiros para ponteiros.
- Alocação dinâmica de memória.
- Criação de bibliotecas estáticas.
- Estruturas de dados utilizando listas encadeadas.

---

# 📚 Recursos

Este projeto exigiu o estudo aprofundado de diversos conceitos fundamentais da linguagem C.

## Manipulação de Memória

- Organização da memória (Stack e Heap).
- Endereços de memória.
- Ponteiros.
- Ponteiros para ponteiros.
- Alocação dinâmica utilizando `malloc()`.
- Inicialização de memória utilizando `calloc()`.
- Liberação de memória utilizando `free()`.

---

## Manipulação de Strings

- Strings terminadas em `'\0'`.
- Diferença entre arrays e ponteiros.
- Cópia de strings.
- Concatenação.
- Comparação de strings.
- Manipulação segura de buffers.

---

## Conversões

- Conversão ASCII ↔ Decimal.
- Conversão de caracteres numéricos.
- Conversão entre inteiros e strings.
- Tratamento de sinais positivos e negativos.

---

## Estruturas de Dados

- Listas simplesmente encadeadas.
- Nós.
- Ponteiros para nós.
- Inserção.
- Remoção.
- Percurso.
- Desalocação de listas.

---

## Ferramentas

- Makefile
- Biblioteca Estática (.a)
- Norminette
- GDB
- Valgrind
- Francinette
- libftTester

---

# 📚 Libft Functions

<!-- | Parte 1 — Libc Functions | Parte 2 — Additional Functions | Bônus — Linked Lists |
|:-----------------------------|:-----------------------------------|:-------------------------|
| `ft_isalpha` | `ft_substr` | `ft_lstnew` |
| `ft_isdigit` | `ft_strjoin` | `ft_lstadd_front` |
| `ft_isalnum` | `ft_strtrim` | `ft_lstsize` |
| `ft_isascii` | `ft_split` | `ft_lstlast` |
| `ft_isprint` | `ft_itoa` | `ft_lstadd_back` |
| `ft_strlen` | `ft_strmapi` | `ft_lstdelone` |
| `ft_memset` | `ft_striteri` | `ft_lstclear` |
| `ft_bzero` | `ft_putchar_fd` | `ft_lstiter` |
| `ft_memcpy` | `ft_putstr_fd` | `ft_lstmap` |
| `ft_memmove` | `ft_putendl_fd` | |
| `ft_memchr` | `ft_putnbr_fd` | |
| `ft_memcmp` | | |
| `ft_strlcpy` | | |
| `ft_strlcat` | | |
| `ft_toupper` | | |
| `ft_tolower` | | |
| `ft_strchr` | | |
| `ft_strrchr` | | |
| `ft_strncmp` | | |
| `ft_strnstr` | | |
| `ft_atoi` | | |
| `ft_calloc` | | |
| `ft_strdup` | | | -->

| Parte 1 — Libc Functions | Parte 1 — Libc Functions | Parte 2 — Additional Functions |
|:----------------------------|:----------------------------|:-----------------------------------|
| `ft_isalpha` | `ft_memchr` | `ft_substr` |
| `ft_isdigit` | `ft_memcmp` | `ft_strjoin` |
| `ft_isalnum` | `ft_strlcpy` | `ft_strtrim` |
| `ft_isascii` | `ft_strlcat` | `ft_split` |
| `ft_isprint` | `ft_toupper` | `ft_itoa` |
| `ft_strlen` | `ft_tolower` | `ft_strmapi` |
| `ft_memset` | `ft_strchr` | `ft_striteri` |
| `ft_bzero` | `ft_strrchr` | `ft_putchar_fd` |
| `ft_memcpy` | `ft_strncmp` | `ft_putstr_fd` |
| `ft_memmove` | `ft_strnstr` | `ft_putendl_fd` |
| `ft_atoi` | `ft_calloc` | `ft_putnbr_fd` |
| `ft_strdup` | | |

### Total Functions
| Section | Functions |
|---------|----------:|
| Part 1 | 23 |
| Part 2 | 11 |
| **Total** | **34** |
<!-- | Bonus | 9 |
| **Total** | **43** | -->

Em sua parte obrigatória o projeto é dividido em duas partes principais:

---

# Parte 1 — Reimplementação da libc

Recriação de funções clássicas da biblioteca padrão da linguagem C relacionadas a:


---
<details>
<summary><strong>🔤 ft_isalpha</strong></summary>

## 📖 Descrição

Verifica se um caractere pertence ao conjunto de letras do alfabeto ASCII.

São consideradas letras válidas:

- `A` até `Z`
- `a` até `z`

Qualquer outro caractere resulta em um retorno indicando que não é alfabético.

---

## 📝 Protótipo

```c
int ft_isalpha(int c);
```

---

## 📥 Parâmetros

### c

O caractere a ser testado.

Embora o parâmetro seja do tipo `int`, normalmente representa um caractere ASCII.

---

## 📤 Valor de Retorno

Retorna um valor diferente de zero caso o caractere seja uma letra do alfabeto.

Retorna `0` caso contrário.

---

## 🎯 Objetivo

Permitir a identificação de caracteres alfabéticos durante validações, análises léxicas e manipulação de textos.

Essa função é amplamente utilizada para verificar entradas do usuário, interpretar tokens e implementar analisadores de texto.

---

## 🧠 Conceitos necessários

- Tabela ASCII.
- Tipo `char` e promoção para `int`.
- Intervalos de caracteres.
- Operadores relacionais (`<`, `>`, `<=`, `>=`).
- Operador lógico (`||`).

---

## ⚠️ Armadilhas comuns

- Esquecer que apenas caracteres ASCII são considerados.
- Considerar letras acentuadas (`á`, `ç`, `ã`, etc.) como válidas.
- Confundir letras com dígitos ou outros caracteres imprimíveis.
- Assumir que o retorno será necessariamente `1`. A especificação garante apenas um valor diferente de zero.

---

## 🔗 Relação com outras funções

- ft_isdigit
- ft_isalnum
- ft_isascii
- ft_isprint
- ft_tolower
- ft_toupper

---

## ⏱️ Complexidade

Tempo: **O(1)**

Espaço: **O(1)**

---

## 📚 Referências

- man isalpha
- ISO C
- POSIX
- The C Programming Language

</details>

---

<details>
<summary><strong>🔢 ft_isdigit</strong></summary>

## 📖 Descrição

Verifica se um caractere representa um dígito decimal na tabela ASCII.

São considerados dígitos válidos:

- `0` até `9`

Qualquer outro caractere resulta em um retorno indicando que não é um dígito decimal.

---

## 📝 Protótipo

```c
int ft_isdigit(int c);
```

---

## 📥 Parâmetros

### c

O caractere a ser testado.

Embora o parâmetro seja do tipo `int`, normalmente representa um caractere ASCII.

---

## 📤 Valor de Retorno

Retorna um valor diferente de zero caso o caractere seja um dígito decimal (`0` a `9`).

Retorna `0` caso contrário.

---

## 🎯 Objetivo

Permitir a identificação de caracteres numéricos durante validações de entrada, conversões de strings para números e processamento de textos.

Esta função é frequentemente utilizada na implementação de funções como `atoi`, validadores de entrada e analisadores léxicos.

---

## 🧠 Conceitos necessários

- Tabela ASCII.
- Tipo `char` e promoção para `int`.
- Intervalos de caracteres.
- Operadores relacionais (`<`, `>`, `<=`, `>=`).
- Operador lógico (`&&`).

---

## ⚠️ Armadilhas comuns

- Confundir o caractere `'5'` com o número inteiro `5`.
- Esquecer que apenas os caracteres ASCII de `'0'` a `'9'` são considerados válidos.
- Considerar sinais (`'+'` e `'-'`) como dígitos.
- Assumir que o retorno será necessariamente `1`. A especificação garante apenas um valor diferente de zero.

---

## 🔗 Relação com outras funções

- ft_isalpha
- ft_isalnum
- ft_isascii
- ft_isprint
- ft_atoi

---

## ⏱️ Complexidade

Tempo: **O(1)**

Espaço: **O(1)**

---

## 📚 Referências

- man isdigit
- ISO C
- POSIX
- The C Programming Language

</details>

---

<details>
<summary><strong>🔠 ft_isalnum</strong></summary>

## 📖 Descrição

Verifica se um caractere é alfanumérico na tabela ASCII.

São considerados caracteres alfanuméricos:

- Letras maiúsculas (`A` a `Z`)
- Letras minúsculas (`a` a `z`)
- Dígitos decimais (`0` a `9`)

Qualquer outro caractere resulta em um retorno indicando que não é alfanumérico.

---

## 📝 Protótipo

```c
int ft_isalnum(int c);
```

---

## 📥 Parâmetros

### c

O caractere a ser testado.

Embora o parâmetro seja do tipo `int`, normalmente representa um caractere ASCII.

---

## 📤 Valor de Retorno

Retorna um valor diferente de zero caso o caractere seja uma letra ou um dígito decimal.

Retorna `0` caso contrário.

---

## 🎯 Objetivo

Permitir a identificação de caracteres alfanuméricos durante validações de entrada, processamento de textos e análise léxica.

Essa função é útil quando letras e números são aceitos, mas caracteres especiais, espaços e símbolos devem ser rejeitados.

---

## 🧠 Conceitos necessários

- Tabela ASCII.
- Tipo `char` e promoção para `int`.
- Intervalos de caracteres.
- Operadores relacionais (`<`, `>`, `<=`, `>=`).
- Operadores lógicos (`&&` e `||`).
- Conceito de caracteres alfanuméricos.

---

## ⚠️ Armadilhas comuns

- Esquecer que espaços (`' '`), quebras de linha (`'\n'`) e tabulações (`'\t'`) não são caracteres alfanuméricos.
- Considerar caracteres especiais (`@`, `_`, `#`, `!`, `%`, etc.) como válidos.
- Considerar letras acentuadas (`á`, `ç`, `ã`, etc.) como alfanuméricas. A função considera apenas caracteres da tabela ASCII.
- Assumir que o retorno será necessariamente `1`. A especificação garante apenas um valor diferente de zero.

---

## 🔗 Relação com outras funções

- ft_isalpha
- ft_isdigit
- ft_isascii
- ft_isprint
- ft_tolower
- ft_toupper

---

## ⏱️ Complexidade

Tempo: **O(1)**

Espaço: **O(1)**

---

## 📚 Referências

- man isalnum
- ISO C
- POSIX
- The C Programming Language

</details>

---

<details>
<summary><strong>🖥️ ft_isascii</strong></summary>

## 📖 Descrição

Verifica se um valor pertence ao conjunto de caracteres da tabela ASCII.

São considerados caracteres ASCII válidos os valores inteiros no intervalo:

- `0` até `127`

Qualquer valor fora desse intervalo resulta em um retorno indicando que não pertence à tabela ASCII.

---

## 📝 Protótipo

```c
int ft_isascii(int c);
```

---

## 📥 Parâmetros

### c

O valor inteiro a ser testado.

Embora normalmente represente um caractere, a função aceita qualquer valor do tipo `int`.

---

## 📤 Valor de Retorno

Retorna um valor diferente de zero caso `c` pertença à tabela ASCII.

Retorna `0` caso contrário.

---

## 🎯 Objetivo

Permitir verificar se um valor pode ser representado utilizando a codificação ASCII de 7 bits.

Essa função é útil para validar entradas antes de realizar operações que dependem exclusivamente do conjunto ASCII.

---

## 🧠 Conceitos necessários

- Tabela ASCII.
- Diferença entre caracteres e valores inteiros.
- Intervalos numéricos.
- Operadores relacionais (`<`, `>`, `<=`, `>=`).
- Operador lógico (`&&`).
- Representação de caracteres em memória.

---

## ⚠️ Armadilhas comuns

- Confundir ASCII com Unicode ou UTF-8.
- Acreditar que todos os caracteres visíveis pertencem ao ASCII. Caracteres como `á`, `ç`, `ã`, `ê` e `€` não fazem parte da tabela ASCII.
- Esquecer que caracteres de controle (`'\n'`, `'\t'`, `'\0'`, etc.) também pertencem ao ASCII.
- Assumir que o retorno será necessariamente `1`. A especificação garante apenas um valor diferente de zero.

---

## 🔗 Relação com outras funções

- ft_isalpha
- ft_isdigit
- ft_isalnum
- ft_isprint

---

## ⏱️ Complexidade

Tempo: **O(1)**

Espaço: **O(1)**

---

## 📚 Referências

- man isascii
- POSIX
- ASCII Standard (ANSI X3.4)
- The C Programming Language

</details>

---

<details>
<summary><strong>🖨️ ft_isprint</strong></summary>

## 📖 Descrição

Verifica se um caractere pertence ao conjunto de caracteres imprimíveis da tabela ASCII.

São considerados caracteres imprimíveis todos os caracteres cujos códigos ASCII estão no intervalo:

- `32` (`' '`, espaço)
- `126` (`'~'`)

Esse intervalo inclui:

- Letras maiúsculas (`A` a `Z`)
- Letras minúsculas (`a` a `z`)
- Dígitos (`0` a `9`)
- Espaço (`' '`)
- Símbolos e caracteres de pontuação (`!`, `@`, `#`, `$`, `%`, etc.)

Os caracteres de controle (como `'\n'`, `'\t'` e `'\0'`) **não** são considerados imprimíveis.

---

## 📝 Protótipo

```c
int ft_isprint(int c);
```

---

## 📥 Parâmetros

### c

O valor inteiro a ser testado.

Embora normalmente represente um caractere, a função aceita qualquer valor do tipo `int`.

---

## 📤 Valor de Retorno

Retorna um valor diferente de zero caso `c` seja um caractere imprimível da tabela ASCII.

Retorna `0` caso contrário.

---

## 🎯 Objetivo

Permitir identificar se um caractere pode ser exibido diretamente na tela ou impresso sem representar um comando de controle.

Essa função é útil para validar entradas, filtrar caracteres invisíveis e processar textos de forma segura.

---

## 🧠 Conceitos necessários

- Tabela ASCII.
- Caracteres imprimíveis.
- Caracteres de controle.
- Intervalos numéricos.
- Operadores relacionais (`<`, `>`, `<=`, `>=`).
- Operador lógico (`&&`).

---

## ⚠️ Armadilhas comuns

- Esquecer que o espaço (`' '`) é considerado um caractere imprimível.
- Considerar `'\n'`, `'\t'` ou `'\0'` como imprimíveis.
- Confundir caracteres imprimíveis com caracteres alfanuméricos. Símbolos como `@`, `#`, `%` e `!` também são imprimíveis.
- Considerar caracteres Unicode ou UTF-8 como pertencentes ao conjunto ASCII.
- Assumir que o retorno será necessariamente `1`. A especificação garante apenas um valor diferente de zero.

---

## 🔗 Relação com outras funções

- ft_isascii
- ft_isalpha
- ft_isdigit
- ft_isalnum

---

## ⏱️ Complexidade

Tempo: **O(1)**

Espaço: **O(1)**

---

## 📚 Referências

- man isprint
- POSIX
- ASCII Standard (ANSI X3.4)
- The C Programming Language

</details>

---
<details>
<summary><strong>📏 ft_strlen</strong></summary>

## 📖 Descrição

Calcula o comprimento de uma string terminada pelo caractere nulo (`'\0'`).

O caractere terminador não faz parte do comprimento retornado.

---

## 📝 Protótipo

```c
size_t ft_strlen(const char *str);
```

---

## 📥 Parâmetros

### str

Ponteiro para o primeiro caractere da string.

A string obrigatoriamente deve terminar com `'\0'`.

---

## 📤 Valor de Retorno

Retorna a quantidade de caracteres existentes antes do primeiro `'\0'`.

---

## 🎯 Objetivo

Permitir que programas descubram o tamanho lógico de uma string sem armazenar esse valor separadamente.

---

## 🧠 Conceitos necessários

- Arrays de caracteres.
- Strings em C.
- Caractere nulo (`'\0'`).
- Ponteiros.
- Aritmética de ponteiros.
- Leitura sequencial de memória.
- Tipo `size_t`.

---

## ⚠️ Armadilhas comuns

- Esquecer que `'\0'` não entra na contagem.
- Passar um ponteiro `NULL`.
- Passar um vetor que não termina em `'\0'`.
- Confundir tamanho da string com tamanho do array.

---

## 🔗 Relação com outras funções

- ft_strdup
- ft_strlcpy
- ft_strlcat
- ft_substr
- ft_strjoin

---

## ⏱️ Complexidade

Tempo: **O(n)**

Espaço: **O(1)**

---

## 📚 Referências

- man strlen
- ISO C
- The C Programming Language

</details>

---

<details>
<summary><strong>🧹 ft_memset</strong></summary>

## 📖 Descrição

Preenche uma região contígua da memória com um valor específico.

A função escreve o mesmo byte em cada posição dos primeiros `n` bytes da região apontada por `b`.

---

## 📝 Protótipo

```c
void *ft_memset(void *b, int c, size_t len);
```

---

## 📥 Parâmetros

### b

Ponteiro para o início da região de memória que será modificada.

### c

Valor utilizado para preencher a memória.

Embora seja recebido como `int`, apenas os 8 bits menos significativos (um byte) são utilizados.

### len

Quantidade de bytes que serão preenchidos.

---

## 📤 Valor de Retorno

Retorna o mesmo ponteiro recebido em `b`.

---

## 🎯 Objetivo

Permitir a inicialização ou redefinição rápida de uma região de memória.

É frequentemente utilizada para:

- Inicializar buffers.
- Limpar estruturas.
- Preparar memória antes do uso.
- Implementar outras funções da biblioteca padrão, como `bzero` e `calloc`.

---

## 🧠 Conceitos necessários

- Memória contígua.
- Bytes.
- Ponteiros genéricos (`void *`).
- Conversão de tipos (*casting*).
- Representação de dados em memória.
- Tipo `size_t`.

---

## ⚠️ Armadilhas comuns

- Acreditar que a função trabalha com elementos em vez de bytes. Ela sempre opera byte a byte.
- Esquecer que apenas um byte de `c` é utilizado.
- Utilizar `memset` para inicializar tipos maiores esperando um valor diferente de `0` ou `255`. Por exemplo, preencher um vetor de `int` com o valor `1` não produzirá inteiros iguais a `1`.
- Passar um tamanho (`len`) maior do que a região de memória disponível, causando comportamento indefinido.
- Utilizar um ponteiro inválido ou `NULL` (quando `len > 0`).

---

## 🔗 Relação com outras funções

- ft_bzero
- ft_memcpy
- ft_memmove
- ft_calloc

---

## ⏱️ Complexidade

Tempo: **O(n)**

Espaço: **O(1)**

---

## 📚 Referências

- man memset
- ISO C
- POSIX
- The C Programming Language

</details>

---

<details>
<summary><strong>🧽 ft_bzero</strong></summary>

## 📖 Descrição

Preenche uma região contígua da memória com bytes de valor zero (`0x00`).

A função escreve o byte `0` em cada uma dos primeiros `n` bytes da região apontada por `s`.

---

## 📝 Protótipo

```c
void ft_bzero(void *s, size_t n);
```

---

## 📥 Parâmetros

### s

Ponteiro para o início da região de memória que será zerada.

### n

Quantidade de bytes que serão preenchidos com zero.

---

## 📤 Valor de Retorno

A função não retorna nenhum valor.

---

## 🎯 Objetivo

Permitir a inicialização ou limpeza de uma região de memória, garantindo que todos os seus bytes contenham o valor `0`.

É frequentemente utilizada para:

- Inicializar estruturas.
- Limpar buffers.
- Preparar memória antes de seu uso.
- Implementar outras funções da biblioteca, como `calloc`.

---

## 🧠 Conceitos necessários

- Memória contígua.
- Bytes.
- Ponteiros genéricos (`void *`).
- Valor nulo em memória (`0x00`).
- Tipo `size_t`.
- Inicialização de memória.

---

## ⚠️ Armadilhas comuns

- Confundir o byte `0` (`0x00`) com o caractere `'0'` (código ASCII `48`).
- Acreditar que a função libera memória. Ela apenas modifica o conteúdo da memória já alocada.
- Passar um valor de `n` maior que a região disponível, causando comportamento indefinido.
- Utilizar um ponteiro inválido ou `NULL` (quando `n > 0`).
- Assumir que zerar uma estrutura sempre produz um estado válido. Algumas estruturas podem exigir inicializações específicas.

---

## 🔗 Relação com outras funções

- ft_memset
- ft_memcpy
- ft_memmove
- ft_calloc

---

## ⏱️ Complexidade

Tempo: **O(n)**

Espaço: **O(1)**

---

## 📚 Referências

- man bzero
- POSIX
- The C Programming Language

</details>

---

<details>
<summary><strong>📋 ft_memcpy</strong></summary>

## 📖 Descrição

Copia uma sequência de bytes de uma região de memória para outra.

A função copia exatamente os primeiros `n` bytes da região apontada por `src` para a região apontada por `dst`.

As regiões de memória **não podem se sobrepor**. Caso haja sobreposição, o comportamento é indefinido.

---

## 📝 Protótipo

```c
void *ft_memcpy(void *dst, const void *src, size_t n);
```

---

## 📥 Parâmetros

### dst

Ponteiro para a região de memória de destino.

### src

Ponteiro para a região de memória de origem.

O conteúdo apontado por `src` não é modificado.

### n

Quantidade de bytes que serão copiados.

---

## 📤 Valor de Retorno

Retorna o mesmo ponteiro recebido em `dst`.

---

## 🎯 Objetivo

Permitir a cópia eficiente de blocos contíguos de memória.

É frequentemente utilizada para:

- Copiar arrays.
- Copiar estruturas.
- Duplicar buffers.
- Implementar outras funções da biblioteca padrão.

Por operar diretamente sobre bytes, a função pode copiar qualquer tipo de dado.

---

## 🧠 Conceitos necessários

- Memória contígua.
- Bytes.
- Ponteiros genéricos (`void *`).
- Ponteiros constantes (`const void *`).
- Conversão de tipos (*casting*).
- Tipo `size_t`.
- Cópia de memória.

---

## ⚠️ Armadilhas comuns

- Utilizar `memcpy` quando as regiões de memória se sobrepõem. Nessa situação deve-se utilizar `memmove`.
- Passar um valor de `n` maior que o tamanho da região de origem ou destino, causando comportamento indefinido.
- Utilizar ponteiros inválidos ou `NULL` (quando `n > 0`).
- Acreditar que a função interpreta o tipo dos dados. Ela copia apenas bytes.

---

## 🔗 Relação com outras funções

- ft_memmove
- ft_memset
- ft_bzero
- ft_memcmp
- ft_memchr

---

## ⏱️ Complexidade

Tempo: **O(n)**

Espaço: **O(1)**

---

## 📚 Referências

- man memcpy
- ISO C
- POSIX
- The C Programming Language

</details>

---

<details>
<summary><strong>🔄 ft_memmove</strong></summary>

## 📖 Descrição

Copia uma sequência de bytes de uma região de memória para outra.

Diferentemente de `ft_memcpy`, esta função garante uma cópia correta mesmo quando as regiões de memória de origem e destino se sobrepõem.

A função copia exatamente os primeiros `n` bytes da região apontada por `src` para a região apontada por `dst`.

---

## 📝 Protótipo

```c
void *ft_memmove(void *dst, const void *src, size_t len);
```

---

## 📥 Parâmetros

### dst

Ponteiro para a região de memória de destino.

### src

Ponteiro para a região de memória de origem.

O conteúdo apontado por `src` não é modificado.

### len

Quantidade de bytes que serão copiados.

---

## 📤 Valor de Retorno

Retorna o mesmo ponteiro recebido em `dst`.

---

## 🎯 Objetivo

Permitir a cópia segura de blocos de memória, inclusive quando as regiões de origem e destino se sobrepõem.

É frequentemente utilizada para:

- Deslocar dados dentro de um mesmo buffer.
- Remover ou inserir elementos em arrays.
- Implementar outras funções da biblioteca padrão.
- Copiar memória quando não se sabe se haverá sobreposição.

---

## 🧠 Conceitos necessários

- Memória contígua.
- Bytes.
- Ponteiros genéricos (`void *`).
- Ponteiros constantes (`const void *`).
- Conversão de tipos (*casting*).
- Tipo `size_t`.
- Sobreposição (*overlap*) de regiões de memória.
- Direção de cópia (início → fim ou fim → início).

---

## ⚠️ Armadilhas comuns

- Acreditar que `ft_memmove` sempre copia da esquerda para a direita. Dependendo da posição de `src` e `dst`, a direção da cópia precisa ser alterada para evitar sobrescrever dados ainda não copiados.
- Confundir `ft_memmove` com `ft_memcpy`. A principal diferença entre elas é justamente o tratamento da sobreposição de memória.
- Passar um valor de `len` maior que o tamanho das regiões de memória, causando comportamento indefinido.
- Utilizar ponteiros inválidos ou `NULL` (quando `len > 0`).
- Esquecer que a função opera sobre bytes e não conhece o tipo dos dados armazenados.

---

## 🔗 Relação com outras funções

- ft_memcpy
- ft_memset
- ft_bzero
- ft_memcmp
- ft_memchr

---

## ⏱️ Complexidade

Tempo: **O(n)**

Espaço: **O(1)**

---

## 📚 Referências

- man memmove
- ISO C
- POSIX
- The C Programming Language

</details>

---

<details>
<summary><strong>📄 ft_strlcpy</strong></summary>

## 📖 Descrição

Copia uma string de origem para uma string de destino, garantindo que a string de destino seja terminada pelo caractere nulo (`'\0'`), desde que o tamanho do buffer de destino seja maior que zero.

A função copia, no máximo, `size - 1` caracteres da string de origem e adiciona o terminador nulo ao final da string copiada.

---

## 📝 Protótipo

```c
size_t ft_strlcpy(char *dst, const char *src, size_t size);
```

---

## 📥 Parâmetros

### dst

Ponteiro para o buffer de destino.

### src

Ponteiro para a string de origem.

O conteúdo apontado por `src` não é modificado.

### size

Tamanho total do buffer de destino, em bytes.

Inclui o espaço necessário para o caractere terminador `'\0'`.

---

## 📤 Valor de Retorno

Retorna o comprimento da string de origem (`src`), desconsiderando o caractere `'\0'`.

Esse valor permite verificar se ocorreu truncamento durante a cópia:

- Se o valor retornado for **menor que `size`**, toda a string foi copiada.
- Se o valor retornado for **maior ou igual a `size`**, ocorreu truncamento.

---

## 🎯 Objetivo

Permitir a cópia segura de strings para buffers de tamanho conhecido, evitando estouros de memória (*buffer overflow*).

Essa função foi criada como uma alternativa mais segura à função `strcpy`, que não verifica o tamanho do buffer de destino.

---

## 🧠 Conceitos necessários

- Strings em C.
- Caractere terminador (`'\0'`).
- Buffers.
- Ponteiros.
- Tipo `size_t`.
- Comprimento de strings.
- Buffer overflow.
- Truncamento de strings.

---

## ⚠️ Armadilhas comuns

- Esquecer de reservar espaço para o caractere `'\0'`.
- Não tratar corretamente o caso em que `size` é igual a `0`.
- Assumir que toda a string foi copiada sem verificar o valor retornado.
- Confundir o tamanho do buffer (`size`) com o comprimento da string (`strlen`).
- Passar um buffer de destino menor do que o necessário.

---

## 🔗 Relação com outras funções

- ft_strlen
- ft_strdup
- ft_strlcat
- ft_memcpy
- ft_memmove

---

## ⏱️ Complexidade

Tempo: **O(n)**

Espaço: **O(1)**

Onde **n** é o comprimento da string de origem.

---

## 📚 Referências

- man strlcpy
- OpenBSD Manual Pages
- FreeBSD Manual Pages
- The BSD Library Functions Manual

</details>

---

<details>
<summary><strong>🔗 ft_strlcat</strong></summary>

## 📖 Descrição

Concatena uma string de origem ao final de uma string de destino, respeitando o tamanho total do buffer de destino.

A função adiciona caracteres de `src` ao final de `dst` até que não haja mais espaço disponível, garantindo que a string resultante seja terminada por `'\0'`, desde que exista pelo menos um byte livre no buffer.

---

## 📝 Protótipo

```c
size_t ft_strlcat(char *dst, const char *src, size_t size);
```

---

## 📥 Parâmetros

### dst

Ponteiro para a string de destino.

Deve estar corretamente terminada por `'\0'`, desde que seu comprimento seja menor que `size`.

### src

Ponteiro para a string de origem.

Seu conteúdo não é modificado.

### size

Tamanho total do buffer de destino, em bytes.

Esse valor representa a capacidade total do buffer, e não o espaço livre disponível.

---

## 📤 Valor de Retorno

Retorna o comprimento da string que **tentou** criar.

Em outras palavras:

```
comprimento inicial de dst + comprimento de src
```

Entretanto, caso `size` seja menor ou igual ao comprimento inicial de `dst`, o retorno será:

```
size + comprimento de src
```

Esse valor permite verificar se ocorreu truncamento durante a concatenação.

- Se o retorno for **menor que `size`**, toda a string foi concatenada.
- Se o retorno for **maior ou igual a `size`**, ocorreu truncamento.

---

## 🎯 Objetivo

Permitir a concatenação segura de strings em buffers de tamanho conhecido, evitando estouros de memória (*buffer overflow*).

A função foi desenvolvida como uma alternativa mais segura à função `strcat`, que não realiza nenhuma verificação sobre o tamanho do buffer de destino.

---

## 🧠 Conceitos necessários

- Strings em C.
- Caractere terminador (`'\0'`).
- Buffers.
- Ponteiros.
- Tipo `size_t`.
- Comprimento de strings.
- Concatenação de strings.
- Buffer overflow.
- Truncamento de strings.

---

## ⚠️ Armadilhas comuns

- Confundir o parâmetro `size` com o espaço livre disponível em `dst`. Ele representa o tamanho total do buffer.
- Não tratar corretamente o caso em que `size` é menor ou igual ao comprimento inicial de `dst`.
- Esquecer de garantir a terminação por `'\0'` quando houver espaço disponível.
- Assumir que toda a string foi concatenada sem verificar o valor retornado.
- Passar um buffer de destino que não esteja corretamente terminado por `'\0'`.

---

## 🔗 Relação com outras funções

- ft_strlen
- ft_strlcpy
- ft_strdup
- ft_memcpy
- ft_memmove

---

## ⏱️ Complexidade

Tempo: **O(n + m)**

Espaço: **O(1)**

Onde:

- **n** é o comprimento inicial de `dst`.
- **m** é o comprimento de `src`.

---

## 📚 Referências

- man strlcat
- OpenBSD Manual Pages
- FreeBSD Manual Pages
- The BSD Library Functions Manual

</details>

---

<details>
<summary><strong>🔗 ft_toupper</strong></summary>

## 📖 Descrição

Converte uma letra minúscula para a sua correspondente maiúscula.

Se o caractere passado como argumento for uma letra minúscula (entre 'a' e 'z' na tabela ASCII), a função retorna a sua versão maiúscula. Caso contrário, o caractere é retornado sem nenhuma alteração.

---

## 📝 Protótipo

```c
int ft_toupper(int c);
```

## 📥 Parâmetros

### c

O caractere a ser verificado e convertido.

O valor é passado como um `int`, que representa o valor numérico do caractere na tabela ASCII.

---

## 📤 Valor de Retorno

Retorna o valor ASCII do caractere correspondente em maiúscula, caso `c` seja uma letra minúscula.

Se `c` não for uma letra minúscula (seja uma letra já maiúscula, um número, pontuação, etc.), retorna o próprio valor `c` inalterado.

---

## 🎯 Objetivo

Fornecer uma maneira padronizada de converter caracteres alfabéticos para letras maiúsculas, replicando o comportamento da função original `toupper` da biblioteca padrão `<ctype.h>`.

---

## 🧠 Conceitos necessários

- Tabela ASCII.
- Tipos numéricos em C (relação entre `char` e `int`).
- Estruturas condicionais básicas.
- Operações matemáticas com valores ASCII (a diferença entre 'a' e 'A' é de 32).

---

## ⚠️ Armadilhas comuns

- Alterar caracteres que não são letras minúsculas. É essencial verificar se o caractere está no intervalo `['a', 'z']` antes de aplicar qualquer operação matemática.
- Assumir que a função lida com caracteres estendidos ou acentuados (como 'á', 'ç', 'é'). A função lida apenas com a tabela ASCII básica.
- Esquecer que a função recebe e retorna um `int`, e não um `char`.

---

## 🔗 Relação com outras funções

- ft_tolower
- ft_isalpha
- ft_isascii

---

## ⏱️ Complexidade

Tempo: **O(1)** (Apenas verificações matemáticas simples)

Espaço: **O(1)** (Nenhuma alocação de memória é necessária)

---

## 📚 Referências

- man toupper
- Manual da biblioteca `<ctype.h>`
- Tabela ASCII

</details>

---

- tolower
- strchr
- strrchr
- strncmp
- memchr
- memcmp
- strnstr
- atoi

---

### Parte 2 — Funções adicionais

Implementação de funções utilitárias propostas pela 42, como:

- ft_substr
- ft_strjoin
- ft_split
- ft_strtrim
- ft_itoa
- ft_strmapi
- ft_striteri

Essas funções passam a compor uma biblioteca pessoal reutilizável durante todo o restante do currículo.

---

<!-- ### Parte Bônus — Linked Lists

A etapa bônus consiste na implementação de uma lista simplesmente encadeada através da estrutura `t_list`.

Foram implementadas funções responsáveis por:

- Criação de novos nós.
- Inserção no início e no final da lista.
- Percurso da lista.
- Remoção de elementos.
- Liberação de memória.
- Aplicação de funções sobre os elementos.

Esta etapa introduz conceitos importantes de estruturas de dados e gerenciamento de memória dinâmica.

--- -->

# 🛠️ Instruções

## Pré-requisitos

O projeto foi desenvolvido em **C**, utilizando apenas as funções permitidas pela especificação da **42**.

É necessário possuir:

- GCC ou Clang
- Make

---

## Compilação

Compilar a biblioteca:

```bash
make
```

Remover arquivos objeto:

```bash
make clean
```

Remover arquivos objeto e biblioteca:

```bash
make fclean
```

Recompilar completamente:

```bash
make re
```

<!-- Compilar incluindo os bônus:

```bash
make bonus
``` -->

---

## Utilização

Após compilada, a biblioteca gera o arquivo:

```text
libft.a
```

Para utilizá-la em outro projeto basta incluir o cabeçalho:

```c
#include "libft.h"
```

e realizar o link da biblioteca durante a compilação.

---

# Referências Utilizadas

- The C Programming Language — Brian Kernighan & Dennis Ritchie.
- The Linux Programming Interface — Michael Kerrisk.
- GNU C Library Documentation.
- Linux Manual Pages (`man`).
- Harm Smits — 42 Docs.
- GeeksForGeeks (conceitos de estruturas de dados).
- cppreference (consulta sobre comportamento das funções da libc).
- Documentação oficial da linguagem C (ISO C).

---

# 🤖 Uso de Inteligência Artificial

## 0. IA's

Durante o desenvolvimento deste projeto foram utilizadas ferramentas de Inteligência Artificial exclusivamente como suporte pedagógico.

O objetivo foi compreender conceitos da linguagem C e auxiliar no processo de aprendizagem, mantendo toda a implementação das funções sob responsabilidade do autor.

---

## 1. Explicação de Conceitos

As IA's auxiliaram na compreensão de:

- Ponteiros.
- Ponteiros para ponteiros.
- Gerenciamento de memória.
- Funcionamento interno da libc.
- Manipulação de strings.
- Conversões ASCII.
<!-- - Estruturas de dados utilizando listas encadeadas. -->

---

## 2. Debugging

Foram utilizadas ocasionalmente para:

- Interpretação de mensagens do compilador.
- Diagnóstico de segmentation faults.
- Análise de problemas envolvendo ponteiros.
- Identificação de erros de lógica.
- Interpretação de testes da Francinette e do libftTester.

---

## 3. Organização do Projeto

A IA também auxiliou na:

- Organização do Makefile.
- Estruturação do projeto.
- Escrita e organização deste README.
- Levantamento das referências bibliográficas utilizadas durante os estudos.

---

# <a id="english"></a>🇺🇸 English Version

*This project was created as part of the 42 curriculum by rosousa-.*

---

# 📝 Description

**Libft** is the first project of the **42** curriculum and serves as the foundation for nearly every subsequent project. Its purpose is to recreate part of the standard C library (**libc**) while developing a personal utility library that can be reused throughout the curriculum.

The project aims to provide a deep understanding of low-level programming concepts, including:

- Memory manipulation.
- String manipulation.
- Dynamic memory allocation.
- Pointer management.
- Pointer-to-pointer semantics.
- Static libraries.
- Linked lists.

At the end of the project, a static library (`libft.a`) is generated and can be linked against future projects.

---

## 🛠️ Instructions

### Prerequisites

The project was written in **C** using only the functions allowed by the 42 subject.

Requirements:

- GCC or Clang
- Make

---

### Compilation

Compile the library:

```bash
make
```

Remove object files:

```bash
make clean
```

Remove object files and the library:

```bash
make fclean
```

Recompile everything:

```bash
make re
```

Compile including bonus functions:

```bash
make bonus
```

---

## 📚 Topics Covered

During the development of this project the following topics were studied:

- Memory management.
- Stack and Heap.
- Strings.
- ASCII conversions.
- Dynamic allocation.
- Pointer arithmetic.
- Linked lists.
- Static libraries.
- Makefiles.
- Debugging.
- Valgrind.
- Norminette.

---

## 🤖 AI Usage

Artificial Intelligence tools were used exclusively as educational support.

They were mainly employed to:

- Explain C language concepts.
- Clarify pointer behavior.
- Explain linked list operations.
- Assist in debugging compiler errors.
- Help organize the project documentation.

The implementation of every function remained entirely the responsibility of the author.
