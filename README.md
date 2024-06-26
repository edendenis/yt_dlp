# Como configurar/instalar/usar o `ytm_desktop` no `Linux Ubuntu`

## Resumo

Neste documento estão contidos os principais comandos e configurações para configurar/instalar/usar o `ytm_desktop` no `Linux Ubuntu`.

## _Abstract_

_In this document are contained the main commands and settings to set up/install/use the `ytm_desktop` on `Linux Ubuntu`._

## Revisão(ões)/Versão(ões)

|Revisão número |Data da revisão |Descrição da revisão                                   |Autor da revisão             |
|:-------------:|:--------------:|:------------------------------------------------------|:----------------------------|
|0              |22/11/2023      |<ul><li>Revisão inicial/criação do documento.</li></ul>|Eden Denis F. da S. L. Santos|

## Controle de configuração/instalação nos Sistemas Operacionais (SO) vs. Computador

|Numero|Computador          |Sistema Operacional (SO) |Tipo de sistema |Status da configuração/instalação|
|:----:|:------------------:|:-----------------------:|:--------------:|:-------------------------------:|
|1     |Dell Precision 7520 |Kali   Linux             |Debian          |OK                               |
|2     |Dell Precision 7520 |Linux Ubuntu             |Ubuntu          |Pendente                         |
|3     |Dell Precision 7520 |Linux Xubuntu            |Ubuntu          |Pendente                         |
|4     |Dell Precision 7520 |Windows 10               |Windows         |Pendente                         |
|5     |Asus                |Kali   Linux             |Debian          |N/A                              |
|6     |Asus                |Linux Ubuntu             |Ubuntu          |Pendente                         |
|7     |Asus                |Linux Xubuntu            |Ubuntu          |OK                               |
|8     |Asus                |Windows 10               |Windows         |Pendente                         |

### Legenda

- **N/A:** Not apllicable/Não aplicável
- **OK:** Zero killed

## Descrição [2]

### `ytm_desktop` (YouTube Music Desktop)

O YTM Desktop é um aplicativo de desktop que oferece acesso conveniente ao YouTube Music fora do navegador. Ele permite que os usuários reproduzam músicas, álbuns, listas de reprodução e rádios personalizadas do YouTube Music diretamente em suas áreas de trabalho, oferecendo uma experiência semelhante à do aplicativo móvel, mas com recursos adicionais, como suporte a atalhos de teclado e integração com o sistema operacional. Essa aplicação é útil para aqueles que desejam acessar facilmente o YouTube Music sem precisar abrir um navegador da web.


## 1. Como configurar/instalar/usar o `ytm_desktop` no `Linux Ubuntu` [1][3]

Para configurar/instalar/usar o `ytm_desktop` no `Linux Ubuntu`, você pode seguir estes passos:

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

Para instalar o ytm_desktop no Linux Ubuntu, você tem duas opções principais: usando o Flatpak ou o Snap.

1. **Usando o Snap:** O Ubuntu já vem com suporte ao Snap por padrão. Para instalar o `ytm_desktop` usando o Snap, você pode utilizar o seguinte comando no terminal: `sudo snap install youtube-music-desktop-app`

    Este comando instalará a versão mais recente do `ytm_desktop` disponível no Snap Store.

### 1.1 Código completo para configurar/instalar/usar

Para configurar/instalar/usar o `ytm_desktop` no `Linux Ubuntu` sem precisar digitar linha por linha, você pode seguir estas etapas:

1. Abra o terminal. Você pode fazer isso pressionando: `Ctrl + Alt + T`

2. Digite o seguinte comando e pressione `Enter`:

    ```
    sudo apt autoclean
    sudo apt autoremove -y
    sudo apt update -y
    sudo apt autoremove -y
    sudo apt autoclean
    sudo apt list --upgradable
    sudo apt full-upgrade -y
    sudo snap install youtube-music-desktop-app
    ```


## Referências

[1] OPENAI. ***Instale ytm_desktop no Ubuntu.:*** Disponível em: <https://chat.openai.com/c/1a2f4026-a131-4346-92a9-dd6ee3526f7b> (texto adaptado). ChatGPT. Acessado em: 15/12/2023 12:00.

[2] OPENAI. ***Vs code: editor popular:*** Disponível em: <https://chat.openai.com/c/b640a25d-f8e3-4922-8a3b-ed74a2657e42> (texto adaptado). ChatGPT. Acessado em: 15/12/2023 12:00.

[3] OPENAI. ***Comandos de manutenção do ubuntu:*** https://chat.openai.com/c/4a8cfaa2-30d6-474d-821f-7047a6a39830. ChatGPT. Acessado em: 15/12/2023 12:00.
