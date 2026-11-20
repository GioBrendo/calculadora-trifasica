# ⚡ Calculadora Trifásica & SEP (Sistemas Elétricos de Potência)

> **Simulador e Calculadora Trifásica Completa para Análise de Circuitos de Potência (Unidade I - Engenharia Elétrica)**

[![GitHub Pages](https://img.shields.io/badge/Demo-GitHub%20Pages-brightgreen?logo=github)](https://giobrendo.github.io/calculadora-trifasica/)
[![HTML5](https://img.shields.io/badge/HTML5-Single--File%20App-orange?logo=html5)](index.html)
[![KaTeX](https://img.shields.io/badge/LaTeX-KaTeX%20Render-blue)](https://katex.org/)
[![Android](https://img.shields.io/badge/Mobile-Android%20APK-green?logo=android)](CalculadoraTrifasica.apk)

---

## 📌 Visão Geral

Aplicação desenvolvida para suporte didático e prático na disciplina de **Sistemas Elétricos de Potência (SEP)**, focando na resolução e visualização completa de circuitos trifásicos sob regime permanente senoidal:

* **Circuitos Equilibrados e Desequilibrados** (cargas em estrela aterrada, estrela isolada e triângulo).
* **Alimentadores Reais**: modelagem de impedância de condutores de fase e retorno de neutro.
* **Deslocamento de Neutro**: cálculo analítico via Teorema de Millman.
* **Componentes Simétricas (Teorema de Fortescue)**: decomposição de tensões e correntes em sequências positiva, negativa e zero ($V_{012}$, $I_{012}$).
* **Qualidade de Energia (PRODIST / IEC)**: cálculo dos fatores de desequilíbrio de tensão (VUF) e corrente (CUF).
* **Compensação Reativa**: dimensionamento automático de banco de capacitores trifásico para correção do fator de potência.
* **Sistema por Unidade (p.u.)**: conversão automática de grandezas reais para base de potência ($S_b$) e tensão ($V_b$).
* **Memória Didática**: renderização analítica passo a passo com equações formatadas em LaTeX/KaTeX.
* **Diagramas Fasoriais Interativos em SVG**: representação vetorial em plano complexo e triângulo de tensões.

---

## 🚀 Como Executar

### 1. Web (Navegador)
Você pode acessar diretamente pelo GitHub Pages:
🔗 **[https://giobrendo.github.io/calculadora-trifasica/](https://giobrendo.github.io/calculadora-trifasica/)**

Ou abrir localmente:
- Basta abrir o arquivo `index.html` (ou `calculadora SImples.html`) em qualquer navegador web moderno.
- Não requer instalação, Node.js ou servidor local (Single-Page Application autocontida).

### 2. Dispositivo Móvel (Android)
- O arquivo [`CalculadoraTrifasica.apk`](CalculadoraTrifasica.apk) está disponível diretamente no repositório para instalação em smartphones e tablets Android com suporte a operação 100% offline.

---

## 🧮 Módulos e Recursos

### 1. 🔌 Fonte Trifásica
- Configurações: **Estrela (Y)** ou **Triângulo ($\Delta$)**.
- Sequência de fases: **Positiva (ABC)** ou **Negativa (CBA)**.
- Ajuste de tensão nominal de linha ou fase com ângulo de referência.

### 2. 🛤️ Linha de Transmissão / Alimentador
- Impedância dos cabos de fase: $Z_L = R_L + jX_L$.
- Impedância do condutor de neutro: $Z_N = R_N + jX_N$.

### 3. 🏭 Carga Trifásica
- Ligações suportadas:
  - Estrela a 4 condutores ($Y$ com neutro conectado).
  - Estrela a 3 condutores ($Y$ com neutro isolado — Teorema de Millman).
  - Triângulo ($\Delta$).
- Modos de impedância:
  - Carga equilibrada ($Z$) ou desequilibrada por fase ($Z_a, Z_b, Z_c$ ou $Z_{ab}, Z_{bc}, Z_{ca}$).
  - Especificação direta em Potência ($P + jQ$, $S$ e FP indutivo/capacitivo).

### 4. 📐 Sistema de Base (p.u.)
- Definição de $S_{base}$ e $V_{base}$.
- Cálculo de impedância de base ($Z_b$) e corrente de base ($I_b$).
- Apresentação dos resultados em grandezas físicas (V, A, $\Omega$, W, var, VA) e em *p.u.*

### 5. ⚖️ Teorema de Fortescue & Qualidade de Energia
- Matriz de transformação de Fortescue usando o operador $a = 1\angle 120^\circ$:
  $$\begin{bmatrix} V_0 \\ V_1 \\ V_2 \end{bmatrix} = \frac{1}{3} \begin{bmatrix} 1 & 1 & 1 \\ 1 & a & a^2 \\ 1 & a^2 & a \end{bmatrix} \begin{bmatrix} V_a \\ V_b \\ V_c \end{bmatrix}$$
- Fator de Desequilíbrio de Tensão:
  $$VUF(\%) = \frac{|V_2|}{|V_1|} \times 100$$
- Verificação de conformidade com os limites normativos do **PRODIST (Módulo 8)** e **IEC 61000-2-2**.

### 6. ⚡ Banco de Capacitores
- Cálculo da potência reativa necessária ($Q_c$) para atingir o fator de potência alvo:
  $$Q_c = P \cdot [\tan(\theta_{atual}) - \tan(\theta_{alvo})]$$
- Dimensionamento dos capacitores por fase (em $\mu\text{F}$) nas ligações Estrela e Triângulo.
- Redução percentual da corrente do alimentador e diminuição das perdas ôhmicas por efeito Joule ($I^2 R$).

### 7. 🧭 Diagramas Fasoriais
- Fasores de tensões de fase, tensões de linha e correntes de linha em plano polar/cartesiano SVG.
- Triângulo de tensões com visualização do ponto de neutro virtual e tensão de deslocamento de neutro ($V_{nN}$).

---

## 📁 Estrutura do Repositório

```text
├── index.html                  # Aplicação web principal (otimizada para GitHub Pages)
├── calculadora SImples.html    # Arquivo original da aplicação
├── CalculadoraTrifasica.apk    # Pacote de instalação Android para uso offline
├── .gitignore                  # Arquivos ignorados pelo Git
└── README.md                   # Documentação do projeto
```

---

## 👨‍💻 Autor

Desenvolvido por **[Giovanni Brendo](https://github.com/GioBrendo)**  
Engenharia Elétrica / Sistemas Elétricos de Potência
