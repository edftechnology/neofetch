# Como instalar/configurar/usar o `neofetch` no `Linux Ubuntu`

## Resumo

Guia para instalar o `neofetch` pelos repositórios oficiais do `Ubuntu` usando `apt`, executar a ferramenta e confirmar a instalação.

## _Abstract_

_Guide to install `neofetch` from the official `Ubuntu` repositories with `apt`, run the tool, and verify the installation._

## Descrição

### `neofetch`

O `neofetch` é uma ferramenta de linha de comando escrita em `Bash` que exibe informações do sistema ao lado do logotipo do sistema operacional ou de uma imagem. O projeto original está arquivado; este guia cobre a instalação do pacote disponibilizado pelos repositórios do `Ubuntu`.

## Pré-requisitos

- Permissão para usar `sudo`
- Repositórios `universe` do `Ubuntu` habilitados
- Conexão com a internet
- `apt` funcional no sistema

O pacote `neofetch` está disponível no componente `universe` em versões do `Ubuntu` que o fornecem. A disponibilidade pode variar conforme a versão do sistema.

## 1. Abrir o `Terminal Emulator`

1. Abrir o `Terminal Emulator`. Você pode fazer isso pressionando:

    ```bash
    Ctrl + Alt + T
    ```

2. Certifique-se de que seu sistema esteja limpo e atualizado.

    2.1 Limpar o `cache` do gerenciador de pacotes `apt`. Especificamente, ele remove todos os arquivos de pacotes (`.deb`) baixados pelo `apt` e armazenados em `/var/cache/apt/archives/`. Digite o seguinte comando:
        
    ```bash
    sudo apt clean
    ```

    2.2 Remover pacotes `.deb` antigos ou duplicados do `cache` local. É útil para liberar espaço, pois remove apenas os pacotes que não podem mais ser baixados (ou seja, versões antigas de pacotes que foram atualizados). Digite o seguinte comando:

    ```bash
    sudo apt autoclean
    ```

    2.3 Remover pacotes que foram automaticamente instalados para satisfazer as dependências de outros pacotes e que não são mais necessários. Digite o seguinte comando:

    ```bash
    sudo apt autoremove -y
    ```

    2.4 Buscar as atualizações disponíveis para os pacotes que estão instalados em seu sistema. Digite o seguinte comando e pressione `Enter`:

    ```bash
    sudo apt update
    ```

    2.5 **Corrigir pacotes quebrados**: Isso atualizará a lista de pacotes disponíveis e tentará corrigir pacotes quebrados ou com dependências ausentes:

    ```bash
    sudo apt --fix-broken install
    ```

    2.6 Limpar o `cache` do gerenciador de pacotes `apt` novamente:

    ```bash
    sudo apt clean
    ```

    2.7 Para ver a lista de pacotes a serem atualizados, digite o seguinte comando e pressione `Enter`:

    ```bash
    sudo apt list --upgradable
    ```

    2.8 Realmente atualizar os pacotes instalados para as suas versões mais recentes, com base na última vez que você executou `sudo apt update`. Digite o seguinte comando e pressione `Enter`:

    ```bash
    sudo apt full-upgrade -y
    ```


## 3. Instalar o `neofetch` via `apt`

1. Habilitar o componente `universe` e atualizar a lista de pacotes:

    ```bash
    sudo add-apt-repository universe
    sudo apt update
    ```

2. Instalar o `neofetch`:

    ```bash
    sudo apt install neofetch -y
    ```

3. Confirmar a instalação consultando a versão:

    ```bash
    neofetch --version
    ```

## 4. Executar o `neofetch`

1. Exibir as informações do sistema:

    ```bash
    neofetch
    ```

2. Consultar as opções disponíveis:

    ```bash
    neofetch --help
    ```

## 5. (Opcional) Remover o `neofetch`

1. Remover o pacote, mantendo os arquivos de configuração do usuário:

    ```bash
    sudo apt remove neofetch -y
    ```

2. Para remover também os arquivos de configuração do sistema:

    ```bash
    sudo apt purge neofetch -y
    ```

## 2. Como consultar informações específicas

O `neofetch` aceita opções para selecionar as informações exibidas. Por exemplo, para mostrar apenas o sistema operacional e o núcleo:

```bash
neofetch --os --kernel
```

Consultar `neofetch --help` para ver as opções disponíveis na versão instalada.

## Compatibilidade

- A disponibilidade do pacote `neofetch` depende da versão do `Ubuntu` e dos componentes habilitados nos repositórios.
- O pacote está no componente `universe` nas versões do `Ubuntu` que o publicam.
- O projeto original está arquivado; atualizações do pacote dependem da manutenção nos repositórios da distribuição.

## 1.1 Código completo para configurar/instalar/usar

Para instalar e executar o `neofetch` no `Linux Ubuntu` sem precisar digitar linha por linha, seguir estas etapas:

1. Abrir o `Terminal Emulator`. Você pode fazer isso pressionando:

    ```bash
    Ctrl + Alt + T
    ```

2. Digitar o seguinte comando e pressionar `Enter`:

    ```bash
    sudo apt clean
    sudo apt autoclean
    sudo apt autoremove -y
    sudo apt update
    sudo apt --fix-broken install
    sudo apt clean
    sudo apt list --upgradable
    sudo apt full-upgrade -y
    sudo add-apt-repository universe
    sudo apt update
    sudo apt install neofetch -y
    neofetch
    ```

## Licença

Este repositório inclui o arquivo `LICENSE.txt`.

## Contato e suporte

Para dúvidas sobre o pacote, consultar as informações do `apt` e a página do pacote do `Ubuntu`. Para informações sobre o projeto original, consultar seu repositório oficial.

## Referências

[1] OPENAI. **Instalar o `neofetch` no `linux ubuntu` pelo `terminal emulator`**. Disponível em: <https://chatgpt.com/g/g-p-6980caf949648191ad6acfcdbe590f9e-instalar/c/6abbe8ac-ca84-83e9-b2f8-857c1b503669>. ChatGPT. Acessado em: 29/09/2026.

[2] UBUNTU. **Neofetch (Jammy)**. Disponível em: <https://packages.ubuntu.com/jammy/neofetch>. Acessado em: 29/09/2026.

[3] UBUNTU. **Neofetch (Noble)**. Disponível em: <https://manpages.ubuntu.com/manpages/noble/man1/neofetch.1.html>. Acessado em: 29/09/2026.

[4] DYLANARAPS. **Neofetch**. Disponível em: <https://github.com/dylanaraps/neofetch>. Acessado em: 29/09/2026.

[5] UBUNTU. **Install and manage packages**. Disponível em: <https://ubuntu.com/server/docs/how-to/software/package-management/>. Acessado em: 29/09/2026.
