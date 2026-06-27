# Cadernos de Estudo

App de estudos com as matérias SQL, Visualização de Dados, Estatística, Power BI e Inteligência Artificial. Cada matéria é organizada por temas, com flashcards e quiz. O SQL ainda tem um modo de prática com um banco SQLite que roda dentro do próprio app.

## O que tem aqui

```
CadernoSQL_App/
  index.html        o app (página única, funciona offline)
  sql-asm.js        motor SQLite usado no modo Praticar
  manifest.json     dados para instalar como app no celular
  icon.png          ícone do app
Cadernos_offline.html   o app inteiro num arquivo só, para abrir em qualquer celular
Caderno_SQL.html        fonte do caderno de SQL
Caderno_SQL.pdf         caderno de SQL para anotar no GoodNotes
Caderno SQL.app         atalho para abrir o app no macOS
```

## Como usar

No computador, abra `CadernoSQL_App/index.html` no navegador.

No celular, salve o `Cadernos_offline.html` no aparelho e abra no Safari (iPhone) ou Chrome (Android). Dá para adicionar à tela inicial como um app. O passo a passo está em `COMO_ABRIR_NO_CELULAR.md`.

Para anotar no iPad, abra o `Caderno_SQL.pdf` no GoodNotes.

No app, o seletor no topo troca de matéria. O progresso de cada matéria fica salvo no navegador do aparelho.

## Regenerar o PDF de SQL

O PDF vem do `Caderno_SQL.html`, gerado com o WeasyPrint:

```bash
pip install weasyprint
python3 -c "from weasyprint import HTML; HTML('Caderno_SQL.html').write_pdf('Caderno_SQL.pdf')"
```

## Crédito

Motor SQL: [sql.js](https://github.com/sql-js/sql.js), o SQLite compilado para JavaScript.
