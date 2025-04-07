# 🔍 Analisador de Sentimentos com Azure AI Language Studio

Este projeto tem como objetivo demonstrar o uso de ferramentas de IA da Microsoft Azure para análise de sentimentos em textos de usuários, simulando avaliações de produtos e serviços de uma plataforma fictícia.

---

## 📁 Estrutura do Projeto

- `inputs/textos.txt`: Arquivo com textos variados simulando avaliações positivas, negativas e neutras.
- `README.md`: Documento explicando o processo, descobertas e aprendizados com o projeto.

---

## ⚙️ Processo Realizado

1. **Coleta de Dados**: Criei textos representando diferentes níveis de satisfação — desde elogios até críticas diretas.
2. **Upload no Language Studio**: Utilizei a ferramenta de Análise de Texto (Text Analytics) do Azure AI Language Studio.
3. **Análise de Sentimentos**: A IA foi capaz de classificar os sentimentos (positivo, negativo ou neutro) de cada texto com base em sua semântica.
4. **Observação dos Resultados**: Avaliei como a IA interpretou nuances dos comentários.

---

## 💡 Aprendizados e Possibilidades

- A ferramenta tem boa capacidade de identificar ironia sutil e críticas disfarçadas em elogios, algo que pode ser valioso em atendimentos e SACs.
- Comentários curtos, como “Falta água”, ainda são corretamente analisados como negativos, o que mostra a robustez do modelo mesmo com entradas mínimas.
- A IA pode ser usada em análises de grandes volumes de avaliações para gerar métricas de satisfação de forma automatizada.

---

## 📈 Potenciais Aplicações

- Plataformas de e-commerce e marketplaces
- Setores de ouvidoria e atendimento ao cliente
- Avaliação de feedbacks em apps, sites e serviços

---

## 🚀 Conclusão

Esse projeto é uma introdução prática e útil ao uso de IA em análise de linguagem natural. Combinando entradas simuladas e análise automatizada, é possível obter insights valiosos sobre a percepção dos usuários com rapidez e escala.

---
