GanSO - Gamificação de noções de Sistemas Operacionais


1. Contexto e Gênero

Gênero: Jogo de tabuleiro educativo.
Contexto: Um jogo para simula o funcionamento de um Sistema Operacional (SO), onde os jogadores assumem o papel de processadores (CPUs/cores). Eles devem competir entre si para executar processos, gerenciar memória, responder corretamente a desafios e vencer a corrida até o fim do tabuleiro.
Objetivo: finalizar os processos (chegar ao fim do tabuleiro), aprendendo conceitos de escalonamento, gerenciamento de processos, memória, arquivos e conceitos de SO em geral.


2. Jornada do Jogador 

Início da Partida: Cada jogador começa com CPU e RAM livres (0% de uso).

Rodada: 
O jogador lança o dado (quantum + evento aleatório).
Avança casas conforme o resultado, mas só confirma o movimento se acertar a pergunta da pilha correspondente à casa.
Se errar, volta para a casa anterior (rollback).

Gestão de Recursos: 
Cada casa/pilha gera consumo de CPU e RAM.
Se o jogador atingir 100% em algum recurso, entra em estado de bloqueio (não joga até liberar).
A cada 5 rodadas, recursos mais antigos são liberados automaticamente.

Eventos Especiais: 
Rejogar dado (30% CPU, 0% RAM).
Travamento por falta de recursos (fica bloqueado).
Interrupções (volta uma casa).

Fim do Jogo:
O jogador que chegar primeiro ao final do tabuleiro conclui a jornada como processo terminado (EXIT).


3. Tipos de Jogadores

Jogadores Estratégicos:
Preferem avançar de forma mais segura, escolhendo perguntas fáceis ou médias, focando em minimizar riscos, garantindo que sempre tenham CPU e RAM disponíveis.

Jogadores Desafiadores:
Preferem assumir riscos maiores, escolhendo perguntas difíceis para tentar avançar mais rápido, gostando de maior competitividade e buscando concluir os processos de forma ousada, mesmo correndo risco de bloqueio.


4. Mecânicas e Conceitos de SO Representados

Processos e Escalonamento: Turnos equivalem a ciclos de CPU; dado é o quantum; perguntas simulam execução bem-sucedida ou falha.

Gerenciamento de Memória: Cada jogada consome CPU/RAM e os processos permanecem alocados por rodadas até serem liberados.

Gerenciamento de Arquivos: Representado pelas pilhas de perguntas, com diferentes níveis de dificuldade.

E/S (Entrada e Saída): Casas especiais podem simular operações de E/S, que bloqueiam temporariamente o processo.

Interrupções: Voltar à casa anterior ou ficar bloqueado.

Estado de Processos: Jogador pode estar em Execução, Bloqueado, ou Terminado.


5. Estrutura de Recursos

Pilhas de Perguntas:

Fácil: 30% CPU, 20% RAM.

Médio: 25% CPU, 25% RAM.

Difícil: 20% CPU, 30% RAM.

Eventos:

Rejogar dado → 30% CPU, 0% RAM.

Travamento → bloqueio até liberar RAM.
