# O Limiar

**LIMIAR** — horror de estranhamento institucional, sistema **ARTEFATO**.

Site oficial da campanha: o livro completo (Volumes 1 e 2), em uma única página navegável.

## O que tem no site

O `index.html` reúne todo o material de desenvolvimento do LIMIAR em 18 partes, com menu lateral fixo e busca em texto completo:

- **00.** Roteiro Mestre de Produção
- **I.** O que é o Limiar — As Doze Leis
- **II.** Cosmologia
- **III.** Sistema ARTEFATO — Como se joga
- **IV.** Guia do Zelador de Mesa
- **V.** Personagens e Modos de Jogo
- **VI.** Os 24 Domínios
- **VII.** Bestiário — 42 Entidades
- **VIII.** Objetos e Documentos
- **IX.** Facções
- **X.** Primeira Noite
- **XI.** Campanhas Intermediárias
- **XII.** O Casulo
- **XIII.** Aparato
- **XIV–XV.** Kits de Playtest (P1 a P5)
- **XVI–XVII.** Prompts de imagem (Bestiário e Domínios)

### Recursos do site

- Menu lateral com destaque automático da seção visível (scrollspy)
- Menu retrátil no celular
- **Busca em texto completo** (caixa "Buscar no livro…" na barra lateral) com navegação entre resultados (Enter / Shift+Enter ou botões ◀ ▶)
- Downloads do material-fonte original (`.docx` e `.xlsx`) direto pela barra lateral

## Estrutura do repositório

```
index.html          → o site (página única, sem dependências externas)
fonte/
  LIMIAR_Obra_Completa.docx       → documento-fonte completo
  LIMIAR_Registro_Canonico.xlsx   → planilha de controle de cânone (domínios, entidades, facções, NPCs etc.)
```

## Como visualizar localmente

Não precisa de build nem de servidor — basta abrir o `index.html` no navegador. Se preferir servir localmente:

```bash
python3 -m http.server 8000
# depois abra http://localhost:8000
```

## Como publicar (GitHub Pages)

1. No repositório, vá em **Settings → Pages**
2. Em "Build and deployment", escolha **Deploy from a branch**
3. Selecione a branch `main` e a pasta `/ (root)`
4. Salve — o site fica disponível em `https://<usuario>.github.io/O-Limiar/`

O arquivo `.nojekyll` já está incluso para evitar que o GitHub processe o site como Jekyll.
