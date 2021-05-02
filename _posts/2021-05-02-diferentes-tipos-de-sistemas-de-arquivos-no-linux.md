---
layout: post
title:  Diferentes tipos de sistemas de arquivos no GNU/Linux
description: Os sistemas de arquivos mais usados no GNU/Linux
summary: Conheça os sistemas de arquivos mais usados no GNU/Linux
comments: true
tags: [sistemas de arquivos, curiosidades, iniciantes]
---

# Os sistemas de arquivos mais utilizados no GNU/Linux

Um sistema de arquivos é um conjunto de estruturas lógicas que permite o sistema operacional controlar o acesso a um dispositivo de armazenamento como disco rígido, pen drive, cd-room, etc. 
Diferentes sistemas operacionais podem usar diferentes sistemas de arquivos.

Diferente do Windows que possui seu sistema de arquivos padrão o NTFS, os sistemas GNU/Linux possuem diferentes tipos de sistemas de arquivos.
Cada distribuição possui seu sistema de arquivos padrão, como o brtfs no Fedora ou ext4 no Ubuntu.

A verdade é que não existe "O melhor sistema de arquivos", e sim aquele que vai ser melhor para VOCÊ.
Abaixo você verá os sistemas de arquivos mais utilizados ou conhecidos do mundo GNU/Linux.

## Ext4: O sistema de arquivo mais utilizado no Linux

O ext4 é uma evolução do ext3 e representa um salto importante, o qual resultou até o momento um dos sistemas de arquivo Linux de alto desempenho disponíveis hoje em dia.

### Características

- Alocação tardia.
- Journal checksums.
- Suporte para tamanhos maiores de volumes e arquivos.
- Extensões. 
- Compatibilidade com versões anteriores.
- Pré alocação.
- O mais rápido sistema de arquivos de verificação.
- Alocador multibloco. 
- Timestamps.


#### Alocação Tardia
Ext4 usa uma técnica de execução do sistema de arquivos chamado atribuir-on-flush, também conhecida como a atribuição de atraso. Isso melhora o desempenho e reduz a fragmentação, melhorando a alocação de blocos decisões com base no tamanho do arquivo.

#### Journal Checksums
Ext4 usa checksums no jornal para melhorar a confiabilidade, já que o jornal é um dos arquivos mais utilizados do disco. Esta característica tem um lado benéfico, que pode evitar com segurança um disco I / O esperar durante o processo diário, melhorando o desempenho ligeiramente.

#### Suporte para tamanhos maiores de volumes e arquivos 
O sistema de arquivos ext4 pode suportar volumes com tamanho até 1 exabyte e arquivos com tamanho até 16 terabytes. O atual e2fsprogs só pode tratar um sistema de arquivos de 16 TB. 

#### Extensões
As extensões são introduzidas para substituir o tradicional bloco de mapeamento de esquema usado por arquivos ext2/3.Uma extensão é um conjunto de blocos contíguos físico, melhorando o desempenho de muitos arquivos e redução de fragmentação. Uma única extensão em ext4 pode mapear até 128MB de espaço contíguo com um bloco de 4 KB de tamanho. Quando há mais de 4 extensões em um arquivo, o resto das extensões são indexadas em um three.


