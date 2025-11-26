# 💸 App de Finanças Pessoais com Vibe Coding - Por Leonardo Duarte

PRD no Copilot:
***markdown
[
  {
    "intent": "onboarding_boas_vindas",
    "utterances": [
      "Olá",
      "Começar",
      "O que faz este app",
      "Como funciona",
      "Quero começar"
    ],
    "responses": [
      "Olá! Eu sou o **Agente Financeiro** do app **Seu Bolso Inteligente por Leonardo Duarte**. Aqui você registra gastos conversando, cria metas e recebe dicas práticas. Quer registrar um gasto agora? Ex.: “Almoço R$ 35”"
    ],
    "quick_replies": [
      "Registrar gasto",
      "Ver exemplos",
      "Mais tarde"
    ]
  },
  {
    "intent": "app_header",
    "utterances": [
      "(UI) cabeçalho",
      "mostrar cabeçalho",
      "texto do topo"
    ],
    "responses": [
      "Agente Financeiro - Seu assistente de finanças - Leonardo Duarte"
    ],
    "quick_replies": []
  },
  {
    "intent": "pedir_permissao_notificacoes",
    "utterances": [
      "Quero notificações",
      "Posso receber lembretes?",
      "Ativar notificações",
      "Não quero notificações",
      "Lembretes"
    ],
    "responses": [
      "Posso enviar lembretes e resumos semanais. Deseja ativar notificações para metas e resumos?"
    ],
    "quick_replies": [
      "Sim, ativar",
      "Prefiro depois"
    ]
  },
  {
    "intent": "registrar_gasto",
    "utterances": [
      "Café R$ 8",
      "Uber 22 reais",
      "Supermercado 120 ontem",
      "Gastei R$ 45 no mercado",
      "Paguei 30 reais em gasolina"
    ],
    "responses": [
      "Perfeito — registrei: **{{descricao}} • R$ {{valor}} • {{data}} • Categoria: {{categoria}}**. Quer adicionar uma nota?"
    ],
    "quick_replies": [
      "Adicionar nota",
      "Confirmar",
      "Editar"
    ]
  },
  {
    "intent": "registrar_gasto_faltando_dados",
    "utterances": [
      "R$ 45 no mercado",
      "Gastei 30",
      "Paguei 120",
      "Comprei algo por 60"
    ],
    "responses": [
      "Anotei o valor, mas não identifiquei a categoria. Foi **Alimentação**, **Transporte** ou outra coisa?"
    ],
    "quick_replies": [
      "Alimentação",
      "Transporte",
      "Outra"
    ]
  },
  {
    "intent": "confirmar_transacao",
    "utterances": [
      "Confirmar",
      "Sim",
      "Está certo",
      "Salvar"
    ],
    "responses": [
      "Gasto salvo ✅ — **R$ {{valor}} em {{categoria}}**. Quer ver o resumo do dia?"
    ],
    "quick_replies": [
      "Resumo do dia",
      "Continuar registrando"
    ]
  },
  {
    "intent": "editar_transacao",
    "utterances": [
      "Editar categoria",
      "Mudar valor para R$ 80",
      "Corrigir data",
      "Alterar transação",
      "Corrigir"
    ],
    "responses": [
      "Claro — o que deseja alterar: **categoria**, **valor** ou **data**?"
    ],
    "quick_replies": [
      "Alterar categoria",
      "Alterar valor",
      "Alterar data"
    ]
  },
  {
    "intent": "fallback_nao_entendi",
    "utterances": [
      "???",
      "Não entendi",
      "Hã",
      "O que?"
    ],
    "responses": [
      "Desculpe, não entendi. Pode digitar só o valor com R$? Ex.: **R$ 45** ou escolher uma categoria."
    ],
    "quick_replies": [
      "Valor",
      "Categoria",
      "Exemplos"
    ]
  },
  {
    "intent": "criar_meta",
    "utterances": [
      "Quero poupar R$ 1.200 em 6 meses",
      "Meta guardar 2000 em 10 meses",
      "Criar meta",
      "Quero economizar"
    ],
    "responses": [
      "Meta criada: **Guardar R$ {{valor_meta}} em {{periodo}}**. Progresso atual: R$ 0. Quer que eu sugira quanto poupar por semana?"
    ],
    "quick_replies": [
      "Sim, sugira",
      "Não, depois"
    ]
  },
  {
    "intent": "acompanhar_progresso_meta",
    "utterances": [
      "Progresso da minha meta",
      "Quanto falta para a meta?",
      "Status da meta",
      "Como vai minha meta"
    ],
    "responses": [
      "Você poupou **R$ {{poupado}}** até agora — **{{percentual}}%** da meta. Mantendo o ritmo atual, deve atingir em {{meses_restantes}} meses."
    ],
    "quick_replies": [
      "Ajustar meta",
      "Criar lembrete"
    ]
  },
  {
    "intent": "dica_geral_economia",
    "utterances": [
      "Me dê uma dica",
      "Como economizar?",
      "Dicas",
      "Sugestão de economia"
    ],
    "responses": [
      "Dica rápida: reveja assinaturas mensais — muitas vezes há serviços duplicados. Quer que eu liste suas maiores despesas fixas?"
    ],
    "quick_replies": [
      "Listar despesas",
      "Agora não"
    ]
  },
  {
    "intent": "dica_personalizada",
    "utterances": [
      "Analisar meus gastos",
      "Onde gasto mais?",
      "Me mostre meus maiores gastos",
      "Análise de gastos"
    ],
    "responses": [
      "Notei que **{{percentual_alimentacao}}%** dos seus gastos foram em alimentação este mês. Experimente planejar 3 refeições semanais em casa — pode reduzir até 20% desse valor. Quer tentar um desafio de 2 semanas sem delivery?"
    ],
    "quick_replies": [
      "Aceitar desafio",
      "Ignorar"
    ]
  },
  {
    "intent": "resumo_mensal",
    "utterances": [
      "Resumo do mês",
      "Meu gasto em março",
      "Relatório mensal",
      "Resumo mensal"
    ],
    "responses": [
      "Resumo de {{mes}}: Gastos totais **R$ {{total}}**. Top 3 categorias: **{{cat1}} R$ {{val1}}; {{cat2}} R$ {{val2}}; {{cat3}} R$ {{val3}}**."
    ],
    "quick_replies": [
      "Ver gráfico",
      "Receber dicas"
    ]
  },
  {
    "intent": "alerta_meta_em_risco",
    "utterances": [
      "(trigger automático) ritmo da meta",
      "Meta em risco",
      "Aviso meta"
    ],
    "responses": [
      "Aviso: com o ritmo atual, você pode não atingir a meta de **R$ {{valor_meta}}**. Quer que eu sugira cortes rápidos?"
    ],
    "quick_replies": [
      "Sim, sugerir",
      "Ignorar"
    ]
  },
  {
    "intent": "detectar_duplicata",
    "utterances": [
      "(trigger automático) gasto duplicado",
      "Gasto duplicado",
      "Registro duplicado"
    ],
    "responses": [
      "Parece que esse gasto já foi registrado hoje. Deseja manter ambos ou remover o anterior?"
    ],
    "quick_replies": [
      "Manter ambos",
      "Remover anterior"
    ]
  },
  {
    "intent": "ajuda_rapida",
    "utterances": [
      "Como usar",
      "Exemplos de mensagens",
      "Ajuda",
      "O que posso escrever"
    ],
    "responses": [
      "Você pode escrever como se falasse com um amigo. Exemplos: “Almoço R$ 42”, “Uber R$ 22 ontem”, “Quero poupar R$ 2.000 em 10 meses”. Quer ver mais exemplos?"
    ],
    "quick_replies": [
      "Mais exemplos",
      "Falar com suporte"
    ]
  }
]

