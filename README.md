
## 🔍 Análise de Sentimentos com Azure AI Search + Language Service

Este projeto foi desenvolvido como parte de um estudo prático em Inteligência Artificial usando os serviços da Azure. O objetivo foi criar uma solução de **busca inteligente de resenhas de clientes**, com destaque para a **análise de sentimentos** automatizada utilizando **Azure AI Search** e o serviço de linguagem do **Azure AI Services**.

---

### ⚙️ Processo de Implementação

#### 1. Criação dos recursos no Azure
Para colocar o projeto em funcionamento, foram criados os seguintes recursos:

- **Azure AI Search**: responsável por indexar os dados e habilitar buscas inteligentes.
- **Azure AI Services (Language)**: para análise de sentimentos e enriquecimento dos dados.
- **Conta de Armazenamento do Azure**: utilizada para armazenar os documentos (resenhas em texto) que serão processados e indexados.

#### 2. Upload das resenhas para o armazenamento
As resenhas utilizadas no projeto foram extraídas de um conjunto de dados simulado. Os arquivos foram enviados para um **container Blob** dentro da conta de armazenamento, por meio de upload direto via portal.

#### 3. Indexação e enriquecimento dos dados
Utilizando o portal do Azure, os dados foram integrados ao serviço de busca por meio do assistente de importação de dados. Durante essa etapa:

- Criou-se um **indexador** que lê os arquivos da conta de armazenamento.
- Aplicou-se um **Skillset** com a funcionalidade de `SentimentSkill`, para identificar e classificar os sentimentos das resenhas como "positive", "neutral" ou "negative".
- O resultado foi um índice rico em informações, com **sentimento**, **localização**, **palavras-chave**, entre outros dados estruturados.

---

### 🔎 Realizando Buscas

A aba **"Search Explorer"** do Azure AI Search permite testar buscas diretamente no índice criado. Exemplo de uma consulta para filtrar resenhas com sentimento positivo:

```json
{
  "search": "sentiment:'positive'",
  "count": true
}
```

🔁 O resultado será uma lista de resenhas com sentimento positivo, incluindo os campos processados automaticamente como:

- Texto da resenha  
- Palavras-chave extraídas  
- Localização mencionada  
- Resultado da análise de sentimento  

---

### 🧠 Resultados e Insights

A análise revelou padrões importantes:

- Resenhas positivas geralmente mencionam atendimento rápido, ambiente agradável e qualidade do produto.
- Feedbacks negativos estão ligados à demora, falhas no produto ou atendimento insatisfatório.
- A extração automática de **palavras-chave** e **localizações** enriquece a experiência de busca, tornando-a mais eficiente e precisa.

---

### 🛠️ Potenciais Aplicações

Essa solução pode ser facilmente adaptada para diversos contextos além de cafeterias, como:

- Avaliações de produtos em e-commerce  
- Comentários de usuários em aplicativos  
- Análises de satisfação de clientes em empresas de serviços  

Além disso, pode ser integrada a:

- **Power BI** para dashboards interativos  
- **Azure Logic Apps** para automações baseadas em feedbacks  
- **Soluções de atendimento com IA**, como chatbots com LUIS  

---

### 💡 Conclusão

O **Azure AI Search**, combinado com **serviços cognitivos**, permite construir soluções robustas para análise de dados textuais com pouco código e muita inteligência. Com esse projeto, foi possível:

- Compreender o funcionamento de pipelines de indexação e enriquecimento no Azure  
- Aplicar técnicas de NLP (Processamento de Linguagem Natural) em dados reais  
- Criar um sistema de busca inteligente com análise de sentimentos integrada  
