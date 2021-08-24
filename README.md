# WikIME CLI

Programa da linha de comando para consultar páginas do
[WikIME](https://wikime.linux.ime.usp.br).

Essa script busca páginas do WikIME, converte-as para texto puro e exibe-as no
terminal.

## Instalação

Baixe a script [wikime](./wikime) e garanta que ela está em seu `$PATH`.

Por exemplo, após baixar `wikime`:

```shell
mkdir -p ~/.local/bin && mv wikime ~/.local/bin/
```

E adicione `~/.local/bin` (ou qualquer outro diretório onde esteja `wikime`) no
seu `PATH` no seu `.bashrc` ou `.zshrc` (ou seja lá qual for a shell que você
esteja usando).

```shell
export PATH=$PATH:$HOME/.local/bin
```

## Uso

Todas as opções e instruções de uso podem ser exibidas rodando `wikime -h`.

```
WIKIME-CLI

    Essa script usa navegadores de internet TUI (terminal UI) para  pesquisar  e
    renderizar artigos do WikIME. O resultado será imprimido para a saída padrão

SINOPSE
    wikime [-BCnNoOpPsSuU] [-b prog] [-c patt] [-i patt] [-l lang]
                   [-X browseroptions] query
    wikime -o [-b prog] [-l lang] query
    wikime [-h]
    wikime -v|-r

    -n  não use cores            - N  cores simples (alias -C)
    -p  display using a pager    - P  não use PAGER
    -o  abra artigo no navegador - O  não abra no navegador
    -s  exibe somente resumo     - S  exibe artigo inteiro
    -u  imprime URL da query     - U  abra URL no navegador
    -v  exibe versão             - h  exibe ajuda
    -t  exibe todas seções disponíveis

    -r           abra página aleatória
    -d           modo debug
    -i patt      padrão de cores (caso sensitivo)
    -I patt      padrão de cores (case-sensitive, alias -c)
    -b prog      use prog como navegador (navegador padrão invocados são elinks,
                 links2, links, lynx or w3m, se existirem)
    -T custom    imprime seção customizada (qualquer coisa em html h2 tag)
    -W url       use url como URL base para WikIME (em outras palavras, use uma
                 Wiki diferente. Pesquisar nesse URL será feito acrescentando o
                 termo de pesquisa no URL)
    -X "options" opções para passar para o navegador
                 (aviso: deve ser em aspas duplo, específico por navegador)

    O termo de pesquisa pode ser qualquer termo.  A script irá  tomar  conta  de
    caracteres especiais. Observe que somente um termo de pesquisa é aceito, mas
    essse termo pode consistir de várias palavras.

    A configuração pode ser controlada criando um arquivo de configuração em
    /home/andre/.config/wikimerc

    Observe que quando pedir  para  abrir  o  artigo  em  um  navegador,  outros
    paramêtros serão ignorados. O mesmo vale para as opções -h e -v.
```

## Licença

Faça qualquer coisa com o código deste repositório. Não me importo.