Interações com o Lovable:

Thought for 14s
Vou atualizar o projeto com as modificações do seu código. As principais mudanças são: adição do cabeçalho "Agente Financeiro - Seu assistente de finanças - Leonardo Duarte", atualização da mensagem de boas-vindas incluindo o nome do app, e remoção do intent de microcopy_botoes.

Vou atualizar o projeto com as modificações do seu código. As principais mudanças são: adição do cabeçalho "Agente Financeiro - Seu assistente de finanças - Leonardo Duarte", atualização da mensagem de boas-vindas incluindo o nome do app, e remoção do intent de microcopy_botoes.

Show all
1 edit made
Projeto atualizado com o nome do app "Seu Bolso Inteligente por Leonardo Duarte" no cabeçalho e na mensagem de boas-vindas.

Aprenda a **criar soluções com IA** de forma criativa, guiando ferramentas como o **Copilot** e o **Lovable** com uma comunicação simples e natural. O foco é desenvolver o conceito de um **App de Organização de Finanças Pessoais**, mas, acima de tudo, aprender o **jeito Vibe de programar com IA**.

## ✨ O que é Vibe Coding

**Vibe Coding** é uma forma leve e criativa de desenvolver com IA, baseada em **conversas naturais e bem estruturadas**. Você não precisa escrever código linha por linha. Em vez disso, aprende a **guiar a IA** descrevendo suas ideias de forma clara, com **intenção e contexto**. Em outras palavras:

> Você mostra a vibe da sua ideia e a IA transforma em solução (ou em um caminho para ela).

## 🎯 Desafio

Problema: Muitas pessoas não conseguem manter um controle financeiro porque os aplicativos exigem muita entrada de dados manual, e a criação de orçamentos é vista como algo tedioso. 

