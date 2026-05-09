# Diagnóstico de retomada - Teoria da Computação

Esta atividade serve para mapear o que você já domina sobre linguagens formais, autômatos, gramáticas e computabilidade.

Responda individualmente. Use suas palavras. Se usar IA depois da primeira tentativa, registre o uso na seção 7.

## 1. Mapa do que eu lembro

Marque cada tópico como: lembro bem, lembro parcialmente, não lembro, nunca vi ou não tenho certeza.

- alfabeto: lembro
- cadeia: lembro
- linguagem: lembro
- gramática: lembro
- autômato finito: lembro
- linguagem regular: lembro
- linguagem livre de contexto: lembro
- linguagem sensível ao contexto: não tenho certeza
- linguagem irrestrita: não tenho certeza
- hierarquia de Chomsky: lembro
- computabilidade: não tenho certeza
- máquina de Turing: lembro

## 2. Definições com exemplo

Explique, com suas palavras e com um exemplo simples, usando o alfabeto `Sigma = {a, b}`.

1. O que é um alfabeto? um alfabeto e a definição dos caracteres que serão utilizados para formar as cadeias.
2. O que é uma cadeia? cadeia é um conjunto formado pelo concatenção de elementos do alfabeto.
3. O que é uma linguagem? linguagem é o conjunto formado pelas cadeias. Ela serve para definir se determinada cadeia faz parta da linguagem ou não.
4. O que é uma gramática? é o conjunto que gera as cadeias. Tem uma definição próxima de linguagem. Enquanto a linguagem trabalha como reconhecedor de cadeias, a gramática trabalha como  gerador de cadeias.

## 3. Linguagens

Considere as linguagens:

```text
L1 = { w em {0,1}* | w termina com 01 }
L2 = { a^n b^n | n >= 0 }
L3 = { a^n b^n c^n | n >= 0 }
```

Para cada linguagem:

1. escreva três palavras que pertencem à linguagem;
3. escreva duas palavras que não pertencem;
4. diga, se souber, em qual classe ela provavelmente se encaixa;
5. explique o motivo em linguagem simples.

Resposta da questão 3.1:
L1 = {001,101,0001}
L2 = {vazio, ab, aabb}
L3 = {vazio, abc, aabbcc}

Resposta da questão 3.2:
L1 = {000,110,0011}
L2 = {a, aab, aabbbb}
L3 = {abcc, aabc, aabbbbcc}

Resposta da questão 3.3:
L1 = automato finito
L2 = livre de contexto
L3 = maquina de turing

Resposta da questão 3.4:
L1 = reconhece cadeia que terminam em 01
L2 = reconhece palavras que tenham ab com mesma quantidade de a e b
L3 = reconhece cadeias que tenham abc com mesma quantidade de a e b e c

Não há problema em dizer "não sei". Nesse caso, escreva o que te deixou em dúvida.

## 4. Autômato finito

Considere o autômato abaixo, sobre o alfabeto `{0,1}`:

```text
Estados: q0, q1, q2
Estado inicial: q0
Estado final: q2

Transições:
q0 --0--> q1
q0 --1--> q0
q1 --0--> q1
q1 --1--> q2
q2 --0--> q1
q2 --1--> q0
```

Responda:

1. Qual linguagem esse autômato parece reconhecer? Resposta: Esse autômato reconhece palavras que terminam com 01.
2. Execute manualmente as cadeias abaixo e diga se aceita ou rejeita: 
   - `01` | resposta: aceita
   - `101`  | resposta: aceita
   - `100`  | resposta: rejeita
   - `1101` | resposta: aceita
   - `111` | resposta: rejeita
3. Monte uma tabela curta mostrando o caminho dos estados para pelo menos duas cadeias.
Resposta:
analisando a cadeia 01:
```text
(q0,0) ---> q1
(q1,1) ---> q2
```

analisando a cadeia 111:
```text
(q0,1) ---> q0
(q0,1) ---> q0
(q0,1) ---> q0
```

## 5. Gramática

Considere a gramática:

```text
S -> aS
S -> b
```

Responda:

1. Gere cinco cadeias produzidas por essa gramática.
2. Descreva a linguagem em palavras.
3. Essa gramática parece regular, livre de contexto ou outra classe? Justifique de forma simples.

Resposta da questão 5.1:
```text
{ab,aab,aaab,aaaab,aaaaab}
```
Resposta da questão 5.2:
```text
gera palavras que tem pelo menos 1 a e termina com b.
```

Resposta da questão 5.3:
```text
Pode ser reconhecida por um autômato finito, desse modo, não há necessidade de memória. Portanto é uma linguagem regular.
```

## 6. Ponto de dificuldade

Escolha um tópico da lista inicial e escreva:

1. o que você entende dele;
2. onde você se confunde;
3. que tipo de explicação ajudaria: desenho, exemplo, exercício guiado, analogia, prova passo a passo ou lista curta.

Resposta da questão 6.1: 
```text
Hierarquia de Chomsky
```

Resposta da questão 6.2: 
```text
Tenho dificuldade em lembra os tipos de linguagem. As vezes confundo a limitação de cada uma. Sobre linguagem regular e Máquina de turing eu não esqueço.
```

Resposta da questão 6.3: 
```text
desenho mostrando a transição do que a linguagem reconhece usando exemplos.
```

## 7. Uso de IA, se houver

Se você usou IA depois da primeira tentativa, registre:

```text
Pergunta feita: "qual a diferença entre linguagem e gramática na teoria da computação?"
Resumo da resposta: 
"A linguagem é o “resultado final”.
A gramática é o “mecanismo de construção”."
Como eu verifiquei: não entendi essa pergunta
O que eu alterei na minha resposta: para mim era a mesma coisa
O que ainda não entendi: não tenho dúvidas
```

## Submissão no Moodle

Depois de finalizar, copie no Moodle:

```text
Repositório:
Commit final:
Autoavaliação: nível atual, maior dificuldade e tópico que precisa ser retomado.
```
