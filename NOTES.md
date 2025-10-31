# 📝 Anotações Técnicas Detalhadas: Azure Speech e Language Studio

Este documento contém anotações técnicas e um passo a passo conceitual dos laboratórios práticos propostos no desafio da DIO, servindo como material de estudo e referência para futuras implementações.

## 1. Laboratório: Azure AI Speech Studio

O foco deste laboratório é a exploração das capacidades de conversão de fala em texto (Speech-to-Text) e texto em fala (Text-to-Speech) através da interface gráfica do Speech Studio.

### 1.1. Configuração Inicial

1.  **Criação do Recurso:** No Portal do Azure, criar um recurso do tipo **Speech Service** (ou **Azure AI services** unificado).
2.  **Região e Preços:** Selecionar a região mais próxima e o nível de preços adequado (Geralmente o **F0 - Gratuito** para testes, mas que requer créditos).
3.  **Acesso ao Studio:** Após a criação, navegar para o Speech Studio (`speech.azure.us`) e selecionar o recurso criado.

### 1.2. Prática 1: Transcrição em Tempo Real (Speech-to-Text)

**Objetivo:** Converter um arquivo de áudio pré-gravado (ou simular a entrada de microfone) em texto.

| Passo | Descrição Técnica |
| :--- | :--- |
| **1.** | Acessar a seção "Real-time speech to text" no Speech Studio. |
| **2.** | Fazer o upload de um arquivo de áudio (.wav, .mp3) com voz clara (simulando uma gravação de reunião ou atendimento). |
| **3.** | **Análise de Resultado:** Observar a precisão da transcrição. O Studio exibe o texto transcrito, o carimbo de data/hora (timestamp) de cada palavra e a pontuação de confiança. |
| **4.** | **Insights:** A pontuação de confiança é crucial para determinar a necessidade de modelos de fala personalizados (Custom Speech) em ambientes ruidosos. |

### 1.3. Prática 2: Síntese de Fala (Text-to-Speech)

**Objetivo:** Converter texto em fala natural utilizando as vozes neurais do Azure.

| Passo | Descrição Técnica |
| :--- | :--- |
| **1.** | Acessar a seção "Audio content creation" ou "Text-to-speech" no Speech Studio. |
| **2.** | Inserir um texto de exemplo (ex: "A inteligência artificial do Azure oferece serviços de fala e linguagem de alta qualidade."). |
| **3.** | **Seleção de Voz:** Escolher uma voz neural em Português (Brasil), como `pt-BR-FranciscaNeural` ou `pt-BR-AntonioNeural`. |
| **4.** | **Ajustes:** Explorar o SSML (Speech Synthesis Markup Language) para ajustar a velocidade, o tom e a ênfase da fala. |
| **5.** | **Resultado:** Gerar e fazer o download do arquivo de áudio resultante (.wav ou .mp3). |

## 2. Laboratório: Azure AI Language Studio

O foco é demonstrar a capacidade de extrair significado e contexto de dados textuais não estruturados.

### 2.1. Configuração Inicial

1.  **Criação do Recurso:** No Portal do Azure, criar um recurso do tipo **Language Service** (ou **Azure AI services** unificado).
2.  **Acesso ao Studio:** Navegar para o Language Studio (`language.cognitive.azure.com`) e selecionar o recurso criado.

### 2.2. Prática 3: Análise de Sentimento e Mineração de Opinião

**Objetivo:** Avaliar a polaridade emocional de um texto.

| Passo | Descrição Técnica |
| :--- | :--- |
| **1.** | Acessar a seção "Analyze text" e selecionar "Sentiment analysis and opinion mining". |
| **2.** | Inserir um texto de avaliação de produto (ex: "O novo recurso de transcrição é excelente, mas o preço da licença é muito caro."). |
| **3.** | **Análise de Sentimento:** O Studio retorna uma pontuação de sentimento geral (ex: 0.75 Positivo). |
| **4.** | **Mineração de Opinião:** O recurso mais avançado identifica que o sentimento é positivo em relação ao "recurso de transcrição" e negativo em relação ao "preço da licença". |
| **5.** | **Insights:** A mineração de opinião é vital para feedback detalhado de clientes, pois permite ações corretivas específicas. |

### 2.3. Prática 4: Extração de Entidades Nomeadas (NER)

**Objetivo:** Identificar e classificar informações importantes em um texto.

| Passo | Descrição Técnica |
| :--- | :--- |
| **1.** | Acessar a seção "Analyze text" e selecionar "Named entity recognition (NER)". |
| **2.** | Inserir um texto com diversas informações (ex: "O Sr. Marcio Gil da empresa Avanade se reunirá com a equipe de São Paulo no dia 15 de Outubro de 2025 para discutir o projeto."). |
| **3.** | **Classificação:** O Studio identifica: |
| | - `Marcio Gil`: Pessoa |
| | - `Avanade`: Organização |
| | - `São Paulo`: Local |
| | - `15 de Outubro de 2025`: Data |
| **4.** | **Insights:** O NER é a base para a indexação de documentos e a criação de bases de conhecimento, transformando texto não estruturado em dados estruturados. |

## 3. Estrutura de Arquivos do Repositório

O repositório está organizado para facilitar a navegação e a documentação:

```
trabalho-avanade/
├── README.md           # Visão geral do desafio, insights e objetivos.
├── NOTES.md            # Anotações técnicas detalhadas e passo a passo conceitual.
└── images/             # Pasta para capturas de tela e evidências visuais.
    └── placeholder.png # Arquivo de exemplo para simular a presença de imagens.
```
