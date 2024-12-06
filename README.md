# Conversão de Imagem para Escala de Cinza e Binária

Repositório do lab "Redução de Dimensionalidade em Imagens para Redes Neurais" da Digital Innovation One.

Este projeto implementa, em Python, a conversão de uma imagem colorida para tons de cinza e para uma versão binarizada (preto e branco) **sem o uso de bibliotecas de processamento de imagem prontas**, como OpenCV ou PIL.

## Objetivo
- **Converter uma imagem colorida (RGB) para escala de cinza.**
- **Binarizar a imagem em preto e branco com base em um limiar (threshold).**

## Funcionamento do Código

### 1. Conversão para Escala de Cinza
- Fórmula utilizada:
  Cinza = 0.2989 * R + 0.5870 * G + 0.1140 * B

- Essa fórmula é baseada no padrão de luminância do modelo **Rec. 601**, que considera como o olho humano percebe a luz. 

### 2. Binarização
- A imagem em escala de cinza é transformada em preto e branco:
  - Pixels com valor **acima do limiar (128)** tornam-se **brancos (255)**.
  - Pixels com valor **abaixo ou igual ao limiar** tornam-se **pretos (0)**.

## Entradas e Saídas
- **Entrada**: Uma imagem colorida no formato PNG.
- **Saídas**:
  - Imagem original (colorida).
  - Imagem em tons de cinza.
  - Imagem binarizada (preto e branco).

## Observações
- Caso a imagem possua um canal alpha (RGBA), ele será ignorado no processamento.
- O código foi escrito para demonstrar conceitos básicos de processamento de imagem sem dependências externas.

