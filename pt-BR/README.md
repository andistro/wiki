# 📄 **Documentação**

<img src="./../assets/flags/brasil.svg" width="32px"> ![ForYou](https://img.shields.io/badge/-Criado_com_❤️-gray)
![Android](https://img.shields.io/badge/Android-gray?logo=android)
![Termux](https://img.shields.io/badge/Termux-gray?logo=data:image/svg%2bxml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCA0OCA0OCI+CgogICAgPCEtLSBTY3JlZW4gYW5kIGJvcmRlci4gLS0+CiAgICA8cGF0aCBmaWxsPSIjMDAwIgogICAgICAgICAgc3Ryb2tlPSIjQkZDQkNEIgogICAgICAgICAgc3Ryb2tlLXdpZHRoPSIyIgogICAgICAgICAgZD0iTTksNgogICAgICAgICAgICAgbDMwLDAKICAgICAgICAgICAgIHEzIDAsMyAzCiAgICAgICAgICAgICBsMCwzMAogICAgICAgICAgICAgcTAgMywgLTMgMwogICAgICAgICAgICAgbC0zMCwwCiAgICAgICAgICAgICBxLTMgMCwgLTMtMwogICAgICAgICAgICAgbDAgLTMwCiAgICAgICAgICAgICBxMCAtMywgMyAtMyIKICAgIC8+CgogICAgPCEtLSBCbG9jayBjdXJzb3IuIC0tPgogICAgPHBhdGggZmlsbD0iI0ZGRiIKICAgICAgICAgIGQ9Ik0xNCwxNAogICAgICAgICAgICAgbDUsMAogICAgICAgICAgICAgbDAsMTAKICAgICAgICAgICAgIGwtNSwwIgogICAgLz4KCjwvc3ZnPgo=)
<!--[![en-US](https://img.shields.io/badge/[en--US]_Installation_and_troubleshooting_guide_🡥-blue?logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIGhlaWdodD0iMjRweCIgdmlld0JveD0iMCAtOTYwIDk2MCA5NjAiIHdpZHRoPSIyNHB4IiBmaWxsPSIjZmZmZmZmIj48cGF0aCBkPSJtNDc2LTgwIDE4Mi00ODBoODRMOTI0LTgwaC04NGwtNDMtMTIySDYwM0w1NjAtODBoLTg0Wk0xNjAtMjAwbC01Ni01NiAyMDItMjAycS0zNS0zNS02My41LTgwVDE5MC02NDBoODRxMjAgMzkgNDAgNjh0NDggNThxMzMtMzMgNjguNS05Mi41VDQ4NC03MjBINDB2LTgwaDI4MHYtODBoODB2ODBoMjgwdjgwSDU2NHEtMjEgNzItNjMgMTQ4dC04MyAxMTZsOTYgOTgtMzAgODItMTIyLTEyNS0yMDIgMjAxWm00NjgtNzJoMTQ0bC03Mi0yMDQtNzIgMjA0WiIvPjwvc3ZnPg==)](./../en-US/README.md)-->

# **Instale distribuições Linux dentro do ambiente Android e sem root.**

Este é um projeto que permite instalar distribuições Linux, como Ubuntu e Debian em dispositivos Android sem necessidade de root. O sistema é executado dentro do ambiente Termux e utiliza VNC para fornecer uma interface gráfica completa, sem modificar as configurações do Android.

Para garantir a confiança e segurança, nenhum sistema é hospedado no repositório - todos são baixados diretamente dos sites oficiais das distribuições. O código do instalador está completamente aberto para verificação

| **Comece selecionando alguma das opções abaixo.** |
|--------------------|
|[**Requisitos**](#Requisitos---)|
||
|[**Instalações necessárias**](#Instalações-necessárias---)|
||
|[**Iniciando a Instalação do sistema**](#iniciando-a-Instalação-do-sistema---)|
|  **↳** [**Baixando o instalador**](#baixando-o-instalador---)|
||
|[**Resolução de problemas**](/wiki/pt-BR/resolucao-de-problemas.md)|
||
|[**DevTools ‐ Padrões de interface de código**](/wiki/pt-BR/DevTools.md)|


<!--
h1
|[** **]()|
h1 alt
|**↳** [** **]()|
h2
|  **↳** [** **]()|
h3
|    **↳** [** **]()|
h4
|      **↳** [** **]()|
-->

> [!IMPORTANT]
> Todo o sistema será execultado dentro do Termux e por não haver root, não irá modificar as configurações do Android. <br>
> Para garantir a confiança desse projeto, nenhum sistema é hopedado aqui, todos sào baixados diretamente no site oficial do sistema operacional.<br>
> O código desse instalador está totalmente aberto para que possa conferir cada arquivo.<br>

>[!WARNING]
> Esse instalador é testado várias vezes, e usa ferramentas oficiais para funcionar e garantir a segurança dos dados, mas caso você instale algum arquivo desconhecido e que contenha malware, não é garantido que não afete a memória interna do aparelho visto que mesmo que o malware execulte somente dentro da maquina virtual, o sistema pode ler e modificar os arquivos da memória interna. Só nã há a possibilidade de modificar arquivos protegidos de sistema como exemplo os da pasta `Android/data`.

# Requisitos [[ ↑ ]](#)

|||Recomendado|Mínimo|Não suportado|
|-|-|-|-|-|
|![Arquiteturas suportadas](https://img.shields.io/badge/-gray?logo=arm&logoColor=white)|Arquiteturas| ![Arm](https://img.shields.io/badge/ARM64-0091BD) | ![Arm](https://img.shields.io/badge/ARMHF-0091BD) |![x86_64](https://img.shields.io/badge/x86__64-gray)|
|![Armazenamento](https://img.shields.io/badge/-gray?logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIGhlaWdodD0iMjRweCIgdmlld0JveD0iMCAtOTYwIDk2MCA5NjAiIHdpZHRoPSIyNHB4IiBmaWxsPSIjZTNlM2UzIj48cGF0aCBkPSJNMTIwLTE2MHYtMTYwaDcyMHYxNjBIMTIwWm04MC00MGg4MHYtODBoLTgwdjgwWm0tODAtNDQwdi0xNjBoNzIwdjE2MEgxMjBabTgwLTQwaDgwdi04MGgtODB2ODBabS04MCAyODB2LTE2MGg3MjB2MTYwSDEyMFptODAtNDBoODB2LTgwaC04MHY4MFoiLz48L3N2Zz4=)|Espaço livre no armazenamento|![64GB](https://img.shields.io/badge/Acima_de_64GB-FBBC04)|![40GB](https://img.shields.io/badge/40GB-gray)|
|![Memória ram](https://img.shields.io/badge/-gray?logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIGhlaWdodD0iMjRweCIgdmlld0JveD0iMCAtOTYwIDk2MCA5NjAiIHdpZHRoPSIyNHB4IiBmaWxsPSIjZTNlM2UzIj48cGF0aCBkPSJNMjQwLTM2MGg4MHYtMjQwaC04MHYyNDBabTIwMCAwaDgwdi0yNDBoLTgwdjI0MFptMjAwIDBoODB2LTI0MGgtODB2MjQwWm0tNDgwIDgwaDY0MHYtNDAwSDE2MHY0MDBabTAgMHYtNDAwIDQwMFptNDAgMTYwdi04MGgtNDBxLTMzIDAtNTYuNS0yMy41VDgwLTI4MHYtNDAwcTAtMzMgMjMuNS01Ni41VDE2MC03NjBoNDB2LTgwaDgwdjgwaDE2MHYtODBoODB2ODBoMTYwdi04MGg4MHY4MGg0MHEzMyAwIDU2LjUgMjMuNVQ4ODAtNjgwdjQwMHEwIDMzLTIzLjUgNTYuNVQ4MDAtMjAwaC00MHY4MGgtODB2LTgwSDUyMHY4MGgtODB2LTgwSDI4MHY4MGgtODBaIi8+PC9zdmc+)|Memória RAM|![](https://img.shields.io/badge/Acima_de_6GB-orange)|
|![Versão do Android](https://img.shields.io/badge/-gray?logo=android&logoColor=white)|Android|![Android 10+](https://img.shields.io/badge/Android_10+-073042)|
|![Root](https://img.shields.io/badge/-gray?logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIGhlaWdodD0iMjRweCIgdmlld0JveD0iMCAtOTYwIDk2MCA5NjAiIHdpZHRoPSIyNHB4IiBmaWxsPSIjZTNlM2UzIj48cGF0aCBkPSJtMjQwLTE2MCA0MC0xNjBIMTIwbDIwLTgwaDE2MGw0MC0xNjBIMTgwbDIwLTgwaDE2MGw0MC0xNjBoODBsLTQwIDE2MGgxNjBsNDAtMTYwaDgwbC00MCAxNjBoMTYwbC0yMCA4MEg2NjBsLTQwIDE2MGgxNjBsLTIwIDgwSDYwMGwtNDAgMTYwaC04MGw0MC0xNjBIMzYwbC00MCAxNjBoLTgwWm0xNDAtMjQwaDE2MGw0MC0xNjBINDIwbC00MCAxNjBaIi8+PC9zdmc+)|Root|![Não é necessário](https://img.shields.io/badge/Não_é_necessário-red)|
|![ADB](https://img.shields.io/badge/-gray?logo=android&logoColor=white)|ADB|![Pode ser necessário](https://img.shields.io/badge/Necessário_a_partir_do_Android_12-073042)|



|||Suportado|Com falhas|Em teste|
|-|-|-|-|-|
||Sistemas| ![Debian](https://img.shields.io/badge/Debian-13-red?logo=debian&logoColor=white) <br>![Ubuntu](https://img.shields.io/badge/Ubuntu-24.04-E95420?logo=ubuntu&logoColor=white)|
||Interface gráfica| ![XFCE](https://img.shields.io/badge/XFCE-2284F2?logo=xfce&logoColor=white)  ![LXDE](https://img.shields.io/badge/LXDE-0068C8?logo=data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjUiIGhlaWdodD0iMjQiIHZpZXdCb3g9IjAgMCAyNSAyNCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHBhdGggZD0iTTE4LjczMzMgOS4yNTkwNEMxNy4yMDA5IDcuNTQ5NTIgMTUuODIgNi40NDUzNiAxMy43NzU4IDkuMzI0MjdDMTIuNTU5NCAxMS4wMzc0IDUuMjU5NjYgMjAuODUwOSAzLjkyMDE5IDIyLjQxNDFDMy41MzExMSAyMi44NjgyIDMuMzAzMTggMjMuMTgzNyAzLjAwNDQ0IDIzLjM2NjdDMy4wMDQ4OSAyMi43NDUzIDguMDQ2NzkgMTQuODU1MiA5LjQ1Nzc4IDEyLjU2ODZDMTEuMTUyNiA5LjgyMjA3IDExLjA5ODggOS45ODI0NiAxMC44OTYgOS45ODMxOUMxMC42MDg5IDkuOTg0MTcgMTAuMDI0OSAxMC40MDI4IDkuMTM2ODcgMTEuMzM4NkM3LjUxNTMxIDEzLjA0NzYgMi43MTI4IDE5LjQwODIgMi4zODE3MSAxOS4zMTAxQzIuNDk2NzMgMTguODQ4IDYuMjUzNTUgMTMuMTU1MSA3Ljk1OTMgMTAuODAwMUM5LjQyOTc0IDguNzY5OTggOC44Njc2NiA4LjYxNTI0IDguMDI0ODUgOC44MTM0M0M0LjQzMzggOS42NTk3NyAwLjEzODg5OSAxMS43MDU5IDAgMTEuNjMyMUMwLjA1MTkzOSAxMS41MjYxIDE0LjQ2NDcgMS41MTA4IDE2LjM5IDEuMzE5MzRDMTYuNjE0MiAxLjI5NzA1IDE3LjA4NzEgMC45MDIwMTkgMTcuOTI5OCAwLjU3Mjk5NkMxOC44NDQ3IDAuMjE1ODE0IDE5LjQ2MDQgLTAuMDc0NzExNyAxOS42MTI3IDAuMDE3MTQwM0MxOC45NDUgMC45NDE5NzQgMTguNTkzNSAxLjEyODA5IDE4LjU4NzYgMS40MjY0MkMxOC41Nzc5IDEuOTE0OTEgMTguNDAxOSAyLjcwNTE4IDE4LjIwOTIgMi45NTc1MUMyMS45MzM3IDUuNDA5MzMgMjMuMzg2OCAxMy43NjkyIDI0LjQ1MDggMjAuNDkzM0MyNC43MDQ3IDIyLjA4OTMgMjQuOTQgMjMuMjg3OCAyNSAyNEMyNC42ODU2IDIzLjIwMDcgMjEuNzA3NyAxMi41NzczIDE4LjczMzMgOS4yNTkwNFoiIGZpbGw9IndoaXRlIi8+Cjwvc3ZnPgo=)|

> [!CAUTION]
> Pode ser que o sistema nem inicie em um dispositivo mais fraco, além de poder causar sobrecarga e danificar componentes internos devido a alta demanta de processamento.

# Instalações necessárias [[ ↑ ]](#)

Para que tudo funcione corretamente, é necessário a instalação do **Termux**, do **Andronix** e do **AVNC**. O Termux irá instalar e executar a distribuição localmente, o Andronix disponibilizará o script de instalação da distribuição e o AVNC irá visualizar e possibilitar o uso da interface gráfica do Ubuntu.
|**Onde baixar**|
|------|
||
|**Termux**|
|<a href="https://github.com/termux/termux-app/releases" target="_blank"><img width="256px" src="./../assets/images/badges/get-it-on-github.png" alt="Baixe pelo GitHub"></a> <a href="https://f-droid.org/pt_BR/packages/com.termux/" target="_blank"><img width="256px" src="./../assets/images/badges/get-it-on-fdroid.png" alt="Baixe pelo F-Droid"></a>|
|**AVNC**|
|<a href="https://github.com/gujjwal00/avnc/releases" target="_blank"><img width="256px" src="./../assets/images/badges/get-it-on-github.png" alt="Baixe pelo GitHub"></a><a href="https://f-droid.org/pt_BR/packages/com.gaurav.avnc/" target="_blank"><img width="256px" src="./../assets/images/badges/get-it-on-fdroid.png" alt="Baixe pelo F-Droid"></a> <a href="https://play.google.com/store/apps/details?id=com.gaurav.avnc" target="_blank"><img width="256px" src="./../assets/images/badges/get-it-on-google-play.png" alt="Baixe pelo Google Play Store"></a>|
> [!WARNING]
> O Termux da Google Play Store está desatualizado e não há mais suporte oficial.


# Iniciando a Instalação do sistema [[ ↑ ]](#)

## Baixando o instalador [[ ↑ ]](#)

1. Baixe o Termux e instale no dispositivo;
2. Baixe o AVNC e instale no dispositivo;
>[!NOTE]
> Você pode usar outro aplicativo de VNC que não seja o AVNC. Esta é somente uma recomendação por ser o aplicativo escolhido para ser usado durante o desenvolvimento
3. Acesse a página de lançamentos para copiar o link de instalação.

>[!NOTE]
> Os lançamentos com a informação `pre-release` são as versões de testes, já a versão `latest` é a estável.

- [Clique aqui para acessar a ultima versão estável](https://github.com/andistro/app/releases/latest)
- [Clique aqui para todos os lançamentos, incluindo as versões de teste](https://github.com/andistro/app/releases)

4. Após copiar o comando, abra o Termux, pressione a tela e clique em `paste` para colar o comando e após isso, tecle `enter ↲` para iniciar a instalação e configuração do AnDistro. Durante o processo, aparecerá uma barra de progresso e após isso, algumas mensagens interativas para finalizar as configurações. A partir daqui, toda a interface será intuitiva e gráfica para facilitar a instalação e caso o queira ter uma visibilidade próxima ao do terminal, usar o comando `andistro terminal` para ter um mini guia de comandos no formato de terminal.
5. No modo padrão do AnDistro, todo o uso é por meio de interface gráfica simples, clica nas opções e depois em `OK`. Quando clicar e a opção ficar em azul, estará selecionado.

