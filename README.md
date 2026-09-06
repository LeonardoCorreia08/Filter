# TTS

Código criado com base na aula 13  do curso de TTS...

# Supressão de Ruído e Processamento de Áudio em Python

Este projeto consiste em um script em Python desenvolvido para o processamento de sinal de áudio. O objetivo principal é a remoção e filtragem de ruídos (como o ruído de um liquidificador sobreposto a uma gravação de voz), utilizando algoritmos de supressão de ruído espectral, conversão mono, ajuste de tom (*pitch shift*) e geração de gráficos de forma de onda.

---

## 📁 Arquivos de Áudio Necessários

Para a execução correta do script, certifique-se de ter os seguintes arquivos `.wav` no mesmo diretório do projeto:

- `voz_1.wav`: Gravação da voz limpa.
- `voz_2.wav`: Gravação da voz combinada com ruído de fundo (liquidificador).
- `voz_3.wav`: Gravação isolada do ruído do liquidificador.
- `Vozf.wav`: Arquivo de áudio para aplicação dos filtros ajustados e alteração de tom.

---

## ⚙️ Funcionalidades do Script

1. **Conversão Estéreo para Mono:**
   - Função utilitária para transformar canais estéreo em canal único através da média das amplitudes.

2. **Supressão de Ruído Espectral (`noisereduce`):**
   - Aplicação de algoritmo para atenuar o ruído constante do liquidificador sem danificar a frequência da voz.
   - Ajuste de parâmetros avançados como `prop_decrease`, `win_length` e `time_mask_smooth_ms`.

3. **Modificação de Tom (Pitch Shift):**
   - Redefinição da taxa de quadros (*frame rate*) utilizando a biblioteca `pydub` para alterar a tonalidade em semitonos.

4. **Análise Visual e Reprodução:**
   - Plotagem do sinal de áudio no domínio do tempo (Tempo x Amplitude) utilizando `matplotlib`.
   - Comparação gráfica entre o sinal original e o sinal filtrado.
   - Execução direta dos áudios no ambiente via `IPython.display.Audio`.

---

## 🛠️ Pré-requisitos e Bibliotecas

As seguintes bibliotecas são necessárias para executar o projeto:

- **NumPy**: Manipulação de arrays e cálculos numéricos.
- **SciPy**: Leitura e manipulação de arquivos WAV.
- **NoiseReduce**: Algoritmo principal para redução de ruído.
- **PyDub**: Manipulação de áudio e alteração de tom.
- **Matplotlib**: Geração de gráficos das formas de onda.
- **IPython**: Reprodução de áudio em notebooks.

---

## 🚀 Como Executar

1. Clone este repositório para a sua máquina local:
   ```bash
   git clone [https://github.com/LeonardoCorreia08/seu-repositorio.git](https://github.com/LeonardoCorreia08/seu-repositorio.git)
