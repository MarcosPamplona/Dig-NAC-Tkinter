# Dig-NAC-Tkinter
Automação Inserção de Pedido Compra

Este código é uma automação de digitação baseada em Excel, com interface gráfica em Tkinter, criada para lançar pedidos automaticamente em um sistema por meio de simulação de cliques e digitação do mouse/teclado (PyAutoGUI).

Ele lê dados de uma planilha Excel e preenche campos de um sistema externo de forma repetitiva e controlada, reduzindo trabalho manual.

1 Interface Gráfica (Tkinter)

Permite ao usuário:

Selecionar um arquivo Excel
Definir coluna inicial e final da planilha
Escolher se o preço será digitado ou não
Iniciar ou cancelar o processo
Mostra um log em tempo real do que está sendo executado.

2 Leitura de Dados (Pandas)

Abre o Excel selecionado.

Utiliza:

Coluna “Código” código do item

Coluna “Valor” preço (opcional)

Outras colunas quantidade por loja


Percorre um intervalo de colunas definido pelo usuário (lojas).

3 Automação de Digitação (PyAutoGUI)

Simula:

Cliques em posições fixas da tela

Digitação de textos e números


Preenche automaticamente:

Loja

TOP

Parceiro

Tipo de negociação

Previsão de entrega

Comprador

Itens do pedido (código, quantidade e preço)



As posições (x, y) são fixas, então o sistema depende da tela, resolução e layout exatos.

4 Controle de Fluxo

Suporta:

Pausa automática entre ações (sleep)

Cancelamento do processo em tempo real


Usa threads para manter a interface responsiva enquanto o robô roda.

5 Regras de Inserção de Itens

Insere até 10 itens por bloco.

Após esse limite, muda para outra área da tela (campos “limite”).

Cada item:

Digita código

Digita quantidade

(Opcional) digita preço

Confirma e adiciona novo item

Finalização

Ao terminar:

Emite um beep sonoro

Exibe mensagem de sucesso

Registra no log
