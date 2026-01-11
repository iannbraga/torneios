# ♟️ Gerenciador de Torneios de Xadrez – Sistema Suíço

Este projeto é um **gerenciador simples e funcional de torneios de xadrez**, desenvolvido em **HTML + Vue 3**, com foco em **torneios amadores reais**, seguindo os princípios do **Sistema Suíço** utilizado pela FIDE.

O sistema foi pensado para ser:
- Fácil de usar
- Executado localmente (sem servidor)
- Didático
- Próximo da prática real de torneios presenciais

---

## 📌 Funcionalidades

### ✔ Estrutura do Torneio
- Definição de:
  - Nome do torneio
  - Ritmo de jogo (Clássicas / Rápidas / Blitz)
  - Número de rodadas
- Cadastro de jogadores com **rating inicial**

### ✔ Sistema Suíço
- **Primeira rodada**:
  - Emparceiramento por **rating**
  - Jogadores mais fortes enfrentam jogadores mais próximos
- **Rodadas seguintes**:
  - Emparceiramento por **pontuação**
  - Agrupamento por score
- **Bye automático**:
  - Aplicado quando há número ímpar de jogadores
  - Vale **1 ponto**
- Evita repetições sempre que possível

### ✔ Controle de cores
- Contagem de partidas de **brancas e pretas**
- Balanceamento básico ao longo do torneio

### ✔ Classificação
- Ordenação por:
  1. Pontos
  2. Buchholz
- Exibe:
  - Rating
  - Pontuação
  - Buchholz
  - Número de partidas de brancas/pretas

### ✔ Exportação
- Exportação da classificação final em **CSV**
- Compatível com Excel, LibreOffice e Google Sheets

---

## 📝 Formato de Entrada dos Jogadores

No campo **Participantes**, utilize **uma linha por jogador**, no formato:

```
Nome, Rating
```

### Exemplo:
```
Iann, 850
Cyntia, 430
Ludik, 806
Gustavo Parro, 769
Sairow, 1090
Lucas,
Alex,
Nilson,
Antonio Potter,
Kalil, 625
Camila,
Maria Clara,
```

### Observações:
- Rating é **opcional**
- Se não informado, o rating será considerado **0**
- Não há distinção de categorias ou sexo

---

## 🧮 Sistema de Pontuação

- Vitória: **1 ponto**
- Empate: **0,5 ponto**
- Derrota: **0 ponto**
- Bye: **1 ponto**

---

## 📊 Desempate – Buchholz

O **Buchholz** é calculado automaticamente como:

> Soma dos pontos de todos os adversários enfrentados pelo jogador

Este é um dos critérios de desempate mais comuns em torneios suíços amadores.

---

## 🚀 Como Usar

1. https://iannbraga.github.io/torneios/
2. Abra o arquivo em qualquer navegador moderno (Chrome, Edge, Firefox).
3. Preencha:
- Nome do torneio
- Número de rodadas
- Lista de participantes
4. Clique em **Iniciar**
5. Após inserir os resultados de cada rodada, clique em **Gerar próxima rodada**
6. Ao final, exporte a classificação em CSV se desejar

Não é necessário:
- Internet
- Servidor
- Banco de dados

---

## ⚠️ Limitações Conhecidas

Este sistema **não implementa todas as regras formais da FIDE**, como:
- Dutch System completo
- Regras avançadas de flutuação
- Controle rígido de cores
- Rating performance
- Emparceiramento 1×N oficial completo

Ele é ideal para:
- Clubes
- Escolas
- Eventos locais
- Torneios rápidos e blitz
- Uso educacional

---

## Regras Básicas do Torneio de Xadrez*

*Movimentos especiais*
* *Roque*: movimento conjunto do *rei com a torre*. Só é válido se:
  * Rei e torre não tiverem se movido;
  * Não houver peças entre eles;
  * O rei não estiver em xeque, nem passar ou terminar em xeque;
  * *O rei deve ser tocado primeiro*. Se tocar primeiro na torre, o roque é inválido.
* *En passant*: captura especial de peão, válida *apenas no lance imediatamente seguinte* ao avanço de duas casas do peão adversário.
* *Promoção*: ao chegar à última fileira, o peão deve ser promovido a *dama, torre, bispo ou cavalo*.


*Empates*
A partida é considerada empatada nos seguintes casos:

* *Rei contra rei*;
* *Rei e bispo contra rei*;
* *Rei e cavalo contra rei*;
* *Afogamento* (jogador sem lances legais e não em xeque);
* *Repetição da mesma posição 3 vezes*;
* *Acordo entre os jogadores*.
*(Regra dos 50 lances não será aplicada neste torneio.)*


*Relógio e conduta*
* O jogador deve *mover a peça e apertar o relógio com a mesma mão*.
* Se uma peça cair:
  * Arrume as peças primeiro;
  * Aperte o relógio depois.
* Em caso de peças derrubadas nos apuros de tempo:
  * A situação será resolvida *no bom senso* entre os jogadores;
  * Se necessário, a partida pode ser retomada da posição anterior aproximada ou aplicada *compensação de tempo*.


*Lances ilegais*
* Lances ilegais não encerram a partida automaticamente.
* Penalização padrão: *acréscimo de 5 segundos no relógio do adversário*.
* Jogadores que estiverem de fora da rodada podem atuar como *auxiliares/juízes informais*.


*Sistema do torneio*
* Sistema *Suíço*.
* A *primeira rodada* pode ser organizada com base no *rating de partidas rápidas do Chess.com*, para evitar confrontos muito desequilibrados logo no início.

---

## 🔧 Tecnologias Utilizadas

- HTML5
- JavaScript (ES6)
- Vue.js 3 (via CDN)
- Bootstrap 5

---

## 🧠 Próximas Evoluções (opcionais)

- Sistema **1×N FIDE**
- Performance Rating
- Sonneborn-Berger
- Salvamento automático (localStorage)
- Exportação compatível com Swiss-Manager / Vega
- Versão PWA (offline)

---

## 📄 Licença

Projeto livre para uso educacional e comunitário.  
Adaptações e melhorias são bem-vindas.

---

♟️ **Projeto focado em simplicidade, clareza e prática real de torneios de xadrez.**
