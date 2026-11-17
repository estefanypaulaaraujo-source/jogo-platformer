# Platformer – Desafio Final

Protótipo de jogo 2D de plataforma, feito como Tech Test do curso de Lógica Computacional.

**Jogar online:** https://estefanypaulaaraujo-source.github.io/jogo-platformer/

**Autor(a):** [seu nome]

## Como jogar

| Ação | Teclas |
|---|---|
| Andar | Setas ← → ou A / D |
| Pular | Espaço, ↑ ou W |

No celular, use os botões na tela.

Colete todas as moedas da fase para abrir a porta (ela fica verde) e encoste nela para passar para a próxima fase. Se cair no buraco, você perde uma vida. São 3 vidas no total.

## Fases

| Fase | Meta | Desafio |
|---|---|---|
| 1 | 5 moedas | Plataformas simples |
| 2 | 7 moedas | Buracos no chão |
| 3 | 9 moedas | Plataforma móvel |

A fase 2 só é liberada depois da fase 1, e a fase 3 só depois da fase 2.

## Conceitos de lógica aplicados

- **Variáveis e tipos de dados (Módulo 3):** `nomeJogador` (texto), `vidas` e `moedas` (números inteiros), `venceu` (booleano) e `estado` (texto).
- **Condicionais SE...SENAO (Módulo 4):** a porta só leva à próxima fase se `moedas >= meta`. Quando as vidas chegam a zero, o jogo termina; senão, a fase recomeça.
- **Laços de repetição (Módulo 5):** o laço principal atualiza o jogo 60 vezes por segundo, e laços `for` movem as plataformas, checam colisões e coletam moedas.
- **Vetores (Módulo 6):** o vetor `FASES` guarda as plataformas, as moedas e a meta de cada fase.
- **Funções (Módulos 7 e 8):** o código é dividido em funções como `carregarFase()`, `atualizar()`, `desenhar()`, `perderVida()` e `proximaFase()`.

## Decisões do projeto

- Usei HTML, CSS e JavaScript em um único arquivo, para o jogo rodar direto no navegador.
- Guardei os dados das fases em um vetor, para adicionar uma fase nova sem mexer na lógica do jogo.
- O contador de moedas volta a zero a cada fase, para cada fase ter o seu próprio desafio.
- As plataformas só bloqueiam por cima, o que deixa a colisão mais simples.
