# construindo-flashcards<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Interações Dinâmicas com CSS</title>
  
  <style>
    /* ==============================================
       1. RESET E ESTILO DA PÁGINA
       ============================================== */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Segoe UI', system-ui, sans-serif;
      background-color: #0f172a;
      color: #f8fafc;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      padding: 20px;
    }

    h1 {
      margin-bottom: 10px;
      font-size: 28px;
      text-align: center;
    }

    .subtitulo {
      color: #94a3b8;
      margin-bottom: 40px;
      text-align: center;
    }

    /* Dica: Use a tecla TAB do teclado para testar a navegação! */

    /* ==============================================
       2. O CONTAINER DOS CARDS
       ============================================== */
    .painel {
      display: flex;
      gap: 24px;
      flex-wrap: wrap;
      justify-content: center;
      max-width: 900px;
      width: 100%;
    }

    /* ==============================================
       3. ESTILIZAÇÃO DO CARD PRINCIPAL
       ============================================== */
    .cartao {
      background-color: #1e293b;
      border: 2px solid transparent; /* Reservando o espaço da borda */
      border-radius: 12px;
      padding: 24px;
      width: 280px;
      transition: all 0.3s ease; /* Deixa a transição suave */
    }

    /* [ :HOVER ] - Quando o mouse passa sobre o card */
    .cartao:hover {
      background-color: #334155;
      transform: translateY(-5px); /* Efeito de flutuar */
      box-shadow: 0 10px 20px rgba(0, 0, 0, 0.4);
    }

    /* [ :FOCUS-WITHIN ] - Quando o link interno do card ganha foco (via TAB) */
    .cartao:focus-within {
      border-color: #38bdf8; /* Borda acende indicando que o bloco está ativo */
      background-color: #1e293b;
      transform: scale(1.02); /* Dá um leve zoom */
    }

    /* Elementos internos do card */
    .cartao h3 {
      font-size: 20px;
      margin-bottom: 12px;
      color: #38bdf8;
    }

    .cartao p {
      color: #94a3b8;
      font-size: 14px;
      line-height: 1.5;
      margin-bottom: 20px;
    }

    /* ==============================================
       4. ESTILIZAÇÃO DOS LINKS/BOTÕES
       ============================================== */
    .link-acao {
      display: inline-block;
      color: #38bdf8;
      text-decoration: none;
      font-weight: 600;
      font-size: 15px;
      padding: 4px 0;
      border-bottom: 2px solid transparent;
      transition: all 0.2s ease;
      outline: none; /* Remove o contorno padrão feio para fazermos o nosso */
    }

    /* [ :HOVER ] no link - Cria o sublinhado animado */
    .link-acao:hover {
      color: #60a5fa;
      border-bottom-color: #60a5fa;
    }

    /* [ :FOCUS ] - O farol do teclado quando o link é selecionado */
    .link-acao:focus {
      color: #0f172a;
      background-color: #38bdf8; /* Cria um destaque de "marca-texto" */
      padding: 4px 8px;
      border-radius: 4px;
    }

    /* [ :ACTIVE ] - O clique rápido (micro-feedback) */
    .link-acao:active {
      transform: scale(0.95); /* Dá a sensação de que o botão foi afundado */
      color: #93c5fd;
    }

    /* [ :VISITED ] - Mostra se você já clicou nesse link antes */
    .link-acao:visited {
      color: #a78bfa; /* Fica roxo sutil se já foi visitado */
    }
  </style>
</head>
<body>

  <h1>Painel de Recursos Interativos</h1>
  <p class="subtitulo">Passe o mouse ou use a tecla <strong>TAB</strong> do seu teclado para testar as interações!</p>

  <main class="painel">
    
    <section class="cartao">
      <h3>Documentação</h3>
      <p>Acesse nossos guias práticos e referências de código para construir páginas incríveis.</p>
      <a href="#doc" class="link-acao">Ver arquivos →</a>
    </section>

    <section class="cartao">
      <h3>Componentes</h3>
      <p>Explore nossa biblioteca de blocos prontos e acelere o desenvolvimento do seu layout.</p>
      <a href="#comp" class="link-acao">Explorar →</a>
    </section>

    <section class="cartao">
      <h3>Comunidade</h3>
      <p>Participe do nosso fórum, tire dúvidas e compartilhe seus projetos com outros devs.</p>
      <a href="#comunidade" class="link-acao">Entrar no grupo →</a>
    </section>

  </main>

</body>
</html>
