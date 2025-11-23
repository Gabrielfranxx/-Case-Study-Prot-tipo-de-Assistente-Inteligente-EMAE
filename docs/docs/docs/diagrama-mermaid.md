# 📊 Diagrama da Arquitetura (Mermaid)

```mermaid
flowchart TD

A[Usuário no Microsoft Teams] --> B[N8N - Orquestração]

B --> C[GPT-4o - Interpretação]
C --> D[Embeddings]
D --> E[Supabase - Armazenamento Vetorial]

B --> F[DeepSeek API - Busca Semântica]
F --> B

E --> F
C --> G[GPT-4o - Geração da Resposta]

G --> B
B --> H[Resposta enviada ao Teams]
