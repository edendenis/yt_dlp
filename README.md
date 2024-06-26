# Como configurar/instalar o `yt-dlp` no Linux Ubuntu

## Resumo

Neste documento estão contidos os principais comandos e configurações para configurar/instalar o Warsaw do `yt-dpl` no Linux Ubuntu.

## _Abstract_

_This document contains the main commands and configurations to configure/install Warsaw from `yt-dpl` on Linux Ubuntu._

## Revisão(ões)/Versão(ões)

|Revisão número|Data da revisão|Descrição da revisão|Autor da revisão|
|:-:|:-:|:-|:-|
|0|04/10/2023|<ul><li>Revisão inicial/criação do documento.</li></ul>|Eden Denis F. da S. L. Santos|
|1|05/11/2023|<ul><li>Incluída a Seção Descrição.</li></ul>|Eden Denis F. da S. L. Santos|

## Controle de configuração/instalação nos Sistemas Operacionais (SO) vs. Computador

|Numero|Computador          |Sistema Operacional (SO) |Tipo de sistema |Status da configuração/instalação|
|:----:|:------------------:|:-----------------------:|:--------------:|:-------------------------------:|
|1     |Dell Precision 7520 |Kali Linux               |Debian          |OK                               |
|2     |Dell Precision 7520 |Linux Ubuntu             |Ubuntu          |Pendente                         |
|3     |Dell Precision 7520 |Linux Xubuntu            |Ubuntu          |Pendente                         |
|4     |Dell Precision 7520 |Windows 10               |Windows         |Pendente                         |
|5     |Asus                |Kali Linux               |Debian          |N/A                              |
|6     |Asus                |Linux Ubuntu             |Ubuntu          |Pendente                         |
|7     |Asus                |Linux Xubuntu            |Ubuntu          |OK                               |
|8     |Asus                |Windows 10               |Windows         |N/A                              |

### Legenda

- **N/A:** Not apllicable/Não aplicável
- **OK:** Zero killed

## Descrição [2]

### `yt-dlp`

O `yt-dlp` é uma ferramenta de linha de comando escrita em Python que permite aos usuários baixar vídeos de inúmeros sites de compartilhamento de vídeos como o YouTube, Facebook, Vimeo, e muitos outros. É um fork do popular `youtube-dlc`, que por sua vez é uma continuação do `youtube-dl`, e traz melhorias significativas em termos de velocidade, funcionalidades e a capacidade de contornar as restrições de download impostas por alguns sites. Com `yt-dlp`, você pode baixar vídeos em diferentes formatos e qualidades, extrair áudio, baixar playlists inteiras, e até mesmo configurar downloads automáticos através de scripts, fazendo dele uma ferramenta versátil e poderosa para armazenamento offline de conteúdo de vídeo.


## 1. Configurar/Instalar o `yt-dlp` Ubuntu [1]

Para configurar/instalar o `yt-dlp`, você pode seguir estas etapas:

1. Abra o terminal. Você pode fazer isso pressionando: `Ctrl + Alt + T`


2. Certifique-se de que seu sistema esteja limpo e atualizado.

    2.1 Limpar o `cache` do gerenciador de pacotes APT. Especificamente, ele remove todos os arquivos de pacotes (`.deb`) baixados pelo APT e armazenados em `/var/cache/apt/archives/`. Digite o seguinte comando: `sudo apt clean`
    
    2.2 Remover pacotes `.deb` antigos ou duplicados do cache local. É útil para liberar espaço, pois remove apenas os pacotes que não podem mais ser baixados (ou seja, versões antigas de pacotes que foram atualizados). Digite o seguinte comando: `sudo apt autoclean`

    2.3 Remover pacotes que foram automaticamente instalados para satisfazer as dependências de outros pacotes e que não são mais necessários. Digite o seguinte comando: `sudo apt autoremove -y`

    2.4 Buscar as atualizações disponíveis para os pacotes que estão instalados em seu sistema. Digite o seguinte comando e pressione `Enter`: `sudo apt update -y`

    2.5 Para ver a lista de pacotes a serem atualizados, digite o seguinte comando e pressione `Enter`:  `sudo apt list --upgradable`

    2.6 Realmente atualizar os pacotes instalados para as suas versões mais recentes, com base na última vez que você executou `sudo apt update -y`. Digite o seguinte comando e pressione `Enter`: `sudo apt full-upgrade -y`

    2.7 Remover pacotes que foram automaticamente instalados para satisfazer as dependências de outros pacotes e que não são mais necessários. Digite o seguinte comando: `sudo apt autoremove -y`

    2.8 Remover pacotes `.deb` antigos ou duplicados do cache local. É útil para liberar espaço, pois remove apenas os pacotes que não podem mais ser baixados (ou seja, versões antigas de pacotes que foram atualizados). Digite o seguinte comando: `sudo apt autoclean`

3. **Você poderá instalar o `yt-dlp` usando o comando**: `sudo apt install yt-dlp -y`

4. Depois de concluir a instalação do `yt-dlp`, você pode usar o comando `yt-dlp` para baixar vídeos do YouTube como demonstrado anteriormente: `yt-dlp https://www.youtube.com/watch?v=VxnHJkpl4oo`

    - Isso deve permitir que você baixe vídeos do YouTube com sucesso.


## 2. Código completo para configurar/instalar

Para configurar/instalar o `yt-dlp`p no Linux Ubuntu sem precisar digitar linha por linha, você pode seguir estas etapas:

1. Abra o terminal. Você pode fazer isso pressionando: `Ctrl + Alt + T`

2. Digite o seguinte comando e pressione `Enter`:

    ```
    sudo apt clean
    sudo apt autoclean
    sudo apt autoremove
    sudo apt update -y
    sudo apt autoremove
    sudo apt autoclean
    sudo apt list --upgradable
    sudo apt full-upgrade -y
    sudo apt install yt-dlp -y
    ```

## Referências

[1] OPENAI. ***Baixar vídeos do youtube.*** Disponível em: <https://chat.openai.com/c/87f54416-69e5-448d-a8c4-b65b7d4ba0ad> (texto adaptado). ChatGPT. Acessado em: 04/10/2023 21:29.

[2] OPENAI. ***Baixar vídeos com `yt-dlp`.*** Disponível em: <https://chat.openai.com/c/6cd29c98-8868-444a-bdc3-47e4c9c2e272> (texto adaptado). ChatGPT. Acessado em: 05/11/2023 23:17.
