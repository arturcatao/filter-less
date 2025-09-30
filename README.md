# 🖼️ Filter (Less) – Filtros de Imagem em C

Este projeto consiste em manipular imagens no formato **BMP** (24 bits), aplicando filtros básicos implementados em **C**.
Com certeza, a parte mais difícil de todo o curso, mas não impossível.

## 📌 Descrição

Uma imagem pode ser representada como uma grade de pixels, onde cada pixel contém valores de **R (vermelho)**, **G (verde)** e **B (azul)**.
No formato **24-bit BMP**, cada pixel possui 8 bits para cada cor, totalizando 24 bits por pixel.

O objetivo do projeto é implementar, em **helpers.c**, funções que alteram os valores de RGB de cada pixel, aplicando diferentes filtros de imagem.

## 📂 Estrutura do Projeto

* **bmp.h** → Define as estruturas usadas para interpretar arquivos BMP.
* **filter.c** → Lida com entrada e saída de arquivos e chama os filtros.
* **helpers.h** → Contém os protótipos das funções de filtro.
* **helpers.c** → Onde você implementa os filtros.
* **Makefile** → Define como compilar o programa.

## 🎨 Filtros Implementados

* **Grayscale** → Converte a imagem para tons de cinza.
* **Sepia** → Aplica o efeito sépia.
* **Reflect** → Reflete a imagem horizontalmente.
* **Blur** → Aplica um desfoque (box blur).

## ▶️ Como Usar

1. Compile o programa:

   ```bash
   make filter
   ```

2. Execute o programa escolhendo o filtro:

   ```bash
   ./filter -g images/yard.bmp out.bmp
   ```

   Onde:

   * `-g` → grayscale
   * `-s` → sepia
   * `-r` → reflect
   * `-b` → blur

O arquivo resultante será salvo como `out.bmp`.

## 🎯 Objetivo

Praticar:

* Manipulação de arrays bidimensionais em C.
* Estruturas (`struct`) para organizar dados.
* Manipulação de arquivos binários.
* Implementação de algoritmos simples de processamento de imagem.

---

Projeto baseado no curso **CS50 – Harvard**.

