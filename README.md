# Analise de Requisitos de Software - Estudo de Caso

Exercicio pratico de analise de requisitos aplicado a sistemas reais, desenvolvido durante o curso Tecnico em Desenvolvimento de Sistemas no Senac Minas.

## Sobre o exercicio

Analise de requisitos funcionais e nao funcionais de 4 sistemas reais, utilizando tecnicas de engenharia de requisitos:

| # | Sistema | Dominio |
|---|---------|---------|
| 1 | Google Maps | Mapeamento e navegacao |
| 2 | Airbnb | Marketplace de hospedagens |
| 3 | Uber | Mobilidade sob demanda |
| 4 | Trello | Gestao visual de projetos (Kanban) |

Cada ficha cobre: mapeamento de atores, 10 funcionalidades principais, priorizacao MoSCoW, requisitos nao funcionais (ISO 25010), cenario de excecao e validacao com o sistema real.

## Estrutura do repositorio

```
├── fichas/                        # Fichas do exercicio (versao original)
│   ├── Ficha_Requisitos_01_Google_Maps.html
│   ├── Ficha_Requisitos_02_Airbnb.html
│   ├── Ficha_Requisitos_03_Uber.html
│   └── Ficha_Requisitos_04_Trello.html
│
├── analise_aprofundada/           # Versao com dados reais e analise tecnica
│   ├── Ficha_Requisitos_01_Google_Maps.html
│   ├── Ficha_Requisitos_02_Airbnb.html
│   ├── Ficha_Requisitos_03_Uber.html
│   └── Ficha_Requisitos_04_Trello.html
│
├── docs/                          # Versoes Word (.docx) para revisao
│   ├── originais/
│   └── analise_aprofundada/
│
├── guia/                          # Material de estudo
│   ├── Guia_de_Estudo_Requisitos.html
│   └── Guia para Coleta e Analise de Requisitos de Software.pdf
│
├── scripts/                       # Scripts de geracao dos documentos Word
│   ├── gerar_fichas_word.py
│   └── gerar_fichas_word_aprofundadas.py
│
└── README.md
```

## Conceitos e tecnicas aplicados

- **IEEE 830**: requisitos mensuraveis, testaveis e rastreaveis
- **ISO 25010**: modelo de qualidade de software (8 caracteristicas)
- **MoSCoW** (DSDM): priorizacao com regra Must Have <= 60% do esforco
- **Cenarios de excecao**: fallback, graceful degradation, tratamento de conflitos
- **Validacao com sistema real**: pos-analise comparando a ficha com o app

## Analise aprofundada

A pasta `analise_aprofundada/` contem versoes enriquecidas com dados reais pesquisados:

- **Google Maps**: 2B MAU, SLA 99,9%, incidente real de fev/2026, fallback TRAFFIC_UNAWARE
- **Airbnb**: Row-level locking em PostgreSQL, Braintree PCI-DSS Level 1, framework Orpheus (99,999% consistencia em pagamentos)
- **Uber**: Matching por grafo bipartido, Filtro de Kalman + Viterbi para GPS, arquitetura DOMA (2.200 microsservicos), grid H3
- **Trello**: Last-write-wins (sem CRDTs/OT), Socket.io, limite de 5.000 cartoes, modo colorblind desde 2014

## Como visualizar

As fichas em HTML podem ser abertas diretamente no navegador. As versoes .docx podem ser abertas no Microsoft Word ou Google Docs.

## Contexto academico

- **Instituicao**: Senac Minas
- **Curso**: Tecnico em Desenvolvimento de Sistemas
- **Disciplina**: UC 7, Aplicacoes em Desenvolvimento Web
- **Aluna**: Thais Oliveira
