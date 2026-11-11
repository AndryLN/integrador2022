# Jogo da Velha da Revolução Francesa — Integrador 2022

Site educativo desenvolvido como **Projeto Integrador 2022** por estudantes do IF Goiano. Ele une um **jogo da velha temático** a conteúdos de apoio sobre a **Revolução Francesa**, para que o jogador aprenda história enquanto se diverte.

🔗 **Acesse online:** https://andryln.github.io/integrador2022/

---

## Funcionalidades

| Página | Arquivo | Descrição |
|---|---|---|
| **Início / Jogo** | `index.html` | Seleção de personagens (Absolutistas = **X**: Luís XVI e Maria Antonieta; Revolucionários = **O**: Robespierre e Danton) e jogo da velha para dois jogadores, com detecção de vencedor, destaque da sequência vencedora e botão **Reiniciar**. O tabuleiro aparece depois que um personagem revolucionário é escolhido. |
| **Guia de personagens** | `pages/guiaperso.html` | Cartões com nome, papel histórico e datas de nascimento e morte de cada personagem, revelados ao passar o mouse. |
| **Guia de personagens (carrossel)** | `pages/guia.html` | Carrossel em CSS puro com as artes dos personagens. É o link "Guia de personagens" da barra de navegação da página inicial. |
| **Revolução Francesa** | `pages/revolucao.html` | Carrossel de 18 páginas ilustradas que contam a história da Revolução Francesa. |
| **Manual de jogo** | `pages/manual.html` | Vídeo tutorial explicando como jogar. |
| **Desenvolvedores** | `pages/desenvolvedores.html` | Cartões com nome e e-mail dos integrantes da equipe. |

Todas as páginas (exceto os carrosséis) compartilham uma barra de navegação fixa no topo.

## Tecnologias

- **HTML5**: estrutura das páginas
- **CSS3**: estilos, animações e carrosséis feitos só com CSS (`input[type=radio]` + seletor `~`)
- **JavaScript (vanilla)**: lógica do jogo da velha (`assets/js/jogo.js`)
- **Bootstrap 5.2.3** (via CDN): usado na página `guiaperso.html`
- **jQuery 1.7.2** (via CDN): incluído na página inicial
- **Google Fonts** (Roboto e DM Sans)
- **GitHub Pages**: hospedagem

Não há etapa de build, gerenciador de pacotes nem back-end: é um site estático.

## Estrutura de diretórios

```
integrador2022/
├── index.html                  # Página inicial: seleção de personagens + jogo da velha
├── README.md
├── pages/                      # Demais páginas do site
│   ├── desenvolvedores.html
│   ├── guia.html               # Carrossel de personagens
│   ├── guiaperso.html          # Guia de personagens com detalhes
│   ├── manual.html
│   └── revolucao.html
└── assets/
    ├── css/                    # Uma folha de estilo por página
    │   ├── desenvolvedores.css
    │   ├── guia.css
    │   ├── guiaper.css
    │   ├── jogo.css            # index.html
    │   ├── manual.css
    │   ├── revolucao.css
    │   └── velha.css           # index.html (tabuleiro + barra de navegação)
    ├── js/
    │   └── jogo.js             # Lógica do jogo da velha e da seleção de personagens
    ├── img/
    │   ├── personagens/        # Retratos e artes dos personagens históricos
    │   ├── desenvolvedores/    # Fotos da equipe (semfoto.png = imagem padrão)
    │   └── revolucao/          # pagina-1.jpg … pagina-18.jpg (carrossel da Revolução)
    └── video/
        └── manualzinho.mp4     # Vídeo do manual de jogo
```

> `index.html` fica na raiz porque é o ponto de entrada usado pelo GitHub Pages.
>
> Em `assets/img/personagens/`, os arquivos `luis-xvi-retrato-callet.jpg`, `maria-antonieta.jpg` e `robespierre.jpg` não são usados por nenhuma página no momento. Eles foram mantidos para preservar todo o material original.

## Instalação e execução

### 1. Clonar o repositório

```bash
git clone https://github.com/AndryLN/integrador2022.git
cd integrador2022
```

### 2. Executar

Como o site é estático, basta abrir o `index.html` no navegador. Para o vídeo e os recursos externos se comportarem como no GitHub Pages, é recomendado usar um servidor local:

```bash
# Com Python 3
python3 -m http.server 8000

# ou com Node.js
npx serve .
```

Depois, acesse **http://localhost:8000** no navegador.

> É necessária conexão com a internet para carregar Bootstrap, jQuery, Google Fonts e a imagem de fundo, que vêm de CDNs externos.

### 3. Publicar (GitHub Pages)

Em **Settings → Pages** no repositório, selecione a branch `main` e a pasta `/ (root)`. O site será publicado em `https://<usuario>.github.io/integrador2022/`.

## Como jogar

1. Na página inicial, escolha os personagens: os **Absolutistas** jogam com **X** e os **Revolucionários** com **O**.
2. Ao escolher um personagem revolucionário (Robespierre ou Danton), o tabuleiro é exibido.
3. Os jogadores alternam as jogadas clicando nas casas; **X** começa.
4. Quem completar uma linha, coluna ou diagonal vence. A sequência vencedora fica destacada.
5. Clique em **Reiniciar** para jogar de novo.

## Equipe

Amanda Neves Liberato · Andrey Loppes Neto · Arthur Lacerda Tristão · Dheniel Rodrigues Luis · Gustavo Antonio Pereira de Morais · Luís Fernando Monteiro · Marcos Filipe Silva · Marcus Vinícius Nunes Silva · Nicoly Soares Qualhate · Samuel Kushi de Paiva · Rennan Fidelis Paim Tavares
