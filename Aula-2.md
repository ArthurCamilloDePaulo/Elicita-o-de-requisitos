Acompanhamento de pedido para o cliente

Historia:
Como cliente do aplicativo, eu quero acompanhar o status do meu pedido em tempo real após a compra, para que eu saiba exatamente quando minha refeição será entregue.

Critério 1: Atualização de status da preparação
Dado que eu fiz um pedido com sucesso e estou na tela de detalhes do pedido,
Quando o restaurante aceitar e me avisar que começou a preparar,
Então a tela deve atualizar o status para Em preparação.

Critério 2: Visualização do entregador a caminho
Dado que o pedido foi coletado pelo entregador,
Quando o status mudar para Saiu para entrega,
Então o aplicativo deve exibir o nome do entregador e a estimativa de chegada.

Critério 3: Notificação de chegada
Dado que o entregador chegou ao meu endereço,
Quando ele marcar no aplicativo dele que chegou,
Então eu devo receber uma notificação no meu celular.

HISTORIA 2: Indisponibilidade de item para o restaurante

Historia:
Como gestor do restaurante, eu quero pausar um item do meu cardápio no painel, para evitar que clientes comprem pratos com ingredientes esgotados.

Critério 1: Desativação imediata no cardápio
Dado que estou logado no painel do restaurante na lista de produtos,
Quando eu desativar o item Hambúrguer X,
Então esse item deve sumir imediatamente do aplicativo para os clientes.

Critério 2: Tentativa de compra de item desativado
Dado que um cliente adicionou o item ao carrinho antes dele ser desativado,
Quando o cliente tentar finalizar a compra,
Então o aplicativo deve avisar que o item ficou indisponível e pedir para remover.

Critério 3: Reativação do item
Dado que o estoque do ingrediente foi reposto,
Quando eu ativar o item novamente no painel,
Então o produto deve voltar a aparecer para compra no aplicativo.

HISTORIA 3: Reportar problema para o entregador

Historia:
Como entregador parceiro, eu quero reportar um imprevisto durante o percurso, para que o suporte tome as providencias e o cliente seja avisado.

Critério 1: Reportar cliente ausente
Dado que estou no endereço de entrega e aguardei 5 minutos,
Quando eu clicar em reportar problema e escolher Cliente não atende,
Então o sistema deve enviar um alerta para o celular do cliente.

Critério 2: Reportar acidente ou quebra do veiculo
Dado que tive um problema no veiculo durante o percurso,
Quando eu selecionar Problema no veiculo e confirmar,
Então o suporte deve ser acionado para falar comigo e o pedido ser reatribuído.

Critério 3: Confirmação de recebimento pelo suporte
Dado que reportei um problema no aplicativo,
Quando o envio for concluído,
Então a tela deve exibir uma mensagem confirmando o recebimento e os próximos passos.

PRIORIZAÇÃO MOSCOW

Must Have: Acompanhar pedido em tempo real. Justificativa: Funcionalidade básica de qualquer aplicativo de entrega. Sem isso o cliente fica sem informações.

Should Have: Gestão de indisponibilidade de itens. Justificativa: Importante para o restaurante não vender o que não tem e evitar cancelamentos após o pagamento.

Could Have: Reportar problemas na entrega. Justificativa: Útil para casos de exceção, mas no inicio pode ser resolvido com um canal direto de atendimento ou suporte.

Wont Have: Automação de reembolso imediato em casos de erro. Justificativa: Casos mais complexos de suporte serão resolvidos manualmente pela equipe nesta primeira versão.
