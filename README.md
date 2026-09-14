# 🌧️ Observatório Aberto da Segurança Hídrica Paulista (OASHP)

> Plataforma aberta, colaborativa e baseada em dados para monitoramento, interpretação e previsão da segurança hídrica dos sistemas de abastecimento do Estado de São Paulo.

---

# Visão Geral

O Observatório Aberto da Segurança Hídrica Paulista (OASHP) busca integrar informações de meteorologia, hidrologia, abastecimento e inteligência artificial em uma única plataforma aberta.

O objetivo não é apenas exibir o nível das represas, mas responder perguntas relevantes para a sociedade:

- Está chovendo nas bacias que realmente abastecem a RMSP?
- Os reservatórios estão ganhando ou perdendo água?
- A chuva atual terá impacto significativo nos sistemas produtores?
- Existe risco futuro para o abastecimento?
- O sistema está melhorando ou piorando?

---

# Missão

Transformar dados públicos dispersos em inteligência aberta para acompanhar a saúde hídrica do Estado de São Paulo, promovendo:

- Transparência
- Ciência aberta
- Participação comunitária
- Tomada de decisão baseada em evidências

---

# Sistemas Monitorados

## Sistema Cantareira

Principais rios:

- Jaguari
- Jacareí
- Cachoeira
- Atibainha
- Juqueri (Paiva Castro)

---

## Sistema Guarapiranga

Principais rios:

- Embu-Guaçu
- Embu-Mirim
- Capivari
- Parelheiros
- Santa Rita
- Vermelho

---

## Sistema Billings

Principais contribuintes:

- Jurubatuba
- Rio Grande
- Taquacetuba
- Rio Pequeno
- Ribeirão Grande

---

# Sistemas de Observação e Pesquisa

Além dos sistemas produtores principais, o projeto também monitora
reservatórios estratégicos de menor porte para pesquisa, validação de
modelos e aprendizado hidrológico.

## Núcleo Operacional

- Cantareira
- Guarapiranga
- Billings
- Alto Tietê
- Rio Grande

Esses sistemas possuem impacto direto no abastecimento da Região Metropolitana de São Paulo.

## Bacias de Aprendizado (Learning Watersheds)

Reservatórios menores podem responder mais rapidamente aos eventos
meteorológicos e servir como ambientes experimentais para validação
dos modelos preditivos.

### Cabuçu

Utilizado para:

- Estudo de resposta hidrológica rápida
- Correlação chuva × aporte
- Validação de algoritmos
- Desenvolvimento da Linguagem da Água

### Tanque Grande

Utilizado para:

- Monitoramento de microbacias
- Estudos de sazonalidade
- Comparação entre sistemas

### Engordador

Utilizado para:

- Modelagem hidrológica
- Estudos ambientais
- Validação geoespacial

### Várzea do Palácio

Utilizado como observatório complementar para análise de comportamento local dos recursos hídricos.

---

Objetivo:

Transformar reservatórios menores em laboratórios naturais de aprendizado para os modelos aplicados posteriormente aos sistemas Cantareira, Guarapiranga e Billings.


# Objetivos

## Curto Prazo

- Consolidar dados públicos
- Criar dashboard aberto
- Monitorar chuva e reservatórios
- Gerar indicadores simples e compreensíveis

## Médio Prazo

- Criar rede colaborativa de monitoramento
- Validar dados locais
- Integrar estações independentes
- Construir indicadores próprios

## Longo Prazo

Desenvolver uma IA especializada em segurança hídrica.

---

# Linguagem da Água

O projeto propõe um conceito experimental denominado:

## Linguagem da Água

Uma representação semântica dos eventos hidrológicos e meteorológicos.

Exemplo:

```text
CHUVA
+
NUVEM
+
RIO
+
BACIA
+
VAZÃO
+
CONSUMO
+
RESERVATÓRIO
```

Esses eventos passam a ser interpretados como entidades de conhecimento e não apenas números.

---

# Arquitetura

```text
SP-Water-Watch/

├── README.md
│
├── data/
│   ├── reservatorios/
│   ├── chuva/
│   ├── satelite/
│   ├── radares/
│   ├── rios/
│   └── municipios/
│
├── models/
│   ├── graph/
│   ├── forecasting/
│   └── ishm/
│
├── dashboard/
│   ├── map/
│   ├── analytics/
│   └── api/
│
├── scripts/
│
├── docs/
│
└── .github/
    └── workflows/
```

---

# Modelo Colaborativo

O projeto pretende funcionar como uma plataforma de ciência cidadã.

## Contribuições permitidas

### Hidrologia

- Correção de rios
- Correção de bacias
- Inclusão de estações
- Validação geográfica

### Meteorologia

- Registros locais de chuva
- Fotografias
- Estações particulares

### Monitoramento Local

- Alagamentos
- Transbordamentos
- Níveis visuais de rios
- Eventos extremos

---

# Estrutura de Dados

## Município

```json
{
  "municipio": "Joanopolis",
  "bacia": "Cantareira",
  "chuva": true,
  "chuva_24h": 18.2,
  "impacto_hidrico": "alto",
  "ultima_atualizacao": "2026-09-13"
}
```

