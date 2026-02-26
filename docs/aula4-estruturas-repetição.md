# Estruturas de Repetição na Lógica de Programação

## Conceito Fundamental

Estruturas de repetição, também chamadas de **loops** ou **laços**, são construções que permitem executar um bloco de código múltiplas vezes, de forma automática, enquanto uma determinada condição for verdadeira . São a base para automação de tarefas repetitivas, processamento de listas e otimização de código .

## Principais Tipos de Estruturas de Repetição

### 1. Estrutura `for` (Para)

O loop `for` é utilizado quando **sabemos antecipadamente quantas vezes** o bloco de código deve ser repetido . Sua sintaxe geralmente inclui três partes: inicialização de uma variável contadora, condição de continuação e expressão de incremento/decremento .

```python
# Exemplo em Python: imprimir números de 1 a 5
for i in range(1, 6):
    print(i)
```

```csharp
// Exemplo em C#: imprimir números de 1 a 5
for (int i = 1; i <= 5; i++)
{
    Console.WriteLine(i);
}
```

### 2. Estrutura `while` (Enquanto)

O loop `while` é adequado quando **não sabemos o número exato de iterações** e a repetição depende de uma condição que pode mudar durante a execução . A condição é testada **antes** da execução do bloco; se for falsa na primeira verificação, o bloco pode nunca ser executado .

```javascript
// Exemplo em JavaScript
let contador = 1;
while (contador <= 5) {
    console.log(contador);
    contador++;
}
```

### 3. Estrutura `do-while` (Faça... Enquanto)

Semelhante ao `while`, mas com a diferença fundamental de que a condição é testada **após** a execução do bloco. Isso garante que o bloco seja executado **pelo menos uma vez**, mesmo que a condição seja inicialmente falsa .

```java
// Exemplo em Java
int numero;
do {
    System.out.print("Digite um número entre 1 e 10: ");
    numero = scanner.nextInt();
} while (numero < 1 || numero > 10);
```

### 4. Estrutura `foreach` (Para cada)

É uma variação do `for` projetada especificamente para **percorrer todos os elementos de uma coleção** (como arrays ou listas) de forma simplificada, sem necessidade de controlar índices manualmente .

```python
# Exemplo em Python (com for tradicional, mas conceito similar)
frutas = ["maçã", "banana", "laranja"]
for fruta in frutas:
    print(fruta)
```

## Comandos de Controle de Fluxo

- **`break`**: Interrompe imediatamente a execução do loop, saltando para a primeira instrução após o bloco de repetição .
- **`continue`**: Interrompe apenas a iteração atual e salta para a próxima iteração do loop .

```javascript
// Exemplo com break e continue
for (let i = 1; i <= 10; i++) {
    if (i === 5) {
        continue; // pula o 5
    }
    if (i === 8) {
        break;    // para no 8
    }
    console.log(i); // imprime: 1,2,3,4,6,7
}
```

## Boas Práticas e Cuidados Importantes

1.  **Evitar Loops Infinitos**: Certifique-se de que a condição do loop se tornará falsa em algum momento. Loops infinitos ocorrem quando a variável de controle não é atualizada corretamente e podem travar o programa .

2.  **Escolha a Estrutura Adequada**:
    - Use `for` quando souber o número exato de repetições .
    - Use `while` quando o número de repetições depender de uma condição que pode variar .
    - Use `do-while` quando precisar garantir pelo menos uma execução .
    - Use `foreach` para percorrer coleções de forma limpa e legível .

3.  **Legibilidade do Código**: Utilize nomes significativos para as variáveis de controle (como `i`, `j` para contadores simples, ou nomes mais descritivos quando apropriado). Comente a lógica do loop se necessário .

4.  **Performance**: Evite aninhar loops desnecessariamente (loops dentro de loops), pois isso pode aumentar drasticamente a complexidade e o tempo de execução .

---

## Referências

LENOVO. **O que é um loop?** Disponível em: <https://www.lenovo.com/pt/pt/glossary/loop/>. Acesso em: 25 fev. 2026. 

PYTHON ACADEMY. **For, While, Loops e Estruturas de Repetição no Python**. Disponível em: <https://pythonacademy.com.br/blog/estruturas-de-repeticao>. Acesso em: 25 fev. 2026. 

BUENO, Gabriel. **Estrutura de Repetição**. Disponível em: <https://gabrielbueno072.github.io/rea-aed/aula_rep.html>. Acesso em: 25 fev. 2026. 

ROCKETSEAT. **Loops em JavaScript: Um Guia Básico para Iniciantes**. Disponível em: <https://rocketseat.com.br/blog/artigos/post/loops-em-javascript-um-guia-basico-para-iniciantes>. Acesso em: 25 fev. 2026. 

DEVMEDIA. **While e Do/While – Laços de Repetições: Estrutura da Linguagem – Parte 1**. Disponível em: <https://www.devmedia.com.br/while-e-do-while-lacos-de-repeticoes-estrutura-da-linguagem-parte-1/18870>. Acesso em: 25 fev. 2026. 

DEVSEM MEDO. **Como funcionam os loops em programação**. Disponível em: <https://devsemmedo.com.br/como-funcionam-os-loops-em-programacao/>. Acesso em: 25 fev. 2026. 

TRYBE. **Estruturas de repetição: quais as 4 principais e quando usá-las?** Disponível em: <https://blog.betrybe.com/desenvolvimento-web/estruturas-de-repeticao/>. Acesso em: 25 fev. 2026. 

BUG, Bios. **Conceitos fundamentais de programação: Variáveis, tipos de dados e muito mais**. DEV Community. Disponível em: <https://dev.to/biosbug/conceitos-fundamentais-de-programacao-variaveis-tipos-de-dados-e-muito-mais-4c9n>. Acesso em: 25 fev. 2026. 

FORMAÇÃO DEV. **Estruturas de repetições em Java (for, while, do-while, for-each)**. Disponível em: <https://blog.formacao.dev/estruturas-de-repeticoes-em-java-for-while-e-do-while-for-each/>. Acesso em: 25 fev. 2026. 