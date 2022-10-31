## Configurando Verifone VX520

Esse artigo ensina como configurar o aparelho verifone VX520 para trabalhar com o Polvo Tickets.

### Índice
 - [Requerimentos](#requerimentos)
 - [Sistema Operacional Navs](#sistema-operacional-navs)
     - [Desinstalado Navs](#desinstalado-navs)
     - [Baixar Navs](#baixar-navs)
     - [Instalando Navs](#instalando-navs)
 - [Atualizar o Driver](#atualizar-o-driver)
 - [Inicialização](#inicialização)
    - [Baixar Inicialização](#baixar-inicialização)
    - [Instalando Inicialização](#instalando-inicialização)
- [Configuração](#configuração)
  - [Setando o Servidor](#setando-o-servidor)
  - [Setando para Produção](#setando-para-produção)


### Requerimentos

- Dois pendrive formatado em FAT32
- Internet via cabo
- :coffee: :coffee: :coffee:

### Sistema Operacional Navs

O Navs é o responsável por todo a comunicação com o `Topedindo Ingressos`, ele faz a ponte para o sistema da verifone, onde se torna mais simples colocar uma aplicação no aparelho Verifone VX 520.

Nessa etapa você vai aprender a desinstalar e instalar o Navs. As vezes não é necessário essa etapa, porque o aparelho já vem de fabrica com a versão homologada.

O Navs homologado é a a versão `v1.51`.

#### Desinstalado Navs

Nessa parte teremos que apagar todo o sistema operacional e arquivos que está na maquina, assim sendo, zerando totalmente ela.

**Etapa 1**

Ligue a maquina e quando aparecer a logo do `Navs`, pressione `ENTER + 7`.

**Etapa 2**

Digite a senha `1 + ALPHA + ALPHA + 66831`

**Etapa 3**

Seguir a seleção de menus:

- `MEMORY FUNCTIONS + ENTER`
- `CLEAR MEM + ENTER`
- `GROUP ID: _1 + ENTER`
- `PASSOWORD GID: 1 + ALPHA + ALPHA + 66831`
- `CLEAR CONFIG.SYS + ENTER`
  - `CLEAR ALL + ENTER`
  - `KEEP PROTECTED VAR + ENTER`
  - `CANCEL (BOTÃO VERMELHO)`
- `CLEAR SPLIT FILES + ENTER`
- `CLEAR GID FILES + ENTER`
- `CLEAR ALL GROUPS + ENTER`
  - `CONFIRM + ENTER`

Agora pressione `CANCEL (BOTÃO VERMELHO)` 4 vezes até visualizar `RESTART` e reinicie o aparelho e agora está tudo apagado.

#### Baixar Navs

Não existe um link direto da `Skytef` para baixar a versão `v1.51`, por isso ela sempre vai ficar disponivel nesse artigo. [Baixar Navs `v1.51`](https://github.com/topedindo/tickets/files/8789597/NAVS.1.51.0.0_producao.zip)

Após o download, formatar o pendrive em FAT32 e colocar somente esse arquivo dentro do pendrive com o nome `verifone.zip`.

#### Instalando Navs

Essa etapa é muito simples, é somente colocar o pendrive no aparelho:

> A entrada do pendrive fica na traseira do aparelho, somente remover a tampa traseira e você vai visualizar a entrada para o pendrive.

 - `PRESSIONAR O ENTER`
  - `Yes`

A máquina irá fazer a instalação do navs e reiniciar algumas vezes, até aparecer a Logo do Navs Skytef

### Atualizar o Driver

Pode ser que seja necessária a atualização do Driver EOS da máquina, para isso você irá precisar do arquivo [Driver EOS](https://github.com/topedindo/tickets/files/8789603/verifone.zip).

O arquivo já irá vim com o nome 'verifone.zip', para fazer a instalação é bem simples:

**Etapa 1**

Ligue a maquina e quando aparecer a logo do `Navs`, pressione `ENTER + 7`.

**Etapa 2**

Digite a senha `1 + ALPHA + ALPHA + 66831`

**Etapa 3**

Seguir a seleção de menus:

- `DOWNLOAD + ENTER`
- `GROUP ID: _1 + ENTER`
- `PASSOWORD GID: 1 + ALPHA + ALPHA + 66831`
- `SINGLE-APP + ENTER`
- `PARTIAL DN1D + ENTER`
- `USB FLASH MEMORY + ENTER`

Agora espere o arquivo ser carregado e pressione `CANCEL` até visualizar `RESTART` e reinicie o aparelho.

### Inicialização

Nessa etapa vamos adicionar os arquivos iniciais para fazer a comunicação com o `Topedindo Ingressos`. Para isso teremos que baixar os arquivos, adicionar a um pendrive e colocar no aparelho.

#### Baixar Inicialização

Bem provável que a mudança dos arquivos de inicialização não seja constante, então [Baixar inicialização](https://github.com/topedindo/tickets/files/8792365/inicializacao.zip).

Após o download colocar somente esse arquivo dentro do pendrive com o nome `verifone.zip`.

#### Instalando Inicialização

Após ter baixando os arquivos de inicialização, vamos colocar esses arquivos no aparelho, coloque o pendrive com os arquivos de inicialização no aparelho e somente seguir as instruções.

> A entrada do pendrive fica na traseira do aparelho, somente remover a tampa traseira e você vai visualizar a entrada para o pendrive.

**Etapa 1**

Ligue a maquina e quando aparecer a logo do `Navs`, pressione `ENTER + 7`.

**Etapa 2**

Digite a senha `1 + ALPHA + ALPHA + 66831`

**Etapa 3**

Seguir a seleção de menus:

- `DOWNLOAD + ENTER`
- `GROUP ID: _1 + ENTER`
- `PASSOWORD GID: 1 + ALPHA + ALPHA + 66831`
- `SINGLE-APP + ENTER`
- `PARTIAL DN1D + ENTER`
- `USB FLASH MEMORY + ENTER`

Agora espere o arquivo ser carregado e pressione `CANCEL` até visualizar `RESTART` e reinicie o aparelho.


### Configuração

Agora já temos a versão correta do `Navs` e já estamos com os arquivos corretos de `Inicialização`, mas precisamos fazer algumas configurações no aparelho.

#### Setando o Servidor

Ligue o aparelho e quando você visualizar a  `LOGO NAV`, você pressione e segura a tecla `#` até aparecer na tela escrito `SENHA`. Essa senha por padrão vem de fábrica em branco, somente `PRESSIONAR O ENTER`, caso não entre na próxima tela a maquina deve estar com uma senha setada, tente descobrir qual é ou você vai ter que desinstalar, instalar o navs e os arquivos de inicialização novamente.

> **Dicas:**
> - O cabo da internet ou chip de dados tem que estar corretamente conectado ao aparelho.
> - Para saber se está conectado a internet, tem que aparecer a mensagem `UP` no canto direito inferior do aparelho.
> - A tecla `ALPHA` muda entre números e letras.

Seguir a seleção de menus:

- `1 CONEXAO`
  - `4 ETHERNET+CHIP`
- `2 REDE`
  - `1 ETHERNET`
  - `2 IP DINAMICO`
- `3 SERVIDOR`
  - `1 IP DESTINO`
    - Apague o texto atual usando a tecla amarela
    - Digite `WWW.TPINGRESSOS.COM.BR` + `ENTER`
  - `2 PORTA`
    - Apague o texto atual usando a tecla amarela
    - Digite `443` + `ENTER`
  - `3 RECURSO`
    - Apague o texto atual usando a tecla amarela
    - Digite `/POS` + `ENTER`
  - `4 HOST`
    - Digite `WWW.TPINGRESSOS.COM.BR` + `ENTER`
  - `5 HTTPS`
    - `1 ATIVA/DESATIVA`
      - `1 ATIVAR`
    - `3 METODO`
      - `4 TLS 1.2`

Pressione `CANCEL` 2x até o aparelho reiniciar.

#### Setando para Produção

Agora já temos a configuração básica e vamos cadastrar o aparelho na aplicação e setar o aparelho para trabalhar em modo produção.

**Cadastrar o aparelho na aplicação**

Entre no [Topedindo Ingressos](http://topedindoingressos.com.br) como `Admin` e cadastre o aparelho com o seu `Serial Number` sem os `-`, esse número é encontrado na parte inferior do aparelho, também é necessário cadastrar uma senha que será para utilizado para acessar o pdv.

**Logue no aparelho**

Agora que você já cadastro o aparelho na aplicação, logue com a senha que você cadastrou para o aparelho.

Seguir a seleção de menus:

- `9 ADMINISTRACAO` (Menu invisível)
  - Digite `894286` + `ENTER`
  - `1 AMBIENTES`
    - Digite a senha do pdv definida no painel do administrativo
    - `1 PRODUCAO`

O aparelho vai reiniciar e vai estar pronto para se usar em modo de produção, com isso a senha de acesso as configurações no aparelho do `Navs` mudou para `894286`.

Qualquer dúvida por favor abra uma issue, que vamos ajudar ou melhorar esse artigo.
