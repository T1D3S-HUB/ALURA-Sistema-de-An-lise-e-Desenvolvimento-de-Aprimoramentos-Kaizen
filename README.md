# ALURA: Sistema de Análise e Desenvolvimento de Aprimoramentos Kaizen

## Sobre o Projeto

O ALURA (Sistema de Análise e Desenvolvimento de Aprimoramentos) é uma ferramenta protótipo desenvolvida em Python para otimizar o processo de coleta e triagem de ideias Kaizen (melhoria contínua) em um ambiente corporativo. Tradicionalmente, a submissão e avaliação de ideias podem ser manuais ou enfrentar desafios na clareza da descrição e no direcionamento correto. O ALURA busca automatizar e enriquecer essa etapa inicial utilizando Inteligência Artificial.

Este projeto foi desenvolvido como parte da **Imersão Inteligência Artificial com Google Gemini** promovida pela Alura.

## Como Funciona

O sistema opera através de uma interface de texto simples (simulando um chat inicial com o funcionário) e orquestra uma série de Agentes de IA, construídos com o Google ADK (Agent Development Kit), para processar cada ideia submetida:

1.  **Agente 1 (Auxiliador):** Coleta os dados brutos do funcionário e da ideia (problema e solução), reestrutura o texto para torná-lo mais claro e objetivo, e verifica (com base em um banco de dados simulado) se há similaridades com ideias já registradas.
2.  **Agente 2 (Técnico):** Analisa a ideia reestruturada para identificar aspectos técnicos, estimar recursos necessários (com base em análise interna, não busca externa), e sugere o setor da empresa mais adequado para avaliar ou implementar a solução (Manutenção, Qualidade, RH, TI, etc.), seguindo diretrizes pré-configuradas.
3.  **Agente 3 (Revisor):** Revisa o processamento dos agentes anteriores, define um status inicial para a ideia (ex: "Pronto para Avaliação Técnica") e adiciona uma nota final, preparando os dados para arquivamento e avaliação humana.

Após o processamento pelos agentes, o sistema gera múltiplos relatórios detalhados (em formato de texto, otimizado para print) que consolidam as informações originais, a análise da IA e o resultado da triagem.

## Funcionalidades Principais

* Interface de texto interativa para submissão de ideias.
* Simulação de banco de dados (em memória) para armazenamento de ideias.
* Reestruturação automática do texto da ideia por IA.
* Detecção de similaridades com ideias anteriores.
* Análise técnica e estimativa de recursos por IA.
* Sugestão de direcionamento da ideia para o setor responsável.
* Revisão e finalização do registro por IA.
* Geração de múltiplos relatórios de status (bruto, processado, finalizado) por ideia.
* Integração com Google Gemini via Google AI Studio SDK e ADK.

## Tecnologias Utilizadas

* Python
* Google Colab
* Google Generative AI SDK (`google-generative-ai`)
* Google Agent Development Kit (`google-generative-ai[notebook]`)

## Como Executar

1.  Clone ou baixe este repositório.
2.  Abra o notebook no Google Colab.
3.  Configure sua Google Gemini API Key nos "Secrets" do Colab com o nome `GOOGLE_API_KEY`.
