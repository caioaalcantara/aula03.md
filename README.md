# Relatório de Atividade: Desmontando a Máquina e Desbloqueando o Raciocínio

**Estudante:** Caio
**Disciplina:** Engenharia de Prompt / Design Profissional
**Data:** 09/03/2026

---

## 1. Etapa 1 – Análise de Tokens (OpenAI Tokenizer)

Nesta etapa, analisei como o modelo processa o meu nome e a frase técnica solicitada.

**Frase analisada:** *"A engenharia de prompt otimiza LLMs"*

### [INSIRA O SEU PRINT DO TOKENIZER AQUI]
> *Dica: Arraste a imagem para o GitHub ou use a sintaxe `![Tokens](caminho-da-imagem.png)`*

**Observações Técnicas:**
- Notei que termos técnicos como **"LLMs"** e palavras longas em português são frequentemente fragmentados em sub-tokens. 
- A contagem de tokens foi superior ao número de palavras, o que comprova que a IA "lê" em blocos morfológicos e não em unidades de dicionário.

---

## 2. Etapa 2 – Teste de Previsibilidade

Simulação do prompt *"O gato come..."* com variações de temperatura (Criativa vs. Técnica).

| Perfil de Resposta | Palavras mais prováveis | Justificativa Lógica |
| :--- | :--- | :--- |
| **Muito Técnica** | 1. Ração<br>2. Peixe<br>3. Carne | Baseia-se em dados biológicos e estatísticos de alta frequência em bases de dados domésticas. |
| **Muito Criativa** | 1. Nuvens<br>2. Silêncios<br>3. O destino | Explora metáforas e conexões semânticas de baixa probabilidade, priorizando a originalidade literária. |

---

## 3. Etapa 3 – Raciocínio CoT (Chain-of-Thought)

**Desafio:** *"Qual é a terceira letra da quinta palavra da frase 'O rato roeu a roupa do Rei de Roma'?"*

### [INSIRA O SEU PRINT DA CONVERSA COM A IA AQUI]

**Análise do Resultado:**
Para chegar ao resultado correto (**letra "u"**), foi necessário aplicar o método **Chain-of-Thought**. Sem o passo a passo, a IA tende a errar devido à tokenização da palavra "roupa". Ao forçar a decomposição:
1. Identificação da 5ª palavra: "roupa".
2. Decomposição em caracteres: r-o-**u**-p-a.
3. Extração do 3º índice.

---

## 4. Conclusão Reflexiva

A principal conclusão desta atividade é que a unidade fundamental de processamento de um LLM não é a letra ou a palavra, mas o **token**. Essa camada de abstração cria uma "miopia" na IA para tarefas que exigem manipulação direta de caracteres.

Task como contagem de letras ou inversão de strings falham porque a IA enxerga blocos numéricos. O uso de **Engenharia de Prompt** (especificamente CoT) funciona como um "óculos" para a IA, permitindo que ela quebre esses blocos e processe informações de forma granular, aumentando drasticamente a precisão em tarefas lógicas complexas.
