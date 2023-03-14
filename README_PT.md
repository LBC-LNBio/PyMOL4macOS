# PyMOL de código aberto para macOS

O PyMOL de código aberto [PyMOL](https://pymol.org) está disponível gratuitamente e pode ser instalado por meio do gerenciador de pacotes [Homebrew](https://brew.sh/).

Este repositório fornece um método para instalar o PyMOL v2.6 no macOS. Se necessário, uma versão em inglês deste guia está disponível [aqui](https://github.com/LBC-LNBio/PyMOL4macOS/blob/main/README.md).

## Download e instalação

Siga estes passos para instalar o PyMOL v2.6:

1. Instale o [Homebrew](https://brew.sh/):

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

2. Instale as dependências do PyMOL (python, xquartz, tcl-tk, Qt5) usando o Homebrew:

```bash
brew install Caskroom/cask/xquartz
brew install tcl-tk
brew install python
pip install pyqt5
```

3. Instale o PyMOL

```bash
brew install brewsci/bio/pymol
```

4. Crie um executável de aplicativo para o PyMOL:

- Abra o Automator, que está em Aplicativos no macOS.
- Crie um novo documento, selecione “Aplicativo”.
- Selecione “Ações” e “Biblioteca” no painel esquerdo. Selecione “Utilitários” e “Executar script de shell”. Arraste isso para o painel principal.
- Escolha `/bin/bash` como um shell.
- Cole o seguinte: `/usr/local/bin/pymol -M`. Se isso não funcionar, verifique o caminho para o PyMOL usando `which pymol` no terminal e use este em vez disso.
- Salve o aplicativo (“Arquivo > Salvar”) na área de trabalho e nomeie-o como “PyMOL”.

5. Inicie o PyMOL v2.6

No terminal, execute:

```bash
pymol
```

ou, você pode iniciar o PyMol clicando duas vezes no aplicativo criado na área de trabalho.
