# 🧮 Filtro Passa-Baixas RC — Simulação em Python

### 🎓 Projeto acadêmico — Engenharia Elétrica / Eletrônica

Este projeto apresenta a **análise, simulação e visualização do comportamento de um filtro passa-baixas RC** utilizando **Python e Jupyter Notebook**.
O trabalho segue as etapas clássicas de projeto, partindo do **cálculo teórico da frequência de corte**, passando pela **resposta em frequência (Bode)** e **simulação de sinais senoidais** de entrada e saída.

---

## 🎯 Objetivo

Demonstrar o comportamento de um **filtro passa-baixas RC de primeira ordem**, analisando:

* A **frequência de corte** $f_c = \frac{1}{2 \pi RC}$
* O **ganho em função da frequência**
* A **atenuação de -3 dB** no ponto de corte
* A **resposta temporal** do sinal de entrada e saída em diferentes frequências

---

## 📖 Conceitos Teóricos

Um **filtro passa-baixas RC** permite a passagem de sinais de **baixa frequência**, atenuando as **altas frequências**.

A função de transferência (em magnitude) é dada por: $|H(f)| = \frac{1}{\sqrt{1 + (f/f_c)^2}}$

**Frequência de corte ($f_c$)**: $f_c = \frac{1}{2\pi RC}$

**Atenuação em -3 dB** ocorre quando $f = f_c$: $|H(f_c)| = \frac{1}{\sqrt{1 + (f_c/f_c)^2}} = \frac{1}{\sqrt{2}} \approx 0.707$

Em decibéis: $20 \log_{10}(0.707) \approx -3 \text{ dB}$
---

## ⚙️ Etapas do Projeto

1.  **Projeto Matemático**
    * Cálculo da frequência de corte com base em R e C.
    * Exibição das fórmulas e resultados.

    > **Nota sobre os Cálculos:**
    > (Aqui você deve inserir os valores e cálculos específicos do seu projeto)
    >
    > **Exemplo de cálculo (se R=1kΩ e C=1µF):**
    > * $R = 1000 \, \Omega$
    > * $C = 1 \times 10^{-6} \, \text{F}$
    > * $f_c = \frac{1}{2 \pi (1000)(1 \times 10^{-6})} \approx \frac{1}{0.006283} \approx 159.15 \, \text{Hz}$

2.  **Resposta em Frequência**
    * Gráfico em escala logarítmica (Bode) mostrando o ganho em dB.
    * Identificação visual da frequência de corte.

3.  **Simulação de Sinais**
    * Geração de sinais senoidais de entrada e saída em:
        * 100 Hz (baixa frequência)
        * $f_c$ Hz (frequência de corte)
        * 10 kHz (alta frequência)

4.  **Análise e Conclusões**
    * Discussão dos resultados observados.
    * Aplicações práticas do filtro.

---

▶️ **Como Executar**  
Clone este repositório:

```bash
git clone https://github.com/seuusuario/filtro-passa-baixas-rc.git
cd filtro-passa-baixas-rc
```

Abra o notebook:

```bash
jupyter notebook filtro_passa_baixas.ipynb
```

Execute as células em ordem e visualize os gráficos.

---

📈 **Resultados Esperados**  

🔹 **Resposta em Frequência**  
O gráfico mostra o ganho em dB decaindo **-20 dB/década** após $f_c$.  
O ponto de corte é claramente identificado em **-3 dB**.

🔹 **Simulação de Sinais**

| Frequência | Comportamento |
|-------------|---------------|
| **100 Hz**  | Sinal praticamente igual à entrada |
| **$f_c$**   | Amplitude reduzida para 70,7% (-3 dB) |
| **10 kHz**  | Sinal fortemente atenuado e defasado (~-90°) |

---

📊 **Análise e Conclusões**  
O filtro projetado apresentou comportamento coerente com a teoria:

- Para $f \ll f_c$: ganho ≈ 0 dB → sinal passa quase sem alteração.  
- Para $f = f_c$: ganho = -3 dB → metade da potência transmitida.  
- Para $f \gg f_c$: atenuação de -20 dB/década.

---

💡 **Aplicações Comuns**

- Sistemas de áudio (controle de tom, crossovers)  
- Antialiasing em conversores ADC  
- Condicionamento de sensores  
- Remoção de ruído de alta frequência
