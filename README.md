# Admissão RH — COOASGO

Sistema web para gerir o **processo admissional** da cooperativa COOASGO, da solicitação de vaga pela filial até a liberação do colaborador apto — passando pelo RH e pela Medicina do Trabalho.

> ⚠️ **Projeto de estudo, em desenvolvimento.** No momento é um protótipo de front-end (maquete navegável). O back-end e o banco de dados ainda serão construídos.

---

## Por que este projeto existe

Hoje o processo de admissão da cooperativa vive espalhado em **e-mails, WhatsApp e documentos Word preenchidos à mão**. Isso gera dois problemas reais:

1. **Ruído de comunicação** entre Filial, RH e Medicina do Trabalho — se alguém esquece de avisar a próxima etapa, o processo trava.
2. **Trabalho manual repetitivo** — agendar exames trocando nome e data em modelos prontos, lembrar de contatar a Medicina, etc.

O objetivo do sistema é **dar visibilidade ao processo**, **automatizar as comunicações** e **eliminar o retrabalho**, para que ninguém dependa da memória de alguém para a admissão andar.

## O que o sistema faz

- Abertura de **Solicitação de Pessoal** pela filial (nova contratação ou substituição).
- **Caixa de entrada** para RH e Medicina acompanharem o que precisa de ação.
- Controle do **status do processo** como uma máquina de estados (da solicitação à conclusão).
- Registro do **resultado médico** (Apto / Inapto, com refazer ou encerrar).
- Acesso por **perfil** (Filial, RH, Medicina do Trabalho).
- *(Planejado)* Disparo automático de **e-mail** a cada etapa e **WhatsApp** de agendamento ao colaborador.

## Como funciona o fluxo

```
Filial abre solicitação → RH avalia → Medicina agenda exames → resultado médico
                                                                      │
                                              Apto → processo concluído (contratos)
                                              Inapto → refazer exames ou encerrar
```

Atores: **Filial** (cria), **RH** (avalia e encaminha), **Medicina do Trabalho** (agenda e registra resultado), **Colaborador** (recebe as comunicações).

## Tecnologias

| Camada | Hoje | Planejado |
|--------|------|-----------|
| Front-end | HTML, CSS, JavaScript | refino de UX |
| Back-end | — | Java + Spring Boot, API REST |
| Banco | — | PostgreSQL ou MySQL |
| Integrações | — | E-mail (SMTP), WhatsApp |

## Estrutura

```
frontend/   → telas (HTML), css/ (estilo único) e img/ (logo, fundo)
docs/       → BACKLOG.md (ideias e melhorias adiadas)
```

## Como rodar

Por enquanto é estático, sem instalação: abra **`frontend/login.html`** no navegador. Escolha um perfil no login para navegar pelo fluxo correspondente.

## Status e roadmap

- ✅ **Fase 0 — Maquete:** telas e navegação do fluxo completo (atual).
- ⬜ **Fase 1 — Modelagem:** entidades e banco de dados.
- ⬜ **Fase 2 — Back-end:** API, CRUD e persistência.
- ⬜ **Fase 3 — Automação e acesso:** e-mail/WhatsApp, autenticação e admin.

## Visão futura

- **Processo demissional** na mesma aplicação. O fluxo de desligamento é muito parecido com o de admissão — muda a documentação e a quantidade de exames (exame demissional) — então reaproveita a mesma estrutura e máquina de estados.
- **Dashboard em Power BI** na conta admin, para acompanhar e controlar as contratações (e futuramente as demissões) por indicadores.

## Autor

**Henrique Duarte** — Facilitador de TI na COOASGO e estudante de Análise e Desenvolvimento de Sistemas. Projeto desenvolvido como aprendizado, a partir de uma dor real da cooperativa.
