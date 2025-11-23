# 🔄 Fluxo Operacional Detalhado

O fluxo operacional foi projetado para funcionar de forma totalmente automatizada entre as ferramentas.

---

## 🧭 1. Entrada pelo Microsoft Teams

Toda mensagem enviada por um colaborador gera um gatilho no N8N.

---

## ⚙️ 2. Orquestração via N8N

O N8N realizava:

- Chamadas às APIs de IA.
- Transformações no payload.
- Salvamento de dados na Supabase.
- Envio de mensagens ao Teams.

Toda a lógica ficava centralizada nele.

---

## 🧠 3. Processamento Inicial (GPT-4o)

1. Interpretação de intenção.
2. Geração de embeddings.
3. Estruturação básica do fluxo desejado pelo usuário.

---

## 🗄️ 4. Armazenamento de Embeddings (Supabase)

- Os vetores eram armazenados em uma tabela com suporte nativo a consultas vetoriais.
- Permitiu histórico navegável por semântica.

---

## 🔍 5. Busca Semântica (DeepSeek)

O modelo recebia:

- Embeddings atuais
- Histórico da base
- Regras de negócio estruturais do RH

E retornava:

- Registros relacionados
- Contextos relevantes
- Tópicos que poderiam complementar a resposta final

---

## 🧾 6. Geração da Resposta Final (GPT-4o)

Incluía:

- Contexto encontrado na base
- Intenção do usuário
- Diretrizes do RH
- Tratamento de linguagem natural

---

## 💬 7. Envio da Resposta via Teams

O usuário recebia tudo no chat, de forma transparente.

---

## 🎯 Resultado

Um fluxo simples, mas funcional, capaz de:

- Responder dúvidas
- Recuperar informações por semântica
- Criar histórico consultável
- Ajudar RH a visualizar o potencial da IA antes de contratar fornecedores
