# Caderno de Estudos — SQL

Caderno de estudos de SQL em dois formatos: um **PDF** para anotar no GoodNotes (iPad) e um **app interativo offline** com navegação por temas, flashcards, quiz e um modo de prática com banco de dados SQLite rodando dentro do próprio app.

O conteúdo é organizado **por temas** (não por ordem de aula). Cada tema mostra, de forma discreta, a data em que foi estudado.

## Estrutura

```
estudos/
├── Caderno_SQL.html        Fonte do caderno (gera o PDF)
├── Caderno_SQL.pdf         PDF pronto para o GoodNotes
├── CadernoSQL_App/
│   ├── index.html          App interativo (página única)
│   └── sql-asm.js          Motor SQLite (sql.js) para o modo Praticar
└── Caderno SQL.app/        Bundle clicável no macOS (abre o app)
```

## Como abrir o app

No Mac, dê dois cliques em `Caderno SQL.app`. Na primeira vez, o macOS pode pedir para clicar com o botão direito e escolher **Abrir** (app não assinado). Como alternativa, abra `CadernoSQL_App/index.html` direto no navegador.

O app funciona **100% offline**. Modos disponíveis:

- **Estudar** — conteúdo por temas, com mapas mentais e exemplos.
- **Flashcards** — perguntas e respostas para revisão.
- **Quiz** — questões de múltipla escolha com correção.
- **Praticar** — escreva consultas SQL reais contra tabelas de exemplo; o app executa e valida o resultado.

O progresso de estudo fica salvo localmente no navegador.

## Como regenerar o PDF

O PDF é gerado a partir de `Caderno_SQL.html` com o WeasyPrint:

```bash
pip install weasyprint
python3 -c "from weasyprint import HTML; HTML('Caderno_SQL.html').write_pdf('Caderno_SQL.pdf')"
```

## Matérias

Cada matéria é um caderno próprio. A primeira é SQL. Visualização de Dados entra como um caderno separado, abrindo no mesmo app.

## Créditos

- Motor SQL: [sql.js](https://github.com/sql-js/sql.js) (SQLite compilado para JavaScript).