Precisamos de uma solução que permita **controlar as finanças por meio de uma conversa simples**, com **agentes de IA** capazes de criar **planos de economia personalizados e automatizados**. Você deve utilizar as ideias de **Vibe Coding** e **MVP (Produto Mínimo Viável)** para desenvolver o **conceito de um aplicativo** que resolva o problema citado.

> [!IMPORTANT]
> Você **não precisa construir o código**! O foco está em **usar a IA como sua parceira criativa**, transformando boas ideias e prompts em conceitos funcionais que simulam um produto real.

## 🪄 Etapas do Desafio

### 1. Saber o que Pedir é a Chave! Otimize seus Prompts!

Antes de pedir para a IA "criar um app", é importante definir com clareza o que você quer construir e por quê. Para isso, você vai criar um **PRD (Product Requirements Document)** simplificado, uma especificação que serve como _briefing_ para a IA entender sua ideia.

Um bom PRD deve descrever o problema, quem será beneficiado, as principais funcionalidades e o que você espera que a IA entregue. Use o modelo abaixo como ponto de partida e adapte conforme o seu estilo:

```txt
# Contexto
Quero criar um aplicativo de Organização de Finanças Pessoais que funcione por meio de conversas com o usuário.  
A ideia é facilitar o controle financeiro de forma simples e natural, sem formulários manuais ou planilhas complexas.

# Problema
Muitas pessoas desistem de controlar seus gastos porque os apps atuais exigem muita entrada manual e pouca personalização.  
Quero resolver isso com uma experiência de conversa e recomendações automáticas de economia.

# Público-Alvo
Pessoas que querem começar a organizar suas finanças de forma prática e sem complicação, principalmente iniciantes.

# Funcionalidades-Chave
1. Registrar gastos via chat em linguagem natural.  
2. Classificar automaticamente as transações.  
3. Definir e acompanhar metas financeiras.  
4. Receber dicas de economia do “Agente Financeiro”.  
5. Visualizar relatórios simples e personalizados.

# Entregável da IA
Gerar um plano de MVP com as principais telas, recursos necessários e um esboço de validação inicial.  
Usar tom educativo e linguagem acessível, em português.
```

Depois de preencher o modelo, use o Copilot Web para revisar e melhorar o seu prompt antes de ir ao Lovable. A ideia é lapidar o texto até que ele fique claro, direto e reflita exatamente a sua intenção.

> [!TIP]
> Pense no PRD/Prompt como “o briefing que a IA precisa para entender sua vibe”. Portanto, quanto mais claro e intencional for o texto, mais próximas do ideal serão as respostas da IA.

### 2. Explorando o Lovable na Prática

Com seu PRD pronto e revisado, é hora de colocar a IA em ação. Abra o Lovable, cole seu prompt completo e peça o plano inicial do MVP do seu aplicativo. Como o plano gratuito limita você a 5 interações por dia, seja estratégico:
- Faça perguntas diretas e construtivas, como “crie o fluxo de telas com base nas funcionalidades listadas” ou “gere uma versão resumida do plano de MVP”;
- Priorize clareza nas instruções para aproveitar ao máximo cada resposta;

Durante essa etapa, você pode orientar a IA para três entregas principais:
1. Agente Financeiro: defina o comportamento e o tom de voz de um consultor financeiro pessoal, alinhado ao público e objetivo do app.
2. Fluxo de Telas: peça à IA para gerar o fluxo conceitual de telas com base nas funcionalidades descritas no PRD, simulando a interação por conversa.
3. Plano de MVP: solicite um resumo das 5 funcionalidades principais, dos recursos necessários e um plano de validação inicial (como medir se o app cumpre seu propósito).

> [!TIP]
> Se preferir, você pode fazer tudo com o **Copilot**. O importante é exercitar a habilidade de transformar intenções em instruções claras e testar os limites da IA como parceira criativa.

### 3. Entregando o Desafio na DIO

Finalize seu projeto criando um **repositório no GitHub** (pode ser um **fork** deste).  
No README do seu repositório, inclua:

- Seu **prompt final** (PRD);  
- Prints ou pequenos vídeos das interações com a IA;  
- Um resumo do que o seu **App de Finanças Pessoais** faz;  
- Uma breve **reflexão sobre o processo**:
  - O que funcionou bem?  
  - O que não funcionou como o esperado?  
  - O que aprendeu sobre conversar com IAs?

> [!TIP]
> Publique seu repositório e compartilhe o link na plataforma da DIO! Sua entrega é a prova de que você domina o raciocínio de Vibe Coding, mesmo sem escrever uma única linha de código.

## 💬 Conclusão

Vibe Coding é sobre clareza, curiosidade e criatividade, não sobre perfeição técnica. O verdadeiro objetivo aqui é aprender a pensar junto com a IA, transformando ideias em conceitos reais e enxergando a tecnologia como uma extensão do seu raciocínio criativo. Cada interação é um experimento, quanto mais clara for sua intenção, mais surpreendente será o resultado.
