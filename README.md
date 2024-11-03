# Chatbot Interativo - Aprendizado Contínuo
Este projeto envolve o desenvolvimento de um chatbot interativo que não apenas responde a perguntas, mas também aprende e se adapta com base nas interações do usuário. O chatbot deve armazenar informações relevantes sobre um tema específico apenas quando o usuário enviar algo verdadeiro ou quando se trata de preferências, como preferir um tom mais formal.

## Requisitos
Interface de Usuário (UI): Utiliza Streamlit para criar uma interface visual do chatbot. A construção rápida da UI não é a prioridade do teste.
LangGraph e Langchain: Utilizados para a construção da solução.
Modelo de Linguagem (LLM): Qualquer modelo de sua preferência, com uma variável de ambiente para a chave de API (recomendado: usar os LLMs da Groq, que são gratuitos).
Base de Dados Vetorial: Utilizada para armazenar informações relevantes, deve estar em um container Docker no projeto.
## Entrega
Código no GitHub: O código-fonte do projeto deve ser disponibilizado em um repositório público no GitHub.
Documentação: Documentação detalhada que explique como instalar as dependências e executar a aplicação localmente, incluindo exemplos de uso e configurações necessárias.
Container Docker: O projeto deve incluir um Dockerfile que permita criar uma imagem Docker, facilitando a execução da aplicação em diferentes ambientes sem conflitos de dependência.
Observações
Este desafio será discutido durante a entrevista, proporcionando a oportunidade de você apresentar suas soluções e decisões tomadas durante o desenvolvimento. Além disso, é uma excelente chance para enriquecer seu portfólio. Se você já possui um projeto que utiliza as tecnologias mencionadas, sinta-se à vontade para compartilhá-lo conosco, o que tornará a implementação deste desafio desnecessária. Sua habilidade em refinar as respostas do modelo de linguagem e construir os agentes será avaliada, sendo que o foco deste desafio não está apenas no código.

## Instalação e Execução
Pré-requisitos
Python 3.9+
Docker
Conta no Groq para obter a chave de API

## Passos para Instalação

```bash
git clone https://github.com/seu-usuario/seu-repositorio.git
cd seu-repositorio
```
### Crie um ambiente virtual e instale as dependências:


```bash
python -m venv venv
source venv/bin/activate  # No Windows use `venv\Scripts\activate`
pip install -r requirements.txt
```
## Configure as variáveis de ambiente:

Crie um arquivo .env na raiz do projeto e adicione sua chave de API do Groq:
.env
LLM_API_KEY=your_groq_api_key
## Execute a aplicação localmente:

```bash

streamlit run app.py
```
## Construa a imagem Docker:

```bash
docker build -t chatbot .
```
Execute o container Docker:

```bash
docker run -p 8501:8501 chatbot
```
## Exemplo de Uso
Acesse a aplicação no navegador em http://localhost:8501.
Digite uma mensagem no campo de texto e pressione Enter.
O chatbot responderá e aprenderá com base nas suas interações.
Estrutura do Projeto
```bash
.
├── app.py                 # Arquivo principal da aplicação Streamlit
├── chatbot.py             # Implementação do chatbot
├── Dockerfile             # Arquivo para criação da imagem Docker
├── requirements.txt       # Dependências do projeto
├── .env                   # Variáveis de ambiente (não incluído no repositório)
└── README.md              # Documentação do projeto
```
## Tecnologias Utilizadas
- Streamlit: Framework para criação da interface do usuário.
- Langchain e LangGraph: Bibliotecas para construção da lógica do chatbot.
- Groq: Serviço de LLM utilizado para geração de respostas.
- Docker: Para containerização da aplicação, garantindo portabilidade e consistência no ambiente de execução.

