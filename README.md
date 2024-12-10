# SpaceAI - Chatbot Espacial

O **SpaceAI** é uma ferramenta de inteligência artificial especializada em fornecer informações sobre o espaço, como satélites, naves e outros objetos astronômicos, além de permitir consultas à NASA para dados sobre objetos celestes.

## Funcionalidades

- **Integração com a API da NASA**: O chatbot é capaz de consultar a API da NASA (Horizons Lookup) para obter informações sobre objetos celestes, como satélites e asteroides, com base em consultas do usuário.
- **Filtragem de conteúdo inadequado**: O chatbot verifica respostas para detectar palavras ofensivas e viés, recusando respostas que contenham conteúdo impróprio ou enviesado.
- **Personalização**: O chatbot pode ser personalizado com uma base de conhecimento adicional, carregada de um arquivo de texto (Horizons Lookup).



## Como Usar 🚀

### Execução do Chatbot 💬

O chatbot começa com uma introdução e pede para o usuário inserir uma consulta. Se o usuário deseja consultar um objeto específico da NASA, ele deve formatar a entrada como:


### Consultas ao Banco de Conhecimento 🌌

Se o chatbot detectar que o usuário está fazendo uma consulta sobre um objeto específico, ele tentará buscar informações na API da NASA usando o nome do objeto.


## Funções Principais 🧠

- **load_knowledge_base**: Carrega o conteúdo da base de conhecimento de um arquivo de texto.
- **load_inappropriate_keywords**: Carrega uma lista de palavras proibidas.
- **load_bias_keywords**: Carrega uma lista de palavras relacionadas a viés.
- **is_inappropriate**: Detecta se uma resposta contém conteúdo inadequado.
- **is_biased**: Detecta se uma resposta contém viés.
- **query_nasa_api**: Consulta a API da NASA para obter informações sobre objetos celestes.
- **process_input**: Processa a entrada do usuário, separando o nome do objeto e a pergunta.


### Detecção de Conteúdo Inadequado e Viés ⚠️

O chatbot verifica se as respostas contêm conteúdo impróprio ou viés com base nas listas de palavras carregadas. Se detectar algo, ele rejeitará a resposta e informará ao usuário.

## Exemplo de Interação 💬

```bash
Bem-vindo a SpaceAI. Ferramenta de inteligência artificial especializada em fatos espaciais, como: satélites, naves e outros.
Para consultar um dado específico e melhorar sua pergunta, separe por ":". Como em: <StringEspecial>: <SuaPergunta>

Você: Eris: Qual é a composição de Eris?
Chatbot: Buscando informações na API da NASA...
Chatbot: A composição de Eris é composta por rochas e gelo, com um núcleo rochoso e uma atmosfera...

