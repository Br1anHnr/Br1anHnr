# LilHog — meu aplicativo de organização financeira

<img src="images/lilhog/icon.png" alt="Ícone do LilHog: um porquinho rosa" width="120" />

Estou desenvolvendo um aplicativo de organização financeira pessoal para iOS, com um assistente de IA para facilitar o registro de movimentações.

## Um pouco da interface

Capturei estas telas na versão web de desenvolvimento, em formato móvel de 390 × 844 pixels. Comecei com o banco vazio e usei uma solicitação fictícia no assistente.

<table>
  <tr>
    <th>Painel financeiro</th>
    <th>Proposta de movimentação</th>
  </tr>
  <tr>
    <td><img src="images/lilhog/painel.jpg" alt="Painel financeiro do LilHog em ambiente local, com valores zerados" width="300" /></td>
    <td><img src="images/lilhog/assistente.jpg" alt="Proposta fictícia de despesa de 25 reais, com os botões Descartar e Confirmar Lançamento" width="300" /></td>
  </tr>
</table>

No exemplo, digitei “Gastei 25 reais no almoço”. Usei a interpretação por regras locais, sem chamar uma API de IA, e deixei a proposta aguardando confirmação.

## A ideia

Quero reunir minhas informações financeiras em uma interface móvel e reduzir o trabalho de preencher cada lançamento manualmente. O assistente recebe uma solicitação em texto e prepara uma proposta que pode ser revisada antes do registro.

## O que estou desenvolvendo

Trabalho na interface, nos dados locais e no assistente financeiro. Organizei o fluxo para que o usuário possa confirmar ou rejeitar cada proposta.

```mermaid
flowchart LR
    A[Solicitação do usuário] --> B[Interpretação]
    B --> C[Proposta de movimentação]
    C --> D[Revisão humana]
    D -->|Confirmar| E[Registro]
    D -->|Rejeitar| F[Descartar]
```

Uso IA para ajudar na interpretação e mantenho os cálculos separados da resposta do modelo. Também tenho um modo de interpretação por regras locais, sem depender de um LLM no dispositivo.

## Como está hoje

O projeto continua em desenvolvimento e mantenho o código privado. Ainda estou validando as integrações online e o comportamento em iOS. Não publiquei uma versão na App Store ou no TestFlight, nem medi resultados de uso por outras pessoas.

## O que quero mostrar a seguir

Quero complementar as capturas com um vídeo do registro de uma despesa, mostrando a confirmação e a atualização do painel. Também pretendo demonstrar a rejeição de uma proposta e validar o fluxo com IA online e em um dispositivo iOS.

[Voltar ao perfil](../README.md)
