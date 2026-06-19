# Análise de Vendas - Xbox Game Pass

## 🎮 Sobre o Projeto
Este projeto tem como objetivo realizar uma análise detalhada das vendas de assinaturas do Xbox Game Pass. Através dos dados fornecidos, buscamos entender o comportamento dos jogadores, o desempenho financeiro dos serviços, a taxa de retenção, a adesão a pacotes adicionais (Add-ons) e o impacto de campanhas promocionais.

## 📂 Dados Utilizados
Os dados brutos estão estruturados na base principal e contêm informações detalhadas de transações de assinantes. As principais colunas disponíveis para análise incluem:
* **Subscriber ID & Name**: Identificação do assinante.
* **Plan**: Categoria do plano assinado (Core, Standard, Ultimate).
* **Start Date**: Data de início da assinatura.
* **Subscription Type**: Periodicidade da cobrança (Monthly, Quarterly, Annual).
* **Auto Renewal**: Indicador de renovação automática (Yes/No).
* **Add-ons**: Informações sobre adesão ao *EA Play Season Pass* e *Minecraft Season Pass*, incluindo preços.
* **Coupon Value & Total Value**: Valor do desconto promocional aplicado e o valor financeiro total pago na transação.

## ❓ Perguntas Estratégicas Respondidas
Com base nas análises e na aba de **Cálculos**, o projeto responde a importantes perguntas de negócios:
1. **Faturamento Geral**: Qual é o faturamento total agregado de todas as vendas de assinaturas?
2. **Retenção (Auto Renovação)**: Qual é o faturamento total de vendas de planos anuais, separados por usuários que optaram ou não pela auto renovação?
3. **Adoção de Serviços Adicionais**: Quantos assinantes adquiriram o *EA Play Season Pass* ou o *Minecraft Season Pass*, e qual foi a receita total gerada exclusivamente por esses complementos?
4. **Impacto de Promoções**: Qual foi o total de cupons promocionais, qual foi o plano (Ultimate, Standard ou Core) que mais se beneficiou financeiramente desses descontos?

## 📊 Instruções para Reprodução do Dashboard

Para reproduzir o painel de indicadores interativo (Dashboard) seguindo as diretrizes do projeto, siga os passos abaixo:

### 1. Preparação dos Dados (Tabelas Dinâmicas)
Utilize a aba `Bases` no Excel (ou ferramentas SQL/BI) para criar os agrupamentos necessários que alimentarão os gráficos:
* **Faturamento**: Crie uma Tabela Dinâmica somando a coluna `Total Value`.
* **Análise de Cupons**: Crie uma Tabela Dinâmica arrastando o campo `Plan` para Linhas e `Coupon Value` para Valores (certificando-se de que está configurado como **Soma**).
* **Add-ons**: Cruze a contagem dos campos de `EA Play` e `Minecraft` pelos tipos de planos (`Plan`).

### 2. Aplicação da Identidade Visual (Assets)
Para garantir que o Dashboard tenha o padrão visual do Xbox, utilize rigorosamente a paleta de cores mapeada na aba `Assets`:
* **Xbox Colors (Cores Principais)**: `#9BC848` e `#22C55E` (Tons de Verde).
* **Menus e Elementos de Destaque**: `#2AE6B1` e `#5BF6A8`.
* **Negative Zone (Planos de fundo e áreas neutras)**: `#E8E6E9`.

### 3. Montagem do Layout
1. Navegue até a aba vazia destinada ao **Dashboard**.
2. **Cabeçalho**: Insira o título oficial **XBOX GAME PASS SUBSCRIPTIONS SALES** no topo.
3. **Indicadores (Cards)**: Adicione cartões numéricos em destaque mostrando o *Faturamento Total* e o *Total de Descontos Concedidos*.
4. **Gráficos Recomendados**:
   * *Gráfico de Colunas/Barras*: Para mostrar o faturamento por tipo de plano (Core vs Standard vs Ultimate).
   * *Gráfico de Rosca/Pizza*: Para visualizar qual plano mais se beneficiou.
   * *Gráfico de Barras Horizontais*: Para evidenciar qual plano tem mais volume se autorenovável ou não.

## 🛠️ Ferramentas e Técnicas
* **Microsoft Excel**: Tabelas Dinâmicas, funções de agregação (SOMASE/SUMIF) e gráficos.

**Projeto desenvolvido por Vitor Jônatas Paiva Barbosa.**

