# Calculadora de Áreas em C – Melhorar o Código

## Enunciado
Foi-te entregue um programa em C que calcula áreas de algumas figuras geométricas. O programa funciona, mas está incompleto e é pouco robusto.

Tens de **analisar o código existente**, perceber como está organizado e **melhorá-lo**:

1. **Acrescentar novos cálculos**: novas fórmulas de áreas e perímetros, cada uma na sua própria função, seguindo o modelo das funções que já existem.
2. **Integrar os novos cálculos no menu**, para que o utilizador os possa escolher.
3. **Tornar o programa mais robusto**, impedindo cálculos com medidas inválidas.
4. **Melhorar a usabilidade**, para que o utilizador possa fazer vários cálculos sem reiniciar o programa.

As especificações de cada tarefa estão mais abaixo. Testa o programa no teu computador antes de cada entrega e faz `commit` com mensagens claras (por exemplo, `Adiciona area do triangulo`).

### Critérios de avaliação
- Correção dos cálculos (testes automáticos)
- Organização do código: uma função por cálculo, nomes claros, indentação
- Histórico de commits regular

---

## Compilar e executar
```bash
gcc areas.c -o areas
./areas
```

## Regras importantes
- Cada cálculo deve ter a **sua própria função** (como `area_quadrado`).
- Usa **exatamente** os números de opção e os textos de saída indicados. Os testes automáticos dependem disso:
  - `Area: 12.00`
  - `Perimetro: 16.00`
  - `Valor invalido`
- Mostra sempre os resultados com 2 casas decimais (`%.2f`).

## Tarefas

| Nº | Tarefa | Opção | Dados lidos | Fórmula | Pontos |
|----|--------|:-----:|-------------|---------|:------:|
| 1 | Área do triângulo | 3 | base, altura | (base × altura) / 2 | 2 |
| 2 | Área do círculo | 4 | raio | PI × raio² | 2 |
| 3 | Área do trapézio | 5 | base maior, base menor, altura | ((B + b) × altura) / 2 | 2 |
| 4 | Área do losango | 6 | diagonal maior, diagonal menor | (D × d) / 2 | 2 |
| 5 | Perímetro do retângulo | 7 | base, altura | 2 × (base + altura) | 2 |
| 6 | Perímetro do círculo | 8 | raio | 2 × PI × raio | 2 |
| 7 | Validação | todas | – | Se alguma medida for ≤ 0, mostra `Valor invalido` em vez do resultado | 4 |
| 8 | Menu repetido | 0 = Sair | – | O menu volta a aparecer depois de cada cálculo, até o utilizador escolher **0** | 4 |
| | | | | **Total** | **20** |

### Exemplo (com todas as tarefas feitas)
```
1-Quadrado 2-Retangulo 3-Triangulo 4-Circulo 5-Trapezio 6-Losango
7-Perimetro retangulo 8-Perimetro circulo 0-Sair
Opcao: 3
Base e altura: 6 4
Area: 12.00

Opcao: 1
Lado: -4
Valor invalido

Opcao: 0
```

## Desafios extra (sem testes automáticos)
- Volume do cubo e da esfera (4/3 × PI × r³).
- Perímetro do triângulo (lê os 3 lados).
- Verificar se o triângulo é possível (cada lado tem de ser menor que a soma dos outros dois).
- Substituir os `if/else` do menu por um `switch`.

## Entrega
Faz `commit` e `push` sempre que terminares uma tarefa. Os testes correm no separador **Actions** e a nota aparece no GitHub Classroom.
