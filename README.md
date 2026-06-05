# Livro Fotográfico sobre Vendas Novas — Dossier de Patrocínio

Página única (Single Page Portfolio) que funciona como **dossier de patrocínio digital** do livro
de fotografia documental e urbanística sobre Vendas Novas, por **João Cruz Fialho**.

- **Tecnologia:** HTML5 + Tailwind CSS (Play CDN) + JavaScript vanilla. **Sem build step.**
- **Ficheiro principal:** [`index.html`](index.html) — é só abrir no browser.

---

## Como ver localmente

Faz duplo-clique em `index.html`, ou serve a pasta:

```powershell
# opcional, para testar o botão de PDF e o lightbox em condições reais
npx serve .
```

## Como publicar (escolhe uma)

**Vercel** (recomendado, igual aos teus outros projetos):
```powershell
cd "D:\IA\LIVRO-VENDAS-NOVAS"
npx vercel --prod --yes
```

**Netlify Drop:** arrasta a pasta para https://app.netlify.com/drop

**GitHub Pages:** faz push da pasta para um repositório e ativa Pages no branch `main`.

---

## O que personalizar

### 1. As fotografias
Já estão integradas as tuas fotos reais (pasta `assets/`): a capa do hero é
`Capa_PaginaAbertura_PalacioPassagens.jpg` e a galeria usa as 9 séries (Mercado, Igreja do Quartel,
Avenida sob Chuva, RA5 Nocturna, Moinho de Vento, Jardim Público, Rotunda do Obus, Chafariz e
Panorâmica). Cada foto entra **duas vezes** no `index.html`:
- `src="..."` → versão pequena (~1500px) usada na grelha;
- `data-full="..."` → versão grande usada no lightbox em ecrã inteiro.

Para trocar/adicionar uma foto, edita esses dois atributos na `<figure class="gallery-fig">`
correspondente. As proporções (`aspect-[...]`) de cada tile foram escolhidas próximas da proporção
nativa da foto para evitar cortes; se mudares uma foto por outra com proporção muito diferente,
ajusta o `aspect-[...]` dessa figura.

### 2. O dossier em PDF
O botão **"Descarregar Dossier (PDF)"** procura o ficheiro `dossier-vendas-novas.pdf` nesta pasta.
- Coloca lá o teu PDF com esse nome e o download passa a funcionar.
- Enquanto o ficheiro não existir, o botão **imprime a própria página** como alternativa.

### 3. Contactos e redes sociais
No fim do `index.html` (secção *Contacto*):
- Email `joaofialho.jf@gmail.com` e telemóvel `+351 960 052 973` já estão preenchidos — confirma/edita.
- Os links de **Instagram / Facebook / LinkedIn** estão como `#` — mete os teus URLs.

### 4. Cores e tipografia
Estão centralizadas no `tailwind.config` dentro do `<head>` (cores `ink`, `graphite`, `navy`, `mist`…
e as fontes `display`/`sans`). Muda aí e aplica-se ao site todo.

### 5. Textos e preços
Conceito, escalões (Bronze 100€ · Prata 250€ · Ouro 500€ · Platina 1000€) e contrapartidas estão em
texto normal no `index.html` — edita à vontade.
