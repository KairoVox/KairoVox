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

#### Compatibilidade com versões anteriores
O sistema de arquivos ext4 é compatível com o ext3 e ext2 Isto irá melhorar o desempenho já ligeiramente, porque alguns novos recursos do ext4 também pode ser usado com ext3 e ext2, tal como o novo algoritmo de alocação de blocos.

#### Pré Alocação
O sistema de arquivos ext4 permite pré-alocação de espaço em disco para um arquivo.

Um novo fallocate () chamada de sistema foi adicionado ao Linux para uso de sistemas de arquivos, incluindo ext4 e XFS, que têm essa capacidade.

#### O mais rápido sistema de arquivos de verificação
No ext4, bloco alocado grupos e secções da tabela de inode são marcados como tal. Isso permite que e2fsck para ignorá-los completamente em uma verificação e reduz o tempo necessário para verificar o sistema de arquivos do tamanho do ext4 é construída para suportar. Esse recurso é implementado na versão 2.6.24 do Linux.

#### Alocador MultiBloco
O alocador multiblock é usado quando a atribuição atrasada é ativado por um sistema de arquivos, ou quando os arquivos são abertos no modo O_DIRECT. Esse recurso não afeta o formato de disco.

#### Timestamps
Ext4 também adiciona um suporte para a data-criado timestamps. Mas, como Theodore Ts'o salienta, ao mesmo tempo que é fácil de adicionar um campo data de criação extra no inode (portanto, tecnicamente permitindo suporte para data criada timestamps em ext4), é mais difícil de modificar ou adicionar o necessário sistema de chamadas, como stat () (que provavelmente exigiria uma nova versão), e as várias bibliotecas que dependem deles (como glibc). Estas alterações exigem a coordenação de vários projetos. Portanto, mesmo se os desenvolvedores implementarem o suporte inicial para a data de criação de carimbos, esse recurso não estará disponível nesse momento para programas de usuário.


