# 🧱 LEGO World Map Builder

Editor visual para criar padrões customizados do set **LEGO World Map (#31203)** — uma página única, sem dependências, que roda no navegador.

🌍 **Demo:** https://ppoffal.github.io/lego-map-builder/

![Built with HTML/CSS/JS](https://img.shields.io/badge/stack-vanilla%20HTML%2FJS-orange) ![No build](https://img.shields.io/badge/build-none-green) ![Single file](https://img.shields.io/badge/files-1-blue)

---

## ✨ Funcionalidades

- **Grade configurável** mapeada nas **placas físicas 16×16** do set, com bordas destacadas e labels (A1, B3, …) para guiar a montagem
- **Upload de imagem-guia** com opacidade ajustável — funciona como referência por baixo das peças
- **✨ Sugestão automática** — gera o padrão inteiro a partir da imagem, mapeando cada célula para a cor LEGO mais próxima (distância perceptual *redmean*)
- **3 tipos de peça 1×1**: com encaixe (stud), lisa (tile) e com furo (hole), renderizadas com efeito 3D
- **25 cores da paleta LEGO** mais usadas em sets como o World Map e o LEGO Art
- **Ferramentas**: pintar, apagar, balde (flood-fill), conta-gotas
- **Contagem de peças** em tempo real, separada por cor + tipo, tanto global quanto **por placa**
- **🔒 Modo Montagem** — switch que bloqueia a edição e abre cada placa em **modal grande (≥900px)** com numeração de linha/coluna para guiar a montagem física
- **Undo (Ctrl+Z)** com histórico de 50 passos — agrupando traços inteiros
- **Exportar PNG** em alta resolução, **salvar/carregar JSON** do padrão

## 🎯 Como usar

1. Suba uma foto de referência (`📁 Upload`)
2. Clique em **✨ Sugerir** para gerar o padrão automaticamente
3. Refine célula a célula com as ferramentas
4. Quando terminar, ative **🔒 Modo Montagem** e clique em cada placa para ver a versão grande durante a montagem física

## ⌨️ Atalhos de teclado

| Tecla | Ação |
|-------|------|
| `P` / `B` | Pintar |
| `E` | Apagar |
| `F` | Preencher (balde) |
| `I` | Conta-gotas |
| `1` `2` `3` | Tipo de peça: encaixe / lisa / furo |
| `+` / `-` | Zoom |
| `Ctrl` + `Z` | Desfazer |
| `Esc` | Fechar modal (no modo montagem) |
| `←` `→` | Navegar entre placas (no modal) |

## 🚀 Rodar localmente

É só um arquivo HTML — não precisa de servidor nem build:

```bash
git clone https://github.com/ppoffal/lego-map-builder.git
cd lego-map-builder
# Abra index.html no navegador
```

Ou sirva localmente:

```bash
python3 -m http.server 8000
# http://localhost:8000
```

## 🛠 Stack

Vanilla **HTML + CSS + JS** num único `index.html`. Canvas API para renderização. Zero dependências, zero pipeline.