---

## Rio

```json
{
  "nome": "Jaguari",
  "bacia": "Cantareira",
  "vazao": 120.4,
  "status": "normal"
}
```

---

## Evento Meteorológico

```json
{
  "tipo": "chuva",
  "municipio": "Joanopolis",
  "intensidade_mm": 18,
  "bacia": "Cantareira",
  "relevancia": 0.92
}
```

---

# Grafo de Conhecimento

O núcleo do projeto será baseado em um Knowledge Graph.

Exemplo:

```text
Joanópolis
      │
      ▼
Rio Jaguari
      │
      ▼
Sistema Cantareira
      │
      ▼
ETA Guaraú
      │
      ▼
População Abastecida
```

---

# Leads Hidrológicos

Lead hidrológico é qualquer evento que indique uma possível alteração futura dos sistemas.

## Exemplos

| Evento | Impacto |
|----------|----------|
| Chuva em Joanópolis | Alto |
| Chuva em Piracaia | Alto |
| Aumento da vazão do Jaguari | Muito Alto |
| Ausência de chuva em toda a bacia | Negativo |
| Recuperação do Sistema Billings | Positivo |
| Avanço de nuvens para a bacia | Positivo |

---

# Camada de Inteligência Artificial

## Princípio Fundamental

A IA não substitui os dados.

A IA interpreta os dados.

---

## Fase 1 — IA Descritiva

Pergunta:

```text
O que está acontecendo?
```

Exemplo:

```text
O Sistema Cantareira apresentou aumento de afluência nas últimas 24 horas.
```

---

## Fase 2 — IA Analítica

Pergunta:

```text
Por que está acontecendo?
```

Exemplo:

```text
O aumento foi provocado por chuvas observadas nas bacias Jaguari e Atibainha.
```

---

## Fase 3 — IA Preditiva

Pergunta:

```text
O que provavelmente acontecerá?
```

Exemplo:

```text
A tendência é de recuperação moderada do reservatório.
```

---

## Fase 4 — IA Estratégica

Pergunta:

```text
O que merece atenção?
```

Exemplo:

```text
A ausência de precipitação nas áreas críticas pode impactar a recuperação do sistema nos próximos dias.
```

---

# Tokens Semânticos

Cada evento observado gera entidades interpretáveis.

Exemplo:

```json
{
  "tipo": "chuva",
  "municipio": "Joanopolis",
  "intensidade": 18,
  "bacia": "Cantareira",
  "relevancia": 0.92
}
```

---

# Categorias de Aprendizado

## Meteorologia

```text
NUVEM
CHUVA
VENTO
UMIDADE
TEMPERATURA
PRESSAO
```

## Hidrologia

```text
RIO
VAZAO
AFLUENCIA
DEFLUENCIA
RESERVATORIO
TRANSPOSICAO
```

## Abastecimento

```text
ETA
PRODUCAO
CONSUMO
DEMANDA
SEGURANCA_HIDRICA
```

## Território

```text
MUNICIPIO
BACIA
SUBBACIA
REGIAO
```

---

# Índice de Segurança Hídrica Metropolitana (ISHM)

Modelo inicial:

```text
40% Volume Armazenado

25% Vazão Afluente

15% Tendência das Nuvens

10% Chuva Observada

10% Histórico Sazonal
```

---

## Classificação

| Faixa | Situação |
|---------|---------|
| 80-100 | Excelente |
| 60-79 | Confortável |
| 40-59 | Atenção |
| 20-39 | Crítica |
| 0-19 | Emergência |

---

# Roadmap

## v0.1

- [ ] Estrutura inicial do projeto
- [ ] Pipeline de coleta
- [ ] Dashboard básico
- [ ] Dados dos reservatórios

## v0.2

- [ ] Mapa interativo
- [ ] Municípios das bacias
- [ ] Integração meteorológica

## v0.3

- [ ] API pública
- [ ] Sistema de indicadores
- [ ] Comentários automáticos

## v0.4

- [ ] Grafo de conhecimento
- [ ] Índice ISHM
- [ ] Leads hidrológicos

## v1.0

- [ ] IA preditiva
- [ ] Linguagem da Água
- [ ] Rede colaborativa em produção

---

# Tecnologias Sugeridas

## Dados

- Python
- Pandas
- GeoPandas

## Infraestrutura

- GitHub
- GitHub Actions
- GitHub Pages

## Visualização

- Leaflet
- MapLibre
- D3.js

## IA

- Gemini
- OpenAI
- Ollama
- Knowledge Graphs
- RAG (Retrieval-Augmented Generation)

---

# Como Contribuir

1. Faça um Fork do projeto
2. Crie uma Branch
3. Faça suas alterações
4. Envie um Pull Request

Toda contribuição relacionada a:

- hidrologia
- geoprocessamento
- meteorologia
- dados públicos
- modelagem preditiva
- inteligência artificial

será bem-vinda.

---

# Licença

MIT License

---

## Frase do Projeto

> "Entender a chuva é importante. Entender para onde ela vai é essencial."
