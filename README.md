Pokemon Battle
Projeto da disciplina ALGORITMOS E ESTRUTURAS DE DADOS.

Professor: Dr. MAXWELL GOMES DA SILVA

Integrantes:

Otavio Mendes Nunes - RA: 5181461
Gabriel Ricardo S. Martins - RA: 5179502
Flávio Henrique S. Faria - RA: 5182898

Entrega principal
A entrega principal do trabalho está em:

Plaintext
POKEMON_BATTLE/Batalha definitiva.ALG
Esse arquivo deve ser aberto no VisuALG 3 e executado com F9.

Estrutura do repositório
Plaintext
POKEMON_TRABALHO_FACULDADE/
|
|-- README.md
|
|-- POKEMON_BATTLE/
|   |-- Batalha definitiva.ALG
Como executar a versão oficial
Abra o VisuALG 3.

Abra o arquivo POKEMON_BATTLE/Batalha definitiva.ALG.

Pressione F9 para iniciar a execução.

Siga as instruções textuais na tela para avançar pelos diálogos e menus.

Fluxo do Jogo e Mecânicas
O jogo reproduz uma experiência inspirada no clássico Pokémon FireRed, trazendo telas de boas-vindas em arte ASCII e batalhas por turnos.

1. Prólogo e Introdução
Boas-vindas: O jogo inicia com uma tela de abertura temática.

Prof. Carvalho: O famoso cientista introduz o jogador ao mundo dos monstrinhos e entrega o seu Pokémon inicial: Pikachu.

2. Sistema de Batalha por Turnos
O núcleo do jogo funciona através de uma estrutura condicional repetitiva (enquanto), alternando ações entre o jogador e uma Inteligência Artificial do inimigo:

Turno do Jogador: Apresenta um menu de escolha numérica com as seguintes opções:

Plaintext
1 - CHOQUE DO TROVAO (Ataque Rápido)
2 - INVESTIDA TROVAO (Ataque Forte)
3 - USAR POÇÃO (Restaurar 10 HP)
4 - CAPTURAR (Jogar Pokebola)
Inteligência Artificial (Inimigo Inteligente): O oponente (Eevee) age baseado no seu nível de vida atual:

Se estiver com vida cheia/normal, ele alterna aleatoriamente entre ataques normais e ferozes (ATAQUE RÁPIDO ou MORDIDA).

Se estiver com vida baixa (<= 6 HP), ele entra em modo defensivo e possui uma alta probabilidade (80%) de usar a habilidade de cura DESEJO (WISH) para se recuperar, ou ataca com desespero caso falhe.

3. Sistema de Captura e Evolução
Captura: O sucesso do arremesso da Pokebola é calculado dinamicamente com base na vida atual do inimigo (quanto menor o HP, mais fácil capturar).

Evolução por Pedra: Caso o Eevee seja capturado com sucesso, o jogo ativa um evento especial onde o jogador encontra uma Pedra Água. Se decidir usá-la, uma sequência de animação ASCII exibe a evolução do Eevee para Vaporeon, liberando a sequência da jornada.

Condições de Vitória e Derrota
Vitória Definitiva: Capturar o Pokémon selvagem e concluir a jornada de evolução com sucesso.

Fim de Jogo (Game Over): Se o HP do Pikachu chegar a zero (hp_jogador <= 0), o jogador é derrotado e o jogo é encerrado.

Fim de Jornada Prematuro: Derrotar o inimigo (zerar o HP dele) sem realizar a captura impede o progresso da jornada, exigindo que o treinador tente novamente para conseguir capturá-lo.
