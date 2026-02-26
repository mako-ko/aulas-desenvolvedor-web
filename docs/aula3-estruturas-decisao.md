# Estruturas de Decisão na Lógica de Programação

## Conceito Fundamental

Estruturas de decisão (ou estruturas condicionais) são mecanismos que permitem que um programa execute diferentes blocos de código com base no resultado de uma ou mais condições booleanas (verdadeiro ou falso). São a base para a criação de algoritmos não lineares, onde o fluxo de execução pode seguir caminhos distintos .

## Principais Tipos de Estruturas de Decisão

### 1. Estrutura `if` (Se)

É a estrutura condicional mais simples. Um bloco de código é executado **apenas se** a condição especificada for verdadeira (`true`). Se a condição for falsa (`false`), o bloco é ignorado e o programa continua na próxima instrução .

```python
# Exemplo em Python
temperatura = 35
if temperatura > 30:
    print("Está quente hoje.")
```

### 2. Estrutura `if-else` (Se... senão)

Permite especificar dois caminhos possíveis. Se a condição for verdadeira, executa o bloco do `if`. Caso contrário (falsa), executa o bloco do `else`. É uma estrutura de **escolha binária** .

```csharp
// Exemplo em C#
int valorCompra = 250;
if (valorCompra >= 300)
{
    Console.WriteLine("Ganhou 10% de desconto!");
}
else
{
    Console.WriteLine("Compre mais R$" + (300 - valorCompra) + " para ganhar desconto.");
}
```

### 3. Estrutura `if-else if-else` (Encadeada)

Utilizada quando há **múltiplas condições** a serem testadas. As condições são avaliadas em ordem sequencial. Assim que uma condição verdadeira é encontrada, seu bloco correspondente é executado e as demais são ignoradas .

```python
# Exemplo em Python
nota = 85
if nota >= 90:
    conceito = "A"
elif nota >= 80:
    conceito = "B"
elif nota >= 70:
    conceito = "C"
else:
    conceito = "D"
```

### 4. Estrutura `switch` (ou `switch-case`)

Ideal para situações onde uma única variável ou expressão é comparada a **múltiplos valores constantes** (casos). Ela seleciona qual bloco de código executar com base na correspondência encontrada. Geralmente inclui um caso `default` (padrão) para quando nenhuma correspondência é encontrada .

```csharp
// Exemplo em C#
int diaSemana = 3;
switch (diaSemana)
{
    case 1:
        Console.WriteLine("Segunda-feira");
        break;
    case 2:
        Console.WriteLine("Terça-feira");
        break;
    case 3:
        Console.WriteLine("Quarta-feira");
        break;
    default:
        Console.WriteLine("Dia inválido ou não mapeado");
        break;
}
```

## Operadores Utilizados em Condições

As condições são construídas utilizando operadores que retornam valores booleanos (`true` ou `false`).

### Operadores Relacionais (Comparação) 
- `>` (maior que)
- `<` (menor que)
- `>=` (maior ou igual a)
- `<=` (menor ou igual a)
- `==` (igual a — **atenção**: dois sinais de igual, diferente de atribuição `=`)
- `!=` (diferente de)

### Operadores Lógicos 
- `&&` ou `and` (E lógico): Verdadeiro se **ambas** as condições forem verdadeiras.
- `||` ou `or` (OU lógico): Verdadeiro se **pelo menos uma** das condições for verdadeira.
- `!` ou `not` (NÃO lógico): Inverte o valor booleano da condição.

## Boas Práticas e Observações Importantes

- **Indentação**: Em linguagens como Python, a indentação define o bloco de código pertencente à condição. Em outras (C#, Java), as chaves `{}` delimitam os blocos, mas a indentação é recomendada para legibilidade .
- **Avaliação em Curto-Circuito**: Em expressões com `&&` (E), se a primeira condição for falsa, a segunda nem é avaliada. Em expressões com `||` (OU), se a primeira for verdadeira, a segunda é ignorada .
- **Condições Mútualmente Exclusivas**: Em uma cadeia `if-else if-else`, apenas um bloco será executado. A ordem das condições importa .

---

## Referências

MICROSOFT. **Instruções de seleção - if, if-else e switch**. Disponível em: <https://learn.microsoft.com/pt-pt/dotnet/csharp/language-reference/statements/selection-statements>. Acesso em: 25 fev. 2026. 

MICROSOFT. **Use conditional and iterative statements**. Disponível em: <https://learn.microsoft.com/ru-ru/training/modules/get-started-xpp-finance-operations/5-cond-statement>. Acesso em: 25 fev. 2026. 

TUDELFT. **Workshop 2: Loop and Conditional Statements**. DigiPedia. Disponível em: <https://digipedia.tudelft.nl/tutorial/workshop-2-loop-and-conditional-statements/>. Acesso em: 25 fev. 2026. 

ALURA. **Praticando C: condicionais com if/else e switch/case**. Disponível em: <https://www.alura.com.br/conteudo/praticando-csharp-condicionais-if-else-switch-case>. Acesso em: 25 fev. 2026. 

ΕΛ/ΛΑΚ Moodle. **Week 1 - Section 2 - Controlling the flow**. Disponível em: <https://elearn.ellak.gr/mod/book/tool/print/index.php?id=1857>. Acesso em: 25 fev. 2026. 

GITHUB PAGES. **Conditionals**. Center for Environmental Measurement and Modeling. Disponível em: <https://cemac.github.io/sc-python/14-conditionals/index.html>. Acesso em: 25 fev. 2026. 