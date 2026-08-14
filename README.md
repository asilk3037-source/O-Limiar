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
- **🎲 Rolar Dados** — rolador do Sistema ARTEFATO completo: monta o pool (Atributo + Perícia + modificador), converte dados em Dados de Ruído conforme o Grau de Assimilação, calcula Êxitos/Sombras/Ressonância, classifica o resultado (Êxito, Êxito Sujo, Custo, Colapso), rola a tabela de Custo (d6) e a tabela de Artefatos (2d6, as 36 completas) automaticamente quando acionadas, e trata a regra de "pool zerado → rola 2 e conta o pior". Mantém histórico da sessão.
- **📋 Ficha de Personagem** — ficha completa (identidade, 4 atributos, 20 perícias, as quatro trilhas — Desgaste, Desalinho, Assimilação, Impressão —, três Âncoras e três Protocolos), salva sozinha no navegador (`localStorage`), com exportação/importação em `.json` para backup. Cada Perícia tem um botão "🎲 Rolar" que já leva a rolagem pronta pra aba de dados.
- **🧟 Bestiário** e **🗺️ Domínios** — galerias de cards navegáveis das 42 entidades e dos 24 domínios, com busca e (no Bestiário) filtro por tipo de bloqueio, com cor própria por tipo. Os dados são lidos direto do texto do livro em tempo real — não há uma cópia separada para manter sincronizada. Clicar num card abre a ficha completa na aba O Livro, com destaque visual no trecho.

### Identidade visual

- Textura sutil de grão/papel no fundo, linhas diagonais na capa, número gigante ("fantasma") atrás do título de cada parte do livro
- Tabelas longas ganham rolagem horizontal própria em telas estreitas, sem nunca quebrar o layout da página
- Botão flutuante de voltar ao topo em capítulos longos
- Bandeja de dados com fundo "de mesa" e dados com relevo 3D; cards com barra âmbar no topo
- Botão do menu no celular corrigido — antes ficava escuro sobre fundo escuro na capa e passava despercebido; agora é âmbar, com contraste alto e um pulso sutil ao carregar a página

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
