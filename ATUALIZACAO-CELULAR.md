# Atualização: Ferramentas de proteção e versão para celular

## Novidades (aba "Proteção")
- **Me acompanhe (trajeto seguro):** defina destino e tempo (10 a 90 min). Se você não tocar em "Cheguei bem", o SOS começa com 5 segundos para cancelar. Aviso com vibração 1 minuto antes, botão "+10 min" e atalho para avisar no WhatsApp que você saiu. Um contador flutuante aparece nas outras telas. Funciona com o app aberto; se você sair do app, o aviso aparece ao voltar.
- **Chamada falsa:** simula uma ligação recebida (nome personalizável, agora, 10 s, 30 s, 1 min ou 5 min), com toque, vibração, tela de chamada e cronômetro. Atalho rápido na tela inicial (toca em 10 s).
- **Rede de apoio:** 190, 180, 192, 193, 197 e 100 com um toque, Ligue 180 pelo WhatsApp oficial (61) 9610-0180 e busca no Google Maps por Delegacia da Mulher, delegacia, hospital, Defensoria Pública e Casa da Mulher Brasileira.
- **Diário de ocorrências:** registre data, tipo, descrição e local; exporte em .txt (ou compartilhe pelo celular) para boletim de ocorrência ou medida protetiva. Fica só no aparelho e é apagado junto em Ajustes → Dados neste aparelho.

## Celular
- Menu inferior com 5 itens (Início, Contatos, Proteção, Localização, Ajustes); "Como usar" fica no menu lateral e na aba Proteção.
- Botão SOS flutuante em todas as telas (exceto Início e pedido em andamento).
- Atalhos rápidos na tela inicial: Me acompanhe, Chamada falsa, Ligar 190, Ligar 180.
- Barra superior fixa e respeitando a área do entalhe (safe area); janelas abrem de baixo para cima (bottom sheet).
- Campos com fonte de 16 px (o iPhone não dá mais zoom ao digitar), botões de no mínimo 48 px.

## Bugs corrigidos
- Segurar o SOS no celular cancelava se o dedo mexesse um pouco (o navegador interpretava como rolagem). Agora o botão usa `touch-action:none`.
- "Atualizar por 15 min" parava de vez quando o GPS demorava a responder (erro de timeout). Agora continua tentando e mantém a última posição.
- "Apagar dados deste aparelho" agora também apaga o diário e o acompanhamento ativo.
- Texto "Emergência padrão preparado" corrigido.

## Testes
45 testes passando (4 novos: aba Proteção, Me acompanhe, diário e chamada falsa).

## Publicar
`npm ci --ignore-scripts && npm test`, depois commit e push para `main`. O Netlify publica sozinho.
