# Tonello Advisory — Site Institucional

Site institucional de página única (one-page) da **Tonello Advisory**, consultoria
em análise financeira, avaliação de ativos e modelagem para projetos de energia e
infraestrutura.

🔗 **Produção:** [www.tonelloadvisory.com.br](https://www.tonelloadvisory.com.br)

---

## Sobre o projeto

Página única, estática e autocontida — sem framework, sem build, sem dependências
de servidor. Todo o site vive em um único arquivo `index.html`, com imagens e
estilos embutidos. A única dependência externa são as fontes do Google, carregadas
via CDN. Funciona offline ao abrir o arquivo diretamente no navegador.

### Seções

1. **Sobre** — trajetória profissional, formação acadêmica e cursos, com link para o LinkedIn
2. **Serviços** — cinco modalidades de engajamento, da modelagem ao suporte pontual
3. **Processo** — as quatro fases da metodologia de análise
4. **Perguntas frequentes** — nove perguntas em formato acordeão
5. **Contato** — e-mail (com cópia rápida) e LinkedIn

---

## Tecnologias

- **HTML5** semântico e **CSS3** (custom properties, grid, flexbox, animações)
- **JavaScript** puro (vanilla) — sem bibliotecas
- Tipografia em **Georgia**
- Acessibilidade: marcação ARIA, navegação por teclado e acordeão em `<details>/<summary>`
  (funciona mesmo sem JavaScript)
- Animações de entrada com *fail-safe* — o conteúdo permanece visível caso o JS não execute

---

## Como executar localmente

Não há etapa de build. Basta abrir o arquivo:

```bash
# clonar o repositório
git clone https://github.com/<usuario>/<repositorio>.git
cd <repositorio>

# abrir no navegador (macOS)
open index.html
# Linux: xdg-open index.html   |   Windows: start index.html
```

Opcional — servir com um servidor local:

```bash
python3 -m http.server 8000
# acesse http://localhost:8000
```

---

## Deploy (GitHub Pages)

O site é publicado via **GitHub Pages** a partir da branch `main`.

1. Em **Settings → Pages**, defina a fonte (*Source*) como branch `main`, pasta `/root`.
2. O arquivo **`CNAME`** aponta o domínio personalizado `www.tonelloadvisory.com.br`.
   Remova-o se não usar domínio próprio.
3. O arquivo **`.nojekyll`** desativa o processamento Jekyll, servindo o HTML como está.
4. Cada `push` para `main` republica o site automaticamente (1–2 minutos).

### Atualizar pelo navegador (sem linha de comando)

Abra `index.html` no GitHub → **Edit** (lápis) ou **Add file → Upload files** para
substituir o arquivo, escreva a mensagem de commit e confirme.

---

## Personalização

Todo o conteúdo e estilo estão em `index.html`:

- **Textos** — edite diretamente o HTML das seções.
- **Cores** — ajuste as *custom properties* em `:root` (ex.: `--ink`, `--paper`, `--mist`).
- **Imagens** — estão embutidas em base64; substitua os respectivos `data:` URIs.

---

## Estrutura

```
.
├── index.html      # site completo (HTML + CSS + JS + imagens embutidas)
├── CNAME           # domínio personalizado do GitHub Pages
├── .nojekyll       # desativa o Jekyll no GitHub Pages
└── README.md       # este arquivo
```

---

## Licença

© 2026 Tonello Advisory. Todos os direitos reservados.
