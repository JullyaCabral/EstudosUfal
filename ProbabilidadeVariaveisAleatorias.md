
## 1. Variáveis Aleatórias Discretas

### 1.1. Distribuição Uniforme Discreta

**Conceito:**  
Cada resultado possui a mesma probabilidade de ocorrer. Se temos um conjunto de \( n \) valores, a chance de cada um aparecer é igual.

**Fórmula:**  

\[
P(X = x) = \frac{1}{n}
\]

**Exemplo Simples – Dado:**  
- Imagine um dado justo com 6 faces.  
- Cada face tem a mesma chance:  
  \[
  P(X = x) = \frac{1}{6} \approx 0.1667, \quad x \in \{1,2,3,4,5,6\}
  \]

**Exemplo Complexo – Soma de Dois Dados:**  
- Ao lançar dois dados, há \( 6 \times 6 = 36 \) resultados possíveis, mas nem todas as somas ocorrem com a mesma frequência.  
- Para a soma 7, as combinações possíveis são:  
  \[
  (1,6), (2,5), (3,4), (4,3), (5,2), (6,1) \quad \Rightarrow \quad 6 \text{ combinações}
  \]
- A probabilidade de obter 7 é:
  \[
  P(X = 7) = \frac{6}{36} = \frac{1}{6} \approx 0.1667
  \]

*Observação:* Embora os resultados individuais sejam uniformemente distribuídos quando se lança um dado, a soma de dois dados já não é uniforme. Essa comparação ilustra a diferença entre “distribuição uniforme” e “função de probabilidade de um resultado composto”.

---

### 1.2. Distribuição de Bernoulli

**Conceito:**  
Modela experimentos com **dois resultados possíveis**, geralmente chamados de "sucesso" (1) e "fracasso" (0). É o modelo básico para experimentos binários.

**Fórmula:**  
\[
P(X = x) = p^x (1 - p)^{1 - x}, \quad \text{para } x \in \{0, 1\}
\]

Onde:
  - \( p \) é a probabilidade de sucesso.
  - \( 1 - p \) é a probabilidade de fracasso.

**Exemplo Simples – Lançamento de Moeda:**  
- Considere \( p = 0.5 \) para cara (sucesso) e 0 para coroa (fracasso).  
- Assim:
  - \( P(X = 1) = 0.5 \)
  - \( P(X = 0) = 0.5 \)

**Exemplo Complexo – Decisão Binária em Experimentos:**  
- Suponha um teste simples onde um medicamento tem 80% de chance de funcionar: \( p = 0.8 \).  
- Assim:
  - Chance do medicamento ser eficaz (\( x = 1 \)):  
    \[
    P(X = 1) = 0.8
    \]
  - Chance de não funcionar (\( x = 0 \)):  
    \[
    P(X = 0) = 0.2
    \]

---

### 1.3. Distribuição Binomial

**Conceito:**  
Representa o número de sucessos em \( n \) ensaios independentes, cada um com probabilidade de sucesso \( p \).

**Fórmula:**  
\[
P(X = k) = \binom{n}{k} p^k (1 - p)^{n - k}, \quad \text{para } k = 0, 1, \dots, n
\]

Onde:
\[
\binom{n}{k} = \frac{n!}{k!(n - k)!}
\]

**Exemplo Simples – 3 Lançamentos de Moeda:**  
- Suponha 3 lançamentos (\( n = 3 \)) com \( p = 0.5 \).  
- Calcular \( P(X = 2) \) (2 caras):
  \[
  P(X = 2) = \binom{3}{2} (0.5)^2 (0.5)^1 = 3 \times 0.25 \times 0.5 = 0.375
  \]

**Exemplo Complexo – Sucesso em Testes Clínicos:**  
- Suponha \( n = 10 \) pacientes e a probabilidade de sucesso de um tratamento é \( p = 0.7 \).  
- Calcular a probabilidade de exatamente 7 sucessos:
  \[
  P(X = 7) = \binom{10}{7} (0.7)^7 (0.3)^3
  \]
Onde:
\[
\binom{10}{7} = \frac{10!}{7!3!} = 120
\]
Portanto:
\[
P(X = 7) = 120 \times (0.7)^7 \times (0.3)^3
\]

---

### 1.4. Distribuição de Poisson

**Conceito:**  
Modela a ocorrência de eventos raros ou independentes em um intervalo fixo (tempo, espaço, etc.) dado um número médio de ocorrências \( \lambda \).

**Fórmula:**  
\[
P(X = k) = \frac{\lambda^k e^{-\lambda}}{k!}, \quad k = 0, 1, 2, \dots
\]

**Exemplo Simples – Acidentes em Um Dia:**  
- Suponha que ocorrem, em média, \( \lambda = 3 \) acidentes por dia.  
- A probabilidade de ocorrerem 2 acidentes num dia é:
  \[
  P(X = 2) = \frac{3^2 e^{-3}}{2!} = \frac{9 e^{-3}}{2}
  \]

**Exemplo Complexo – Chamadas em um Call Center:**  
- Um call center recebe em média 1.5 ligações por minuto. Em 10 minutos, o valor médio será \( \lambda = 15 \).  
- Para calcular a probabilidade de receber exatamente 12 ligações:
  \[
  P(X = 12) = \frac{15^{12} e^{-15}}{12!}
  \]

---

## 2. Variáveis Aleatórias Contínuas

### 2.1. Distribuição Normal

