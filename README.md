# Quiz de Estudo

Quiz web estático para estudar para a prova. As questões ficam em `QUESTOES.json`
e são exibidas por `index.html` (HTML + JS puro, sem dependências).

## Como usar
- Modo **Embaralhado** ou **Ordem original**
- Feedback imediato (verde = certo, vermelho = errado) + comentário da resposta
- Barra de progresso e tela de resultado com porcentagem

## Formato das questões (`QUESTOES.json`)
```json
[
  {
    "numero_questao": "1",
    "enunciado": "Texto da pergunta",
    "instrucao": "Selecione a resposta:",
    "alternativas": [
      { "letra": "A", "texto": "...", "correta": false, "comentario_da_resposta": "..." },
      { "letra": "B", "texto": "...", "correta": true,  "comentario_da_resposta": "..." }
    ]
  }
]
```

## Publicar no GitHub Pages
1. Crie um repositório em https://github.com/new (ex.: `quiz-prova`), público.
2. Envie os arquivos (no terminal, dentro desta pasta):
   ```bash
   git init
   git add .
   git commit -m "Quiz de estudo"
   git branch -M main
   git remote add origin https://github.com/SEU-USUARIO/quiz-prova.git
   git push -u origin main
   ```
3. No repositório: **Settings > Pages > Branch: `main` / `/root` > Save**.
4. Em ~1 min o link fica disponível em `https://SEU-USUARIO.github.io/quiz-prova/`.

## Testar localmente
O navegador bloqueia o JSON via `file://`. Rode um servidor local:
```bash
npx http-server -p 8000
```
e acesse `http://localhost:8000`.
