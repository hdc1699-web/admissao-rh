# Backlog — ideias guardadas

Lugar pra anotar o que decidimos **adiar** de propósito, pra não atrapalhar a fase atual.
Nada aqui se perde; cada item volta na fase certa do roadmap.

## Automação (Fase 4)
- Coleta dos dados do candidato via formulário externo (Google Sheets / WhatsApp) que
  retorna JSON e alimenta o banco automaticamente. Gatilho cogitado: nome+sobrenome ou ID gerado.
- Mesma ideia para os documentos do candidato.
- Disparo automático de e-mail a cada mudança de status (registro corporativo).
- Disparo de WhatsApp para o colaborador com os exames agendados.

## Primeira missão de JavaScript (camada de comportamento)
- Na tela de Solicitação de Pessoal: o campo **"Por quem?"** deve aparecer **somente**
  quando o tipo de contratação for **"Substituição"**. Hoje ele fica sempre visível.

## Sementes de banco de dados (Fase 1 — modelagem)
- A tela revelou que "Funcionários da filial" é uma informação real e reutilizada
  (alimenta tanto "vagas disponíveis" quanto a lista "Por quem?"). Vira tabela.
- A lista de campos se dividiu naturalmente em **Solicitação** e **Candidato** -> duas entidades.
