# Especificação de Caso de Uso — Biblioteca Online

## 1. Sistema escolhido

O sistema escolhido é uma **Biblioteca Online**, que permite aos leitores consultar o catálogo e reservar livros. Os funcionários da biblioteca também utilizam o sistema para registrar empréstimos e devoluções. Um serviço externo é utilizado para enviar notificações aos leitores.

## 2. Atores do sistema

- **Leitor (ator principal):** consulta o catálogo e solicita a reserva de livros.
- **Bibliotecário (ator principal):** registra empréstimos e devoluções de livros.
- **Serviço de Notificações (ator secundário):** outro sistema que recebe solicitações da Biblioteca Online e envia avisos aos leitores.

## 3. Casos de uso contemplados no diagrama

1. Consultar catálogo.
2. Reservar livro.
3. Realizar empréstimo.
4. Registrar devolução.
5. Enviar notificação.

## 4. Especificação do caso de uso: Reservar livro

**Ator:** Leitor.

**Descrição:** Permite que um leitor solicite a reserva de um livro disponível ou entre na fila de espera caso todos os exemplares estejam emprestados.

**Gatilho:** O leitor seleciona um livro no catálogo e escolhe a opção “Reservar”.

**Pré-condições:**
- O leitor deve estar cadastrado e autenticado no sistema.
- O livro deve estar cadastrado no catálogo da biblioteca.
- A conta do leitor não pode estar bloqueada.

**Pós-condições:**
- Se houver exemplar disponível, uma reserva é registrada em nome do leitor.
- Se todos os exemplares estiverem emprestados, o leitor é incluído na fila de espera.
- O sistema registra a operação e solicita o envio de uma notificação ao leitor.

### Fluxo principal

1. O leitor acessa o catálogo da Biblioteca Online.
2. O leitor pesquisa e seleciona o livro desejado.
3. O sistema apresenta os dados do livro e a situação dos exemplares.
4. O leitor seleciona a opção “Reservar”.
5. O sistema verifica se o leitor está autenticado e se sua conta está regular.
6. O sistema verifica a disponibilidade de exemplares.
7. O sistema registra a reserva em nome do leitor.
8. O sistema confirma a reserva na tela.
9. O sistema solicita ao Serviço de Notificações o envio de uma confirmação ao leitor.

### Fluxo alternativo — Livro sem exemplar disponível

**Quando acontece:** No passo 6 do fluxo principal, quando todos os exemplares do livro estão emprestados.

1. O sistema informa que não há exemplares disponíveis no momento.
2. O sistema oferece ao leitor a opção de entrar na fila de espera.
3. O leitor confirma que deseja entrar na fila.
4. O sistema registra o leitor na fila de espera do livro.
5. O sistema informa a posição do leitor na fila e solicita uma notificação.

**Retorno:** O fluxo retorna ao passo 8 do fluxo principal, apresentando a confirmação da solicitação (entrada na fila de espera, em vez de uma reserva imediata).

### Exceção — Conta do leitor bloqueada

**Quando acontece:** No passo 5 do fluxo principal, quando o sistema identifica que a conta do leitor está bloqueada.

1. O sistema interrompe a solicitação de reserva.
2. O sistema informa que a conta está bloqueada e que não é possível reservar livros.
3. O sistema orienta o leitor a procurar a biblioteca para regularizar a situação.
4. O sistema não registra a reserva nem inclui o leitor na fila de espera.

**Retorno:** O caso de uso é encerrado sem concluir a reserva. O leitor pode tentar novamente depois que a conta for regularizada.

## 5. Observações

O diagrama apresenta a fronteira do sistema, os cinco casos de uso, dois atores principais, um ator secundário (sistema externo) e suas associações. A especificação detalha um dos casos de uso conforme os itens solicitados na atividade.
