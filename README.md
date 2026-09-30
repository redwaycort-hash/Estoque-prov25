# Estoque Pro V21 — Render

Pacote server-side para colocar o Estoque Pro em produção no Render. Inclui banco SQLite, autenticação, perfis, auditoria, reservas, fichas, assinatura de saída, IA/comando de voz e a calculadora V21 com os cálculos de produção.

## Render
1. Envie o conteúdo deste pacote para um repositório GitHub.
2. No Render, crie um Web Service usando esse repositório ou use o `render.yaml` como Blueprint.
3. O serviço usa Docker e expõe a porta definida por `PORT`.
4. Configure os secrets `ADMIN_PASSWORD` e `OPENAI_API_KEY` no Render.
5. O banco fica em `/app/data/estoque.db`; o `render.yaml` configura um Persistent Disk nesse caminho.

## Login
Usuário inicial: `REDWAY_MASTER`
Senha: a definida por `ADMIN_PASSWORD` no Render.

Não coloque senha real ou chave da OpenAI no GitHub.

## Calculadora V21
- Cós: 1,3 m/peça, rolo 50 m.
- Refletivo: 1 m/peça, rolo 50 m, 20 rolos/caixa.
- Elástico: 0,8 m/peça, rolo 25 m.
- Botão de ferro: 100 = 210 g.
- Coquinho: 100 = 78 g.
- Etiqueta de tamanho: 0,35 g/peça.
- Etiqueta de composição: 0,4 g/peça.
- Pares do corte: metros de tecido ÷ (medida do corte × 2).
