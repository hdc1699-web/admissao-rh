# Backlog — ideias guardadas

Lugar pra anotar o que decidimos **adiar** de propósito, pra não atrapalhar a fase atual.
Nada aqui se perde; cada item volta na fase certa do roadmap.

## Automação (Fase 4)
- Coleta dos dados do candidato via formulário externo (Google Sheets / WhatsApp) que
  retorna JSON e alimenta o banco automaticamente. Gatilho cogitado: nome+sobrenome ou ID gerado.
- Mesma ideia para os documentos do candidato.
- Disparo automático de e-mail a cada mudança de status (registro corporativo).
- Disparo de WhatsApp para o colaborador com os exames agendados.

## Comportamento (JavaScript) pendente
- Na tela da Medicina, agendamento: ao confirmar, o exame agendado ganha um **✓** de
  confirmação (o aparecer/ocultar dos campos por exame já foi implementado).
- Na tela da Medicina, ação final: **APTO** e **INAPTO-definitivo** -> "Finalizar processo"
  (notifica Filial, RH e candidato; só muda o texto do aviso). Exceção: **INAPTO + refazer=sim**
  NÃO finaliza, volta para o agendamento (loop). A ação/botão muda conforme o caso (JS).

## Sementes de banco de dados (Fase 1 — modelagem)
- A tela revelou que "Funcionários da filial" é uma informação real e reutilizada
  (alimenta tanto "vagas disponíveis" quanto a lista "Por quem?"). Vira tabela.
- A lista de campos se dividiu naturalmente em **Solicitação** e **Candidato** -> duas entidades.

## Admin e controle de acesso (Fase 3)
- Painel **admin** (operado pelo Henrique) para cadastrar setores, funções e filiais,
  e vincular cada usuário ao seu setor/filial.
- Com isso o usuário **não seleciona setor manualmente** — o sistema já sabe pelo login,
  reduzindo erro de digitação e evitando que um setor enxergue/atue em outro (autorização).