**Conceito:**  
A Distribuição Normal (ou Gaussiana) é simétrica em torno da sua média e modela muitos fenômenos naturais. Cada observação tende a se concentrar próxima da média com a frequência caindo de forma exponencial à medida que se afasta.

**Fórmula (Função Densidade de Probabilidade):**  
\[
f(x) = \frac{1}{\sigma \sqrt{2 \pi}} \exp \left( -\frac{1}{2} \left( \frac{x - \mu}{\sigma} \right)^2 \right)
\]
Onde:
  - \( \mu \) é a média.
  - \( \sigma \) é o desvio padrão.

**Exemplo Simples – Normal Padrão:**  
- Parâmetros: \( \mu = 0 \), \( \sigma = 1 \).  
- A probabilidade de \( X \) estar no intervalo \( [-1, 1] \) é aproximadamente 68.27% (regra dos 68-95-99.7).

**Exemplo Complexo – Alturas de uma População:**  
- Suponha que a altura de uma população segue uma normal com \( \mu = 170 \) cm e \( \sigma = 10 \) cm.  
- Para calcular a probabilidade de uma pessoa medir mais de 190 cm:
  1. Calcule o valor \( z \):
     \[
     z = \frac{190 - 170}{10} = 2.0
     \]
  2. Use a tabela de \( z \) ou funções do R (como `pnorm`):
     \[
     P(X > 190) = 1 - P(X \leq 190) \approx 1 - 0.9772 = 0.0228
     \]
- Assim, há aproximadamente 2.28% de chance de uma pessoa medir mais de 190 cm.

---

### 2.2. Distribuição Exponencial

**Conceito:**  
Modela o tempo entre eventos em um processo onde os eventos ocorrem de forma contínua e independente. Tem a propriedade sem memória, ou seja, o tempo restante para o próximo evento é independente do tempo já decorrido.

**Fórmula (Função Densidade de Probabilidade):**  
\[
f(x) = \lambda e^{-\lambda x}, \quad x \geq 0
\]
Onde \( \lambda \) é a taxa (o inverso do tempo médio de ocorrência).

**Exemplo Simples – Tempo de Atendimento:**  
- Se o tempo médio de atendimento é de 5 minutos, então:
  \[
  \lambda = \frac{1}{5} = 0.2
 

 \]
- Para calcular a probabilidade do atendimento ocorrer em **até 3 minutos**:
  \[
  P(X \leq 3) = 1 - e^{-\lambda \cdot 3} = 1 - e^{-0.6}
  \]

**Exemplo Complexo – Espera Longa:**  
- Com os mesmos parâmetros (\( \lambda = 0.2 \)), para calcular a probabilidade de esperar **mais de 10 minutos**:
  \[
  P(X > 10) = e^{-\lambda \cdot 10} = e^{-2} \approx 0.1353
  \]
- Ou seja, há aproximadamente 13.53% de chance de um tempo de espera maior que 10 minutos.

---

### Relacionando com Scripts no R

No R, você pode usar funções próprias para cada uma dessas distribuições:  

- **Uniforme:**  
  - Gerar números aleatórios: `runif(n, min, max)`  
  - **Exemplo:** `runif(100, 1, 6)` (mas note que para um dado normalmente se usa números discretos)

- **Bernoulli e Binomial:**  
  - `rbinom(n, size, prob)` para gerar amostras.  
  - **Exemplo (Bernoulli):** `rbinom(100, size = 1, prob = 0.5)`  
  - **Exemplo (Binomial):** `rbinom(100, size = 3, prob = 0.5)`

- **Poisson:**  
  - `rpois(n, lambda)`  
  - **Exemplo:** `rpois(100, lambda = 3)`

- **Normal:**  
  - `rnorm(n, mean, sd)`  
  - **Exemplo:** `rnorm(100, mean = 170, sd = 10)`

- **Exponencial:**  
  - `rexp(n, rate)`  
  - **Exemplo:** `rexp(100, rate = 0.2)`

Essas funções permitem explorar e visualizar os conceitos através de simulações e gráficos, como com `hist()`, `plot()`, etc.

---

## Conclusão

Em resumo, cada distribuição tem sua aplicação e fórmula associada:

- **Discretas:**
  - **Uniforme:** \( P(X = x) = \frac{1}{n} \)
  - **Bernoulli:** \( P(X = x) = p^x (1 - p)^{1 - x} \)
  - **Binomial:** \( P(X = k) = \binom{n}{k} p^k (1 - p)^{n - k} \)
  - **Poisson:** \( P(X = k) = \frac{\lambda^k e^{-\lambda}}{k!} \)

- **Contínuas:**
  - **Normal:**  
    \[
    f(x) = \frac{1}{\sigma \sqrt{2 \pi}} e^{-\frac{1}{2} \left( \frac{x - \mu}{\sigma} \right)^2}
    \]
  - **Exponencial:**  
    \[
    f(x) = \lambda e^{-\lambda x}, \quad x \geq 0
    \]

Cada um dos exemplos simples explica o conceito básico, enquanto os casos mais complexos demonstram como aplicar as fórmulas em situações práticas que podem ser simuladas no R. Conforme você se familiarizar com essas fórmulas, ficará mais fácil montar os scripts e interpretar os resultados.

Se desejar aprofundar em algum tópico ou explorar exemplos de código mais específicos, posso expandir em mais detalhes. Boa sorte nos estudos e na prova!

--- 

Agora as fórmulas estão com a notação matemática bem estruturada!

Claro! Aqui está o conteúdo completo formatado como documento, com título e organização adequada para impressão ou entrega:

---
