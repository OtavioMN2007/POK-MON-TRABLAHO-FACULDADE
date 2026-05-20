# BatalhaPokeFireRed

Projeto da disciplina **ALGORITMOS E ESTRUTURAS DE DADOS**.

Professor: Dr. Maxwell Gomes Da Silva

Integrantes:

- Otávio Mendes Nunes - RA: 5178278
-  - RA:
-  - RA:

## Entrega principal

A entrega principal do trabalho esta em:

```text
BATTLE FIRE.ALG
```

Esse arquivo deve ser aberto no **VisuALG 3** e executado com **F9**.

## Como executar

1. Abra o VisuALG 3.
2. Abra o arquivo `BATTLE FIRE.ALG`.
3. Pressione F9.
4. Pressione ENTER na tela de boas-vindas para comecar sua jornada.

## Sobre o jogo

O jogo simula um sistema de batalha no estilo **Pokemon FireRed**, rodando inteiramente no terminal do VisuALG. O jogador recebe o **Pikachu** como Pokemon inicial e enfrenta batalhas sequenciais contra Pokemons selvagens.

O programa apresenta:

- Tela de boas-vindas com arte ASCII do titulo Pokemon.
- Apresentacao do Professor Carvalho em arte ASCII.
- Arte ASCII do Pikachu antes da primeira batalha.
- Arte ASCII dos Pokemons inimigos durante as batalhas.

## Batalhas

### Batalha 1 — ZONA SELVAGEM

| | Pokemon | HP |
|---|---|---|
| Jogador | Pikachu | 25 |
| Inimigo | Eevee (selvagem) | 20 |

Se o Eevee for capturado, ele **evolui automaticamente para Vaporeon** e a batalha 2 e liberada.

### Batalha 2 — CAMINHO DAS CHAMAS

| | Pokemon | HP |
|---|---|---|
| Jogador | Vaporeon | 35 |
| Inimigo | Charizard (selvagem) | 30 |

> A Batalha 2 so e acessivel se o jogador capturar o Eevee na Batalha 1.

## Controles — Acoes por batalha

Durante cada batalha, o jogador escolhe uma acao digitando o numero correspondente e pressionando ENTER:

```text
1 - Ataque rapido
2 - Ataque forte
3 - Usar POTION (cura 10 de HP)
4 - Capturar (jogar Pokebola)
```

### Golpes do Pikachu (Batalha 1)

```text
CHOQUE DO TROVAO   Ataque rapido  — causa de 5 a 7 de dano
INVESTIDA TROVAO   Ataque forte   — causa de 7 a 12 de dano (super efetivo)
```

### Golpes do Vaporeon (Batalha 2)

```text
JATO DE AGUA   Ataque rapido  — causa de 3 a 10 de dano (muito eficaz)
SURF           Ataque forte   — causa de 6 a 15 de dano (golpe devastador)
```

## Itens

```text
POTION   Recupera 10 de HP do Pokemon do jogador.
         Cada batalha comeca com 2 Potions disponiveis.
         Nao e possivel usar Potion se o HP ja estiver no maximo.
```

## Captura

Para capturar um Pokemon, escolha a opcao **4 - CAPTURAR** durante a batalha. A chance de captura e calculada com base no HP atual do inimigo: quanto menor o HP, maior a chance de sucesso.

```text
Gotcha! [Pokemon] foi capturado!   — captura bem-sucedida
Ah nao! [Pokemon] escapou!         — captura falhou
```

## Inteligencia artificial dos inimigos

Os Pokemons inimigos possuem comportamento dinamico:

- **Eevee**: quando com HP baixo, pode usar **DESEJO (WISH)** para se curar. Nos outros turnos, alterna entre **ATAQUE RAPIDO** e **MORDIDA (BITE)**.
- **Charizard**: quando com HP baixo, pode usar **DESCANSO (REST)** para se curar. Nos outros turnos, alterna entre **LANCACHAMAS**, **EXPLOSAO** e ataques normais.

## Resultados possiveis

```text
[Pokemon] desmaiou...          O jogador perdeu a batalha.
[Pokemon] desmaiou. Voce venceu!   O inimigo foi derrotado, mas nao capturado.
Gotcha! [Pokemon] foi capturado!   Vitoria com captura — desbloqueia a proxima batalha.
```

## Variaveis principais

```text
nome_jogador    Nome do Pokemon do jogador
nome_inimigo    Nome do Pokemon inimigo
hp_jogador      HP atual do jogador
hp_inimigo      HP atual do inimigo
hp_max_jogador  HP maximo do jogador (para limitar a cura)
hp_max_inimigo  HP maximo do inimigo (para limitar a cura)
pocoes_jogador  Quantidade de Potions restantes
capturado       Logico — indica se o inimigo foi capturado
dano            Dano calculado por turno
tentativa       Valor aleatorio usado no calculo de captura
acao_inimigo    Valor aleatorio usado na IA do inimigo
```
