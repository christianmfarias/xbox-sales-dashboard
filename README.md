
# 📊 Dashboard de Vendas Xbox

Este repositório contém um painel interativo desenvolvido no Excel para análise de assinaturas e vendas relacionadas aos serviços Xbox.

---

## 🗂 Estrutura do Arquivo

O arquivo Excel é composto pelas seguintes planilhas:

- **Assets**: Elementos visuais como paleta de cores e ícones.
- **Bases**: Base de dados principal com informações detalhadas dos assinantes.
- **Cálculos**: Tabelas auxiliares com somatórios e agrupamentos.
- **Dashboard**: Área de visualização consolidada com gráficos e indicadores.

---

## 🧠 Técnicas de Análise de Dados

### 1. Limpeza e Preparação de Dados
- Conversão de datas (`Start Date`) para o tipo `datetime`.
- Normalização de colunas booleanas como `Auto Renewal`, `EA Play Season Pass`, etc.
- Tratamento de valores ausentes e substituição de traços por zeros ou nulos.

### 2. Criação de Métricas
- Cálculo do valor total da assinatura com base em componentes adicionais e descontos.
- Extração de indicadores por tipo de plano e periodicidade da assinatura.

### 3. Segmentação de Dados
- Agrupamento por tipo de plano (`Core`, `Standard`, `Ultimate`).
- Filtros por tipo de assinatura (`Monthly`, `Quarterly`, `Annual`).
- Uso de segmentações (slicers) para facilitar a navegação no Excel.

---

## 📘 Detalhamento das Métricas

### 🔹 `Subscription Price`
- **Descrição**: Valor base da assinatura do plano (`Core`, `Standard`, `Ultimate`).
- **Exemplo**: R$15 para o plano Ultimate.

---

### 🔹 `EA Play Season Pass Price`
- **Descrição**: Valor adicional cobrado se o assinante optou pelo passe de temporada do EA Play.
- **Condição**: Só é aplicado se a coluna `EA Play Season Pass` for **"Yes"**.
- **Exemplo**: R$30 se o passe estiver ativo.

---

### 🔹 `Minecraft Season Pass Price`
- **Descrição**: Valor adicional cobrado se o assinante optou pelo passe de temporada do Minecraft.
- **Condição**: Só é aplicado se a coluna `Minecraft Season Pass` for **"Yes"**.
- **Exemplo**: R$20 se o passe estiver ativo.

---

### 🔹 `Coupon Value`
- **Descrição**: Valor de desconto aplicado à assinatura.
- **Exemplo**: R$5 de desconto.

---

### 🔹 `Total Value`
- **Descrição**: Soma total da assinatura considerando todos os componentes.
- **Fórmula estimada**:

```math
Total Value = Subscription Price + EA Play Season Pass Price + Minecraft Season Pass Price - Coupon Value
