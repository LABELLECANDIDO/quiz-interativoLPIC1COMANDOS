# ⌨️ Quiz LPIC-101 — Comandos & Caminhos

Quiz interativo para treinar as questões da certificação **LPIC-101** em que a resposta precisa ser **digitada**: um comando ou um caminho exato. Não há alternativas A/B/C/D/E.

Todo o projeto está em um único arquivo HTML, sem dependências, sem build e sem servidor.

## 🚀 Como usar

1. Baixe ou clone este repositório.
2. Abra o arquivo [`lpic101-comandos.html`](lpic101-comandos.html) em qualquer navegador moderno.
3. Escolha um modo de treino e comece a digitar.

> Funciona offline. O progresso fica salvo no `localStorage` do navegador (chave `lpic101_cmd_v1`).

## 🎮 Modos de treino

| Modo | Descrição |
|------|-----------|
| 🎴 **Flashcard** *(recomendado)* | As questões se repetem em ordem aleatória até você acertar **todas**. Ideal para memorizar. |
| 🎲 **Aleatório (1x)** | Passa por todas as questões uma única vez, em ordem embaralhada, como um simulado. |
| 📋 **Sequencial** | Percorre as questões na ordem original. Útil para revisar com calma. |

## ✨ Funcionalidades

- **Resposta digitada:** digite o comando ou caminho e pressione **Enter**.
- **Correção flexível:** não diferencia maiúsculas de minúsculas, ignora espaços extras e aceita caminhos com ou sem barra final (`/usr/local/bin` = `/usr/local/bin/`).
- **Respostas alternativas:** algumas questões aceitam mais de uma resposta válida (ex.: `/proc/mounts` ou `/proc/self/mounts`).
- **Feedback imediato:** quando você acerta, o quiz avança sozinho. Quando erra, ele mostra a resposta correta e uma explicação, e você clica em "Próxima →".
- **Estatísticas em tempo real:** respondidas, acertos, erros, aproveitamento (%) e questões restantes, com barra de progresso.
- **Histórico:** mostra as últimas 8 respostas. Use o botão 📜 para exibir ou ocultar.
- **Resumo final:** classificação do desempenho e lista das questões em que você mais errou.
- **Progresso persistente:** você pode fechar a aba e continuar depois.

## 📚 Conteúdo

São 11 questões de dois tipos:

- **COMANDO:** `jobs`, `nice`, `renice`, `watch`, `df`, `updatedb`
- **CAMINHO:** `/proc/cmdline`, `/proc/mounts`, `/etc/inittab`, `/etc/yum.repos.d/`, `/usr/local/bin/`

Cada questão traz uma explicação curta do comando ou arquivo.

## 🛠️ Adicionando questões

As questões ficam no array `Q`, dentro da tag `<script>` do HTML:

```js
{
  q: `Texto da pergunta (aceita <code>HTML</code>)`,
  c: "resposta-padrao",
  aliases: ["resposta-alternativa"], // opcional
  kind: "cmd",                        // "cmd" ou "path"
  e: `Explicação exibida após responder`
}
```

- `kind: "path"` ativa a tolerância à barra final.
- O total de questões é calculado automaticamente. Se você mudar a quantidade, atualize também os textos fixos que citam "11 questões" no HTML.

## 🧰 Tecnologias

- HTML5, CSS3 e JavaScript puro (vanilla)
- `localStorage` para salvar o progresso

## 📄 Licença

Projeto de estudo para uso pessoal e educacional.
